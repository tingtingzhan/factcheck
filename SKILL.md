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

Apply these guards to any factual claim made about a **source record**. The
"source record" is whatever the user has provided as the ground truth for the
scenario: the uploaded documents, transcript, dataset, case file, or narrative.
Wherever a guard says "cite the source," it means point to the specific
sentence, line, or passage in that provided material.

The guards live in the module files below, grouped by the kind of claim they
check. This `SKILL.md` is only the hub: the load-bearing rules are in the
modules.

>[!important] Read the modules that apply
>
>These module files **are** the skill. Before committing any claim, read the
>module that matches the move you are about to make and apply every guard in it.
>A single response usually touches several modules; when it does, run each
>relevant module's checks, not just the closest one.

## Module index

- **`evidence-and-opinion.md`** — what counts as fact vs. opinion, how to weight opinion, traceability of every claim, *consistent-with* vs. *established*, and how to classify a "fact" the user supplies. **Start here; it governs everything downstream.**
- **`attribution-and-direction.md`** — who did what, to whom, in which direction, on which item: cause, agency/direction, per-item attribution, multi-actor tallies, and broken-commitment verbs.
- **`claims-about-parties.md`** — claims about a party's traits, capacity, capability across time, interior/epistemic states, and whether they "succeeded" or "got away."
- **`prescription-and-calibration.md`** — counterfactuals and advice, exposure/base-rate register, enforcement gating, artifact-status defaults, rigged demonstrations, and manufactured faults.
- **`maintaining-this-skill.md`** — how to correct an error and edit these files without importing scenario-specific context.

## Standing lenses (apply to every prompt)

Unlike the module guards, which fire on a specific move, these two lenses run on
every analysis regardless of subject.

>[!tip] Hanlon's Razor
>
>For all prompts, analyze with Hanlon's Razor (https://en.wikipedia.org/wiki/Hanlon%27s_razor) in mind: *"Never attribute to malice that which is adequately explained by stupidity."*


>[!tip] Homo economicus vs. Flawed Human
>
>For all prompts, analyze each scenario under two alternative assumptions:
>
>- that the person(s) or party(ies) are Homo economicus (https://en.wikipedia.org/wiki/Homo_economicus)
>- that they are not very smart and not very honest — flawed yet relatable, possessing the earnest imperfections of human nature
