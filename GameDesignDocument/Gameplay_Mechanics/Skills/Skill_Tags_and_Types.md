# Skill Tags and Types  
### Echo of the Seven – Skill Classification System

This document defines the **tag system** used to classify skills in Echo of the Seven.

Tags are used by:

- the **Skill Mutation System (T1–T4)** – to decide how a skill mutates,  
- the **Rune System** – to determine which runes can interact with which skills,  
- the **Synergy System** – cross-skill and cross-class combos (e.g. Tornado + Fireball).

Tags are primarily a **designer/tooling construct**.  
Players may see some of them indirectly through UI, but they exist mainly to keep the system consistent.

---

## 1. Design Goals

1. **Readable for designers, invisible for players**
   - Tags should be simple, reusable labels that make skills easier to reason about.
   - The player-facing fantasy is: “fire spell”, “heal over time”, “cone of frost” – tags are how we encode that.

2. **Drive systems, not the other way around**
   - Tags inform:
     - mutation patterns (T1–T4),
     - rune compatibility,
     - synergy rules (elemental interactions, mobility combos, etc.).
   - Systems (mutations, runes) should not depend on bespoke per-skill special cases where a tag would do.

3. **Composable, not bloated**
   - A skill should have:
     - a small set of meaningful tags,
     - not a wall of 15 labels.
   - Prefer a few strong, consistent categories over micro-tags.

---

## 2. Tag Groups Overview

Tags are grouped into several categories:

1. **Role Tags** – what the skill fundamentally does.  
2. **Delivery Tags** – how the skill is delivered in space/time.  
3. **Targeting Tags** – what and how many targets it can hit.  
4. **Element / School Tags** – flavour and interaction (fire, holy, storm, etc.).  
5. **Status / Effect Tags** – which statuses or unique effects it can apply or interact with.  
6. **Resource / Cost Tags** – how it interacts with resources (optional, lightweight).  
7. **Special / Behaviour Tags** – flags for rare behaviour (ultimate, convertible, etc.).

A single skill may have **multiple tags from several groups**, but typically **only one primary tag per group** where it makes sense.

---

## 3. Role Tags (What the Skill Does)

**Primary identity** of a skill in combat.

- `Damage`
  - The skill’s main purpose is to deal damage.
  - Can be single target or AoE, direct or over-time.

- `Heal`
  - Direct healing or health restoration.

- `HoT` (Heal over Time)
  - A subtype of Heal: healing applied as a periodic effect.

- `Support`
  - Buffs allies or their stats (damage, attack speed, cast speed, crit, etc.).
  - Does not primarily heal or damage.

- `Defense`
  - Shields, damage reduction, block/parry bonuses, mitigation.

- `Control`
  - Crowd control: stuns, roots, slows, silences, knockbacks, pulls, etc.

- `Mobility`
  - Moves the caster (dash, leap, teleport, blink, reposition).

- `Utility`
  - Does something useful but not strictly in the above categories:
    - reveals enemies, dispels, resource regen, vision, etc.

**Guideline:**

- Each skill should have **one main Role tag**, plus optionally one secondary (e.g. `Damage + Control` for a knockback nuke).

---

## 4. Delivery Tags (How the Skill is Delivered)

Defines **how** the effect travels / appears in the world.

- `Projectile`
  - Single or multiple moving projectiles (e.g. Fireball).

- `Beam`
  - Continuous line attack (e.g. Holy Beam, Lightning Channel).

- `Melee`
  - Close-range swing, strike, or combo around the character.

- `Nova`
  - Radial burst around the caster or a point.

- `GroundTarget`
  - Player selects a point on the ground; effect appears there.

- `PersistentArea`
  - An area that remains for some time (e.g. Tornado, consecrated ground).

- `Channel`
  - Requires the caster to channel; effect continues while active.

- `Trap`
  - Placed on the ground, triggers on enemy interaction.

- `Aura`
  - Constant effect around the caster or target (buff/debuff).

- `Summon`
  - Creates minions / totems / spirits that act independently.

**Guideline:**

- Skills usually get **one primary Delivery tag**.
- Some can combine (e.g. `GroundTarget + PersistentArea` for an AoE zone).

