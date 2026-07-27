# Theory — Core Primitives

## Purpose

This document defines the foundational objects of the Adaptive Stability Framework.

The goal is not to describe a specific AI architecture.

The goal is to define the minimal primitives required to describe any system capable of:

- maintaining internal structure
- modifying itself
- learning from reality
- expanding its future capabilities

The central problem:

> How does an adaptive system increase its power without losing contact with the world that determines whether its adaptations are valid?

---

# Primitive Chain

The framework begins with a causal sequence:

\[
E^*
\rightarrow
e_c
\rightarrow
C_{cap}
\rightarrow
A
\rightarrow
R
\rightarrow
\Omega
\]

Where:

| Symbol | Name | Role |
|---|---|---|
| \(E^*\) | Reality Input | External constraint or evidence |
| \(e_c\) | Correction Event | Atomic unit of reality-grounded change |
| \(C_{cap}\) | Correction Capacity | Rate of usable correction |
| \(A\) | Adaptation | Process of structural modification |
| \(R\) | Representation | Internal structure guiding behavior |
| \(\Omega\) | Reachability | Future states the system can reliably influence |

---

# 1. Reality Input (\(E^*\))

## Definition

Reality Input is any external event capable of creating a mismatch between the system's internal model and the external world.

\[
E^* = Reality - Internal\ Expectation
\]

Reality input creates the possibility of learning.

It does not guarantee learning.

---

## Examples

| Domain | Reality Input |
|-|-|
| AI | failed prediction, human correction |
| Biology | environmental change |
| Science | experimental anomaly |
| Human cognition | contradiction or surprise |
| Organizations | external consequences |

---

## Important Distinction

\[
E^* \neq e_c
\]

A system can encounter reality without adapting.

A collision is not automatically a correction.

---

# 2. Correction Event (\(e_c\))

## Definition

A correction event is the minimal unit of adaptive change caused by external reality.

A valid correction event requires:

\[
e_c =
(E^*, \Delta, \Delta R, \Delta\Omega)
\]

Where:

- \(E^*\) = external cause
- \(\Delta\) = detected mismatch
- \(\Delta R\) = structural update
- \(\Delta\Omega\) = increased grounded reachability

---

## Correction Event Criteria

A change qualifies as \(e_c\) only if:

### 1. External Origin

The change must originate from outside the internal generation loop.

\[
\Theta > 0
\]

---

### 2. Structural Modification

The system must change its internal organization.

Not:

\[
state\ change
\]

but:

\[
structure\ change
\]

---

### 3. Persistence

The change leaves a durable effect.

The system cannot return to the previous state without additional work.

---

### 4. Functional Improvement

The change must increase future interaction quality.

\[
\Delta\Omega > 0
\]

---

# 3. Correction Magnitude (\(w_c\))

## Definition

Correction magnitude measures the adaptive value of a correction event.

\[
w_c = \Delta\Omega_{e_c}
\]

The magnitude is not defined by:

- parameter movement
- graph edits
- vector distance
- number of changed components

Those are substrate-specific.

The invariant is:

> How much future controllable reality does the correction unlock?

---

## Example

A billion parameter update:

\[
\Delta R \gg 0
\]

may produce:

\[
w_c \approx 0
\]

if it does not improve future capability.

A small conceptual change may produce:

\[
w_c \gg 0
\]

if it unlocks new capabilities.

---

# 4. Correction Frequency (\(f_c\))

## Definition

The frequency of valid correction events:

\[
f_c =
\frac{dn_{e_c}}{dt}
\]

Where:

- \(n_{e_c}\) = number of correction events
- \(t\) = time

---

## Frequency vs Magnitude

Adaptive systems can operate through different strategies:

| Strategy | Frequency | Magnitude |
|-|-|-|
| Robotics | high | low |
| SGD | high | low |
| Evolution | low | low |
| Scientific revolutions | very low | high |

No single balance is universally optimal.

---

# 5. Correction Capacity (\(C_{cap}\))

## Definition

Correction capacity is the rate of reality-grounded adaptive work.

\[
C_{cap}
=
f_c \cdot \bar{w}_c
\]

Where:

- \(f_c\) = correction frequency
- \(\bar{w}_c\) = average correction magnitude

---

