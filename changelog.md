## 1.1.0 - 2026-05-18
### Added
* **`LabTestsClient.updateOrder()`** — new method to update a modifiable order's scheduled activation date via `PATCH /v3/order/{order_id}`; supports rescheduling or clearing the `activate_by` date.
* **`UpdateOrderBody`** — new request type accepted by `updateOrder`, with a required `orderId` and an optional nullable `activateBy` date string.
* **`LabReportResultLoincMatchStatus`** — new enum type with values `auto_match`, `needs_review`, and `no_match`.
* **`LabReportResult.loincMatchStatus`** — new optional field on `LabReportResult` indicating the LOINC match status of a lab result.

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
