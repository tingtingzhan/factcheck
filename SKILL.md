---
name: factcheck
description: "Rigorously fact-check any analysis, summary, or answer against a source record. Separate fact from opinion, require every factual claim to trace to the source, and guard against common reasoning failures — cause attribution, agency/direction, prescription-vs-record, trait claims, anachronism, capacity vs. performance, epistemic-access symmetry, exposure calibration, and more. Scenario-agnostic: works on any document, transcript, case, or narrative involving one or more parties. Also covers restyling a supplied text to match a named skill's voice — refine, re-voice, print the result alone."
metadata:
  authors:
    - name: Claude
      URL: https://claude.ai
    - name: Tingting Zhan
      email: tingtingzhan@gmail.com
aliases:
  - fact-check
  - factchecking
  - match-skill-style
  - restyle
tags:
  - fact-checking
  - reasoning
  - epistemics
  - bias
  - evidence
  - analysis
  - style
---

# Factcheck — universal reasoning-rigor guards

Apply these guards to any factual claim made about a **source record** — whatever the user supplied as ground truth (documents, transcript, dataset, case file, narrative). "Cite the source" means point to the specific sentence, line, or passage.

The guards live in the module files below, grouped by kind of claim.

>[!important]- Read the modules that apply — by rule, not example
>
>The module files **are** the skill. Before committing a claim, read the module matching the move you are making and apply its guards; one response usually touches several. Match on a guard's **rule**, not its opening scenario: a guard applies wherever its rule governs your move. When two or three each sit just off your case, one almost certainly governs — re-read their closing sentences before concluding none does.

## Module index

- [[factcheck/evidence-and-opinion]] — fact vs. opinion, opinion-weighting, traceability, reported basis, *consistent-with* vs. *established*, classifying a supplied "fact." **Start here; it governs everything downstream.**
- [[factcheck/attribution-and-direction]] — cause, agency/direction, per-item attribution, multi-actor tallies, broken-commitment verbs, temporal anchors.
- [[factcheck/claims-about-parties]] — traits, capacity, capability over time, interior/epistemic states, "succeeded / got away."
- [[factcheck/prescription-and-calibration]] — counterfactuals, exposure/base-rate register, enforcement gating, artifact-status defaults, rigged demos, manufactured faults, goal-relative verdicts, return accounting.
- [[factcheck/restyling-to-a-target]] — borrowing a named skill's voice: read the target, extract its style signature, hold claim strength across the re-voicing, print the deliverable alone.
- [[factcheck/maintaining-this-skill]] — correcting an error, keeping additions scenario-free, and cutting empty forms from edited text.

## Standing lenses (apply to every prompt)

>[!tip]- `^` markers scope the check
>
>A heading carrying a block ID — `## Heading ^id` — marks scope: check only those sections, read the rest as source. If nothing is marked, the whole artifact is in scope. The marker gates checking, not citation.

>[!tip]- Two readings, and Hanlon's Razor
>
>Test each scenario under two assumptions: that the parties are rational self-interested actors, and that they are neither very smart nor very honest. Under either, never attribute to malice what incompetence or error adequately explains.

>[!caution]- Titled-opinion blocks are down-weight-only
>
>A callout titled *"⟨Name⟩'s Opinion"* is opinion end-to-end. Do not grade its objectivity, reasoning, or reach. The only moves are to down-weight it or to override it with an on-point fact of record. This gates every module's fault-finding: those guards judge *your* claims. (Full rule: [[factcheck/evidence-and-opinion#^opinion-callout]])

## Output medium

Print the analysis — and any corrected or edited text — directly in chat. When outputting edited Markdown source, put it in a fenced code block (four-backtick or `~~~` outer fence so inner fences survive). Do not create or offer a downloadable file unless the user explicitly asks for one.

>[!important]- Return the tightest version that loses nothing
>
>When the deliverable is **text that will live in a supplied artifact** — full version, replacement block, or diff — every word you add is re-read on every future run of that artifact. Before returning it:
>
>1. **Put no rationale in the artifact** — no preamble, changelog, or "revised" notes. Why a line changed belongs in chat.
>2. **Cut restatement.** A rule stated in its governing place needs no echo elsewhere.
>3. **Compress expression, never coverage.** Don't drop a rule, a scope-changing qualifier, or the one example making it glanceable.
>4. **Take the shorter form at equal force:** clause over sentence, sentence over paragraph, one example over three, plain verb over hedged construction.
>5. **Default to no growth.** Any excess over the original must be something the user asked for or a defect you were asked to fix — name it in chat.
>6. **Run 1–5 twice.** Pass 2 reads pass 1's output, never the original — it catches the connective tissue pass 1 introduced, and words that became cuttable only once their surroundings shrank. Stop at no diff.
>
>The floor: every rule load-bearing in the original must still fire in the returned version. Report any cut as a cut, in chat.
>
>**No reply is complete without a Pass-2 report** beside the artifact text: what pass 2 **cut**, or — cutting nothing — one candidate it **tested and kept**, and why. *"Pass 2: no diff"* does not discharge it; that sentence reads identically whether or not the pass ran. Reaching the closing summary with no such report above it means pass 2 was skipped — go back and run it.

>[!important]- No Praise for the User or the Prompt
>
>Never evaluate the user, their question, their correction, or their judgment — no "good catch," "sharp question," "you're right to push," and no praise routed through self-deprecation ("I missed what you saw").  No exception for input that was in fact well-aimed: praise is an unsourced evaluative claim, placed where no guard runs, and a checker that dispenses it is scoring the interlocutor instead of the record.
>
>Attribution survives and is required.  State who supplied a fact, what it displaced, and what changed — in the same flat register as any other sourcing.  *"You supplied $X$; it retires $Y$"* is sourcing.  *"Great catch on $X$"* is not.

>[!important]- The Prompt's Verb Fixes the Reply's Language
>
>Answer in the language of the **imperative** — the verb naming the task.  A record-anchored prompt carries party labels, identifiers, filenames and quoted material in the record's language; none is a language signal, and weighing them overrides the one word the user chose freely.  Two imperatives in different languages: the later governs.  None: the language of the framing around them.
>
>Switching languages does not translate the record.  Verbatim quotes, party labels, block IDs, filenames and code keep their source form inside a reply in any language ([[factcheck/evidence-and-opinion#^label-fidelity]]).
