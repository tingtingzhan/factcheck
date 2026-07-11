# Evidence & opinion — what counts as fact

The foundation layer: how to tell fact from opinion, how much to weight opinion,
the requirement that every claim trace to the record, the *consistent-with* vs.
*established* discipline, and how to classify a "fact" the user hands you. Apply
these before anything in the other modules.


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


>[!caution] Consistency vs. Establishment
>
>Apply the *"consistent with $X$ but does not establish $X$"* distinction uniformly, not selectively.
>
>Where the record is merely _consistent with_ a conclusion, it must be stated as consistent-with, not as established.


>[!caution] Verify a Correction Against the Record BEFORE Labeling It
>
>When the user issues a correction or supplies a "fact," do **not** classify it as *new / external / unsupported* on recall alone. First **search the source record** for it. Only then label:
>- **already on record** $\rightarrow$ cite the exact passage (`.md` file + line) and treat as established; do not call it "new information";
>- **contradicts the record** $\rightarrow$ flag the conflict, quote both;
>- **genuinely absent** $\rightarrow$ *then* mark it an addition/speculation.
>
>Declaring a correction "not in the record" without having searched is itself a retrieval failure —and mis-sourcing an on-record fact as "new" wrongly implies the user's correction lacks a basis it in fact has. Retrieve, then label.


>[!caution] Label Fidelity — use the record's own term; don't swap in an adjacent category
>
>When the source record gives a thing its own name — a clause, an offense, a status, a mechanism, a diagnosis, a rule — carry **that** name. Before substituting a more familiar taxonomic label, verify the substitute's **defining criteria** are actually met by the item on record.
>
>Adjacent categories that share a domain and a rough shape are the trap: they differ in the **consequences, scope, or elements** that make the classification matter. Swapping one for its neighbor keeps a real anchor in the record — so the claim survives a shallow traceability check — while asserting a category the record does not support. This is the labeling analogue of *Per-Item Attribution*: there, don't carry an attribute across sibling items; here, don't carry a claim across sibling *categories*.
>
>- **Name it from the record, not from the nearest label in memory.** If the record calls it $X$, do not rename it to the cousin-category $Y$ because $Y$ is the term you reach for first.
>- **If you must classify beyond the record's wording,** state it as your classification, cite the defining feature that puts the item in that bin, and confirm no feature on record excludes it.
>- **Different consequences ⇒ different category.** If $X$ and $Y$ would license different downstream claims — different remedies, thresholds, obligations, or exposure — they are not interchangeable, and the substitution is a factual error, not a paraphrase.
