
# Rune Crafting – Player-Facing Overview  
### Echo of the Seven – Runic System

Rune crafting is the process of turning **runic words** into **active rune stones** that can be socketed into gear or used in rituals.

It is:

- **unlocked later in the game** (not at level 1),  
- **highly skill-based** (both in-story and mechanically),  
- influenced by **character stats and class archetype**,  
- and potentially **dangerous** when dealing with high-tier runes.

For information about the runic alphabet and discovery of letters, see:  
- `runic_alphabet_player_version.md`  
For information about tracking glyphs, fragments and inscriptions, see:  
- `runic_journal.md`

---

## 1. Unlocking Rune Crafting

Rune crafting is not available at the start of the game.

### 1.1. Story Unlock

- The player unlocks rune crafting after:
  - reaching a certain level / story chapter, and  
  - completing a dedicated **“First Engraving”** quest with a runesmith / Guardian / scholar.
- This quest:
  - explains the **basic risks** of handling runes,  
  - grants access to a **Rune Station** in a hub area,  
  - rewards the player with:
    - one **safe Tier 1 rune word**,  
    - a small number of **blank rune stones**.

### 1.2. Rune Stations

Rune crafting can only be performed at specific locations:

- rune altars,  
- runesmith forges,  
- ancient focus platforms.

Each Rune Station provides access to the **Rune Crafting UI**.

---

## 2. Ingredients & Requirements

To craft a rune, the player needs:

1. **Blank Rune Stone**
   - A mundane stone prepared for engraving.
   - Comes in quality tiers (e.g. basic → enhanced → masterwork).
   - Low-tier stones are safer but have lower potential.

2. **Runic Word**
   - Either:
     - a **known word** recorded in the **Runic Library**,  
     - or a **custom letter combination** the player wants to test.
   - Only **2–3 letter sequences** can be attempted.

3. **Catalysts / Materials**
   - Optional but highly recommended, especially for higher tiers:
     - elemental essences (fire, frost, shadow, light, etc.),  
     - rare metals or monster parts,  
     - faith-related items for sacred runes.
   - Catalysts increase:
     - stability,
     - maximum potential effect,
     - or chances to avoid corruption.

4. **Character Capability**
   - Some rune words may require:
     - a minimum **character level**,  
     - certain **stat thresholds** (e.g. INT, STR, DEX, FTH),  
     - or special story flags (e.g. “has completed Guardian Trial”).

If requirements are not met, the UI should clearly indicate:

- `INSUFFICIENT KNOWLEDGE`,  
- `STATS TOO LOW`,  
- or `MISSING MATERIALS`.

---

## 3. Crafting Flow (Player Perspective)

At a Rune Station, the basic flow is:

1. **Select Base**
   - Choose:
     - a **blank stone**,  
     - or an **existing rune** to overwrite (with warning).

2. **Choose Word**
   - Option A: pick a **known word** from the Runic Library.  
   - Option B: manually select **letters** (experimental crafting):
     - if the combination is unknown, this is a **discovery attempt**.

3. **Add Catalysts (Optional)**
   - Slot in optional materials:
     - increase stability,
     - bias towards certain effects,
     - reduce corruption risk.

4. **Engraving Minigame**
   - The player traces, times or clicks through **segments of the glyphs**.
   - Performance creates a **base quality score**, e.g.:
     - `Crude`, `Stable`, `Perfect`.
   - Higher tiers and more complex words:
     - have stricter timing windows,
     - punish mistakes more severely.

5. **Result & Outcome**
   - After engraving, the game rolls the outcome based on:
     - minigame performance,  
     - character stats & class,  
     - rune tier & word difficulty,  
     - catalysts and stone quality.

The result is presented with clear feedback and a lore-flavoured description.

---

## 4. Outcomes: Success, Failure & Corruption

### 4.1. Positive Outcomes

Examples (naming subject to change):

- **Crude Rune**
  - Effect works, but weaker than intended.
  - Slightly lower numbers or shorter duration.

- **Stable Rune**
  - Standard, expected power level.
  - This is the baseline quality for a decent crafting attempt.

- **Refined / Perfect Rune**
  - Above-average stats or minor bonus effect.
  - Only possible with:
    - strong performance in the engraving minigame,
    - appropriate stats,
    - and/or high-quality stones and catalysts.

### 4.2. Neutral / Failure Outcomes

- **Inert Stone**
  - The word fails to bind.
  - The blank stone is consumed or downgraded.
  - No active rune is created.

- **Cracked Rune**
  - The rune partially forms but is unstable.
  - Effect may:
    - be weaker than a Crude Rune,
    - have shorter duration,
    - or come with minor drawbacks (e.g. small self-damage on use).
  - Can be:
    - salvaged for fragments,
    - or reforged at a cost.

### 4.3. Corrupted Outcomes

Especially with higher-tier words (T3, T4), failures can become **dangerous**:

- **Corrupted Rune**
  - The word binds in a twisted way.
  - The rune grants a powerful effect combined with a strong drawback.
  - Example:
    - greatly increased damage but slowly drains health,
    - powerful shield that also reduces healing received.

Corruption chances increase when:

- the player’s stats are too low for the rune’s difficulty,
- catalysts are missing,
- the engraving performance is poor,
- the word belongs to **high tiers** (especially T4 arcane runes).

