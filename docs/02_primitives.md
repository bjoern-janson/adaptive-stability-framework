# 02 — Core Primitives

## Overview

To study adaptive systems, we need substrate-independent primitives.

The goal is not to define intelligence by implementation.

A neural network, a biological brain, a memory graph, and a scientific community may operate through different mechanisms, but they share a common problem:

> How does a system accumulate useful structure while remaining coupled to reality?

This document defines the initial primitive objects.

The proposed causal chain:

\[
Reality \rightarrow Correction \rightarrow Adaptation \rightarrow Representation \rightarrow Reachability
\]

---

# 1. Reality Input (\(E^*\))

## Definition

\(E^*\) represents external information capable of challenging or modifying the current internal state of an adaptive system.

It is the difference between:

- what the system currently expects
- what reality actually produces

Examples:

| Domain | Reality Input |
|---|---|
| AI | failed prediction, user correction, environment feedback |
| Biology | environmental pressure |
| Science | experimental anomaly |
| Human cognition | surprise, contradiction, new evidence |
| Organizations | market feedback, external consequences |

Reality input alone is not learning.

A system can receive information without changing.

Therefore:

\[
E^* \neq Correction
\]

Reality becomes meaningful only when it causes structural adaptation.

---

# 2. Correction Event (\(e_c\))

## Definition

A correction event is the smallest unit of reality-grounded structural change.

A correction event requires four conditions:

\[
e_c =
\{
External\ Cause,
Mismatch,
Structural\ Update,
Improved\ Future\ Adaptation
\}
\]

A system has experienced a correction event when:

1. the change originated from external reality
2. a mismatch was detected
3. internal structure changed
4. future behavior becomes better aligned with reality

---

## What Is Not a Correction Event?

### Internal mutation

A system modifying itself without external grounding:

\[
Internal\ Change \not\Rightarrow e_c
\]

Example:

An AI inventing a new belief because it is internally consistent.

---

### Temporary state adjustment

A temporary response is not structural correction.

Example:

A robot arm compensating for a disturbance.

The motor position changes.

The control policy does not.

---

### Information accumulation

Receiving more data does not guarantee correction.

A system can accumulate information while becoming more wrong.

---

# 3. Correction Frequency (\(f_c\))

Correction frequency measures how often valid correction events occur.

\[
f_c = \frac{dn_{e_c}}{dt}
\]

where:

- \(n_{e_c}\) = number of valid correction events
- \(t\) = time

Frequency describes the rhythm of adaptation.

Examples:

| System | Correction Frequency |
|---|---|
| Robotics | extremely high |
| Neural learning | high |
| Evolution | low |
| Scientific paradigms | very low |

High frequency is not automatically better.

A system can require:

- many small corrections
- rare transformative corrections

---

# 4. Correction Magnitude (\(w_c\))

## Definition

Correction magnitude measures the adaptive work created by a correction event.

A representation-specific definition is avoided.

The goal is not:

- parameter distance
- latent vector movement
- graph edit distance

Those describe implementations.

Instead:

\[
w_c = \Delta \Omega_{e_c}
\]

where:

- \(w_c\) = correction magnitude
- \(\Delta \Omega_{e_c}\) = increase in reality-grounded reachability caused by the correction event

---

## Why This Matters

A large internal change may have little adaptive value.

Example:

Changing billions of neural weights to memorize irrelevant information:

\[
\Delta Representation \gg 0
\]

but:

\[
\Delta \Omega \approx 0
\]

Conversely:

A small conceptual change can create enormous reachability.

Example:

A scientific discovery that changes future engineering possibilities:

\[
\Delta Representation \ll \Delta \Omega
\]

---

# 5. Correction Capacity (\(C_{cap}\))

## Definition

Correction capacity represents the total rate at which a system can convert reality feedback into useful adaptive change.

It combines:

- correction frequency
- correction magnitude

\[
C_{cap}=f_c \cdot \bar{w}_c
\]

where:

- \(f_c\) = correction frequency
- \(\bar{w}_c\) = average correction magnitude

---

## Interpretation

A system can increase correction capacity through:

### More frequent feedback

More opportunities to detect error.

### More meaningful corrections

Greater structural improvement per event.

### Better correction efficiency

More useful adaptation per unit of feedback.

---

# 6. Adaptation (\(A\))

## Definition

Adaptation is the process by which a system changes its internal mechanisms in response to reality.

Adaptation is not simply change.

A random mutation is not necessarily adaptation.

A change becomes adaptation when:

\[
Reality \rightarrow Change \rightarrow Improved Future Interaction
\]

---

# 7. Representation (\(R\))

## Definition

Representation is the internal structure used to compress, organize, and guide future behavior.

Examples:

| System | Representation |
|---|---|
| Brain | concepts, memories, beliefs |
| LLM | weights, activations |
| Memory system | signatures, nodes |
| Science | theories, equations |
| Organization | procedures, culture |

---

## Representation Has No Intrinsic Value

A larger representation is not automatically better.

The important question:

\[
Does the representation increase valid adaptive reach?
\]

A representation that cannot survive reality testing is accumulated divergence.

---

# 8. Reachability (\(\Omega\))

## Definition

Reachability measures the future states a system can reliably influence.

It represents:

- possible actions
- achievable outcomes
- controllable futures

---

## Reachability Is Not Entropy

Entropy measures uncertainty.

Reachability measures agency.

A deterministic robot arm demonstrates this distinction:

- low uncertainty
- high causal control

Therefore:

\[
\Omega \neq H
\]

---

## Operational View

A system increases reachability when it gains the ability to reliably achieve outcomes that were previously unavailable.

A correction event is valuable because:

\[
e_c \rightarrow \Delta\Omega
\]

---

# 9. Reality Permeability (\(\Theta\))

## Definition

Reality permeability measures how effectively external reality can influence structural updates.

A system with high permeability:

- receives external evidence
- allows internal revision
- preserves correction pathways

A system with low permeability:

- filters contradictory evidence
- reinforces existing structures
- becomes internally closed

---

Conceptually:

\[
0 \leq \Theta \leq 1
\]

where:

\[
\Theta=1
\]

represents maximum openness to reality correction.

and:

\[
\Theta=0
\]

represents complete insulation.

---

# 10. Divergence (\(D\))

## Definition

Divergence is accumulated distance between internal structural claims and reality-grounded capability.

Divergence emerges when:

\[
\frac{d\Omega_{nom}}{dt} > C_{cap}
\]

The system creates internal structure faster than reality can validate it.

---

## Divergence Dynamics

\[
\frac{dD}{dt}
=
\delta(t)-R(D)
\]

where:

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

and:

- \(D\) = accumulated divergence
- \(\delta\) = correction deficit
- \(R(D)\) = restoration capacity

---

# Primitive Stack

The complete dependency chain:

Reality (E*)
|
v
Correction Event (e_c)
|
v
Correction Power (C_cap)
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
Future Interaction With Reality


---

# Summary

The central claim:

> Adaptive systems do not remain intelligent by avoiding error. They remain intelligent by maintaining the capacity to transform error into improved future reachability.

The fundamental resource is not information.

It is reality-grounded correction.
