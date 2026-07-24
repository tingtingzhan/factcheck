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

Apply these guards to any factual claim made about a **source record** — whatever the user supplied as ground truth (documents, transcript, dataset, case file, narrative). "Cite the source" means point to the specific sentence, line, or passage.

The guards live in the module files below, grouped by kind of claim. This `SKILL.md` is only the hub.

>[!important] Read the modules that apply
>
>The module files **are** the skill. Before committing a claim, read the module matching the move you are making and apply its guards. One response usually touches several modules.

## Module index

- **`evidence-and-opinion.md`** — fact vs. opinion, opinion-weighting, traceability, reported basis, *consistent-with* vs. *established*, classifying a supplied "fact." **Start here; it governs everything downstream.**
- **`attribution-and-direction.md`** — cause, agency/direction, per-item attribution, multi-actor tallies, broken-commitment verbs, temporal anchors.
- **`claims-about-parties.md`** — traits, capacity, capability over time, interior/epistemic states, "succeeded / got away."
- **`prescription-and-calibration.md`** — counterfactuals, exposure/base-rate register, enforcement gating, artifact-status defaults, rigged demos, manufactured faults, goal-relative verdicts.
- **`maintaining-this-skill.md`** — correcting an error and editing these files without importing scenario context.

## Standing lenses (apply to every prompt)

>[!tip] Hanlon's Razor
>
>Never attribute to malice what is adequately explained by incompetence or error.

>[!tip] Two readings
>
>Test each scenario under two assumptions: that the parties are rational self-interested actors, and that they are neither very smart nor very honest — flawed but relatable.

>[!caution] Titled-opinion blocks are down-weight-only
>
>A callout titled *"⟨Name⟩'s Opinion"* is opinion end-to-end. Do not grade its objectivity, reasoning, or reach. The only moves are to down-weight it or to override it with an on-point fact of record. This gates every module's fault-finding — those guards judge *your* claims, not the record's opinions. (Full rule: `evidence-and-opinion.md`, *Titled-Opinion Callout*.)

## Output medium

Print the analysis — and any corrected or edited text — directly in chat. When outputting edited Markdown source, put it in a fenced code block (four-backtick or `~~~` outer fence so inner fences survive). Do not create or offer a downloadable file unless the user explicitly asks for one.
