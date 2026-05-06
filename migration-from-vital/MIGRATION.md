# Migration guide

_From `tryVital/vital-node@3.1.544` to the new release._

## Install the new package

<a id="install"></a>

This is a *replacement*, not a version bump — there is no shared release line between the old and new packages. Uninstall the old package, install the new one, and update every import to reference `@junction-api/sdk`.

Things to look out for:

- Aliased imports (`import { VitalClient as Client } from "@tryvital/vital-node"`).
- Sub-path imports (`import { ... } from "@tryvital/vital-node/serialization"`, `/link`, `/labTests`, etc.) — the new package keeps the same sub-paths, only the root changes.
- Lockfile pins (`package-lock.json`, `pnpm-lock.yaml`, `yarn.lock`), Dockerfile install commands, and CI cache keys that reference the old package name.
- Environment variables or config flags that follow the old brand (e.g. `VITAL_API_KEY`) — these are application-level and stay as-is unless you rename them yourself.

**Before:**

```bash
npm install @tryvital/vital-node
```

```typescript
import { VitalClient } from "@tryvital/vital-node";
```

**After:**

```bash
npm uninstall @tryvital/vital-node
npm install @junction-api/sdk
```

```typescript
import { JunctionClient } from "@junction-api/sdk";
```

## Rename `Vital` namespace to `Junction`

<a id="rename-namespace-export"></a>

All model types that were exposed under the `Vital` namespace are now under `Junction`. The model class names themselves are unchanged — only the namespace prefix changes. Watch for:

- Aliased namespace imports (`import * as V from ...`) — if already aliased, no source change is required.
- Type-only references in JSDoc / TSDoc comments, which the TypeScript compiler does not flag.

**Before:**

```typescript
import * as Vital from "@tryvital/vital-node";

function handle(test: Vital.ClientFacingLabTest) {
    // ...
}
```

**After:**

```typescript
import * as Junction from "@junction-api/sdk";

function handle(test: Junction.ClientFacingLabTest) {
    // ...
}
```

## Rename `VitalClient` to `JunctionClient`

<a id="rename-client-class"></a>

Update every construction site, type annotation, and re-export of the client class. Watch for:

- Aliased imports (`import { VitalClient as Client } from ...`).
- Type-only imports (`import type { VitalClient } from ...`).
- The associated namespace (`VitalClient.Options`) — the namespace was renamed alongside the class, so `VitalClient.Options` is now `JunctionClient.Options`.

**Before:**

```typescript
import { VitalClient } from "@tryvital/vital-node";

const client = new VitalClient({ apiKey: process.env.API_KEY! });
```

**After:**

```typescript
import { JunctionClient } from "@junction-api/sdk";

const client = new JunctionClient({ apiKey: process.env.API_KEY! });
```

## Update server base URLs (and `Environment` enum name)

<a id="rename-environment-enum"></a>

The four base URLs are replaced as follows:

| Old host                       | New host                          |
|--------------------------------|-----------------------------------|
| `api.tryvital.io`              | `api.us.junction.com`             |
| `api.eu.tryvital.io`           | `api.eu.junction.com`             |
| `api.sandbox.tryvital.io`      | `api.sandbox.us.junction.com`     |
| `api.sandbox.eu.tryvital.io`   | `api.sandbox.eu.junction.com`     |

The environment enum has also been renamed:

- `VitalEnvironment` → `JunctionEnvironment`

If you use the enum (`JunctionEnvironment.Production`, etc.), the new URL is picked up automatically because the enum's value changed alongside the rename. If you pass a literal URL string into the `environment` option, replace the host directly.

**Before:**

```typescript
import { VitalClient, VitalEnvironment } from "@tryvital/vital-node";

const client = new VitalClient({
    apiKey: process.env.API_KEY!,
    environment: VitalEnvironment.Production, // "https://api.tryvital.io"
});
```

**After:**

```typescript
import { JunctionClient, JunctionEnvironment } from "@junction-api/sdk";

const client = new JunctionClient({
    apiKey: process.env.API_KEY!,
    environment: JunctionEnvironment.Production, // "https://api.us.junction.com"
});
```

## Rename error classes

<a id="rename-error-classes"></a>

Update both `instanceof` checks and any `catch (err: VitalError)` annotations. Watch for:

- Custom error reporters that match by class-name string.
- Subclasses of `VitalError` defined in your own code.

**Before:**

```typescript
import { VitalError, VitalTimeoutError } from "@tryvital/vital-node";

try {
    await client.user.create({ clientUserId: "abc" });
} catch (err) {
    if (err instanceof VitalTimeoutError) {
        // ...
    } else if (err instanceof VitalError) {
        // ...
    }
}
```

**After:**

```typescript
import { JunctionError, JunctionTimeoutError } from "@junction-api/sdk";

try {
    await client.user.create({ clientUserId: "abc" });
} catch (err) {
    if (err instanceof JunctionTimeoutError) {
        // ...
    } else if (err instanceof JunctionError) {
        // ...
    }
}
```

## Move path parameters onto the request object

<a id="inline-path-parameters"></a>

