# FTracker v1.3.9 — Audit Cleanup

Base: FTracker_v1.3.8_Workout_Checkbox_Catalog_Fixed(3).zip

## Applied confirmed fixes
- Fixed malformed CSS declaration in modal safe-area rule (`position: relative; padding-top: ...`).
- Removed proven no-op self-alias assignments for `saveCatalogProduct` and `addFoodEntry` from the final canonical block.
- Kept the existing working final bindings for `renderCatalogList` and `updateWorkoutProgressUI`.
- Unified manifest and Service Worker build/cache version to `ftracker-v1.3.9-audit-cleanup`.

## Audit findings intentionally not aggressively removed
Several historical override chains remain, including Progress Picker, Import/Backup and Workout Progress generations. They are functionally active or have uncertain dependencies. They were not deleted without dependency proof to avoid breaking the stable PWA.

## Validation
- JavaScript syntax checked for every inline script block.
- PWA version/cache identifiers synchronized.
- Archive root contains application files directly (no nested project folders).

## FTracker v1.4.0 — Index Engine v1
- Added goal-aware Index Engine with BODY / TRAINING / optional NUTRITION blocks.
- Missing blocks are excluded and remaining weights are normalized.
- Added calibration / preliminary / full confidence phases.
- Added measurement trend processing with confirmation-based anomaly filtering, EMA smoothing and dead zones.
- Added goal-specific interpretation for gain, cut and maintenance.
- Training consistency now treats 13–17 workouts per 30 days as the ideal zone; 15 is no longer a hard pass/fail target.
- Consistency combines frequency, distribution and historical smoothing to tolerate isolated missed sessions.
- Updated visible app version, manifest version/build and Service Worker cache version.
