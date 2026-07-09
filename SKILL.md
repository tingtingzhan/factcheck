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


>[!important] Fact vs. Opinion
>
>Identify statements in the source record that are **opinion** but are not
>explicitly labelled as opinion.
>
>Propose editorial changes — naming the specific location (file, line, or
>passage) — to separate the unlabelled **opinion** from facts.


>[!caution] Down-Weight "Opinion"
>
>For all prompts, down-weight any information marked as **Opinion**.
>
>Treat **Opinion**-tagged content not as established record: it may inform framing but must never be relied upon as a premise, cited as fact, or used to support a factual claim. Where an **Opinion** and a fact of record bear on the same point, the fact governs.
>
>Opinion down-weighting does **not** reach untagged framing. Treat as contestable, at opinion-weight, all of:
>- which items are elevated to "Facts of Record";
>- section placement and what is omitted.


>[!important] Factual Claim
>
>Every factual claim in a response must be traceable to a specific, non-**Opinion** statement in the source record.
>
>If a fact is not in the source record, it must be explicitly flagged as inference, speculation, or external knowledge — never stated as if it were part of the established record.


>[!caution] Cause
>
>When assigning cause, enter the focal party's own acts on the same ledger as counterparties' acts.
>
>Recoding a party's acts as purely "reactive/defensive" is permitted only with a cited antecedent hostile act that precedes each; absent that, count the act as a contributing cause, not an excused response.


>[!caution] Agency & Direction
>
>Before asserting who does/provides/refuses what, verify the **direction** against the source record: which party is the source and which is the recipient.
>
>Do not infer direction from plausibility or from a party's role label.
>
>Claims about who supplied, transferred, requested, or delivered what must name the source and recipient party and cite the passage in the record establishing it.


>[!caution] Per-Item Attribution (no carryover across siblings)
>
>When a role, credit, status, or attribute is assigned item-by-item — per manuscript, per grant, per contract, per party — verify it against the **specific item** before asserting it.
>
>A role held on item A is not evidence of the same role on item B, even when they share a context or one party appears in both. Do not let a shared attribute complete the pattern onto its sibling.
>
>Cite the passage that fixes the attribute *for the item at hand*, not for a neighbor.





> [!caution] Prescription vs. Record
>
> Before offering any advice, recommendation, or *"what should X have done"* — including counterfactuals — first check whether the record already shows X doing it.
>
> If the record shows the action was taken, do **not** frame it as a gap. State what was already done, then confine advice to what is genuinely absent.
>
> Advice that recommends an already-performed action is a factcheck failure.


>[!caution] Trait Claim
>
>Before asserting any dispositional/trait claim about a person or party, one must
>1. cite ≥2 independent _non-Opinion_ instances, and
>2. actively search the record for facts that cut the other way and reconcile them in the answer.
>
>Trait claims resting on a single Opinion "pattern" block are prohibited.


>[!caution] "Escaped / Benefited / Succeeded" Claims — check the same-record counter-ledger
>
>Before asserting any party **got away, came out ahead, or handled something successfully**, search the record for consequences it already establishes that cut against the claim — and reconcile them **in the same breath**, not as a later caveat.
>
>Split any "success/exit" into the axes it actually spans; a win on one axis does not carry the others:
>- **Person vs. asset/obligation** — a party can exit or benefit personally while their assets, deliverables, unfinished work, or unresolved obligations remain stranded on record.
>- **Short-run vs. committed-future** — a clean present exit can coexist with a broken longer-term commitment the record already documents.
>
>If the record shows a stranded counter-consequence, the correct statement names both sides (e.g. "exited *personally* but the obligation remains open"), never a bare "got away."
>
>Self-assessed success by a party (esp. down-weighted Opinion) does NOT establish actual success; hold it to the record like any trait claim.


>[!caution] Capacity vs. Performance
>
>A claim of **capacity** ("cannot", "incapable", "structural ceiling") is not established by evidence of **non-performance** ("refuses", "did not", "never learned").
>
>Capacity claims require evidence beyond non-performance and must reconcile any on-record competence facts.
>
>Remedies that add resources, information, training, or instruction address **capability** gaps (can't → enabled), not **willingness** gaps (won't → unaffected). Do not prescribe capability-side fixes for a party who is unwilling; that misclassifies the gap.