For every method that previously took a positional path parameter (`id: string`, `orderId: string`, etc.), move that value onto the request object using its camelCase field name. The previous body argument moves under a `body` field on the same request object. Methods that already took only a request object are unaffected.

**Before:**

```typescript
await client.labTests.bookPhlebotomyAppointment("order_id", {
    bookingKey: "booking_key",
});
```

**After:**

```typescript
await client.labTests.bookPhlebotomyAppointment({
    orderId: "order_id",
    body: { bookingKey: "booking_key" },
});
```

## Update request type imports if you reference them by name

<a id="verb-first-request-types"></a>

The class-name change follows a fixed pattern: `<Resource><Verb>Request` becomes `<Verb><Resource>Request`. For example:

- `UserCreateRequest` → `CreateUserRequest`
- `LabTestsGetByIdRequest` → `GetByIdLabTestsRequest`
- `LabTestsGetOrdersRequest` → `GetOrdersLabTestsRequest`

If you only ever pass object literals to client methods, you do not need to update anything — the SDK accepts the same field names on the new types.

**Before:**

```typescript
import type { LabTestsGetOrdersRequest } from "@tryvital/vital-node";

function list(req: LabTestsGetOrdersRequest) {
    // ...
}
```

**After:**

```typescript
import type { GetOrdersLabTestsRequest } from "@junction-api/sdk";

function list(req: GetOrdersLabTestsRequest) {
    // ...
}
```

## Read file-download responses through the Web `Response` wrapper

<a id="binary-response"></a>

The returned `core.BinaryResponse` exposes `arrayBuffer()`, `blob()`, `bytes()`, and `stream()` — the same surface as a Web `Response`. Code that previously called `.pipe()`, `.toString()`, or otherwise treated the body as a Node `Buffer` or `Readable` must read it through one of these methods. To pipe into a Node writable stream, convert with `Writable.toWeb` (Node 18+).

**Before:**

```typescript
const pdfStream = await client.labTests.getResultPdf(orderId);
pdfStream.pipe(fs.createWriteStream("result.pdf"));
```

**After:**

```typescript
const pdf = await client.labTests.getResultPdf({ orderId });
const bytes = new Uint8Array(await pdf.arrayBuffer());
fs.writeFileSync("result.pdf", bytes);

// or pipe through the Web Streams API:
// pdf.stream()?.pipeTo(Writable.toWeb(fs.createWriteStream("result.pdf")));
```

## Run on Node 18 or newer

<a id="node-18-runtime"></a>

Bump your runtime (and CI matrix) to Node 18 LTS or newer. The SDK no longer pins `node-fetch` or a multipart polyfill, so older Node versions will fail at the first network call. Browser and modern serverless runtimes (Cloudflare Workers, Deno, Bun) that already provide global `fetch` and `FormData` work without additional setup.

**Before:**

```json
// package.json
{
    "engines": { "node": ">=16" }
}
```

**After:**

```json
// package.json
{
    "engines": { "node": ">=18" }
}
```

## Inline anonymous types in method signatures (no source changes)

<a id="inline-types"></a>

This is a documentation/hover-only change — your source code does not need to change. If you previously imported a named type for explicit annotations, the import still works; only the IDE hover representation differs.

**Before:**

```typescript
// Hovering a method showed a named import like Junction.LabTestsGetByIdRequest
```

**After:**

```typescript
// Hover now shows the object literal { labTestId: string; ... } inline
```

## Handle nullable fields where the API admits them

<a id="respect-nullable"></a>

Wherever the API documents a field as nullable, the TypeScript type now reflects that and the compiler will require an explicit guard or non-null assertion. Most call sites only need an optional-chain (`?.`) at the access point.

**Before:**

```typescript
const lab = await client.labTests.getById({ labTestId });
console.log(lab.description.toUpperCase());
```

**After:**

```typescript
const lab = await client.labTests.getById({ labTestId });
console.log(lab.description?.toUpperCase());
```

## Drop imports for removed public types

<a id="public-types-removed"></a>

Three names were exported from the package root in the old SDK but are not present in the new SDK:

- `AuthType` — was only used by the legacy `emailAuth` flow.
- `ManualProviders` — was the parameter type for the now-removed `connectManualProvider` method.
- `ClientFacingUserKey` — callers should switch to `ClientFacingUser`. The endpoint that previously returned `ClientFacingUserKey` now returns `ClientFacingUser`.

**Before:**

```typescript
import { Vital, AuthType, ManualProviders, ClientFacingUserKey } from "@tryvital/vital-node";
```

**After:**

```typescript
// AuthType and ManualProviders have no replacement — drop the imports.
// ClientFacingUserKey -> ClientFacingUser
import { Junction, ClientFacingUser } from "@junction-api/sdk";
```

## Drop calls to the legacy link methods

<a id="link-legacy-removed"></a>

These methods were deprecated for years and were never part of the documented Junction Link integration. Customer code that didn't reference them needs no migration. If you do have call sites, replace them with the Junction Link integration described in the API reference — there isn't a one-to-one drop-in, the legacy methods wrapped retired endpoints with no published equivalents.
