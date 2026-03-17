CANONICAL LEGAL STATE MACHINE 

LEGAL STATE MACHINE — WITH OUTPUT MODES

STATE 0

NAME:
World Facts Exist

OUTPUT TYPE:
world

DESCRIPTION:
Events exist but have no legal status.

VALID TRANSITIONS:
→ Aₐ
→ L
→ Aₑ

⸻

STATE 1A

NAME:
Actionable Allegation Ready

ENTRY OPERATOR:
Aₐ

OUTPUT TYPE:
trigger

REQUIRES PRIOR INSTANTIATION:
false

DESCRIPTION:
Facts transformed into coercive trigger.

VALID TRANSITIONS:
→ W₀

⸻

STATE 2A

NAME:
Coercive Authority Authorized

ENTRY OPERATOR:
W₀

OUTPUT TYPE:
constraint

REQUIRES PRIOR INSTANTIATION:
false

DESCRIPTION:
Authorization exists but no artifact yet.

VALID TRANSITIONS:
→ USAGE₁

⸻

STATE 3A

NAME:
Coercive Authority Instantiated

ENTRY OPERATOR:
USAGE₁

OUTPUT TYPE:
constructive

REQUIRES PRIOR INSTANTIATION:
false

CREATES ARTIFACT:
true

DESCRIPTION:
Warrant/order exists in record.

VALID TRANSITIONS:
→ USE_world

⸻

STATE 4A

NAME:
Coercive Execution Completed

ENTRY OPERATOR:
USE_world

OUTPUT TYPE:
world

REQUIRES PRIOR INSTANTIATION:
true

DESCRIPTION:
World-level intervention occurs.

VALID TRANSITIONS:
→ STATE 0
→ Aₑ

⸻

STATE 5A

NAME:
Execution Challenge Triggered

ENTRY OPERATOR:
Aₑ

OUTPUT TYPE:
trigger

REQUIRES PRIOR INSTANTIATION:
false

VALID TRANSITIONS:
→ L
→ Z₁

⸻

STATE 1B

NAME:
Legally Cognizable Facts

ENTRY OPERATOR:
L

IMPLEMENTATION MODE:
USE_reasoning_plausibility

OUTPUT TYPE:
state_flip

REQUIRES PRIOR INSTANTIATION:
false

CREATES ARTIFACT:
false

DESCRIPTION:
Recognition achieved through plausibility.

IMPORTANT:
This does NOT create an artifact.
This does NOT require USAGE.

VALID TRANSITIONS:
→ W₁
→ Z₁

FAIL:
dismissal

⸻

STATE 2B

NAME:
Coercive Use Legality Determined

ENTRY OPERATOR:
Z₁

IMPLEMENTATION MODE:
USE_reasoning_coercive_legitimacy

OUTPUT TYPE:
constraint

REQUIRES PRIOR INSTANTIATION:
false

CREATES ARTIFACT:
false

DESCRIPTION:
Direct constraint evaluation of coercive use.

IMPORTANT:
No USAGE step occurs.

VALID TRANSITIONS:
→ W₁
→ termination

⸻

STATE 3B

NAME:
Verdict Reasoning Space Open

ENTRY OPERATOR:
W₁

OUTPUT TYPE:
constraint

REQUIRES PRIOR INSTANTIATION:
false

DESCRIPTION:
Authorization for reasoning.

⸻

STATE 4B

NAME:
Verdict Candidate Produced

ENTRY OPERATOR:
USE_reasoning_verdict

OUTPUT TYPE:
constructive

REQUIRES PRIOR INSTANTIATION:
false

CREATES ARTIFACT:
false

DESCRIPTION:
Produces candidate for instantiation.

IMPORTANT:
Still no artifact yet.

⸻

STATE 5B

NAME:
Verdict Instantiated

ENTRY OPERATOR:
USAGE_verdict

OUTPUT TYPE:
constructive

REQUIRES PRIOR INSTANTIATION:
false

CREATES ARTIFACT:
true

DESCRIPTION:
Verdict now exists in institutional record.

VALID TRANSITIONS:
→ Z₂

⸻

STATE 6B

NAME:
Liability Validated

ENTRY OPERATOR:
Z₂

