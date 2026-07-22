# factcheck

Scenario-agnostic reasoning-rigor guards for fact-checking any analysis, summary, or answer against a **source record** (a document, transcript, dataset, case file, or narrative). Separate fact from opinion, trace every claim to the record, and guard against common reasoning failures.

`SKILL.md` is the entry point: the source-record definition, the always-on lenses, and an index. The guards live in the module files, grouped by the kind of claim each checks. Read the module matching the move you are about to make; a single response usually touches several.

```
factcheck/
├── README.md
├── SKILL.md                          # hub: intro, standing lenses, module index
├── evidence-and-opinion.md           # fact vs. opinion, traceability, consistent-with vs. established
├── attribution-and-direction.md      # cause, direction, per-item roles, tallies, broken-commitment verbs
├── claims-about-parties.md           # trait, capacity, capability-over-time, epistemic-access, "got away"
├── prescription-and-calibration.md   # counterfactuals, exposure register, enforcement gating, artifact status
└── maintaining-this-skill.md         # edit-time meta-guards: error repair, keep additions skill-agnostic
```

## Using it

- **Analyzing a record** → apply `evidence-and-opinion.md` first (it governs the rest), then whichever of `attribution-and-direction.md`, `claims-about-parties.md`, and `prescription-and-calibration.md` match the claims in play. The lenses in `SKILL.md` run on every prompt.
- **Editing this skill** → follow `maintaining-this-skill.md`. Guards are delivered as a patched file or exact diff, never edited in place, and any conversationally-added guard is stripped of scenario-specific context first.
