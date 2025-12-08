# Skill Mutation System  
### Echo of the Seven – Active Skill Mastery (T1–T4)

This document describes how **active combat skills evolve over time** through usage-based mastery tiers (T1–T4).

The goal is simple:

> The more you use a skill, the more it changes – from a basic attack into a signature move with its own identity.

This system is **independent from runes** and **independent from gear**.  
Runes and items can *modify* or *synergise* with mutations, but they do not replace them.

---

## 1. Design Goals

1. **Play the way you like → get rewarded for it**
   - Skills evolve naturally as the player uses them.
   - No need to “grind a separate XP bar” – casting the skill *is* the progression.

2. **Each skill tells a story**
   - T1: basic, reliable version.  
   - T2: introduces a new condition or status.  
   - T3: that condition cascades or spreads.  
   - T4: climax mutation – powerful, often on-kill or chain effect.

3. **No respec anxiety**
   - Mutations are **earned, not chosen** (for now: linear progression).
   - You never “ruin” a skill by picking the wrong node; you just keep mastering it.

4. **Clear fantasy per skill**
   - Fire skills evolve into chain explosions and spreading burns.  
   - Bleed skills evolve into ramping damage and execution tools.  
   - Frost skills evolve into control, slow and shatter mechanics, etc.

---

## 2. Mastery Tiers Overview (T1–T4)

Every active skill has **four mastery tiers**:

- **Tier 1 – Base Form**
- **Tier 2 – Status Introduction**
- **Tier 3 – Status Interaction / Spread**
- **Tier 4 – Climax / On-Kill / High-Impact Effect**

Mutations are **additive**:
- T2 keeps everything from T1 and adds a new behaviour.
- T3 keeps T1+T2 and adds more interaction.
- T4 adds a final, powerful twist.

### 2.1. Tier 1 – Base Skill (T1)

- Available **from the moment the skill is unlocked**.
- Represents the simplest version:
  - direct damage,
  - basic heal,
  - straightforward dash, etc.
- All tooltips and descriptions at this point only show **T1 behaviour**.

**Example (Fireball, Mage):**

- Launches a single projectile at a target.
- Deals moderate fire damage on impact.
- No status effects yet.

---

### 2.2. Tier 2 – Status Introduction (T2)

Unlocked after the player has used the skill a certain number of times  
(e.g. **1,000 casts** – baseline, tunable per skill).

At T2, the skill gains a **conditional effect**, such as:

- chance to apply:
  - burn, bleed, chill, poison, mark, weaken, etc.
- extra resource interaction:
  - small mana refund on hit,
  - gain a bit of Focus/Fury, etc.

**Example (Fireball T2):**

- Fireball now has a chance to **ignite** the target:
  - applies a burning DoT for a short duration.

---

### 2.3. Tier 3 – Status Interaction / Spread (T3)

Unlocked after further usage  
(e.g. **3,000 total casts** of that skill).

At T3, the mutation focuses on:

- **spreading** the status,
- **intensifying** it,
- or making it interact with nearby enemies.

Common patterns:

- Status spreads from the primary target to enemies nearby.
- Repeated hits ramp the DoT or debuff.
- Hitting an already afflicted target causes an **extra effect**.

**Example (Fireball T3):**

- If Fireball ignites a target:
  - the burn can **spread to nearby enemies**,  
  - either on a timer tick or on additional triggers (like critical hits).

The skill is no longer just “hit one target and forget” – it starts creating **situational plays**.

---

### 2.4. Tier 4 – Climax / On-Kill Mutation (T4)

Unlocked at the final usage threshold  
(e.g. **4,000 total casts** of that skill).

T4 is meant to feel like:

- a **signature move** for players who truly commit to a skill,
- a high-impact effect that can define entire builds.

Typical T4 behaviours:

- On-kill explosions,
- chain reactions,
- large AoE conversions,
- strong buff windows after a specific condition.

**Example (Fireball T4):**

- If Fireball **kills** an enemy who is currently burning:
  - the target **explodes**,
  - dealing fire damage in an area around the corpse,
  - potentially igniting nearby enemies.

Combined with T2/T3:

- T2: Fireball can ignite.  
- T3: burn can spread.  
- T4: killing burning enemies causes explosions → chain reactions are possible.

---

## 3. Progression Mechanics (Usage-Based Mastery)

### 3.1. Per-Skill Counters

- Each skill tracks its own **“casts used” counter**.
- Only **successful casts** (that actually fire/resolve) count:
  - no farming by spamming into the void if we decide to prevent it.