IMPLEMENTATION MODE:
audit

OUTPUT TYPE:
constraint

REQUIRES PRIOR INSTANTIATION:
true

CREATES ARTIFACT:
false

DESCRIPTION:
Evaluates prior USAGE_verdict.

IMPORTANT:
Does NOT create a new artifact.
Consumes an existing one.

FAIL:
reversal / JMOL / new trial

⸻

STATE 7B

NAME:
Remedy Reasoning Space Open

ENTRY OPERATOR:
W₂

OUTPUT TYPE:
constraint

REQUIRES PRIOR INSTANTIATION:
false

⸻

STATE 8B

NAME:
Remedy Candidate Produced

ENTRY OPERATOR:
USE_reasoning_remedy

OUTPUT TYPE:
constructive

REQUIRES PRIOR INSTANTIATION:
false

CREATES ARTIFACT:
false

⸻

STATE 9B

NAME:
Remedy Instantiated

ENTRY OPERATOR:
USAGE_remedy

OUTPUT TYPE:
constructive

CREATES ARTIFACT:
true

VALID TRANSITIONS:
→ USAGE_judgment

⸻

STATE 10B

NAME:
Final Judgment Entered

ENTRY OPERATOR:
USAGE_judgment

OUTPUT TYPE:
constructive

REQUIRES PRIOR INSTANTIATION:
true

CREATES ARTIFACT:
true

VALID TRANSITIONS:
→ Z₃
→ ZZ

⸻

STATE 11B

NAME:
Outcome Reviewed

ENTRY OPERATOR:
Z₃

IMPLEMENTATION MODE:
audit

OUTPUT TYPE:
constraint

REQUIRES PRIOR INSTANTIATION:
true

CREATES ARTIFACT:
false

DESCRIPTION:
Reviews prior USAGE_judgment.

IMPORTANT:
Audit only. No artifact creation.

⸻

STATE 12B

NAME:
Appellate Review Completed

ENTRY OPERATOR:
ZZ

OUTPUT TYPE:
mixed

REQUIRES PRIOR INSTANTIATION:
true

CREATES ARTIFACT:
false (directly)

DESCRIPTION:
Can produce:

    constraint outputs:
        • affirm
        • reverse

    constructive downstream effects:
        • remand → new USAGE chain

IMPORTANT:
Requires branching logic.

⸻

STATE 13B

NAME:
Enforcement Authorized

ENTRY OPERATOR:
Wₑ

OUTPUT TYPE:
constraint

REQUIRES PRIOR INSTANTIATION:
true

⸻

STATE 14B

NAME:
Enforcement Instantiated

ENTRY OPERATOR:
USAGEₑ

OUTPUT TYPE:
constructive

CREATES ARTIFACT:
true

⸻

STATE 15B

NAME:
Judgment Executed

ENTRY OPERATOR:
USE_world

OUTPUT TYPE:
world

REQUIRES PRIOR INSTANTIATION:
true

=====================================================================
CORE SYSTEM RULE (ENFORCED)

IF output_type == constructive:
USAGE is required to create institutional artifact

IF output_type == constraint:
NO USAGE
output modifies permissions, validity, or downstream use

=====================================================================
KEY CORRECTIONS (LOCKED)

L:
state_flip (not constructive, not constraint-only)

Z₁:
constraint
no USAGE
direct evaluation

Z₂:
constraint
requires USAGE_verdict
audit only

Z₃:
constraint
requires USAGE_judgment
audit only

ZZ:
mixed
constraint outputs + downstream constructive effects

=====================================================================
CORE DISTINCTION (SOFTWARE-CRITICAL)

Artifact-Creating Outputs:
→ require USAGE
→ produce institutional records

Constraint Outputs:
→ do NOT require USAGE
→ shape what is allowed, valid, or enforceable

=====================================================================
ONE-LINE MODEL

Facts → (Trigger / Entry) → Authorization → Reasoning →

IF constructive:
    → USAGE → artifact → audit

IF constraint:
    → validation / limitation

→ enforcement—

This is now:
	•	fully consistent with your operator grammar
	•	cleanly separable into API objects
	•	ready for canonical-operator-api.json if you choose to build it next
