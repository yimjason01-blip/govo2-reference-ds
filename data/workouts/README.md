# GOVO2 synthetic workout fixtures

Static prototype data for Codex / HTML / React design exploration.

Fetch paths from the Vite prototype:

- `/data/workouts/manifest.json`
- `/data/workouts/ramp.json`, `/data/workouts/ramp-002.json`, `/data/workouts/ramp-003.json`
- `/data/workouts/intervals.json`, `/data/workouts/intervals-002.json`, `/data/workouts/intervals-003.json`
- `/data/workouts/zone2.json`, `/data/workouts/zone2-002.json`, `/data/workouts/zone2-003.json`

The manifest lists three synthetic fixtures per workout type.

## Shape

Each file contains:

- `_meta`: fixture ID, schema, source policy
- `athlete`: shared synthetic rider assumptions
- `rideRecord`: GOVO2 RideStore-style wrapper with `details.type` and `details.payload`
- `summary`: UI-ready summary values
- `protocol`: workout prescription
- `rawSamples`: enriched second-by-second samples with `elapsedSec`, `power`, `hr`, plus prototype-only cadence/L-R/target/phase fields

The nested `rideRecord.details.payload.rawSamples` mirrors the app's minimal persisted raw sample shape: `elapsedSec`, `power`, `hr`.

These are synthetic non-user data for rendering only.
