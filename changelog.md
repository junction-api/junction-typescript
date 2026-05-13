## 1.1.0 - 2026-05-13
### Added
* **`LabReportResultLoincMatchStatus`** — new enum type with values `auto_match`, `needs_review`, and `no_match` representing the LOINC match status of a lab report result.
* **`LabReportResult.loincMatchStatus`** — new optional field on `LabReportResult` exposing the LOINC match status for a given result.

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
