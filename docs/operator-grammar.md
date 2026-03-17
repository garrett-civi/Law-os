:::

Operator Grammar — Canonical Legal Execution Model

Overview

This document defines the operator grammar for the Law-OS system.

It models how facts move through legal processes using a structured sequence of operators:
	•	A = trigger
	•	L = recognition (entry)
	•	W = authorization
	•	USE = reasoning or execution
	•	USAGE = institutional instantiation
	•	Z = evaluation

The system distinguishes between two output modes:
	•	Constructive outputs → create institutional artifacts
	•	Constraint outputs → shape permission, validity, or downstream use

This distinction is foundational.

⸻

Output Type System

Every operator produces one of the following output types:

Output Type	Meaning
constructive	Creates institutional artifacts (requires USAGE)
constraint	Limits, validates, or shapes downstream use (no USAGE required)
state_flip	Changes system status without creating an artifact
mixed	Can produce both constraint and constructive effects
world	Real-world events or state changes
trigger	Initiates a processing path


⸻

Core Rule

IF output_type == constructive:
    require USAGE (artifact creation)

IF output_type == constraint:
    do NOT require USAGE
    apply limitation / permission effect


⸻

System Invariants
	•	No liability exists at the world level
	•	All reasoning occurs in USE_reasoning
	•	Not all USE_reasoning leads to USAGE
	•	Constructive outputs create institutional artifacts
	•	Constraint outputs shape validity, admissibility, or enforcement
	•	L is a state flip at entry
	•	Z₁ is a direct constraint output
	•	Z₂ and Z₃ audit prior instantiated artifacts
	•	ZZ produces mixed outputs

⸻

PATH 1 — COERCIVE PIPELINE

STAGE                     | OPERATOR   | TYPE              | OUTPUT TYPE   | REQUIRES PRIOR INSTANTIATION | CREATES ARTIFACT | INPUT                         | OUTPUT
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
World Visibility          | O → P → R  | world observation | world         | NO                           | NO               | real-world events              | recorded facts
Action Trigger            | Aₐ         | trigger           | trigger       | NO                           | NO               | recorded facts                 | actionable allegations
Coercive Authorization    | W₀         | authorization     | constraint    | NO                           | NO               | allegations                    | authority to use force
Authority Instantiation   | USAGE₁     | instantiation     | constructive  | NO                           | YES              | W₀                             | warrant / order
Execution                 | USE_world  | execution         | world         | YES                          | NO               | authority                      | search / arrest
World Update              | —          | state change      | world         | NO                           | NO               | execution                      | altered state
Recognition Re-entry      | Aₑ         | trigger           | trigger       | NO                           | NO               | execution record               | challenge
Z₁ Legitimacy             | Z₁         | evaluation        | constraint    | NO                           | NO               | execution + authority          | lawful / unlawful


⸻

PATH 2 — ADJUDICATIVE PIPELINE

Recognition Interface

Claim Entry               | L                       | recognition       | state_flip    | NO  | NO  | recorded facts       | legally cognizable facts
Threshold Reasoning       | USE_reasoning_plaus     | reasoning         | state_flip    | NO  | NO  | allegations          | plausibility determination
Z₁ (if triggered)         | Z₁                      | evaluation        | constraint    | NO  | NO  | execution facts      | admissibility outcome


⸻

Verdict Phase

Authorization             | W₁                      | authorization     | constraint    | NO  | NO  | cognizable facts     | reasoning space open
Reasoning                 | USE_reasoning_verdict   | reasoning         | constructive  | NO  | NO  | evidence             | liability candidate
Instantiation             | USAGE_verdict           | instantiation     | constructive  | NO  | YES | candidate            | verdict record
Z₂ Audit                  | Z₂                      | evaluation        | constraint    | YES | NO  | verdict record       | validated / invalidated


⸻

Remedy Phase

Authorization             | W₂                      | authorization     | constraint    | NO  | NO  | liability            | remedy space open
Reasoning                 | USE_reasoning_remedy    | reasoning         | constructive  | NO  | NO  | liability + facts    | remedy candidate
Instantiation             | USAGE_remedy            | instantiation     | constructive  | NO  | YES | remedy               | remedy record


⸻

Judgment Formation

Judgment                  | USAGE_judgment          | instantiation     | constructive  | YES | YES | verdict + remedy     | final judgment
Z₃ Audit                  | Z₃                      | evaluation        | constraint    | YES | NO  | judgment             | validated / modified


⸻

Appellate Layer

Meta Review               | ZZ                      | meta-reasoning    | mixed         | YES | NO  | prior Z outputs      | affirmed / reversed / remanded

	•	Can produce constraint outputs (affirm, reverse)
	•	Can trigger new constructive paths (remand → new USAGE)

⸻

Enforcement

Authorization             | Wₑ                      | authorization     | constraint    | YES | NO  | judgment             | enforcement authority
Instantiation             | USAGEₑ                  | instantiation     | constructive  | NO  | YES | Wₑ                   | writ / enforcement record
Execution                 | USE_world               | execution         | world         | YES | NO  | authority            | seizure / transfer


⸻

Post-Execution Challenge

Execution Challenge       | Aₑ                      | trigger           | trigger       | NO  | NO  | execution facts      | re-entry into system


⸻

Core Architectural Insight

The system operates on two distinct output paths:

1. Constructive Path

USE_reasoning → USAGE → institutional artifact → Z audit

2. Constraint Path

USE_reasoning → constraint / validation output

No artifact is created.

⸻

Final Compression

Facts → Entry → Authorization → Reasoning →

    (A) Constructive:
        → USAGE → artifact → audit

    (B) Constraint:
        → validation / limitation

→ Enforcement


⸻

Key Clarification

Z₂ requires prior USAGE_verdict
Z₃ requires prior USAGE_judgment

They do not create new artifacts.
They evaluate existing ones.

⸻

Summary

Law-OS is a structured operator system that:
	•	transforms facts into enforceable outcomes
	•	separates artifact creation from permission control
	•	explicitly models evaluation as a distinct layer

This enables:
	•	deterministic legal reasoning
	•	programmable adjudication
	•	system-level validation of legal outputs

⸻

One-Line Definition

Law-OS models law as operators that create outcomes
and operators that constrain which outcomes are valid.

:::

