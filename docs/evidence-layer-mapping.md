Evidence Layer Mapping (FRE → Operators)

Overview

This document maps the Federal Rules of Evidence onto the Law-OS architecture.

Its purpose is to show where evidence doctrine operates within the system, and what kind of control each rule exerts over:
	•	visibility
	•	record formation
	•	legal entry
	•	inference
	•	admissibility
	•	validation
	•	appellate review

This document treats evidence doctrine as part of the system’s inference control and permission architecture.

⸻

I. Core Principle

Evidence doctrine does not create liability.

It regulates what facts may enter,
what inferences may be drawn,
and what outputs may legitimately be built.


⸻

II. Canonical Placement

The evidence layer sits across four main zones:

WORLD / VISIBILITY
--------------------------------
O → P → R

ENTRY / RECOGNITION
--------------------------------
L  (plausibility / legal cognizability)

ADJUDICATIVE REASONING
--------------------------------
M₁  factfinding
M₂  doctrinal mapping

VALIDATION / REVIEW
--------------------------------
Z₂
ZZ


⸻

III. High-Level Mapping

FRE Domain	Law-OS Location	Function
Relevance	L, M₁, Z₂	screens inferential connection
Authentication	R → L, M₁	confirms item is what it claims to be
Best Evidence	R, M₁, Z₂	protects record integrity
Hearsay	M₁, Z₂	controls out-of-court assertion use
Prejudice / Confusion / Waste	M₁, W₁, Z₂	limits distorted inference
Character / Propensity	M₁, Z₂	constrains forbidden inferential routes
Impeachment	M₁	tests reliability of evidentiary source
Judicial Notice	L, M₂	imports publicly recognized facts
Presumptions	M₂, W₁	structures inferential allocation
Appellate Evidentiary Review	ZZ	reviews admissibility / evidentiary error


⸻

IV. Layer-by-Layer Mapping

1. O → P → R (Visibility / Record Layer)

This is not yet evidence in the full legal sense. It is pre-legal visibility and record formation.

Relevant doctrines here

FRE 901 — Authentication
Function:

connects the item offered to the claim that it is genuine

Law-OS placement:

R → L threshold
and M₁ if challenged

Meaning:
	•	before a record can be used as legal input, the system must know what it is
	•	authentication protects the transition from raw record to usable evidentiary item

Best Evidence Rule (FRE 1001–1008)
Function:

protects integrity of documentary or recording-based proof

Law-OS placement:

R internal integrity
M₁ evidentiary use
Z₂ if distorted

Meaning:
	•	the system checks whether the record used is the right form of the proof
	•	this is an integrity control, not a liability rule

Core insight

Authentication and best-evidence doctrine govern
whether records may serve as valid inputs to inference.


⸻

2. L (Recognition / Entry Layer)

This is where facts become legally cognizable.

Relevant doctrines here

Relevance (FRE 401)
Function:

asks whether a fact has any tendency
to make a material proposition more or less probable

Law-OS placement:

L

Meaning:
	•	relevance is one of the earliest inferential filters
	•	if facts do not connect to a material proposition, they do not strengthen entry

Judicial Notice (FRE 201)
Function:

permits certain adjudicative facts to enter without ordinary proof

Law-OS placement:

L
M₂

Meaning:
	•	judicial notice can move publicly recognized facts upstream
	•	this is directly relevant to PDIM, PNE, and PRDi logic

Public Records / Official Materials
Function:

allow publicly generated institutional records
to contribute to legal recognition

Law-OS placement:

L

Meaning:
	•	public records can strengthen plausibility before discovery
	•	this is one of the mechanisms by which the system imports density at entry

Core insight

At L, evidence doctrine is operating as an entry filter.
It asks:
What can count early enough to support legal recognition?


⸻

3. M₁ (Factfinding Layer)

This is the primary evidentiary zone.

Relevant doctrines here

FRE 401 / 402 — Relevance / General Admissibility
Function:

limit the evidentiary field to facts that matter

Law-OS placement:

M₁

Meaning:
	•	M₁ should only reason from facts with inferential relevance to disputed issues

FRE 403 — Prejudice, Confusion, Waste
Function:

blocks evidence whose inferential dangers outweigh its value

Law-OS placement:

M₁
W₁ as preconfigured inference boundary
Z₂ if violated

Meaning:
	•	403 is a distortion-control doctrine
	•	it protects the reasoning chamber from bad inferential inputs

Hearsay Rules (FRE 801–807)
Function:

control whether out-of-court assertions may be used for truth

Law-OS placement:

M₁
Z₂ if improperly relied upon

Meaning:
	•	hearsay doctrine regulates the reliability of inferential foundations
	•	it is not just about source form, but about inferential legitimacy

Character / Propensity Rules (FRE 404–405)
Function:

limit forbidden inferential moves

Law-OS placement:

M₁

Meaning:
	•	these doctrines do not just exclude categories of proof
	•	they block specific inferential routes the system deems illegitimate

Habit / Routine Practice (FRE 406)
Function:

permits pattern-based inference under certain conditions

Law-OS placement:

M₁

