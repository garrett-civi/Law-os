
:::writing{variant=“standard” id=“73841”}

Constructive vs Constraint Outputs

Overview

This document defines a core invariant of the Law-OS architecture:

All system outputs fall into two primary categories:
	1.	Constructive outputs
	2.	Constraint outputs

This distinction governs how operators behave, how state transitions occur, and how the system must be implemented in code.

⸻

I. Core Distinction (Locked)

Constructive outputs → create institutional artifacts → require USAGE

Constraint outputs → do not create artifacts → do NOT require USAGE

This replaces the incorrect assumption that:

USE_reasoning → USAGE → Z

That sequence only applies to constructive paths, not all legal outputs.

⸻

II. Output Types

The system recognizes the following output types:

Output Type	Meaning
constructive	creates an institutional artifact
constraint	limits, validates, or conditions downstream use
state_flip	changes system status without creating an artifact
mixed	produces both constraint and downstream constructive effects
world	world-level event or state change
trigger	initiates a processing path


⸻

III. Canonical Operator Paths

Constructive Path

USE_reasoning → USAGE → institutional artifact → Z audit

Examples:
	•	verdict
	•	remedy
	•	judgment
	•	enforcement writ

⸻

Constraint Path

USE_reasoning → constraint output (Z or equivalent)

Examples:
	•	plausibility filtering
	•	suppression (Z₁)
	•	appellate reversal logic

No artifact is created.

⸻

IV. Canonical Classification

1. Recognition Layer (L)

USE_reasoning_plausibility → L

Type: state_flip
USAGE required: No
Artifact created: No

L changes system status from:

recorded facts → legally cognizable facts

It does not create an institutional object.

⸻

2. Coercive Legitimacy (Z₁)

Aₑ → USE_reasoning_coercive_legitimacy → Z₁

Type: constraint
USAGE required: No
Artifact created: No

Effect:
	•	permits or blocks downstream use of evidence or coercive power

⸻

3. Verdict Phase

USE_reasoning_verdict → USAGE_verdict → Z₂

Type: constructive
	•	USE_reasoning_verdict produces a candidate
	•	USAGE_verdict creates the institutional artifact

Z₂ then audits that artifact.

⸻

4. Remedy Phase

USE_reasoning_remedy → USAGE_remedy

Type: constructive

Creates remedy artifacts used in judgment formation.

⸻

5. Judgment Formation

USAGE_judgment → Z₃

Type: constructive

Creates the final judgment artifact.

⸻

6. Z₂ and Z₃ (Critical Clarification)

USAGE_verdict → Z₂
USAGE_judgment → Z₃

Type: constraint (audit)
Requires prior instantiation: Yes
Creates artifact: No

Z₂ and Z₃:
	•	consume existing artifacts
	•	validate or invalidate them
	•	do NOT create new artifacts

⸻

7. Appellate Layer (ZZ)

ZZ

Type: mixed

ZZ produces:

Constraint outputs
	•	affirm
	•	reverse

Constructive downstream effects
	•	remand
	•	vacatur
	•	modification (which triggers new USAGE downstream)

⸻

8. Enforcement

Wₑ → USAGEₑ → USE_world

Type: constructive

Creates enforceable institutional artifacts (writs, enforcement records).

⸻

9. Execution Challenge (Aₑ)

Aₑ → USE_reasoning → Z₁

Type: constraint

Triggers legality review of executed power.

⸻

V. Master Table (Invariant Map)

STAGE                     TYPE              NEEDS USAGE?

L                         state_flip        NO
Z₁                        constraint        NO
Z₂                        constraint/audit  requires prior USAGE_verdict
Z₃                        constraint/audit  requires prior USAGE_judgment

verdict                   constructive      YES
remedy                    constructive      YES
judgment                  constructive      YES
enforcement               constructive      YES

ZZ                        mixed             SOMETIMES


⸻

VI. Core System Rule (Implementation)

IF output_type == constructive:
    require USAGE
    create institutional artifact

IF output_type == constraint:
    do NOT require USAGE
    apply downstream limitation or permission effect


⸻

VII. Structural Insight

The system contains two forms of power:

1. Constructive Power

Creates institutional reality.

Examples:
	•	verdict
	•	judgment
	•	writ

⸻

2. Constraint Power

Limits what reality can be constructed from.

Examples:
	•	Z₁ suppression
	•	plausibility filtering
	•	appellate reversal

⸻

VIII. Why This Matters

1. Prevents Category Collapse

Without this distinction, the system would incorrectly model:

suppression = object creation

Which breaks the architecture.

⸻

2. Explains Missing USAGE Steps

Some steps do not require USAGE because:

they are not building anything
they are constraining what can be built


⸻

3. Aligns with Core Invariants

presence ≠ use
use ≠ instantiation
instantiation ≠ evaluation
evaluation ≠ construction


⸻

4. Enables Machine Implementation

This distinction allows direct encoding in software:

constructive outputs → artifact pipeline

constraint outputs → permission / validation pipeline


⸻

IX. Final Compression

The system does not only build outcomes.

It governs what is allowed to be built.

:::

