---
title: Recovery Windows
project: asomaticunraveling
metric: days from load event to return-to-baseline
license: CC BY-SA 4.0
---

# Recovery Windows

The primary outcome variable for the experiment engine: how long the system takes to return to baseline after a defined load event. The long-term goal is compression of this number across comparable events.

**Metric definition.** Recovery window = number of days from the load event to the first day baseline pain and body-scan scores return to pre-event levels. Onset lag (6–48 hr delayed symptom surfacing) is inherent to the condition and is part of the window, not excluded from it.

**Condition tags.** Each entry notes the maintenance condition in effect, because professional bodywork cadence is a variable until Phase 0 locks it constant.
- `no-recent-bodywork` — >~3 weeks since last professional body session
- `cadence-held` — monthly bodywork cadence in effect

| Date | Load event | Event class | Recovery window (days) | Condition | Notes |
|---|---|---|---|---|---|
| 2026-07 | Back-to-back Boulder conferences (2×6 hr) | Social / environmental | ≥7 (elevated at logging) | no-recent-bodywork | Baseline dataset. Recovery stall coincides with ~30-day bodywork gap. |

*Add a row per logged experiment. Once cadence is held constant, the trend line across `cadence-held` entries is the deliverable.*
