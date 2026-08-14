## [2.0.0] - 2026-08-14
### Breaking Changes
- **`LabReportResultIsSensitive`** — renamed to **`LabReportResultSensitivity`**; replace all imports and references with the new name.
- **`LabReportResult.isSensitive`** — field renamed to `sensitivity` (typed as `LabReportResultSensitivity`); update all property accesses accordingly.

### Added
- **`LabTestsClient`** unmatched-result methods — `listUnmatchedResultTestCases()`, `createUnmatchedResultTest()`, `getUnmatchedResultTest()`, `listUnmatchedResults()`, `getUnmatchedResult()`, `acceptUnmatchedResult()`, and `resolveUnmatchedResult()` provide a full management surface for unmatched lab results.
- **`CompendiumClient.searchOrderableTests()`** — new method to search orderable tests by provider IDs and target lab via `POST /v3/compendium/search_orderable_tests`, accepting `SearchOrderableTestsBody` and returning `SearchOrderableTestsResponse`.
- **Lab-test pricing types** — new types (`GetLabTestPricingResponse`, `LabTestPanelPricing`, `MarkerPricingResponse`, `PricingModifierRange`, and related) plus optional `includePricing` and `labAccountId` fields on `GetPaginatedLabTestsRequest` and `GetMarkersLabTestsRequest`.
- **Match-review webhook types** — `ClientFacingMatchReviewChanged`, `ClientFacingMatchReviewUpdated`, and `MatchReviewWebhookPayload` added for lab-result match-review lifecycle events.
- **`JunctionError.requestId`** — new getter returning the `x-request-id` response header; `JunctionTimeoutError` now extends `JunctionError` for consistent error properties.

### Changed
- **`additionalBodyParameters`** in `RequestOptions` — now merged into the serialized request body across all resource clients (`CompendiumClient`, `AggregateClient`, `LinkClient`, `UserClient`, `InsuranceClient`, `OrderClient`, `PayorClient`, `TestkitClient`, and others).
- **`LabReportClient` parse-job endpoints** — `@beta` designation removed; these endpoints are now considered stable.
- **New enum values and optional fields** — `Labs.Mtl`, `OAuthProviders.GoogleHealth`, `Providers.GoogleHealth`, `ParsingJobFailureReason.TooManyPages`/`ProcessingError`, and `ClientFacingResource.ResultTable` added; optional fields `logoUrl`, `website`, `sourceInterpretation`, `pricing`, and `Query.align` added to existing types.

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
