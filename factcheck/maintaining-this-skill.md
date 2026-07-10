# Maintaining this skill — correcting errors & editing the guards

Meta-guards that fire at *edit* time rather than analysis time: how to turn a
correction into a durable fix, and how to keep any conversationally-added guard
free of the context it was born in.


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
>Do **not** edit an `.md` skill file in place.   Deliver the patched file — or the exact diff — for the user to apply.


>[!important] Keep Conversational Additions Skill-Agnostic
>
>When a guard is added to or edited into this skill through conversation, verify the wording carries no context from any other skill that happened to be co-invoked in that conversation. factcheck guards are scenario-agnostic and portable; a live discussion will be anchored in some particular record, and its specifics leak easily into the phrasing.
>
>Before committing an addition, strip every non-general element:
>- named parties, roles, or characters from the worked example;
>- domain-, artifact-, or fact-specific nouns pulled from the record at hand;
>- any premise true only of the co-invoked skill's setup, not of records in general.
>
>Keep the worked example in the conversation; let only the abstracted reasoning class enter the skill file. Test each clause: would it read correctly against an unrelated record? If it needs the originating scenario to make sense, it is not yet a guard — re-abstract it.
