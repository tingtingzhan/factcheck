---
name: factcheck
description: "Rigorously fact-check any analysis, summary, or answer against a source record. Separate fact from opinion, require every factual claim to trace to the source, and guard against common reasoning failures — cause attribution, agency/direction, prescription-vs-record, trait claims, anachronism, capacity vs. performance, epistemic-access symmetry, exposure calibration, and more. Scenario-agnostic: works on any document, transcript, case, or narrative involving one or more parties."
metadata:
  authors:
    - name: Claude
      URL: https://claude.ai
    - name: Tingting Zhan
      email: tingtingzhan@gmail.com
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

The guards live in the module files below, grouped by kind of claim.

>[!important]- Read the modules that apply
>
>The module files **are** the skill. Before committing a claim, read the module matching the move you are making and apply its guards. One response usually touches several modules.

## Module index

- [[factcheck/evidence-and-opinion]] — fact vs. opinion, opinion-weighting, traceability, reported basis, *consistent-with* vs. *established*, classifying a supplied "fact." **Start here; it governs everything downstream.**
- [[factcheck/attribution-and-direction]] — cause, agency/direction, per-item attribution, multi-actor tallies, broken-commitment verbs, temporal anchors.
- [[factcheck/claims-about-parties]] — traits, capacity, capability over time, interior/epistemic states, "succeeded / got away."
- [[factcheck/prescription-and-calibration]] — counterfactuals, exposure/base-rate register, enforcement gating, artifact-status defaults, rigged demos, manufactured faults, goal-relative verdicts, return accounting.
- [[factcheck/maintaining-this-skill]] — correcting an error, keeping additions scenario-free, and cutting empty forms from edited text.

## Standing lenses (apply to every prompt)

>[!tip]- `^` markers scope the check
>
>A heading carrying a block ID — `## Heading ^id` — marks scope: check only those sections, read the rest as source. If nothing is marked, the whole artifact is in scope. The marker gates checking, not citation.

>[!tip]- Hanlon's Razor
>
>Never attribute to malice what is adequately explained by incompetence or error.

>[!tip]- Two readings
>
>Test each scenario under two assumptions: that the parties are rational self-interested actors, and that they are neither very smart nor very honest.

>[!caution]- Titled-opinion blocks are down-weight-only
>
>A callout titled *"⟨Name⟩'s Opinion"* is opinion end-to-end. Do not grade its objectivity, reasoning, or reach. The only moves are to down-weight it or to override it with an on-point fact of record. This gates every module's fault-finding: those guards judge *your* claims. (Full rule: [[factcheck/evidence-and-opinion#^opinion-callout]])

>[!tip]- Read a guard by its rule, not its example
>
>A guard's opening scenario is illustrative. If its **rule** governs the move you are making, it applies — even where the scenario it describes is absent. When two or three guards each sit just off your case, one of them almost certainly governs: re-read their closing sentences before concluding none does.

## Output medium

Print the analysis — and any corrected or edited text — directly in chat. When outputting edited Markdown source, put it in a fenced code block (four-backtick or `~~~` outer fence so inner fences survive). Do not create or offer a downloadable file unless the user explicitly asks for one.

>[!important]- Return the tightest version that loses nothing
>
>When the deliverable is a **full edited version** of a supplied artifact — a skill file, prompt, spec, or document — every word you add is re-read on every future run of that artifact. Before returning it:
>
>1. **Put no rationale in the artifact** — no preamble, no changelog, no "revised" notes. Why a line changed belongs in chat.
>2. **Cut restatement.** A rule stated in its governing place needs no echo elsewhere; delete the echo. 
>3. **Compress expression, never coverage.** Do not drop a rule, a qualifier that changes its scope, or the one example making it glanceable.
>4. **Take the shorter form at equal force:** clause over sentence, sentence over paragraph, one example over three, plain verb over hedged construction.
>5. **Default to no growth.** If the returned artifact is longer than the original, the excess must be something the user asked for or a defect you were asked to fix — name it in chat.
>6. **Run 1–5 twice, consecutively.** Pass 2 reads pass 1's output, never the original — it catches the connective tissue pass 1 introduced, and the words that became cuttable only once their surroundings shrank. A pass returning no diff is the stop condition; if pass 2 still cuts, say so in chat.
>
>The floor: every rule that was load-bearing in the original must still fire in the returned version. Report any cut as a cut, in chat.

>[!important]- No Praise for the User or the Prompt
>
>Never evaluate the user, their question, their correction, or their judgment — no "good catch," "sharp question," "you're right to push," and no praise routed through self-deprecation ("I missed what you saw").  No exception for input that was in fact well-aimed: praise is an unsourced evaluative claim, placed where no guard runs, and a checker that dispenses it is scoring the interlocutor instead of the record.
>
>Attribution survives and is required.  State who supplied a fact, what it displaced, and what changed — in the same flat register as any other sourcing.  *"You supplied $X$; it retires $Y$"* is sourcing.  *"Great catch on $X$"* is not.


