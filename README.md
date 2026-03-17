# Law-OS

A structured legal reasoning system that models how facts become legally actionable outcomes through visibility, recognition, inference, and enforcement.

Law-OS separates:
- what happens in the world  
- what the legal system recognizes  
- what reasoning is permitted  
- what outcomes can be constructed  
- what constraints limit those outcomes  

This repository defines a **modular, operator-driven architecture** for legal reasoning that is both human-readable and machine-executable.

---

## Core Thesis

Legal systems do not simply produce outcomes.

They:

1. **recognize facts**
2. **constrain reasoning**
3. **authorize inference**
4. **construct institutional outputs**
5. **enforce world changes**

Law-OS models this as a pipeline with two fundamental output types:

- **Constructive outputs** → create institutional reality (require USAGE)
- **Constraint outputs** → limit what can be constructed (no USAGE required)

---

## Canonical Architecture

### Capacity → World → System → Execution

Capacity Level
↓ (exercise)
World Level (events, states)
↓ (recognition)
System Level (legal meaning, reasoning, outputs)
↓ (execution)
World Alteration

---

## Two Core Pipelines

### PATH 1 — Coercive Pipeline
(allegation → authority → execution → review)

- Actionable allegations (Aₐ)
- Coercive authorization (W₀)
- Institutional instantiation (USAGE₁)
- World execution (USE_world)
- Legitimacy review (Z₁)

---

### PATH 2 — Adjudicative Pipeline
(facts → reasoning → liability → remedy → judgment → enforcement)

- Recognition (L — plausibility)
- Verdict reasoning (USE_reasoning_verdict → USAGE_verdict)
- Liability audit (Z₂)
- Remedy reasoning (USE_reasoning_remedy → USAGE_remedy)
- Judgment formation (USAGE_judgment)
- Outcome review (Z₃)
- Appellate supervision (ZZ)
- Enforcement (Wₑ → USAGEₑ → USE_world)

---

## Operator Grammar

Law-OS is built on three core operators:

| Operator | Function |
|--------|--------|
| **USE_reasoning** | produces legal meaning |
| **USAGE** | instantiates institutional objects |
| **Z** | evaluates legitimacy |

---

## Output Types (Critical Distinction)

### 1. Constructive Outputs
Create institutional reality

Examples:
- verdict
- judgment
- writ

Structure:

USE_reasoning → USAGE → object → Z-review

---

### 2. Constraint Outputs
Limit what can be constructed

Examples:
- plausibility filtering (L)
- suppression (Z₁)
- appellate reversal logic (ZZ)

Structure:

USE_reasoning → Z (constraint)

---

## Key Modules

### Public Data Injection Module (PDIM)

Located at:

USE_reasoning_plausibility (L-stage)

Function:
- inject publicly attributable narrative and data into plausibility
- increase factual density
- convert speculative inference into reasonable inference

PDIM enables:

- use of public narrative (PNE)
- use of public records/data (PRDI)
- attribution-based factual elevation
- reduced reliance on discovery

**Core Insight:**
Public institutional data can be used at the recognition stage, not just the evidence stage.

---

## Why This Matters

### 1. Eliminates Hidden Layer Confusion
Separates:
- world events
- legal recognition
- reasoning
- instantiation
- evaluation

---

### 2. Prevents Category Errors
Example:
- suppression is NOT object creation
- plausibility is NOT liability
- evaluation is NOT construction

---

### 3. Enables Machine Execution
The system can be expressed as:

IF output_type == CONSTRUCTIVE:
require USAGE

IF output_type == CONSTRAINT:
apply limitation

---

### 4. Reveals Two Forms of Power

#### Constructive Power
Creates legal reality

#### Constraint Power
Controls what reality can be created

Constraint power is structurally dominant.

---

## Initial Modules

- `canonical-pipeline.md`
- `public-data-injection-module.md`

---

## Roadmap

Planned modules:

- operator grammar layer
- evidence doctrine mapping (FRE alignment)
- inference control engine
- appellate review modeling (ZZ layer)
- enforcement challenge module (Aₑ)
- AI-assisted plausibility drafting tools

---

## Status

Early-stage system architecture.

Actively being formalized into:
- modular specifications
- developer-readable formats
- legal-tech applications

---

## Vision

Law-OS is a foundation for:

- legal reasoning engines  
- litigation tooling  
- AI-assisted pleading systems  
- institutional decision systems  
- governance infrastructure  

---

## One-Line Summary

Law-OS does not just produce legal outcomes.

It governs what outcomes are allowed to exist.