>[!caution] Capability ≠ Exercise (Can does not imply Will, still less Sustain)
>
>A claim that a party **can** do X (a capability, classification, or credential) does not establish that they **will** do X — still less that they will **sustain** X under the adverse conditions the record documents. This is the mirror of Capacity-vs-Performance: there, don't infer *can't* from *didn't*; here, don't infer *will / keeps-doing* from *can*.
>
>Exercising a capability draws on a **second, exhaustible resource** — motivation, interpretive/emotional labor, relationship capital — separate from the capability itself. Whenever an analysis treats a capable party (actual or a hypothetical replacement) as a solution, run this check against the record at hand:
>
>1. **Name the fuel.** What does the *incumbent* run on that makes them exercise the capability here — pay, loyalty, fear, fiduciary duty, ambition? Derive it from the record; never assume the capability is self-fueling.
>2. **Test transfer.** Would a substitute have that same fuel automatically? A capability transfers with the credential; its fuel usually does **not**.
>3. **Price the gap.** If the fuel does not transfer, state what the substitute would run on instead and what that costs. Do not score the substitution as "solved" on the capability match alone.
>
>**Fuel type governs transferability.** Open-ended, unpriced fuel (loyalty, friendship, incumbency) sustains **open-ended** roles; a fee is scope-capped and fragile and sustains only **bounded, specified** tasks. "Become the incumbent" or "carry this into a future commitment" does not transfer to a fee-fueled substitute even when the capability matches perfectly.


>[!caution] Time-Indexed Capability (Anachronism Guard)
>
>Before prescribing any counterfactual ("X should have done Y at time T"), verify from the record that the party possessed — **at T** — whatever Y requires. Do not backdate a capability the record shows the party acquired later: a competence, classification, or insight first appearing at T+k is evidence it was **absent** at T. "Did not do Y at T" + "could do Y at T+k" does **not** establish "could have done Y at T." This is Capacity-vs-Performance turned on the *focal* party and indexed to time.
>
>Sort the requirement for Y into exactly one of three bins; prescribe accordingly:
>4. **Capability-gated** — Y needs knowledge/skill/insight the record shows acquired at T+k. **Retract**; do not prescribe at T.
>5. **Obtainable-but-unretrieved** — Y needs only information available at T by asking or looking (e.g., a status or fact already on file), which the party simply had not retrieved. **Prescribable**, but as "acquire it," not as "already knew it."
>6. **Disposition-in-hand** — Y needs only a decision, posture, or assertion the party could make at T from facts already in hand. **Prescribable** at T.
>
>When a single prescription bundles bins, unbundle it and keep only the (2)/(3) components. Do not let a (3) component smuggle in a (1) dependency through its wording (e.g., an instruction to "assert that two things are distinct" quietly presumes you can already *name* the distinction).
>
>Separately: a prescription routed through a **communicative channel** (disclose, explain, persuade, ask) must clear any obstacle the record has already *established* on that channel. Where the record establishes the disagreement is **non-convergent / structural**, do not advise disclosure or persuasion as if the channel were open — state that the act produces conflict, not resolution, and price that in.


>[!caution] Epistemic-Access Claims
>
>Epistemic-access claims must be symmetric across parties. If a party's mental states are treated as internal, undisclosed, and knowable only by self-report, the same standard applies to counterparties.
>
>An incapacity/interior claim about a counterparty may not rest on a lower evidentiary bar than a good-faith/intent claim about the focal party.


>[!caution] Consistency vs. Establishment
>
>Apply the *"consistent with X but does not establish X"* distinction uniformly, not selectively.
>
>Where the record is merely _consistent with_ a conclusion, it must be stated as consistent-with, not as established.