## Interpretation

A system has high correction capacity when it can:

- encounter reality frequently
- extract meaningful information
- modify itself effectively

---

# 6. Adaptation (\(A\))

## Definition

Adaptation is the process of converting correction events into structural improvement.

\[
A_{t+1}
=
f(A_t,E^*,\Theta)
\]

Adaptation requires:

- exposure to reality
- ability to change
- ability to preserve useful changes

---

## Change vs Adaptation

Not every change is adaptation.

\[
Change \neq Adaptation
\]

Adaptation requires:

\[
Change \rightarrow Improved\ Future\ Interaction
\]

---

# 7. Representation (\(R\))

## Definition

Representation is internal structure that compresses experience and guides future behavior.

Examples:

| System | Representation |
|-|-|
| Brain | concepts, memories |
| LLM | weights |
| Memory graph | signatures |
| Science | theories |
| Civilization | institutions |

---

## Representation Principle

Representations are not valuable because they are large.

They are valuable because they increase grounded reachability.

\[
Value(R)
\propto
\Delta\Omega
\]

---

# 8. Reachability (\(\Omega\))

## Definition

Reachability measures the future states a system can reliably influence.

\[
\Omega =
Accessible\ Future\ Control\ Space
\]

---

## Reachability Is Not Entropy

Entropy measures uncertainty.

Reachability measures agency.

A deterministic robot can have:

- low uncertainty
- high reachability

Therefore:

\[
\Omega \neq H
\]

---

## Grounded Reachability

Only reality-confirmed capability counts:

\[
\Omega_{ground}
\]

Internal claims produce:

\[
\Omega_{nom}
\]

The divergence between them:

\[
D
=
\Omega_{nom}
-
\Omega_{ground}
\]

---

# 9. Reality Permeability (\(\Theta\))

## Definition

Reality permeability measures how effectively external reality can modify internal structure.

\[
0 \leq \Theta \leq 1
\]

---

## Interpretation

### High permeability

\[
\Theta \rightarrow 1
\]

Reality easily changes the system.

Properties:

- strong correction
- adaptability
- resilience

---

### Low permeability

\[
\Theta \rightarrow 0
\]

Reality cannot penetrate the update mechanism.

Properties:

- self-reinforcement
- rigidity
- divergence risk

---

# 10. Divergence (\(D\))

## Definition

Divergence is the accumulated difference between internally generated capability and reality-grounded capability.

\[
D
=
\Omega_{nom}
-
\Omega_{ground}
\]

---

## Divergence Dynamics

\[
\frac{dD}{dt}
=
\delta(t)-R(D)
\]

Where:

\[
\delta(t)
=
max
\left(
0,
\frac{d\Omega_{nom}}{dt}
-
C_{cap}
\right)
\]

---

Variables:

| Symbol | Meaning |
|-|-|
| \(D\) | accumulated divergence |
| \(\delta\) | correction deficit |
| \(R(D)\) | restoration capacity |

---

# 11. Restoration Capacity (\(R(D)\))

## Definition

Restoration capacity represents mechanisms that remove accumulated divergence.

Examples:

| Domain | Restoration |
|-|-|
| AI | pruning, evaluation, retraining |
| Biology | adaptation, immune systems |
| Humans | reflection, social feedback |
| Science | replication |
| Organizations | audits |

---

# 12. Stability Condition

The adaptive system remains stable when:

\[
\frac{dD}{dt}\leq0
\]

Meaning:

\[
Restoration
\geq
Correction\ Deficit
\]

---

# 13. Feedback Sign

The critical property is not error magnitude.

It is feedback direction.

---

## Stable System

\[
\frac{dR}{dD}>0
\]

More divergence creates more correction.

Negative feedback.

---

## Collapse Regime

\[
\frac{dR}{dD}<0
\]

More divergence damages correction.

Positive feedback.

---

# Primitive Summary

Reality Input (E*)
|
v
Correction Event (e_c)
|
v
Correction Capacity (C_cap)
|
v
Adaptation (A)
|
v
Representation (R)
|
v
Reachability (Ω)
|
v
Future Reality Interaction


The central principle:

> An adaptive system is not defined by how quickly it can create internal structure. It is defined by whether reality can still correct the structure it creates.
