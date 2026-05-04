## 1.0.0 - 2026-05-04
### Breaking Changes
* **`MealInDbBaseClientFacingSource`** — new required field `calendarDate: string` added; existing code that constructs or assigns this type without `calendarDate` will fail to compile. Add `calendarDate` to all usages.
### Added
* **`AuthOption`** type and **`auth`** option on `BaseClientOptions` — pass `false` to disable authentication, a function returning auth headers, an `AuthProvider` instance, or `HeaderAuthProvider.AuthOptions` to override auth at the client level.
* **`isAuthProvider`** — new exported type guard in `core/auth` for checking whether a value implements the `AuthProvider` interface.
* **`forwardCompatibleEnum_`** — new schema builder utility for forward-compatible enum deserialization that tolerates unknown values.
### Changed
* **`Micros`**, **`SampleData`**, and **`LabResultsRaw`** serialization — record values in `minerals`, `traceElements`, `vitamins`, `performingLaboratories`, and `sampleInformation` now accept `null` values in addition to their typed values, improving compatibility with API responses.

## 0.0.1 - 2026-05-01
* Initial SDK generation
* 🌿 Generated with Fern

