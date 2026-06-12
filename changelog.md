## [2.0.0] - 2026-06-12
### Breaking Changes
- **`LabReportResultIsSensitive`** — renamed to **`LabReportResultSensitivity`**; update all references from `LabReportResultIsSensitive` to `LabReportResultSensitivity`.
- **`LabReportResult.isSensitive`** — field renamed to `sensitivity` (typed as `LabReportResultSensitivity`); update all property accesses from `.isSensitive` to `.sensitivity`.

### Added
- **`AlignExpr`**, **`AlignExprCarry`**, **`CarryForwardExpr`**, **`CarryBackwardExpr`**, and **`CarryNearestExpr`** — new types supporting post-aggregation carry/fill operators for CQ queries.
- **`Query.align`** — new optional field accepting an `AlignExpr` to materialise and fill missing datetime buckets after group-by aggregation.
- **New enum values** `google_health` added to `OAuthProviders` and `Providers`; `too_many_pages` added to `ParsingJobFailureReason`.

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
