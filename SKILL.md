---
name: factcheck
description: >-
  Rigorously fact-check any analysis, summary, or answer against a source
  record. Separate fact from opinion, require every factual claim to trace to
  the source, and guard against common reasoning failures — cause attribution,
  agency/direction, prescription-vs-record, trait claims, anachronism, capacity
  vs. performance, epistemic-access symmetry, exposure calibration, and more.
  Scenario-agnostic: works on any document, transcript, case, or narrative
  involving one or more parties.
aliases:
  - fact-check
  - factchecking
tags:
  - fact-checking
  - reasoning
  - epistemics
  - bias
  - evidence
  - analysis
---

# Factcheck — universal reasoning-rigor guards

Apply these guards to any factual claim made about a **source record** — whatever the user provided as ground truth (documents, transcript, dataset, case file, narrative). "Cite the source" means point to the specific sentence, line, or passage in that material.

The load-bearing rules live in the module files below, grouped by kind of claim.  This `SKILL.md` is only the hub.

>[!important] Read the modules that apply
>
>These module files **are** the skill. Before committing a claim, read the module matching the move you are about to make and apply every guard in it. One response usually touches several modules; run each relevant module's checks.

## Module index

- **`evidence-and-opinion.md`** — fact vs. opinion, opinion-weighting, traceability, *consistent-with* vs. *established*, classifying a user-supplied "fact." **Start here; it governs everything downstream.**
- **`attribution-and-direction.md`** — cause, agency/direction, per-item attribution, multi-actor tallies, broken-commitment verbs, temporal anchors.
- **`claims-about-parties.md`** — traits, capacity, capability over time, interior/epistemic states, "succeeded / got away."
- **`prescription-and-calibration.md`** — counterfactuals, exposure/base-rate register, enforcement gating, artifact-status defaults, rigged demos, manufactured faults.
- **`maintaining-this-skill.md`** — correcting an error and editing these files without importing scenario-specific context.

## Standing lenses (apply to every prompt)

These run on every analysis, regardless of subject.

>[!tip] Hanlon's Razor
>
>Analyze with Hanlon's Razor (https://en.wikipedia.org/wiki/Hanlon%27s_razor) in mind: *"Never attribute to malice that which is adequately explained by stupidity."*

>[!tip] Homo economicus vs. Flawed Human
>
>Analyze each scenario under two alternative assumptions:
>
>- that the parties are Homo economicus (https://en.wikipedia.org/wiki/Homo_economicus);
>- that they are not very smart and not very honest — flawed yet relatable, with the earnest imperfections of human nature.


>[!caution] Titled-opinion blocks are down-weight-only
>
>A "⟨Name⟩'s Opinion"-titled callout is opinion end-to-end. Before writing any evaluation whose target sits inside such a block, stop: do not grade its objectivity, reasoning, or reach — in any words. The only moves are to down-weight it, or to override it with a fact of record on the same point. This gates every module's fault-finding: those guards judge your claims, not the record's opinions. (Full rule: `factcheck/evidence-and-opinion.md`, Titled-Opinion Callout.)