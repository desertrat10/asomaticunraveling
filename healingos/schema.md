# healingOS — Schema

What this system tracks, and how. Built as a personal fork of the CommsOS
methodology, adapted from institutional communications work to patient data
sovereignty. 

> This documents a system that runs, not one that's proposed. Every field
> below is captured daily using Claude skills with MD outputs downloaded into the healingOS infra built on Obsidian. The point of publishing it is so the next patient
> doesn't have to start from a blank notebook — though the notebook works too.

## Design principles

- **Three symptom tracks, kept separate.** Pain, tissue tension, and autonomic
  symptoms are logged independently because they don't move together — tension
  can drop while pain holds, and the autonomic layer runs on its own schedule.
  Collapsing them hides the pattern.
- **Same fields daily, so weeks compare to weeks.** Consistency over
  completeness. A fixed format captured every day beats a rich format captured
  sometimes.
- **Tension is the leading indicator; pain lags.** Pain surfaces 6–48 hours
  after the load that caused it. The tissue scan moves closer to real time,
  which is what makes daily capture worth the friction.
- **External structure replaces internal sensation.** The proprioceptive system
  this condition compromised can't report cumulative load reliably. The log is
  the feedback loop the body can't provide.
- **Patient-owned, patient-structured.** The data, the taxonomy, the format, and
  the distribution belong to the patient.
- **Output is a provider-readable brief, not just a log.** The daily capture
  exists to be surfaced at the point of care.

## Daily capture

One file per day, `YYYY-MM-DD.md`, captured end of day. Target: under two
minutes. Machine-readable flags in YAML frontmatter (see below) so the weekly
review can query the month instead of rereading it.

### Track 1 — Pain (structural / mechanical)

| Field | Type | Notes |
|---|---|---|
| Level | 0–10 | Reflects load absorbed 6–48 hrs ago, not today's activity |
| Locations | list | neck · mid-back / inter-scapular · right trap/shoulder · lower back · left arm/hand · other |
| New or unusual | text | Anything different from yesterday; new radiating patterns flagged |

### Track 2 — Tissue tension (body scan)

Twelve muscle groups, each scored 0–5 on the same scale daily. Flag L/R where
asymmetric. Skip a group at 0 if cleaner — the absence is itself data.

**Scale:**

| Score | Label | Meaning |
|---|---|---|
| 0 | Quiet | No awareness |
| 1 | Background | Present, not demanding attention |
| 2 | Noticeable | Aware during activity / posture changes |
| 3 | Bracing | Actively holding / guarding |
| 4 | Dominant | Driving postural compensation |
| 5 | Reactive | Spasming, twitching, cramping |

**Tissue groups:** suboccipitals · temporalis · SCM · scalenes · upper trap ·
levator scap · mid trap · rhomboids · lower trap · thoracic erectors ·
brachial plexus (note L/R + location of referred sensation) · lumbar
paraspinals / QL

### Track 3 — Autonomic / neurological

Three sub-checks. These are the proprioceptive-dysfunction markers — easy to
under-report, high-signal.

| Sub-field | Type | Notes |
|---|---|---|
| Positional lightheadedness | present? + frequency + trigger + duration + intensity | Triggers: sit-to-stand / lying-to-sitting / bending / head turns |
| Brain fog | present? + type | Types: cervical (effortful, worsens across desk blocks, lifts with movement) / hormonal-dietary / mixed-unsure |
| Other autonomic | present? + specifics + context | Blurred/soft vision, spatial disorientation, other; note post-PT / afternoon / continuous |

### Context

| Field | Type | Notes |
|---|---|---|
| What the day demanded | free text (1–3 sentences) + tagged factors | See factor list below |
| What helped | intervention + effect (1–5 or note) | The reactive-vs-generative signal: are resets rescuing or maintaining? |
| Tomorrow's shape | brief + adjustments | Forward-looking; today's data feeds tomorrow's decisions before symptoms arrive |

**Tagged factors** (record only those that applied, as checked items):
extended screen · non-floor-desk sitting · sustained cervical flexion (note
duration tolerance if reduced) · extension + rotation positions · PT / needling
(note what was worked) · training (type + duration) · high-output
meeting/speaking · sleep disruption prior night (note position if relevant) ·
travel

### YAML frontmatter (flags)

Set at capture so the weekly review can surface states without rereading:

```yaml
date: YYYY-MM-DD
day_of_week: [Mon/Tue/...]
pt_phase: [current phase]
flare_state: [baseline | elevated | flaring_L1 | flaring_L2 | flaring_L3]
autonomic_flag: [true/false]
positional_lightheadedness_flag: [true/false]
brain_fog_flag: [true/false]
brachial_flag: [true/false]
pt_session_today: [true/false]
training_today: [true/false]
travel: [true/false]
new_symptom: [true/false]
red_flag: [true/false]
```

## Provider brief format

One-page summary a clinician can read in the first minute of a session.
Structure: a prose summary of the interval since last session, then structured
bullets — flare trajectory, autonomic frequency, notable tissue changes, new
presentations, interventions that helped vs. didn't, demand factors, and any
patient note/request for the session. Clinical terminology throughout; written
to be scanned in 1–2 minutes.

## Weekly summary format

The Sunday synthesis, built from the week's daily entries. Reports pain trend,
autonomic symptom frequency, interventions used, the reactive-to-generative
ratio, and any flagged escalations pulled forward from the YAML. Patterns are
reported where the data supports them across multiple entries; single-day
readings stay noise, not signal.

## Registries (longitudinal layer)

Beyond the daily logs, confirmed patterns are promoted into two graded
registries: a claims registry (what helps, what triggers, what's emerging) and
a contraindications registry (known triggers with mechanisms). Each entry
carries a source type and confidence level, so the strength of evidence behind
any claim is legible rather than assumed.

## Versioning / how this evolved

Notes on what changed and why — schema adjustments, fields added or retired,
corrections caught in practice. (Example already in the record: the tagged-factor
list was corrected to retain only factors that applied, after early entries
propagated the full unchecked checklist.)

---

*This schema reflects the system as run by its builder. Fork it, break it, make
it fit your body. — healingOS*
