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

To keep the system coherent and easy to reason about, designers can follow these **pattern guidelines** when defining T2–T4 mutations.  
These are not hard rules, but recommended shapes for most skills.

### 5.1. Damage Skills

Typical fantasy: **“basic hit → apply status → status interacts → big payoff”**

- **T2 – Status Introduction**
  - The skill gains a chance (or guarantee under some condition) to apply a status effect, e.g.:
    - Burn, Bleed, Poison, Chill, Shock, Mark, Weaken, etc.
  - The status should:
    - match the skill’s element/role,
    - be visible in the UI (icon, visual cue).

- **T3 – Status Interaction / Spread**
  - The skill now **interacts** with its own status:
    - spread it to nearby enemies,
    - ramp its power over time or with repeated hits,
    - trigger a secondary effect when re-applied.
  - Example patterns:
    - “Hitting a burning target increases burn damage.”
    - “Bleeding targets take extra damage from this skill.”
    - “Poison jumps to nearby enemies when the target dies.”

- **T4 – High-Impact Payoff**
  - The skill gains a **strong, visible climax effect**, often:
    - on-kill,
    - on-crit,
    - or when hitting heavily afflicted targets.
  - Common T4 shapes:
    - explosion on kill,
    - extra projectile(s) or chain,
    - empowered “execute” window,
    - large AoE conversion.

Damage skills should feel:
- **reliable** at T1,
- **interesting** at T2–T3,
- **spectacular** at T4.

---

### 5.2. Defensive / Support Skills

Typical fantasy: **“selfish effect → better for you → share with others → emergency button”**

- **T2 – Secondary Benefit**
  - Add a small, clear extra effect, e.g.:
    - small self-heal or shield,
    - resist buff,
    - resource boost (mana, stamina, focus),
    - short mitigation window.

- **T3 – Sharing / Extension**
  - The effect starts to **affect others** or **cover more time/space**:
    - splash healing,
    - aura extension,
    - copying a buff to nearby allies,
    - increased duration on refreshed applications.

- **T4 – Clutch / “Oh Shit” Behaviour**
  - The skill becomes a **strong emergency tool** when used at the right time:
    - big shield or mitigation when target is low HP,
    - group cleanse or strong debuff removal,
    - revive-like behaviour (if allowed by game design),
    - massive temporary buff with a meaningful cooldown.

Support/defensive skills should make players feel like they can **save a fight** when used well, especially at T4.

---

### 5.3. Mobility Skills

Typical fantasy: **“basic movement → small bonuses → interaction with space/enemies → stylish, dramatic move”**

- **T2 – Efficiency Buff**
  - Mobility skill gains minor utility, e.g.:
    - shorter cooldown on hit or on dodge,
    - small speed bonus after using the skill,
    - brief dodge/parry window,
    - resource gain if used correctly.

- **T3 – Interaction with Terrain or Enemies**
  - Movement leaves behind or creates **something in the world**:
    - a trail (fire, poison, slow, frost),
    - knockback or mark on enemies you pass through,
    - trap-like effect at starting or ending position.

- **T4 – Dramatic Upgrade**
  - The skill gets a big, visually clear enhancement:
    - teleport/cloning variant,
    - second activation window (double dash, blink return),
    - large AoE effect at start/end (shockwave, vortex, stun),
    - strong synergy with statuses already present on enemies.

Mobility skills at T4 should change how players **position and think** in combat, not tylko „+5% speed”.

---

## 6. Interaction with Runes (High-Level)

Full rune mechanics and Tier Sync (T4 Skill + T4 Rune) are described in separate rune documents.  
This section only defines how **mutations and runes conceptually relate**.

### 6.1. Mutations Are Intrinsic

- T1–T4 behaviours are **intrinsic** to the skill.
- Once unlocked by usage:
  - they are **always active**,  
  - regardless of:
    - gear,
    - runes,
    - or other systems.
- Respeccing runes or items **does not remove** T2–T4 effects.

### 6.2. Runes Modify or Amplify Mutations

Runes interact with mutated skills by **modifying** or **amplifying** existing behaviour.  
They do **not** define the base logic of the skill.

Examples of what runes can do:

- Increase or reshape T2 status effects:
  - longer burn duration,
  - stronger bleed ramp,
  - more reliable chill application.
- Enhance T3 interactions:
  - faster or wider spread,
  - stronger secondary effects on afflicted targets.
- Boost T4 payoffs:
  - larger explosion radius,
  - extra projectiles on trigger,
  - stronger execute damage,
  - “next skill” bonuses after a T4 condition is met (e.g. “after a Combustion explosion, your next spell deals extra damage”).

### 6.3. Synergy, Not Replacement

- Runes **never** unlock T2–T4 tiers.
  - Only **usage** of the skill does that.
- Runes **ride on top of** unlocked mutations:
  - making them hit harder,
  - trigger more often,
  - or combo better with other skills.
- High-tier rune synergy (e.g. **T4 skill + T4 rune → signature effect**) is:
  - handled in rune-specific documents,
  - but always respects the core T1–T4 behaviour defined here.

---

## 7. Example Skill – Fireball (Full T1–T4)

**Class:** Mage  
**Role:** Core single-target / small AoE fire spell.

This example follows the damage pattern from section 5.1.

### Tier 1 – Basic Fireball (T1)

- Launch a fire projectile at a target.
- Deal moderate fire damage on impact.
- No status effects yet.

### Tier 2 – Ignite (T2)

- Fireball now has a chance to **ignite** enemies:
  - applies a burning damage-over-time effect for a short duration.

### Tier 3 – Spreading Flames (T3)

- If an ignited enemy is:
  - hit again by Fireball, **or**
  - the burn naturally ticks to its final moments,
- the burning effect can **spread** to nearby enemies.

This turns Fireball into a **status engine**, not just a single hit.

### Tier 4 – Combustion (T4)

- If a burning enemy:
  - **dies from Fireball**, or
  - **dies while burning** from Fireball’s Ignite,
- they **explode**, dealing fire damage around them.
- The explosion can also:
  - ignite nearby enemies,
  - feeding back into T2/T3 (more burns → more spread → more potential explosions).

Fireball now has a full identity:

- T1 – simple direct hit.  
- T2 – applies fire status (Burn).  
- T3 – spreads the fire.  
- T4 – creates explosive chain reactions.

### 7.1. Rune Examples (High-Level)

Rune effects (defined in rune docs) could do things like:

- `+X% cast speed for Fireball`
- `+Y% burn duration on Ignite`
- `+Z% explosion radius or damage for Combustion`
- `After Fireball hits a burning enemy, your next spell deals extra damage`

Additionally, a **Tier 4 Fire Rune** socketed into a **T4 Fireball**  
may unlock a **signature Tier Sync effect** (e.g. a periodic triple-fireball barrage)  
– see `Rune_Synergy_and_Skill_Mastery.md` for those high-end interactions.

---

## 8. Summary

The **Skill Mutation System** turns repeated use of a skill into:

- **growth** – each tier adds new layers of behaviour,  
- **identity** – damage, support and mobility skills evolve in distinct, thematic ways,  
- **reward** – players who specialise in a skill unlock powerful, unique behaviour at T4.

Key properties:

- Mastery (T1–T4) is:
  - **per-skill**,  
  - **usage-based**,  
  - permanent once unlocked.

- Mutations are designed to work hand-in-hand with:
  - **runes** (amplifiers and Tier Sync effects),  
  - **scaling systems** (stats, level, gear),  
  - **skill tags/types** (element, role, delivery method).

Runes, scaling and tags extend what is defined here,  
but they never replace the core fantasy of a skill’s **own evolution**.


