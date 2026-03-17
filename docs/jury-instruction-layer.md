:::writing{variant=“standard” id=“86173”}

Jury Instruction Layer (W₁ → Inference Boundary Programming)

Overview

This document defines the role of jury instructions within the Law-OS architecture.

Jury instructions are not merely guidance.

They are:

formal constraints that define the permissible inference space

They operate at:

W₁ (authorization layer)

and function as ex ante inference control.


⸻

With this file, your system now includes:

- evidence layer
- inference layer
- motion layer
- AND now:
- inference boundary programming (W₁)

That completes the full reasoning control stack.

⸻

I. Core Principle

Jury instructions program the boundaries of reasoning
before factfinding and doctrinal mapping occur.

They determine:
	•	what must be proven
	•	how facts may be interpreted
	•	what inferences are allowed or forbidden
	•	how burdens are allocated

⸻

II. Canonical Placement

L → W₁ → M₁ → M₂ → USAGE_verdict → Z₂

More precisely:

W₁ sits between recognition and reasoning

It defines the inference space within which:
    M₁ (factfinding)
    M₂ (doctrinal mapping)
must operate


⸻

III. Function of W₁

W₁ = inference boundary authorization

It performs four primary functions:

1. Element Definition

defines the legal structure the jury must apply

Example:
	•	elements of negligence
	•	elements of a contract claim
	•	elements of a criminal offense

⸻

2. Burden Allocation

defines who must prove what and to what standard

Examples:
	•	preponderance of the evidence
	•	clear and convincing evidence
	•	beyond a reasonable doubt

⸻

3. Permissible Inference Programming

defines what inferential moves are allowed

Examples:
	•	circumstantial evidence is permitted
	•	intent may be inferred from conduct
	•	pattern evidence may or may not be used

⸻

4. Forbidden Inference Blocking

prohibits specific inferential routes

Examples:
	•	no propensity reasoning
	•	no improper bias-based conclusions
	•	no speculation outside the record

⸻

IV. Output Type Classification

W₁ → constraint

	•	does NOT create an institutional artifact
	•	does NOT require USAGE
	•	defines downstream reasoning limits

⸻

V. Relationship to Evidence Doctrine

W₁ incorporates and operationalizes evidentiary rules:

FRE 403 → encoded as exclusion instructions

FRE 404 → encoded as no-propensity instructions

hearsay limits → encoded in admissibility and use constraints

Meaning:

evidence doctrine constrains inputs

jury instructions constrain reasoning on those inputs


⸻

VI. Relationship to Inference Control Doctrine

W₁ operates before M₁

It defines the inference space
that M₁ and M₂ must stay within

Mapping:

W₁ → defines allowed inference set

M₁ → generates inference within that set

M₂ → maps inference to legal elements

Z₂ → audits whether inference stayed within bounds


⸻

VII. Relationship to Motions

motions in limine → shape W₁

12(b)(6) → precedes W₁ (entry)

summary judgment → may bypass W₁ entirely

JMOL → tests whether W₁-constrained inference was sufficient

new trial → tests whether W₁ was violated or misapplied

appeal (ZZ) → reviews correctness of W₁


⸻

VIII. Failure Modes

Improper W₁ configuration produces:

1. Over-permissive inference space

allows speculation or improper reasoning

Result:

invalid verdict → Z₂ failure → reversal risk


⸻

2. Over-restrictive inference space

prevents legitimate reasoning

Result:

distorted factfinding → unfair outcome → Z₃ / ZZ issues


⸻

3. Mis-specified elements or burdens

incorrect legal framework

Result:

structural error → likely reversal at ZZ


⸻

IX. Structural Insight

W₁ is where law becomes executable.

It translates doctrine into constraints on reasoning.

Without W₁:

M₁ would generate unconstrained inference
M₂ would apply doctrine inconsistently
Z₂ would lack a stable evaluation baseline


⸻

X. PDIM Interaction

PDIM strengthens L by increasing factual density.

W₁ then determines:

how that increased factual density may be used

Meaning:

PDIM affects what enters

W₁ affects how it can be used


⸻

XI. Cross-Stage Invariants

W₁ must precede M₁ reasoning

All M₁ inference must comply with W₁ constraints

M₂ mapping must follow W₁-defined structure

Z₂ audits compliance with W₁

ZZ reviews correctness of W₁ itself


⸻

XII. Final Compression

W₁ defines the rules of reasoning

M₁ uses those rules to interpret facts

M₂ uses those rules to assign legal meaning

Z₂ checks whether the rules were followed

ZZ checks whether the rules were correct


⸻

One-Line Definition

Jury instructions are the system’s method of programming the permissible space of inference before legal reasoning occurs.

:::