Baseline thresholds (subject to balancing):

- **T1** – default skill, unlocked when the skill is acquired.
- **T2** – 1,000 casts.
- **T3** – 3,000 casts total.
- **T4** – 4,000 casts total.

These values can be:

- tuned per skill,
- tuned per class,
- or globally adjusted if progression feels too slow/fast.

### 3.2. Retroactive Progress

If thresholds change in a patch:

- Players with higher counters automatically unlock the appropriate tiers.
- No need to “re-grind” old skills.

---

## 4. UI & Player Feedback

### 4.1. Skill Mastery Indicator

Each skill in the hotbar / skill tree can show:

- a **small tier badge** (T1–T4),
- a **progress bar** or percentage to the next tier.

Example:

- T2 unlocked:
  - icon shows `II`,
  - tooltip: `Mastery: Tier 2 (1,370 / 3,000 casts to Tier 3)`.

### 4.2. Unlock Moments

When a skill reaches a new tier:

- Play a **short visual and audio cue** (no huge cutscene, but noticeable).
- Show a **small pop-up**:
  - “Fireball reached Tier 3: Burning enemies can now spread the flames to others nearby.”
- Update the skill tooltip to include **all current tier effects**.

---

## 5. Design Patterns for Mutations

To keep the system coherent, designers can follow some patterns:

### 5.1. Damage Skills

- **T2** – gain a chance to apply a status (burn, bleed, poison, chill).  
- **T3** – interacting with that status:
  - spread, ramp, or secondary effect when re-applied.  
- **T4** – big, often on-kill or on-crit:
  - explosion,
  - extra projectile,
  - empowered “finisher”.

### 5.2. Defensive / Support Skills

- **T2** – add a small secondary benefit:
  - small heal, shield, resist buff, resource boost.
- **T3** – share or extend effect to allies:
  - splash healing,
  - aura extension,
  - buff transfer.
- **T4** – strong clutch behaviour:
  - big shield on low HP,
  - group cleanse,
  - revive-like effect (if allowed).

### 5.3. Mobility Skills

- **T2** – smaller CD on hit / dodge bonus / short buff after movement.
- **T3** – interaction with terrain or enemies:
  - leaving behind a trail (fire, poison, slow),
  - knocking back or marking enemies passed through.
- **T4** – dramatic effect:
  - teleport variants,
  - second activation window,
  - AoE effect at start or end of movement.

---

## 6. Interaction with Runes (High-Level)

Full rune mechanics are described elsewhere, but the key rules are:

1. **Mutations are intrinsic to the skill**
   - T1–T4 behaviours are always active once unlocked,
   - regardless of runes, items or gear.

2. **Runes modify or amplify mutations**
   - e.g. runes can:
     - increase burn duration from T2,
     - make T3 spread stronger or faster,
     - boost T4 explosion radius,
     - or add “next skill” bonuses after a mutated effect triggers.

3. **Synergy, not replacement**
   - Runes **do not unlock T2–T4**.  
   - They make already unlocked mutations **hit harder, trigger more often, or create combos with other skills**.

---

## 7. Example Skill – Fireball (Full T1–T4)

**Class:** Mage  
**Role:** Core single-target / small AoE fire spell.

- **Tier 1 – Basic Fireball**
  - Launch a fire projectile at a target,
  - deal moderate fire damage on impact.

- **Tier 2 – Ignite**
  - Fireball now has a chance to **ignite** enemies:
    - apply a burning damage-over-time effect.

- **Tier 3 – Spreading Flames**
  - If an ignited enemy is hit again or the burn naturally ticks:
    - the burning effect can **spread** to nearby enemies.

- **Tier 4 – Combustion**
  - If a burning enemy **dies from Fireball or while burning**:
    - they **explode**, dealing fire damage around them,
    - potentially igniting nearby enemies (synergises back into T2/T3).

Rune examples (separate system) can then say:

- `+ cast speed for Fireball`
- `+ burn duration`
- `+ explosion radius for burning kills`
- `next skill deals extra damage after Fireball hits a burning enemy`

without touching the core T1–T4 logic.

---

## 8. Summary

The **Skill Mutation System** turns repeated use of a skill into a feeling of:

- **growth** – the skill becomes more complex and more satisfying,  
- **identity** – each ability has its own mutation fantasy,  
- **reward** – players who specialise in a skill unlock powerful, unique behaviour.

T1–T4 mastery is:

- **per-skill**,  
- **usage-based**,  
- and designed to work hand-in-hand with:
  - runes,
  - scaling,
  - and skill tags/types (see separate documents).

