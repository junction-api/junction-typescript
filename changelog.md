## 2.0.0 - 2026-09-24

### Added

* **Checkout** — added `CheckoutClient` methods for quotes and checkout sessions, with checkout webhook types.
* **Order pricing and tracking** — added `LabTestsClient.estimateOrderSetPricing()` and `getOrderTracking()`, pricing and tracking types, and an order-tracking webhook type.
* **Test-kit idempotency** — added optional idempotency controls when creating a test-kit order.
* **Result and status details** — added stale-result indicators and expanded order-status values.
* **Horizon AI device reliability** — added reliability columns for query selection, grouping, and aggregate expressions.

### Changed

* **Pricing conditions** — `PricingModifierMarkerPricingConditions.keys` is now required; callers constructing this type must supply it.

### Removed

* **Legacy timeseries methods** — removed the non-grouped `vitals` methods (including `steps()` and `heartrate()`) and their request types. Use the corresponding `*Grouped()` methods and handle their paginated grouped responses.
* **Hypnogram timeseries** — removed `hypnogram()`, `hypnogramGrouped()`, their types, and the sleep-stream hypnogram field. Use sleep-cycle summaries and events.
* **Deprecated event fields** — removed `ClientFacingSource.name`, `logo`, and `slug`; `ProviderConnectionCreated.source`; and `HistoricalPullCompleted.isFinal`. Use source context, `ProviderConnectionCreated.provider`, and the completed event itself.

## 1.3.0 - 2026-08-14

### Added

* **Orderable-test search** — added `CompendiumClient.searchOrderableTests()` and the related request and response types.
* **Unmatched lab-result management** — added methods for listing, testing, reviewing, accepting, and resolving unmatched results, together with match-review webhook types.
* **Lab-test pricing** — added pricing types and optional `includePricing` and `labAccountId` request fields.
* **Provider and lab coverage** — added Google Health provider and OAuth values and the MTL lab value.
* **Lab metadata** — added optional source interpretation, lab logo URL, and lab-location website fields.

### Changed

* **Request controls** — added SSE reconnection settings and support for merging `additionalBodyParameters` into serialized request bodies.
* **Errors** — `JunctionError.requestId` exposes the response request ID, and `JunctionTimeoutError` now extends `JunctionError` while remaining an `Error`.

### Beta

* **Aggregate and lab-report states** — added the result-table resource and processing-error parsing state without affecting the stable-surface SemVer calculation.

## 1.2.0 - 2026-06-05
### Added
* **`AlignExpr`** — new public symbol
* **`AlignExprCarry`** — new public symbol
* **`CarryBackwardExpr`** — new public symbol
* **`CarryForwardExpr`** — new public symbol
* **`CarryNearestExpr`** — new public symbol
### Changed
* **`Query`** — new optional field(s): align
### Beta
* **`LabReportResult`** — field(s) removed: isSensitive
* **`LabReportResultIsSensitive`** — public symbol removed
* **`LabReportResultSensitivity`** — new public symbol

## 1.1.0 - 2026-05-27
### Added
* **`LabTestsClient.updateOrder()`** — new method to update a modifiable order's scheduled activation date via PATCH, accepting an `UpdateOrderBody` with `orderId` and optional `activateBy`.
* **`UpdateOrderBody`** — new request type for the `updateOrder` method, supporting `orderId` and an optional nullable `activateBy` date string.
* **`LabReportResultIsSensitive`** and **`LabReportResultLoincMatchStatus`** — new enum types added as optional fields on `LabReportResult` to surface sensitivity classification and LOINC match status.
* **`GetOrderCommunicationSettingsResponse`**, **`PatchOrderCommunicationSettingsBody`**, and **`PatchOrderCommunicationSettingsResponse`** — new types for managing order-level SMS communication settings.

## 1.0.1 - 2026-05-07
* chore: deprecate sleep stream method
* Mark the `GetStreamBySleepId` method on `SleepClient` as deprecated via
* a `@deprecated` JSDoc tag. This signals to consumers that the method
* should no longer be used and may be removed in a future release.
* Key changes:
* Added `@deprecated` annotation to `SleepClient.GetStreamBySleepId`
* 🌿 Generated with Fern

## 1.0.0 - 2026-05-06
* Initial SDK generation
* 🌿 Generated with Fern