Meaning:
	•	habit doctrine is a controlled pattern inference doctrine

Impeachment / Credibility (FRE 607–609, etc.)
Function:

tests the reliability of the source from which inference is drawn

Law-OS placement:

M₁

Meaning:
	•	impeachment doctrine modulates how much inferential weight a source can carry

Core insight

M₁ is where evidence doctrine most visibly regulates inference generation.


⸻

4. M₂ (Doctrinal Mapping Layer)

This is where facts are mapped onto legal elements.

Relevant doctrines here

Presumptions
Function:

allocate inferential burdens and structured conclusions

Law-OS placement:

M₂
W₁

Meaning:
	•	presumptions structure doctrinal inference
	•	they are not raw factfinding, but controlled legal translation

Judicial Notice
Function:

permits established facts to operate inside doctrinal reasoning

Law-OS placement:

M₂

Meaning:
	•	once facts are judicially noticed, they can function as doctrinal anchors

Core insight

M₂ uses evidence-derived facts,
but its main work is legal translation, not raw evidentiary intake.


⸻

5. Z₂ (Verdict / Liability Validation)

This is where evidentiary use is audited.

Relevant doctrines here

Sufficiency / Record Support
Function:

tests whether the verdict rests on enough admissible support

Law-OS placement:

Z₂

Meaning:
	•	Z₂ asks whether the inferential path from evidence to verdict was legitimate

FRE-based distortion review
Function:

tests whether the operative evidentiary regime was distorted

Law-OS placement:

Z₂

Examples:
	•	verdict resting on speculation
	•	verdict dependent on improperly admitted evidence
	•	verdict built on inferential gaps

Core insight

Z₂ is where evidence doctrine becomes verdict-audit doctrine.


⸻

6. W₁ (Inference Space Authorization)

This is the often-overlooked evidence-control layer.

Relevant doctrines here

Motions in limine
Jury instructions
Burden allocation
Permitted inferential boundaries
Law-OS placement:

W₁

Meaning:
	•	W₁ defines the inferential space in which M₁ and M₂ may operate
	•	this is where the court pre-configures permissible evidentiary use

Core insight

W₁ is ex ante inference control.
It determines what kinds of evidentiary reasoning are allowed before deliberation begins.


⸻

7. Z₃ (Outcome / Remedy Validation)

Evidence doctrine is less direct here, but still relevant.

Role here

Evidence does not mainly decide what remedy exists.
It helps ensure the remedy rests on:
	•	supported findings
	•	non-speculative measurement
	•	lawful remedial scope

Examples:
	•	damages unsupported by record
	•	remedy exceeding factually justified scope

Law-OS placement:

Z₃

Core insight

At Z₃, evidence doctrine operates through support and proportionality,
not through ordinary admissibility screening.


⸻

8. ZZ (Appellate Review)

This is where evidentiary doctrine becomes review doctrine.

Relevant doctrines here

Abuse of discretion review
Often used for:
	•	FRE 403 rulings
	•	admission/exclusion judgments
	•	trial evidentiary management

De novo review
Used for:
	•	legal interpretation of evidence rules
	•	doctrinal structure questions

Harmless error
Function:

asks whether evidentiary error changed the legitimacy of the outcome

Law-OS placement:

ZZ

Core insight

ZZ governs whether evidentiary error is merely present
or system-legitimacy significant.


⸻

V. Special Mapping Table

Doctrine	Primary Location	Secondary Location	Role
FRE 401 relevance	L, M₁	Z₂	inferential connection
FRE 403 prejudice/confusion	M₁, W₁	Z₂, ZZ	distortion control
FRE 901 authentication	R → L	M₁	identity / genuineness
Best evidence	R, M₁	Z₂	record integrity
Hearsay	M₁	Z₂, ZZ	reliability of asserted truth
Character / propensity	M₁	Z₂	forbidden inferential route control
Habit	M₁	M₂	permitted pattern inference
Judicial notice	L, M₂	ZZ	public fact importation
Presumptions	M₂, W₁	ZZ	inferential allocation
Harmless error	ZZ	—	appellate effect screening


⸻

VI. PDIM Connection

PDIM interacts most strongly with:

L
Judicial Notice
Public Records
Relevance
Authentication

Why:

PDIM increases plausibility by importing publicly verifiable material
into the recognition stage.

This does not eliminate evidence doctrine.
It changes when some evidence-like materials become system-relevant.

Core insight

PDIM is an evidence-adjacent density mechanism
that strengthens L by using public, attributable, and judicially cognizable materials.


⸻

VII. Final Compression

R layer doctrines
→ determine whether records are valid inputs

L layer doctrines
→ determine whether facts can enter legal meaning space

M₁ doctrines
→ regulate inferential use of evidence

M₂ doctrines
→ regulate doctrinal translation of evidence-derived facts

Z₂ doctrines
→ audit verdict legitimacy

ZZ doctrines
→ review evidentiary error and inferential legitimacy system-wide


⸻

One-Line Definition

Evidence doctrine in Law-OS is the system of rules that regulates
what facts may enter, what inferences may be drawn, and whether
those inferences may legitimately support legal outcomes.

