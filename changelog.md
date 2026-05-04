## 1.0.0 - 2026-05-04
### Breaking Changes
* **`MealInDbBaseClientFacingSource`** now includes a required `calendarDate: string` field (YYYY-mm-dd format). Existing code that constructs or destructures this type must be updated to handle the new field.
* **`JunctionEnvironment`** URLs have changed from `tryvital.io` to `junction.com` for all four environments (`Production`, `ProductionEu`, `Sandbox`, `SandboxEu`). If you hard-coded or compared against the old URLs, update accordingly.
### Added
* **`AuthOption`** union type and **`auth`** property on `BaseClientOptions` allow per-client authentication overrides: pass `false` to disable auth, a function returning auth headers, an `AuthProvider` instance, or raw `HeaderAuthProvider.AuthOptions`.
* **`isAuthProvider`** type-guard helper is now exported from the core auth module.
* **`forwardCompatibleEnum_`** schema builder added for forward-compatible enum deserialization.
### Fixed
* **`Micros`**, **`SampleData`**, and **`LabResultsRaw`** serializers now correctly allow `null` values inside record fields, matching the actual API contract.

## 0.0.1 - 2026-05-01
* Initial SDK generation
* 🌿 Generated with Fern

