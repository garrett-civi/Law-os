:::writing{variant=“standard” id=“73912”}

Path 2 — Adjudicative & Enforcement Flow

Overview

Path 2 governs the transformation of recorded facts into legally recognized claims, adjudicated outcomes, and enforceable judgments.

This path controls:

recognition → reasoning → instantiation → validation → judgment → enforcement

It is the only path that produces liability, remedies, and final judgments.

⸻

I. Canonical Sequence

O → P → R
↓
L
↓
W₁
↓
USE_reasoning
↓
USAGE_verdict
↓
Z₂
↓
W₂
↓
USE_reasoning
↓
USAGE_remedy
↓
USAGE_judgment
↓
Z₃
↓
ZZ
↓
Wₑ
↓
USAGEₑ
↓
USE_world


⸻

II. Stage Breakdown

1. World to Record

O → P → R

	•	O (Observation): raw events
	•	P (Perception): interpreted awareness
	•	R (Record): persisted facts

Output:

recorded_facts

No legal meaning exists yet.

⸻

2. Legal Recognition (L)

USE_reasoning_plausibility → L

Transforms recorded facts into legally cognizable claims.

Inputs:

recorded_facts

Rules:
	•	non-conclusory factuality
	•	element anchoring
	•	reasonable inference of liability
	•	doctrinal operativity
	•	speculation boundary
	•	public record integration (PDIM-compatible)

Output:

legally_cognizable_facts

Type:

state_flip (no artifact created)

This is the entry point into adjudication.

⸻

3. Authorization of Reasoning Space (W₁)

W₁

Opens the adjudicative reasoning domain.

Inputs:

legally_cognizable_facts
admissible_evidence

Outputs:

verdict_reasoning_space

Examples:
	•	jury instructions
	•	judge-defined reasoning boundaries

Type:

constraint


⸻

4. Verdict Reasoning (USE_reasoning)

USE_reasoning_verdict

Produces a liability candidate.

Internal modules:

M1 — factfinding
M2 — doctrinal meaning assignment
Inference Control — relation strength and plausibility regulation

Outputs:

verdict_candidate
liability_candidate

Type:

constructive (pre-instantiation)


⸻

5. Verdict Instantiation (USAGE_verdict)

USAGE_verdict

Creates the institutional verdict artifact.

Outputs:

verdict_record
liability_record

Type:

constructive (artifact created)


⸻

6. Liability Validation (Z₂)

Z₂

Audits the validity of the instantiated verdict.

Inputs:

verdict_record
liability_record

Tests:

Zb (dominant):
- evidentiary integrity
- record support
- doctrinal coherence
- reasonable inference vs speculation

Za (bounded):
- absence of bad-faith distortion

Outputs:

validated_liability
invalidated_liability

Type:

constraint (requires prior USAGE_verdict)


⸻

7. Remedy Authorization (W₂)

W₂

Opens remedy determination space.

Inputs:

validated_liability

Outputs:

remedy_reasoning_space

Type:

constraint


⸻

8. Remedy Reasoning (USE_reasoning)

USE_reasoning_remedy

Produces a remedy candidate.

Outputs:

remedy_candidate

Includes:
	•	damages calculation
	•	equitable remedy selection
	•	restitution logic

Type:

constructive (pre-instantiation)


⸻

9. Remedy Instantiation (USAGE_remedy)

USAGE_remedy

Outputs:

remedy_record

Type:

constructive


⸻

10. Judgment Formation (USAGE_judgment)

USAGE_judgment

Combines verdict and remedy into a final judgment.

Inputs:

verdict_record
remedy_record

Outputs:

final_judgment

Type:

constructive (composite artifact)


⸻

11. Outcome Validation (Z₃)

Z₃

Audits the proportionality and legitimacy of the judgment.

Inputs:

final_judgment

Tests:

Za (primary):
- proportionality
- fairness
- burden balance

Zb (constraints):
- legal authority
- procedural correctness
- enforceability

Outputs:

validated_judgment
modified_judgment

Type:

constraint (requires prior USAGE_judgment)


⸻

12. Appellate / Meta Review (ZZ)

ZZ

Reviews prior stages.

Inputs:

recognition_record
verdict_record
remedy_record
final_judgment
Z outputs

Outputs:

affirmed
reversed
remanded
modified

Type:

mixed (constraint + downstream constructive effects)


⸻

13. Enforcement Authorization (Wₑ)

Wₑ

Grants authority to enforce judgment.

Outputs:

authority_to_enforce

Type:

constraint


⸻

14. Enforcement Instantiation (USAGEₑ)

USAGEₑ

Outputs:

writ_record
enforcement_record

Type:

constructive


⸻

15. World Execution (USE_world)

USE_world

Executes the judgment in the real world.

Outputs:

property_transfer
funds_seizure
injunction_enforcement
custody_change

Type:

world


⸻

III. Output Classification

L                → state_flip
W₁, W₂, Wₑ       → constraint
USE_reasoning    → constructive (pre-instantiation)
USAGE_*          → constructive
Z₂, Z₃           → constraint (audit)
ZZ               → mixed
USE_world        → world


⸻

IV. Core Invariants

Liability does not exist before Z₂ validation

Remedy does not exist before liability validation

Judgment requires both verdict and remedy instantiation

Z₂ and Z₃ do not create artifacts — they audit them

ZZ can both constrain and trigger new construction

Enforcement requires separate authorization and instantiation

World execution occurs outside the system layer


⸻

V. Failure Outcomes

Failure at L → dismissal / no entry

Failure at Z₂ → liability invalidated

Failure at Z₃ → judgment modified or vacated

Failure at ZZ → reversal or remand

Failure at enforcement → no execution


⸻

VI. Final Compression

Facts → Recognition → Reasoning → Instantiation

→ liability validated (Z₂)
→ remedy produced
→ judgment instantiated
→ outcome validated (Z₃)

→ enforcement → world execution


⸻

One-Line Definition

Path 2 governs how facts become liability, how liability becomes judgment, and how judgment becomes enforceable reality.

:::