Some corrupted runes may actually be **valuable to certain builds**, but they are always risky.

---

## 5. Tiers & Difficulty (High-Level)

Rune words are broadly divided into **tiers** (T1–T4). From a crafting point of view:

- **T1 (Basic)**
  - Low risk, low reward.
  - Ideal for early experimentation.
  - Failure usually results in Inert or Cracked, not Corrupted.

- **T2 (Advanced Basics)**
  - Higher numbers, more focused bonuses.
  - Moderate risk of Cracked results.

- **T3 (Rare / Build-Defining)**
  - Strong, specialised effects.
  - Requires better stones, and usually catalysts.
  - Some chance of Corrupted outcomes on failure.

- **T4 (Mythic / Endgame)**
  - Can drastically alter how skills or builds function.
  - Very demanding in terms of:
    - stats,
    - materials,
    - and crafting precision.
  - Failure can easily produce **dangerous Corrupted runes**.

Not every character is equally suited to craft every rune tier.

---

## 6. Stats & Class Influence (High-Level)

Rune crafting is affected by both **stats** and **class archetype**.  
Exact formulas are a dev detail, but the player-facing fantasy is:

- **Intelligence (INT)**
  - Improves success and quality for:
    - complex, arcane, elemental and control runes.
  - Crucial for **Arcane T4** runes.

- **Faith (FTH)**
  - Improves:
    - healing, warding and blessing runes.
  - Crucial for sacred / divine runes.

- **Strength (STR)**
  - Favours:
    - physical damage, impact and “brutal” runes.
  - Increases chances to craft high-quality **martial runes**.

- **Dexterity (DEX)**
  - Favours:
    - mobility, crit, evasion, and precision-focused runes.
  - Improves engraving accuracy for fast, intricate glyphs.

### Class Archetype Modifiers

Each class archetype receives **hidden bonuses** for certain rune types:

- **Mage**
  - Bonus to arcane and elemental runes, especially at higher tiers.
- **Warrior**
  - Bonus to physical damage, on-hit and defensive runes.
- **Rogue**
  - Bonus to crit, evasion, mobility and on-kill runes.
- **Paladin / Priest**
  - Bonus to healing, shields and faith-based runes.

This means:

- Any class can **use** runes,  
- but different builds excel at crafting **different kinds** of high-tier runes.

---

## 7. Experimentation vs. Known Recipes

There are two main ways to craft:

### 7.1. Crafting from Known Words (Recipes)

- Choose a word that is already:
  - discovered in the **Runic Library**,  
  - and marked as a valid rune.
- Crafting shows:
  - expected rune type (e.g. “fire damage rune”),
  - difficulty/tier,
  - recommended stats and catalysts.

Safer, more predictable – but requires prior discovery.

### 7.2. Experimental Crafting (Unknown Combinations)

- Manually choose letters to form:
  - a 2–3 letter sequence the player has not yet unlocked as a word.
- Outcome possibilities:
  - discover a **new valid word** (added to Runic Library),
  - produce an inert or cracked stone,
  - accidentally create a **Corrupted rune**.

This supports:

- advanced players who want to test theories about the language,
- a sense that the system is deeper than just “known recipes”.

---

## 8. Upgrading, Re-Engraving & Removing Runes

### 8.1. Upgrading

Some runes (especially T1–T2) can be:

- reforged into higher quality versions, or  
- combined into improved variants (e.g. merging two similar T1 into one stronger T2).

This usually requires:

- multiple copies of the same rune,  
- additional materials,  
- and a higher-level Rune Station.

### 8.2. Re-Engraving

Players can choose to:

- overwrite an existing rune on a stone,  
- or strip the stone back to a blank-ish state with a loss of power.

High-tier runes may:

- resist re-engraving,  
- risk cracking or corrupting if forced.

### 8.3. Removing from Gear

Socketing and unsocketing rules depend on overall itemisation design, but general guidelines:

- Low-tier runes:
  - relatively cheap and safe to remove or replace.
- High-tier runes:
  - may require:
    - special tools,
    - rare materials,
    - or accepting a chance that the rune (or item) is destroyed in the process.

---

## 9. Safety Nets & Early-Game Experience

To avoid punishing new players too harshly:

- Early rune quests and T1 crafting:
  - use safer stones,
  - reduce or remove corruption chances,
  - only produce:
    - Stable, Crude, or Inert outcomes.
- The “First Engraving” quest:
  - guarantees at least one working T1 rune,
  - demonstrates failure, but in a controlled, low-stakes way.

Real danger and high risk–high reward crafting:

- is mostly reserved for:
  - T3–T4 words,
  - rare materials,
  - and endgame content.

---

## 10. Summary

Rune crafting is:

- a **late-unlock, high-impact system** that grows from the player’s understanding of the runic alphabet,  
- deeply tied to:
  - **exploration** (finding words and letters),
  - **stats and class fantasy** (who is good at which runes),
  - **risk vs. reward** (stable vs. corrupted outcomes).

Players who:

- explore thoroughly,  
- listen to NPCs,  
- study their Runic Journal,  
- and dare to experiment at Rune Stations

will gradually assemble a **unique library of runes** and define their own runic “style” for each character.
