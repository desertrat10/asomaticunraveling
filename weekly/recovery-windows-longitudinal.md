---
title: "Recovery Windows — Longitudinal Return-to-Baseline"
type: metric-dataset
metric: "days from load event to return-to-baseline"
last_updated: 2026-10-15
repo: asomaticunraveling
license: CC BY-SA 4.0
---

# Recovery Windows — Longitudinal Return-to-Baseline

> Extracted from weekly experiment logs W01–W19 (2026-04-13 through 2026-08-23). Each row represents a discrete load event with a documented recovery arc. Events without a logged return-to-baseline are marked open or estimated. Clinician names replaced with provider codes (PT1, PT2). Pain values use the midpoint convention where ranges are logged (e.g., 7/8+ = 7.5, 6/7 = 6.5).

## Recovery Arc Table

| Date | Event / Trigger | Immediate Cost | Latency to Flare | Peak Flare Level | Days to Baseline | Notes |
|---|---|---|---|---|---|---|
| 2026-04-15 | PT1 session — dry needling, cervical traction, bilateral soft tissue work | Upper traps at 7 post-needle (+24h) | ~24h to brachial onset; ~72h to peak | L2 (pain 7, five scan groups at 5) | ~4 days (L1 by +96h, resolving) | 96-hour cascade; left brachial inflammation at +48h, bilateral brachial by +96h. Release toolkit non-responsive at +48h mark. Longest documented arc in the early record. |
| 2026-04-20 | Substitute PT session — proprioceptor work, manual fascial release, laser headlamp exercise, ulnar nerve work. No needling (declined by patient request) | Autonomic onset ~4h post-session; couch-bound by evening | Same day | L2 (pain 7, nausea new to cluster) | 6 days (baseline_low by 2026-04-25; med-free by 2026-04-26) | First session without needling; still produced L2 flare. Nausea entered the post-PT autonomic cluster for the first time. Recovery confounded by cycle onset 9 days early on day 3. |
| 2026-04-22 | Coffeeshop session 1.5h + extended horizontal-rig typing + sleep deficit (recalibration day 2 post-PT) | Autonomic escalation post-coffeeshop; bilateral ulnar nerve irritation | Same day (afternoon onset) | L1 (pain 6, autonomic through evening) | ~1 day (improved by 2026-04-23 but autonomic continued) | Contrast pair: identical-duration coffeeshop on day 6 produced no reaction. Variable identified as recalibration window stacking, not seating itself. |
| 2026-04-24 | Travel day — 25 min surface-road drive + 1h seated podcast recording + manual gear setup (recalibration day 4, cycle day 2) | Dual-task motor/cognitive degradation; pain pre-med 7 + autonomic | Same day | L1 (pain 7 pre-med → 4 post-med) | ~1 day (best autonomic day on 2026-04-25) | First documented dual-task degradation. Real-time load detection and early exit preserved driving margin. |
| 2026-07-22 | Breakthrough-past-med event #1 (30-day window) | Pain exceeded medication coverage | — | Elevated | Unknown | Referenced in W19 PCP brief; daily log source not in the weekly export set. |
| 2026-07-28 | Breakthrough-past-med event #2 | Pain exceeded medication coverage | — | Elevated | Unknown | Referenced in W19 PCP brief. |
| 2026-07-31 | Lumbar spasm event (E8) — first in the 3-event cluster | Lower back spasm | — | — | Unknown | Start of the lumbar cluster (E8–E10). Lumbar/QL scan at 5 on this date (the only 5 in W16). |
| 2026-08-04 | Cardio PT session 2 — HR-gated protocol | — | — | — | Lumbar event within 48h | 3 of 4 cardio sessions in the protocol block followed by a lumbar event inside 48h. |
| 2026-08-12 | Cardio PT session 3 — HR-gated protocol | Threshold HR 108 (clean capture) | — | — | Lumbar event within 48h | — |
| 2026-08-13 | Bilateral brachial/ulnar recurrence | Brachial scan at 2 | — | — | Not returned to 0 (15+ consecutive non-zero scanned days through W19) | Last brachial 0 was 2026-08-07. Strength/grip check unactioned through W19. |
| 2026-08-17 | PT2 session 4 — manual therapy + cupping, right-side triggers, some left-side work | Pain 7/8+ (highest in 30-day window); five scan groups at 5; breakthrough-past-med | Same day | Elevated (not classified as formal flare) | 1 day (whole-scan drop to 2–3 by 2026-08-18) | Fastest resolution in W19 despite highest acute cost. New couch rig confounds the 24h recovery (two generators arriving same day). |
| 2026-08-19 | Cardio PT session 4 — stair stepper, 15:47 (longest in block), initiated at elevated baseline (pain 6, 48h post-PT2, post dog walk) | Pain 6→7; autonomic 0→3–4 (stop criterion breached at min 9, session ran 6:47 past it) | ~6.5h to lumbar spasm | Pain 7 sustained; lumbar spasm overnight (E10) | ~2 days (pain to 5/6 by 2026-08-21 pre-yoga; lumbar resolved by 2026-08-20 afternoon with yin pigeon) | First cardio session from an elevated symptom baseline. Stop-criterion deviation documented. Third lumbar event in the 2026-07-31 cluster. |
| 2026-08-21 | PT yoga session — full sequence, 29:49, all Zone 1, pain flat 5→5, autonomic 1→2 sub-stop | Session itself cost-neutral (pain flat, autonomic sub-stop) | Post-session window: two right-rotation spikes at coffeeshop (~2h after); bilateral by +24h | Elevated (self-logged 2026-08-22; no flare record created) | ~2 days (spikes diminished, fewer and less intense by 2026-08-23) | New descriptor: catching/rubbing/grating at cervical discs on active right rotation. Confounded by post-session driving and 2h non-controlled seating. X13 candidate event (twist exposure unverifiable from block-label-only logging). |

## Summary Statistics (W01–W19)

| Metric | Value |
|---|---|
| Total documented load events | 14 |
| Events with complete recovery arc | 6 |
| Events with partial/estimated arc | 3 |
| Events referenced without daily source | 5 |
| Median days to baseline (complete arcs) | ~2 days |
| Longest documented arc | 6 days (2026-04-20 substitute PT → med-free 2026-04-26) |
| Shortest documented arc | 1 day (2026-08-17 PT2 session → scan floor 2026-08-18) |
| Breakthrough-past-med events (30-day window ending 2026-08-17) | 3 (2026-07-22, 2026-07-28, 2026-08-17) |
| Lumbar spasm events (total confirmed) | 10 (E1–E10); 3 in the cluster since 2026-07-31 |
| Brachial non-zero streak | 15+ consecutive scanned days (since 2026-08-08 through end of W19) |

## Data Integrity

- Events from W03–W18 are referenced in aggregate where they appear in W01, W02, or W19 cross-references but have not been individually extracted from their source weekly logs. A complete extraction across all 19 weekly logs would populate the table fully.
- Pain values use the midpoint convention stated in W19 frontmatter.
- "Days to baseline" is measured to the first day at or below the patient's running baseline for that window, not to the first day of any improvement.
- Cycle-day data is absent or unreliable for most events — identified as the single highest-value data gap in the corpus (2026-08-20 pattern scan).
