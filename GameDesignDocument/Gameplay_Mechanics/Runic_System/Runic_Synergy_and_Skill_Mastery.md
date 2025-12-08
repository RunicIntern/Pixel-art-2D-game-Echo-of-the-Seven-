# Rune Synergy and Skill Mastery  
### Echo of the Seven – High-Tier Interactions

This document describes how **runes** interact with the existing **Skill Mutation System (T1–T4)** and how they enable:

1. **Tier Sync** – powerful effects when a high-tier skill is paired with a matching high-tier rune.  
2. **Rune-Enhanced Support** – turning strong heals/HoTs into group-saving defensive moments.  
3. **Cross-Class Skill Combos** – coordinated plays between different classes (e.g. tornado + fireball).

It builds on:
- `Skill_Mutation_System.md` – how skills evolve from T1 to T4.  
- `Runic_Alphabet_*.md` – how runes and rune tiers work.

Runes **do not replace** skill mutations.  
They **amplify** them and create high-end synergy opportunities.

---

## 1. Design Principles

1. **Layers, not overlap**
   - Skill mutations (T1–T4) define the **base behaviour** of abilities.  
   - Runes provide **extra power** and occasional signature effects, especially at high tier combinations (T4+T4).

2. **Clarity**
   - A player should always understand:
     - what the skill does on its own (T1–T4),  
     - what the rune adds on top.

3. **Endgame reward**
   - The most spectacular combos (e.g. triple fireball barrage, group-wide bulwark) require:
     - a mastered skill (T4),  
     - and a matching high-tier rune (T4).

4. **Synergy across roles**
   - Support and DPS are encouraged to coordinate:
     - tank ultimates amplifying healer HoTs,  
     - elemental combos between casters (fire + wind, etc.).

---

## 2. Tier Sync – Skill Tier + Rune Tier

**Tier Sync** happens when:

- a skill has reached a certain **mutation tier** (e.g. T4),  
- and the player equips a **matching rune** of the same **tier** and **type**.

This unlocks a **signature synergy effect** for that skill.

### 2.1. Basic Rules

- Tier sync is checked per skill:
  - Skill mutation tier: `Skill_Tier`  
  - Socketed rune tier (of appropriate aspect/type): `Rune_Tier`
- If `Skill_Tier >= N` and `Rune_Tier >= N` and the rune’s aspect matches the skill’s theme:
  - unlock a special synergy effect for that tier (usually designed for **T4+T4**).

Tiers below T4 can also gain smaller bonuses, but the **main fantasy** is:

> **T4 Skill + T4 Rune = “ultimate” version of that spell.**

---

### 2.2. Example: Fireball (Mage) – Tier Sync with Inferno Rune

**Base skill mutation (recap):**

- **T1 – Fireball**  
  - Single fire projectile, moderate damage on impact.

- **T2 – Ignite**  
  - Fireball has a chance to apply **Burn** (fire DoT).

- **T3 – Spreading Flames**  
  - Burn can spread to nearby enemies under certain conditions.

- **T4 – Combustion**  
  - Killing a burning enemy with Fireball causes an **explosion**,  
    dealing AoE fire damage and potentially igniting nearby targets.

This is the skill’s **internal evolution**, independent of runes.

---

### 2.3. T4 Skill + T4 Rune: “Inferno Barrage”

Now, the player equips a **Tier 4 Fire Rune** on Fireball, e.g.:

- **Rune Name (placeholder):** `Inferno Core`  
- **Rune Tier:** T4  
- **Rune Aspect:** Fire / Destruction

**Tier Sync Effect (concept):**

> When Fireball is at **T4** and socketed with **Inferno Core (T4)**,  
> it occasionally triggers **Inferno Barrage** instead of a normal cast.

**Inferno Barrage behaviour:**

- Fireball splits into **three rapid-fire projectiles**,  
  cast in quick succession (barrage-style).
- Each projectile:
  - explodes on impact in a **small AoE**,  
  - deals extra flat fire damage.
- This effect:
  - does **not** require the target to be burning,  
  - may have a proc condition (e.g. “every X casts” or “Y% chance on cast”).

Examples of parameters (tunable):

- Proc: `15–20%` chance on cast, or guaranteed every `5th` cast.  
- Damage: each barrage shot deals `~70%` of a normal Fireball’s direct damage,  
  but with extra AoE = strong clear potential.

**Key points:**

- The player still benefits from T2–T4 mutations:
  - barrage shots can ignite, spread burn, and trigger Combustion explosions.  
- The rune does **not** change the mutation path; it **rides on top of it**.

---

## 3. Rune-Enhanced Support – HoT + Tank Ultimate + T4 Rune

This section illustrates how runes can turn a strong heal-over-time effect into a **group-saving defensive cooldown**, especially when combined with tank ultimates.

### 3.1. Base Skill: Renewing Light (Healer)

**Class:** Healer / Priest / Cleric (placeholder)  
**Type:** Single-target HoT

**Mutations:**

- **T1 – Renewing Light**
  - Places a heal-over-time effect on a single ally (e.g. the tank).

- **T2 – Adaptive Recovery**
  - HoT heals slightly more when the target is at low HP.

- **T3 – Layered Grace**
  - Refreshing the HoT partially stacks remaining healing instead of overwriting it.

- **T4 – Critical Mercy**
  - When Renewing Light heals a target who is under a certain HP threshold:
    - it briefly increases **all healing received** by that target.

This gives a natural **“tank HoT”** progression without runes.

---

### 3.2. Tank Ultimate: Guardian’s Rally

**Class:** Tank (Warrior / Guardian archetype)  
**Type:** Defensive ultimate