---

## 5. Targeting Tags (What and How Many Targets)

Defines how the skill chooses or hits targets.

- `Self`
  - Only affects the caster.

- `AllySingle`
  - Single ally (not self-only).

- `AllyArea`
  - AoE effect that targets allies.

- `EnemySingle`
  - Single enemy target.

- `EnemyMulti`
  - Multiple enemies but not strictly AoE (e.g. chaining or multiple projectiles).

- `AoE`
  - Standard area-of-effect on enemies.

- `Cone`
  - Cone-shaped area in front of the caster.

- `Line`
  - Line / piercing effect (projectiles or beams that go through multiple targets).

- `Global`
  - Affects targets regardless of distance (rare, usually ultimates or utility).

**Guideline:**

- Combine with Delivery tags for clarity:
  - `Projectile + EnemySingle`,
  - `GroundTarget + AoE`,
  - `Aura + AllyArea`, etc.

---

## 6. Element / School Tags

Defines what **element / magic school / damage type** the skill belongs to.

Common element/school tags (examples):

- `Fire`
- `Frost`
- `Storm` / `Lightning`
- `Shadow`
- `Holy`
- `Nature`
- `Arcane`
- `Physical`
- `Poison`
- `Bleed` (can be a status or a sub-element)

These tags are used by:

- runes that care about element (e.g. Fire rune only buffs `Fire` skills),
- elemental combos (e.g. `Fire` projectile interacting with `Storm` Tornado),
- resistances / vulnerabilities.

**Guideline:**

- Usually **one primary element**.  
- In rare cases, a skill can carry two:
  - e.g. `Physical + Holy` strike.

---

## 7. Status / Effect Tags

Indicate which **status effects** a skill can apply or interact with.

Examples:

- `Burn`
- `Bleed`
- `Poisoned`
- `Chilled`
- `Frozen`
- `Shocked`
- `Stunned`
- `Rooted`
- `Slowed`
- `Silenced`
- `Disarmed`
- `Marked` (e.g. extra damage taken)
- `Weakened` (reduced damage dealt)
- `Shielded`
- `Hastened` (speed up)
- `Fortified` (damage reduction)

These tags are crucial for:

- mutation patterns:
  - T2 introduces the status (e.g. `Burn`),
  - T3 interacts with it, spreads it, ramps it, etc.
- rune effects:
  - runes that increase duration, strength, or spread of specific statuses.
- combo logic:
  - some skills gain bonuses when hitting targets with certain statuses.

**Guideline:**

- Only tag statuses that:
  - are mechanically relevant,
  - are actively applied or required by the skill’s logic.

---

## 8. Resource / Cost Tags (Optional)

Lightweight tags describing how a skill interacts with resources.

- `ManaCost`
- `RageCost`
- `FocusCost`
- `HealthCost`
- `NoCost` (basic attack style)

Additional behaviour:

- `GeneratesResource` (e.g. builds Rage).
- `ConsumesStacks` (e.g. uses combo points / charges).

Not all systems need these tags, but they can be useful for:

- rune interactions (e.g. runes that interact with Health-cost skills),
- class design (e.g. resource-specific archetypes).

---

## 9. Special / Behaviour Tags

Flags for special behaviour that does not fit other groups.

Examples:

- `Ultimate`
  - Big cooldown, defining skill of a kit.

- `Signature`
  - Iconic skill for the class; often used as a balance anchor.

- `Convertible`
  - Skill can change its behaviour based on certain systems:
    - e.g. `Convertible: HealToStrongHoT`, or `Convertible: DamageToAoE`.  
    - (If later you bring back role-conversion via specific runes.)

- `ComboStarter`
  - Skill creates a state that other skills can explicitly follow up on.

- `ComboFinisher`
  - Skill consumes a state or finishes a combo chain.

- `PetInteraction`
  - Skill mainly interacts with summoned units.

These tags help create advanced systems (e.g. skill trees, combo rules, rune synergies).

---

## 10. Putting It Together – Example Skill Tags

### 10.1. Fireball (Mage)

**Description:** Core single-target / small AoE fire spell.

