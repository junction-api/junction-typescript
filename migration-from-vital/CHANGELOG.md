# Changelog

_Major release. Baseline: `tryVital/vital-node@3.1.544`._

## Breaking changes

- **Package renamed: @tryvital/vital-node to @junction-api/sdk** — [migration steps](MIGRATION.md#install)
  The published npm package has been renamed from `@tryvital/vital-node` to `@junction-api/sdk`. Uninstall the old package and install the new one. This is a replacement, not a version bump — there is no overlap window where both packages publish the same release. After installing the new package, update every import to point at `@junction-api/sdk` and update the imported symbols per the rename sections below.
- **Namespace export renamed: Vital to Junction** — [migration steps](MIGRATION.md#rename-namespace-export)
  The package's namespace alias has changed from `Vital` to `Junction`. Code that does `import { Vital } from "@tryvital/vital-node"` (or `import * as Vital from ...`) and references types as `Vital.SomeType` must switch to `Junction` and `Junction.SomeType`.
- **Top-level client class renamed: VitalClient to JunctionClient** — [migration steps](MIGRATION.md#rename-client-class)
  The default exported client class has been renamed from `VitalClient` to `JunctionClient`. Update every `new VitalClient(...)` construction site and every type annotation that references `VitalClient`.
- **Server base URLs replaced (Environment enum also renamed)** — [migration steps](MIGRATION.md#rename-environment-enum)
  The SDK's server base URLs have been replaced as part of the rebrand:

  - `api.tryvital.io` → `api.us.junction.com`
  - `api.eu.tryvital.io` → `api.eu.junction.com`
  - `api.sandbox.tryvital.io` → `api.sandbox.us.junction.com`
  - `api.sandbox.eu.tryvital.io` → `api.sandbox.eu.junction.com`

  The environment enum has also been renamed:

  - `VitalEnvironment` → `JunctionEnvironment`

  If you pass an environment value through the enum (e.g. `JunctionEnvironment.Production`), the new URL is picked up automatically once you switch to the renamed enum. If you pass a literal URL string into the client `environment` option, you must update the string yourself.
- **Error classes renamed** — [migration steps](MIGRATION.md#rename-error-classes)
  The thrown error classes have been renamed:

  - `VitalError` → `JunctionError`
  - `VitalTimeoutError` → `JunctionTimeoutError`

  Update `catch` blocks and `instanceof` checks. Both classes are still re-exported from the package root.
- **Path parameters are now inline on the request object** — [migration steps](MIGRATION.md#inline-path-parameters)
  Methods that previously accepted a positional path-parameter argument followed by a request object now take a single request object containing the path-parameter fields. For example:

  ```typescript
  // Before
  client.labTests.bookPhlebotomyAppointment("order_id", { bookingKey: "..." });

  // After
  client.labTests.bookPhlebotomyAppointment({ orderId: "order_id", body: { bookingKey: "..." } });
  ```

  Methods that already took only a request object are unaffected.
- **Per-endpoint request types renamed to read verb-first** — [migration steps](MIGRATION.md#verb-first-request-types)
  Generated per-endpoint request interface names have been reordered so the verb leads, e.g. `LabTestsGetOrdersRequest` is now `GetOrdersLabTestsRequest` and `LabTestsGetRequest` is now `GetLabTestsRequest`. Most callers pass an object literal and never name these types, but if you import them for explicit type annotations on helper functions, you must update the type names.
- **File-download responses return a Web Response wrapper** — [migration steps](MIGRATION.md#binary-response)
  Endpoints that download binary content (PDFs, raw lab files) now resolve to a `core.BinaryResponse` object with Web-platform methods: `arrayBuffer()`, `blob()`, `bytes()`, and `stream()` (which returns a Web `ReadableStream`). Code that previously called `.pipe()`, `.toString()`, or otherwise treated the body as a Node `Buffer` or `Readable` must read it through one of these methods.
- **Node 18+ required at runtime** — [migration steps](MIGRATION.md#node-18-runtime)
  The SDK now relies on the platform's native `fetch` and `FormData` globals. Node 16 and earlier are no longer supported. The previously bundled `node-fetch` runtime dependency and the Node-16 multipart shim have been removed. If you run on Node 16, upgrade to Node 18 LTS (or newer) before adopting this release.

## New & improved

- **New top-level resources: lab accounts, order transactions, compendium search**
  The SDK now exposes three new top-level resource modules:
  
  - `client.labAccount` — read your team's lab accounts (`getTeamLabAccounts`).
  - `client.orderTransaction` — fetch the consolidated order-transaction view (`getTransaction`).
  - `client.compendium` — convert and search lab-test compendium entries (`convert`, `search`).
  
  Accompanying model types appear under the namespace export (`Junction.ClientFacingLabAccount`, `Junction.ClientFacingOrderTransaction`, `Junction.ConvertCompendiumResponse`, etc.). See the API reference for endpoint details.
- **Inline anonymous types in method signatures** — [migration steps](MIGRATION.md#inline-types)
  Method signatures and IDE hovers now show inline object types instead of named imports for many anonymous shapes. The named types are still exported, so existing imports continue to compile; the change is mostly visible when reading hover docs.
- **Raw response shapes formalized — `*V2InDB` types are now `*Raw`**
  Endpoints whose responses were previously typed as `*V2InDB` now use `*Raw` types. The values are unchanged; only the type names differ:
  
  - `ActivityV2InDB` → `RawActivity`
  - `BodyV2InDB` → `RawBody`
  - `DeviceV2InDB` → `RawDevices`
  - `SleepV2InDB` → `RawSleep`
  - `WorkoutV2InDB` → `RawWorkout`
  
  If you imported one of the old names directly, switch to the new `Raw*` type.
- **Client-scoped passthrough fetch**
  The client now exposes a `fetch` method that proxies a Web-style fetch call through the same auth provider, base URL, and default headers configured on the client. Use it to call endpoints the SDK does not yet model, without re-implementing auth and URL handling.
  
  ```ts
  const res = await client.fetch("/v3/some/new/endpoint", { method: "GET" });
  const data = await res.json();
  ```
- **Optional fields now reflect API nullability** — [migration steps](MIGRATION.md#respect-nullable)
  Fields that the API marks as nullable are now typed as nullable/optional in TypeScript, matching what you actually receive on the wire. Existing code that already accounted for missing fields keeps working; code that assumed non-nullable values may need a guard or non-null assertion in places where the new typing surfaces a possible `null`.
- **Corepack-aware packageManager field**
  The published `package.json` declares `packageManager: pnpm@10.x`. Repos using Corepack will automatically switch to pnpm when running scripts in this package's directory. Consumers using npm or yarn directly remain unaffected; CI configs that pin a specific package manager via Corepack enforcement may need to opt out for this dependency.

## Removed

- **Public types removed** — [migration steps](MIGRATION.md#public-types-removed)
  Three top-level public types were removed from the SDK with no equivalent. If you imported any of these, drop the import:
  
  - `AuthType` — was used by the legacy `email_auth` flow only.
  - `ManualProviders` — was the parameter type for the now-removed `connectManualProvider` method (one of the legacy link methods, see above). With that method gone, this enum is removed too.
  - `ClientFacingUserKey` — the endpoint that used to return this model now returns `ClientFacingUser` instead. If you depended on the user-key shape, switch to reading the user fields off `ClientFacingUser` directly.
- **Legacy link methods removed** — [migration steps](MIGRATION.md#link-legacy-removed)
  These methods have been deprecated for over two years and were never part of the documented Junction Link integration path; they should not have been in the SDK in the first place. They are removed in this release:

  - `link.emailAuth`
  - `link.passwordAuth`
  - `link.startConnect`
  - `link.connectManualProvider`
  - `link.tokenState`
  - `link.isTokenValid`

  The supporting request/body classes that backed these methods are removed alongside them:

  - `BeginLinkTokenRequest`
  - `EmailAuthLink`
  - `PasswordAuthLink`
  - `LinkTokenValidationRequest`
  - `ManualConnectionData`

  If you have call sites referencing these methods, see the Junction Link API reference for the documented integration path.
