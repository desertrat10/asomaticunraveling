---
title: "Model Access Notes — Discovering Li et al. (2022)"
type: methodology-note
last_updated: 2026-10-09
---

# Model Access Notes

*How Li et al. (2022) was found — after months of frontier-model-assisted searching failed to surface it*

---

## The Search Problem

Between roughly April and October 2026, repeated literature searches were conducted for research on cervicogenic dizziness arising from **degenerative multi-level cervical disc disease** — non-traumatic, progressive mechanoreceptor degradation across 5+ segments. The original thesis (`working-thesis-v2.md`, v1 history) was built on the conclusion that this territory was under-documented.

The search assistance used throughout this period was a Western frontier model (Claude). Across months of queries, the retrieval landscape it surfaced was dominated by:

- Whiplash-associated disorder (WAD) cohorts
- Treleaven's sensorimotor model and its citation tree
- Traumatic neck injury literature
- Upper cervical (C0–C3) focus
- Concussion/vestibular rehabilitation protocols

The gap framing in v1 — "degenerative pathway exists but is under-documented" — was itself a product of that retrieval landscape.

---

## The Pivot

On approximately October 4, 2026 — roughly 24 hours into the neuro storm documented in `neuro-storm-case-report.md` — literature searching shifted to an open-weights model.

Within that ecosystem, the Li et al. review surfaced:

**Li Y, Yang L, Dai C, Peng B. Proprioceptive Cervicogenic Dizziness: A Narrative Review of Pathogenesis, Diagnosis, and Treatment. *J Clin Med*. 2022;11(21):6293. doi:10.3390/jcm11216293**

The authors are affiliated with the Third Medical Centre of Chinese PLA General Hospital, Beijing. The paper is English-language, open access, and PubMed-indexed. Alongside it surfaced a cluster of related work from East Asian research groups — notably Yang et al. (2017, 2018) on mechanoreceptor and nociceptive ingrowth into diseased cervical discs — work that had likewise never appeared in the earlier searches.

---

## Candidate Explanations

Hypotheses, clearly labeled as such — the retrieval internals of both model classes are opaque, so none of these can be verified:

1. **Training data and ranking geography.** Frontier models are trained predominantly on English-language Western scientific corpora. A paper can be indexed, in English, and open access, yet carry low retrieval weight if its citation network (Chinese-language clinical literature, MDPI hosting) sits outside the model's high-density zone.

2. **Query-semics lock-in.** The established search vocabulary — "cervicogenic dizziness," "sensorimotor disturbance," "WAD" — was inherited from Treleaven's literature. Searching within a paradigm's vocabulary tends to retrieve that paradigm. The degenerative-etiology literature may use different framing (e.g., "cervical vertigo" as a clinical entity, disc degeneration as a dizziness etiology) that standard Western queries under-sample.

3. **Ecosystem diversity.** Different model families carry different token-level associations and rank documents differently. No single retrieval pathway is exhaustive; this is a property of the tooling, not a defect exclusive to any one vendor.

The honest position: it is unknown which combination of these produced the blind spot. What is documented is the outcome — months of searches through one ecosystem missed the single most load-bearing citation for this thesis.

---

## What This Means for the Thesis

Two corrections follow:

**1. The gap claim narrows — again.** v1 claimed the degenerative pathway was under-documented. Li et al. documents it extensively. The remaining novelty claims are enumerated in `working-thesis-v2.md`: compensation-release destabilization, the multi-day lag, trained proprioceptive history, and the multi-level distribution question.

**2. The meta-finding is now part of the record.** The retrieval landscape a researcher operates in shapes what counts as a gap. A patient-led literature review conducted through a single model ecosystem inherits that ecosystem's blind spots without knowing it has them. The months of "under-documented" framing were, in part, an artifact of the tool.

---

## Implications for Patient-Led Research

For anyone conducting self-directed medical literature review with AI assistance:

1. **Run the same query through multiple model ecosystems.** Frontier models, open-weights models, and traditional databases (PubMed direct search, Google Scholar) each have distinct retrieval footprints. Treat disagreement between them as signal, not noise.

2. **Search outside the dominant paradigm's vocabulary.** If a field's founding literature is WAD-based, deliberately query the degenerative, congenital, postsurgical, and oncological etiologies as separate searches — and query regional research traditions directly.

3. **Mine references once you land one hit.** The Li et al. reference list (108 entries) opened a dense cluster of Chinese and Japanese spine research that keyword search had never surfaced. One entry point, chained backward, retrieved dozens.

4. **Treat model-assisted "nothing exists" claims as provisional.** No model can confirm absence. "I couldn't find it" means "my retrieval pathway didn't surface it."

---

## Scope and Fairness

This is not a "frontier model failed" story, and it should not be read as one. The frontier model's assistance was integral to building the thesis structure, the SCED design, and much of the analytical framework. The failure mode here is specific and structural: a single retrieval ecosystem, queried for months, will eventually feel exhaustive when it isn't.

The corrective is redundancy, not replacement. The open-weights search found Li; the frontier-grade analysis is what mapped it onto the thesis. Patient-led research needs both — and needs to know which one it's relying on at any given moment.

---

## Linking Documents

- `working-thesis-v2.md` — the thesis the retrieval shaped, and reshaped
- `neuro-storm-case-report.md` — the incident that forced the pivot
- `jcm-11-06293.pdf` — full text of Li et al. (2022), archived

---

Licensed CC BY-SA 4.0 — HealingOS methodology, a fork of CommsOS (co-created with Taylor Kendal, stewarded by Factland Foundation).