**Behaviour:**

- When activated:
  - Increases the **tick rate** of active HoTs on the tank.  
  - Extends their remaining **duration** by a few seconds.  
  - Causes those HoTs to **spread** to nearby allies within a certain radius:
    - each ally receives a reduced-strength copy of the HoT.

Even without runes, this creates a powerful **healer + tank combo**:

- Healer keeps Renewing Light on the tank,  
- Tank uses Guardian’s Rally during heavy damage windows,  
- The group benefits from additional healing during the burst.

---

### 3.3. T4 Rune: Bulwark Sigil – Turning HoT into a Group Bulwark

Now, the healer equips a **Tier 4 Holy/Protection Rune** on Renewing Light:

- **Rune Name (placeholder):** `Bulwark Sigil`  
- **Rune Tier:** T4  
- **Rune Aspect:** Holy / Protection

**Tier Sync Effect (T4 Skill + T4 Rune):**

> When Renewing Light is at **T4** and socketed with **Bulwark Sigil (T4)**,  
> each target affected by Renewing Light gains powerful defensive buffs.

Additional effects provided by Bulwark Sigil:

- **Shield:**  
  - a barrier equal to a percentage of the target’s max HP.

- **Damage Reduction:**  
  - incoming damage reduced by a fixed percentage while the HoT is active.

- **Offensive Boost:**  
  - small but meaningful increase to **attack speed** and/or **cast speed**,
  - emphasising that well-protected allies can fight more aggressively.

When combined with **Guardian’s Rally**:

- The tank receives:
  - fast-ticking HoT, shield, damage reduction, and offensive buff.  
- Nearby allies receive:
  - a mini-version of all of the above when the HoT spreads.

Result:

> At high tiers, one well-timed HoT + tank ultimate + T4 rune  
> becomes a **coordinated defensive moment** that can stabilise the entire party.

Still, this remains:

- gated behind:
  - T4 skill mastery,
  - T4 rune acquisition,
  - and proper timing and coordination.

---

## 4. Cross-Class Skill Combos – Tornado + Fireball

This section covers **synergy between different classes’ abilities**, independent of runes, but potentially enhanced by them.

### 4.1. Base Skill: Stormcaller’s Tornado (Shaman)

**Class:** Shaman / Stormcaller  
**Type:** Persistent AoE control

**Behaviour (simplified):**

- Summons a **Tornado** at a target location.
- Tornado:
  - pulls enemies slightly towards its center,
  - deals periodic physical / air damage,
  - lasts for a set duration.

Mutations (example pattern):

- **T2** – increased pull strength or duration.  
- **T3** – Tornado can occasionally knock enemies up or slow their movement.  
- **T4** – Last tick of the Tornado deals a stronger burst of damage or a stronger displacement.

---

### 4.2. Elemental Combo: Tornado + Fireball (Mage)

Now we define a **world interaction rule**:

> When a **Fireball projectile** hits an **active Tornado**,  
> an **elemental combo** is triggered.

**Effects of the combo:**

1. **Tornado is “ignited”**
   - In addition to its usual damage, the Tornado:
     - deals extra **fire damage** each tick,  
     - visually changes to a firestorm / flaming vortex.

2. **Fireball is “shredded” into mini-fireballs**
   - At the moment of impact with the Tornado:
     - Fireball splits into several **smaller fire projectiles**,  
     - These smaller projectiles are:
       - launched out of the Tornado in random or semi-controlled directions,  
       - deal reduced individual damage,  
       - but travel faster and cover a wider area.

The result:

- A **single-target / small AoE** spell (Fireball)  
- + a **control AoE** (Tornado)  
→ together become a **wide-area chaos spell** that:
  - burns enemies caught in the Tornado,
  - sprays smaller fireballs outward for crowd damage.

This combo does **not require runes** to function, but:

- T4 skill mutations on Tornado and Fireball  
- and high-tier runes on each spell
  - can further increase:
    - fire damage per tick,
    - number of mini-fireballs,
    - pull strength or duration,
    - combo proc frequency.

---

## 5. Balancing & Constraints

To keep synergy powerful but under control:

1. **Gated by Tier**
   - Signature effects are reserved for high-tier combinations:
     - e.g. T4 skill + T4 rune,  
     - or T3+ combos with toned-down impact.

2. **Aspect Matching**
   - Only runes with the correct **aspect/type** (Fire, Holy, Storm, etc.)  
     can unlock the synergy for a given skill.

3. **Limited Slots**
   - Players can only assign runes to a limited number of skills.  
   - Choosing where to place a T4 synergy rune is a meaningful decision.

4. **Role Protection**
   - Support-oriented synergies (like Bulwark Sigil) should not out-damage true DPS classes.  
   - Offensive synergies should not grant more healing/shielding than real healers.

5. **Clear Tooltips**
   - Each synergy:
     - should be clearly described in the skill + rune tooltip combo,  
     - should indicate that it is unlocked by tier sync (for example: “Unlocked at Skill Tier 4 + Rune Tier 4”).

---

## 6. Summary

- **Skill Mastery** (T1–T4) defines how abilities evolve as they are used.  
- **Runes** add an extra layer of power and enable:
  - **Tier Sync** (T4 skill + T4 rune → signature effect),  
  - **Rune-Enhanced Support** (strong defensive/offensive group moments),  
  - **Cross-Class Skill Combos** (elemental interactions like Tornado + Fireball).

Together, these systems:

- reward long-term mastery of specific skills,  
- encourage cooperative play and party synergy,  
- and create memorable “big moments” in combat without erasing class identities.

