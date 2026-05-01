## 1.0.0 - 2026-05-01
### Breaking Changes
* **`MealInDbBaseClientFacingSource`** — a new required `calendarDate` field (`string`, mapped from `calendar_date`) has been added to the interface. Any code that constructs this type without providing `calendarDate` will fail to compile. Add `calendarDate: "YYYY-mm-dd"` to all object literals or construction sites for this type.

## 0.0.1 - 2026-05-01
* Initial SDK generation
* 🌿 Generated with Fern

