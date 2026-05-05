## 1.0.0 - 2026-05-05
### Breaking Changes
* **`JunctionEnvironment`** URLs have changed from `tryvital.io` to `junction.com` domains — update any hardcoded URL comparisons or overrides to use the new `junction.com` endpoints.
* **`MealInDbBaseClientFacingSource`** now requires a `calendarDate: string` field — add `calendarDate` to any object literals or constructors that build this type.
### Added
* **`LabReportResultSampleType`** and **`LabReportResultMeasurementKind`** — new non-exhaustive enum types exposed as optional fields `sampleType` and `measurementKind` on `LabReportResult`.
* **`AuthOption`** type and `auth` property on `BaseClientOptions` — pass `false` to disable auth, a function, an `AuthProvider`, or auth options to override authentication per-client.
* **`isAuthProvider`** — new exported helper function to type-narrow an unknown value to `AuthProvider`.
### Fixed
* **`Micros`**, **`SampleData`**, and **`LabResultsRaw`** serialization now correctly handles nullable values within record fields.

## 0.0.1 - 2026-05-01
* Initial SDK generation
* 🌿 Generated with Fern

