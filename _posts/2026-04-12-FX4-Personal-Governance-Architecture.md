---
title: "FX4: Personal Governance Architecture"
date: 2026-04-12
categories: [electronics]
tags: [C++, Vibe Code, AI, Systems Thinking, Humor]
status: "Complete"
image: "assets/project_photos/FX4_PGA/FX4_personal_governance_system_illustration.png"
excerpt: "FX4 is a conceptual decision architecture that guides day-to-day choices by a deterministic, rule-based evaluation loop. As if you were a predictable, well-behaved system instead of a sleep-deprived, erratic and emotional sack of skin."
---

## Overview

**Liberation through deterministic constraint.**

FX4 is a conceptual decision architecture that guides day-to-day choices by a deterministic, rule-based evaluation loop. As if you were a predictable, well-behaved system instead of a sleep-deprived, erratic and emotional sack of skin.

It is not a productivity tool, a habit tracker, or a rigid hierarchy. **It is a deterministic governance model to attempt to offer liberation from the eternal and attriting burden of personal agency.**

The system is built around four core domains in priority order:

1. **Fuel** → nutrition, recovery, energy management
2. **Fitness** → physical capability, training, resilience
3. **Family** → relationships, responsibility, presence
4. **Freedom** → autonomy, choice, long-term positioning

**Fuel** and **Fitness** are given day-to-day priority because they directly impact our capacity to deliver for our ultimate priorities, **Family** & **Freedom**. They can so easily be cast aside for Family and Freedom's sake with well-meaning and virtuous intent, but doing so has cumulative, highly detrimental and snowballing chain effects. They are the means to the desired end state.

> *"Discipline equals Freedom"* — Jocko Willink  
> *"The chains of habit are too light to be felt until they are too heavy to be broken"* — Samuel Johnson

---

## Technical Approach

### Why Code?

This project is expressed in code as a nod to neurodivergents, those who think in systems & syntax, to those who need to dissect and recompile in their own way before deploying. It's somewhat tongue in cheek whilst, comically, actually providing a precise, unambiguous way to express day-to-day decision logic.

The implementation is written in C++ as a conceptual executable that could serve as an engine for game theory simulation in future iterations.

### The Four F's & Override Logic

![Personal Governance Architecture (FX4 PGA)]({{ '/assets/project_photos/FX4_PGA/Personal_Governance_Architecture_FX4_PGA.png' | relative_url }})

While `ops_normal == 1`, the system evaluates each domain in priority order. However, two conditional flags provide override authority taking conditional precedence over all domains

- **Family Flag** - Interrupts the normal priority order to address immediate family-related demands.
- **Work Flag** - Interrupts the normal priority order to address immediate work-related demands.


### Simulation Mechanics

The executable presents the user with each step and prompts for input:

| Input | Action |
|-------|--------|
| `n` | Next step (proceed to next domain) |
| `w` | Toggle work_flag interrupt |
| `f` | Toggle family_flag interrupt |
| `q` | Quit |

When a flag interrupt is active and conditions require override:

| Input | Action |
|-------|--------|
| `o` | Override and move to next step |
| `c` | Continue and tend to flag until it clears |

### Override Consequences

The system tracks override counts for both work and family flags:

- Each override increments the respective counter
- Override counts decay by 1 after each complete pass (if no new override occurred in current pass)
- **Critical**: Choosing to continue (`c`) allow flag servicing but resets the entire loop count to zero

Loop count milestones trigger feedback:
- **7 days** → "Good stuff"
- **30 days** → "Outstanding"

---

## Execution

### Core Philosophy

FX4 exists because humans are inconsistent under:
- **Fatigue**
- **Stress**
- **Competing obligations**

It externalises decision logic, reduces cognitive load, and reinforces consistent alignment with defined values. Feelings are treated as **low-trust signals** unless explicitly defined as conditions.

### What It's Not

- Not a rigid schedule
- Not "balance"
- Not motivation-dependent
- Not emotional

### What It Is

- A personal governance architecture acting as a **North Star**
- A **deterministic decision model**
- A way to make choices predictable, defensible, and aligned

---

## Specifications

| Parameter | Value |
|-----------|-------|
| Language | C++ |
| Type | Conceptual decision architecture / Simulation engine |
| Execution | Interactive command-line loop |
| License | MIT |
| Repository | [github.com/mgreenhough/FX4-Personal-Governance-Architecture](https://github.com/mgreenhough/FX4-Personal-Governance-Architecture) |


---