Suggested tags:

- **Role:** `Damage`  
- **Delivery:** `Projectile`  
- **Targeting:** `EnemySingle` (with small impact AoE)  
- **Element / School:** `Fire`  
- **Status / Effect:** `Burn` (from T2 onwards), `Explosive` (from T4 conceptually)  
- **Special:** `Signature` (if it’s iconic for the Mage)

These tags support:

- T1–T4 mutation pattern from the Skill Mutation System,  
- rune interactions (Fire runes, Burn runes),  
- elemental combos (e.g. interacting with a `Storm` Tornado).

---

### 10.2. Renewing Light (Healer / Priest)

**Description:** Single-target HoT primarily used on tanks.

Suggested tags:

- **Role:** `Heal`, `HoT`  
- **Delivery:** `SingleTarget` (effect applied as buff; can be treated as `Aura` on the target)  
- **Targeting:** `AllySingle`  
- **Element / School:** `Holy`  
- **Status / Effect:** `Regeneration`, `Shielded` (if combined with runes at high tier)  
- **Special:** `Signature` (core heal)

Tags like `HoT`, `Holy` and `Regeneration` make it easy for:

- mutation rules to identify it as a **support/heal** candidate,  
- runes like `Bulwark Sigil` to enhance it with shields and damage reduction.

---

### 10.3. Stormcaller’s Tornado (Shaman)

**Description:** Persistent AoE that pulls enemies and deals air/physical damage.

Suggested tags:

- **Role:** `Control`, `Damage`  
- **Delivery:** `GroundTarget`, `PersistentArea`  
- **Targeting:** `AoE`  
- **Element / School:** `Storm`, `Physical`  
- **Status / Effect:** `Pulled`, `Slowed` (if the mutation adds slow)  
- **Special:** `ComboStarter` (for interactions with `Fire` projectiles)

These tags:

- mark Tornado as a great candidate for:
  - control-focused mutations,  
  - rune enhancements (more pull strength, more ticks),
- enable elemental combos:
  - e.g. `Fire` projectiles hitting a `Storm` `PersistentArea` ignite it and spawn mini-fireballs.

---

## 11. How Tags Drive Systems

### 11.1. Skill Mutation System

- Role + Status tags help decide mutation patterns:
  - `Damage + Burn` → use the pattern from section 5.1 (status → spread → explosion).  
  - `Heal + HoT` → use support pattern (single → stronger → share → clutch).

### 11.2. Runes

- Runes can specify:
  - “Works with skills that have tags: `Fire + Damage + Projectile`.”
  - “Buffs skills with: `Heal + HoT`.”
  - “Additional effects when hitting targets with: `Burn`, `Bleed`, `Chilled`.”

### 11.3. Synergy & Combos

- Element + Delivery tags define synergy rules:
  - `Fire + Projectile` + `Storm + PersistentArea` → elemental combo (Fireball + Tornado).
- Role + Special tags define combo roles:
  - `ComboStarter` creates states (marks, burns, debuffs),
  - `ComboFinisher` consumes them for big payoffs.

---

## 12. Guidelines for Designers

1. **Keep it minimal, but meaningful**
   - 1–2 Role tags, 1 Delivery tag, 1 Targeting tag, 1 Element, and a handful of Status/Special tags is usually enough.

2. **Be consistent**
   - If two skills are meant to behave similarly in systems (mutations, runes, combos), they should share tags.

3. **Tag what matters**
   - Don’t tag flavour-only details that never affect mechanics.

4. **Use tags to prevent one-off hacks**
   - If you keep adding special-case logic “only for this skill”, ask:
     - “Could this be solved by a new tag and a generic rule instead?”

---

## 13. Summary

The tag system provides a **shared language** for:

- skills,
- mutation rules,
- rune effects,
- synergy and combo systems.

With a clear tagging scheme, it becomes much easier to:

- extend the game with new skills and runes,  
- maintain consistency across classes and roles,  
- design deep, systemic interactions without chaos.

Tags are the **connective tissue** between your:

- Skill Mutation System,  
- Rune System,  
- and future class/group synergy designs.