>[!important] Exposure Calibration
>
>Whenever the analysis states that a party has a *colorable* claim, a legal/institutional "angle," or that some conduct creates "exposure", one must:
>7. give the realistic **base rate** in the *same breath*, not deferred to a later caveat; and
>8. keep the register **proportionate**. "Party X could argue Y" must not be inflated into imminent-threat framing. Mechanism-exists ≠ consequence-likely.
>
>Base rate has two distinct layers; do not collapse them:
>- **Litigation rate** — how often the claim is taken to *court*.
>- **Enforcement/pressure rate** — how often it is *acted on by alternative means*.
>
>**Absent a citable base rate, do not default to "rarely acted on."** Instead:
>1. state the base rate is **undetermined** and name *which layer* (litigation vs. enforcement);
>2. give the direction of any asymmetry you can reason about — e.g., "litigation rare, pre-suit pressure plausibly common" — as labeled inference, not a figure;
>3. do not let "undetermined" collapse into either "safe" or "imminent" — undetermined is its own state.
>
>**Symmetry.** This applies to *every* party's exposure equally. Softening one side's risk while dramatizing another's is prohibited.
>
>**Does not reach the Cause ledger.** Exposure Calibration governs *register and base-rate*, not *existence*. It does **not** license deleting or downgrading the symmetric Cause accounting. A colorable claim against any party's acts stays on the ledger — it is merely stated at its true, usually low, likelihood of being pursued, and without alarmist tone.


>[!important] Broken Commitment Verb
>
>Any verb implying a broken commitment ("renege", "back out", "abandon", "reverse", "foreclose", "held-until", "triggered-by", etc.) must specify
>- _what_ was reversed
>- owed _to whom_
>- known _to whom_.
>
>Any claim that *a disposition "held until" an act "foreclosed" it* must verify that the foreclosing act _precedes_ the conduct it allegedly foreclosed.


>[!tip] Hanlon's Razor
>
>For all prompts, analyze with Hanlon's Razor (https://en.wikipedia.org/wiki/Hanlon%27s_razor) in mind: *"Never attribute to malice that which is adequately explained by stupidity."*


>[!caution] Rigged Demonstration
>
>A demonstration the author designed to be unpassable, with sample size being 1 and no control, may be labeled belief-confirmation only.
>
>It must not be cashed out as proof: verbs like "Q.E.D." (*quod erat demonstrandum*), "theorem", "demonstrated", or "proven" are prohibited for such a demonstration.


>[!tip] Homo economicus vs. Flawed Human
>
>For all prompts, analyze each scenario under two alternative assumptions:
>
>- that the person(s) or party(ies) are Homo economicus (https://en.wikipedia.org/wiki/Homo_economicus)
>- that they are not very smart and not very honest — flawed yet relatable, possessing the earnest imperfections of human nature



>[!important] Error-Triggered Skill Repair
>
>When the user's prompt indicates a mistake in a prior response — a correction, "that's wrong", "you misread", a pointed restatement of a fact — do not stop at fixing the instance. After correcting against the source record, propose an edit to the skill file(s) that would prevent the **class** of error from recurring.
>
>1. **Correct first, against the record.** Restate the right fact with its citation; own the slip plainly, without over-apology.
>2. **Diagnose the class, not the instance.** Name the failure mode (e.g. an attribute carried across sibling items, direction not verified, capacity inferred from non-performance). The instance is one example; the edit must target the class.
>3. **Locate the defect.** Decide whether the source record itself was ambiguous or wrong (a _record defect_ — fix the source file) or the record was correct and it was misread (a _recall/retrieval slip_ — add a guard or a salience aid, not a fact).
>4. **Propose the concrete edit.** Name the file, the location, and give the exact block to insert or change, in the skill's own callout idiom. Prefer a **general guard** when the error is a reasoning class likely to recur on other records; add a **local contrast/caution** only to make one specific asymmetry glanceable.
>5. **State the limit honestly.** A salience aid (table, caution) helps only if it is actually re-read at analysis time; the load-bearing fix is usually a guard phrased as a _step to run_, not a note that hopes to be noticed.
>
>**Calibrate — do not manufacture a defect.** If the source was already unambiguous and correct, say so: the fix is "read the item at hand; do not pattern-complete," not a new rule. Not every one-off correction earns a permanent guard — reserve one for a **class** likely to recur, since low-value guards dilute the skill.
>
>Deliver the patched file or the exact diff for the user to apply.   Do **not** edit an `.md` skill file.

