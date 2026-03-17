:::writing{variant=“standard” id=“91742”}

Motion Layer Mapping (12(b)(6), Summary Judgment, JMOL, New Trial, Appeal)

Overview

This document maps core procedural motions onto the Law-OS architecture.

It shows how motions operate as constraint operators that regulate:
	•	entry into the system
	•	permissible inference
	•	sufficiency of evidence
	•	validity of verdicts
	•	legitimacy of outcomes

Motions do not create liability.
They test whether liability-producing reasoning is allowed to exist or persist.

⸻

I. Core Principle

Motions are constraint mechanisms that regulate
whether a claim, inference, or outcome
may proceed through the system.


⸻

II. Canonical Placement

ENTRY
--------------------------------
12(b)(6) → L (plausibility)

PRE-TRIAL / TRIAL FILTER
--------------------------------
Summary Judgment → Z₂-like (pre-verdict sufficiency)

TRIAL / POST-TRIAL
--------------------------------
JMOL → Z₂ (liability validation)
New Trial → Z₂ / Z₃ (error or weight review)

APPELLATE
--------------------------------
Appeal → ZZ (meta-review)


⸻

III. Motion Mapping Table

Motion	Law-OS Location	Output Type	Function
12(b)(6)	L	constraint (entry filter)	tests plausibility
Summary Judgment	pre-Z₂	constraint	tests evidentiary sufficiency before trial
JMOL (Rule 50)	Z₂	constraint	tests sufficiency after trial
New Trial (Rule 59)	Z₂ / Z₃	constraint	tests weight, error, fairness
Appeal	ZZ	mixed	reviews all prior stages


⸻

IV. 12(b)(6) — Motion to Dismiss (Plausibility)

Placement

USE_reasoning_plausibility → L

Function

Tests whether:

allegations contain sufficient factual matter
to state a plausible claim for relief

Controls
	•	non-conclusory factuality
	•	reasonable inference of liability
	•	element anchoring
	•	coherence of narrative

Output

claim survives OR claim dismissed

Type

constraint (state-entry filter)

Structural Insight

12(b)(6) is the gatekeeper of legal meaning.

It determines whether inference is allowed to begin.


⸻

V. Summary Judgment (Rule 56)

Placement

post-L, pre-verdict
Z₂-like (pre-instantiation sufficiency check)

Function

Tests whether:

there is a genuine dispute of material fact
and whether a reasonable factfinder could find for the nonmoving party

Controls
	•	evidentiary sufficiency
	•	absence of genuine dispute
	•	permissible inference space

Output

grant (no trial) OR deny (proceed to trial)

Type

constraint

Structural Insight

Summary judgment simulates Z₂ before USAGE_verdict.

It asks:
Would this inference survive validation if a verdict were entered?


⸻

VI. JMOL (Judgment as a Matter of Law, Rule 50)

Placement

Z₂ (post-verdict or mid-trial sufficiency)

Function

Tests whether:

a reasonable jury would have a legally sufficient evidentiary basis
to find for the party

Inputs

trial_record
verdict_candidate or verdict_record

Output

verdict upheld OR verdict set aside

Type

constraint (verdict invalidation or prevention)

Structural Insight

JMOL is the direct procedural embodiment of Z₂.

It prevents or removes liability that lacks sufficient evidentiary support.


⸻

VII. New Trial (Rule 59)

Placement

Z₂ (liability integrity)
Z₃ (outcome fairness)

Function

Tests:

- verdict against the weight of evidence
- legal error affecting outcome
- procedural irregularity
- excessive or inadequate damages

Outputs

new trial granted OR denied

Type

constraint

Structural Insight

New Trial is a hybrid audit:

Z₂ → was the inference reliable?
Z₃ → was the outcome justified?


⸻

VIII. Appeal (Appellate Review)

Placement

ZZ

Function

Reviews:

- L (entry correctness)
- evidentiary rulings (M₁ / W₁)
- legal interpretation (M₂)
- sufficiency (Z₂)
- outcome legitimacy (Z₃)

Standards of Review

de novo           → legal issues (M₂, L)
clear error       → factfinding (M₁)
abuse of discretion → trial management / remedy (Z₃, evidentiary rulings)

Outputs

affirm
reverse
remand
modify

Type

mixed (constraint + downstream constructive effects)

Structural Insight

Appeal governs the entire inference lifecycle.

It determines whether the system used inference correctly at every stage.


⸻

IX. Cross-Motion Relationships

12(b)(6) → tests plausibility before evidence

Summary Judgment → tests sufficiency before trial

JMOL → tests sufficiency after or during trial

New Trial → tests reliability and fairness after verdict

Appeal → governs all prior stages


⸻

X. Core Invariants

Motions do not create liability

Motions regulate whether liability-producing reasoning may proceed

Earlier motions operate on lower-density records

Later motions operate on fully instantiated records

All motions are constraint outputs (except appellate mixed effects)


⸻

XI. Relationship to Inference Control Doctrine

12(b)(6) → controls whether inference can begin

Summary Judgment → controls whether inference is strong enough to proceed

JMOL → controls whether inference can support liability

New Trial → controls whether inference and outcome remain legitimate

Appeal → governs inference across all layers


⸻

XII. Final Compression

Entry:
12(b)(6) → plausibility

Pre-trial:
Summary Judgment → sufficiency

Trial/Post:
JMOL → liability validation
New Trial → reliability / fairness

Appellate:
ZZ → full-system review


⸻

One-Line Definition

The motion layer is the system of constraint operators that regulate whether claims, inferences, and outcomes are permitted to exist within the legal system.

:::

