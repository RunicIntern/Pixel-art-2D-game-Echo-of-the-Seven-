# Runic Journal – System & UX Overview  
### Echo of the Seven – Runic System

The **Runic Journal** is an in-game codex that tracks the player’s **knowledge about the runic alphabet**:

- which glyphs (letters) they have seen,  
- where those glyphs appeared,  
- what NPCs have said about them,  
- which fragments (half-words) and inscriptions have been recorded.

The Journal focuses on **mystery, context and investigation**.  
It does **not** automatically solve puzzles or reveal full rune recipes.

For confirmed, working rune words and their effects, see the **Runic Library** (separate system).

---

## 1. Purpose & Design Goals

The Runic Journal exists to:

- Help players **remember and revisit** the runic clues they’ve encountered.
- Make exploration and reading **feel meaningful**, not throwaway.
- Support **theory-crafting and note-taking** without giving away answers.
- Provide a natural home for:
  - glyph sketches,
  - fragments,
  - place descriptions,
  - NPC notes.

Design principles:

1. **Record, don’t solve**  
   - The Journal stores information the player has actually found.  
   - It doesn’t auto-complete missing letters or auto-discover meanings.

2. **Partial, evolving knowledge**  
   - Entries can change as the player learns more (e.g. new NPC quote, new location).

3. **World as a text**  
   - Shrines, doors, tombs and ruins become “pages” in a book the player can study.

---

## 2. Unlock & Access

### 2.1. Unlock Condition

The Journal can unlock in one of two ways (exact choice is a design decision):

- **Option A – Early Unlock**  
  - Available from the start of the game.  
  - The first runic glyph automatically creates the first entry.

- **Option B – Story Unlock (recommended)**  
  - The Journal UI appears after a key story moment, for example:
    - after meeting a runic scholar / Guardian,
    - after interacting with a major runic monument for the first time.
  - The NPC can directly hint:
    > “You will not remember all these marks. Write them down.  
    > This language punishes those who pretend they understand it.”

Recommended: **Option B** for a stronger narrative moment.

### 2.2. Access in UI

- The Journal is a **separate tab / menu** (e.g. `Runes → Journal`).  
- It has its own icon (e.g. a bound book with a glowing glyph on the cover).  
- It is distinct from the **Runic Library**, which stores working rune words.

---

## 3. Journal Structure

The Journal is divided into three main sections:

1. **Glyphs** – individual letters (symbols).  
2. **Fragments** – partial words or broken inscriptions.  
3. **Inscriptions** – contextual notes about specific locations and objects.

Future extensions (optional):

- **People** – NPCs associated with runes.  
- **Theories** – player-written notes or auto-generated summaries.

---

## 4. Glyphs – Single Letters

The **Glyphs** tab shows all runic letters the player has encountered in any form.

### 4.1. Glyph List

- Displayed as a grid or list of **glyph tiles**.
- Each tile shows:
  - the symbol (icon),
  - state of knowledge (e.g. `SEEN`, `HEARD`, `INTERPRETED`),
  - a small indicator of how many places it has appeared.

Unknown or not-yet-seen letters **do not appear**.  
The player only sees glyphs they have actually encountered.

### 4.2. Glyph Entry Layout

Clicking a glyph opens a detailed entry with:

1. **Glyph Icon**  
   - A clean, high-contrast drawing of the symbol.

2. **Knowledge State**  
   Possible states (examples):

   - `SEEN` – the player has seen the symbol somewhere, but knows nothing about it.  
   - `MENTIONED` – an NPC has talked about this symbol by name or description.  
   - `INTERPRETED` – the player has enough hints to show a rough meaning (still not a full rune recipe).  
   - `CONFLICTING` – the Journal has recorded **contradictory explanations** from different sources.

3. **Known Meanings (If Any)**

   A short list with tags and notes, e.g.:

   - **“Associated with: protection, oath”**  
   - “Some scholars call it ‘The Oath’. A priest in Ashenwall insists it represents ‘binding’ rather than ‘shielding’.”

   - These are **partial interpretations**, not final truths.

4. **Locations Where Seen**

   A chronological or collapsible list, for example:

   - Roadside chapel near **Brackenford**  
   - Sealed door in **Old Bloodmine**  
   - Tomb of **Sir Halver**  
   - Banner of the **Sun Oath** mercenaries

   Each entry may include a short description:

   > “Carved on the base of a small wayside altar. Villagers touch it for luck.”

5. **NPC Notes & Quotes**

   All dialogue snippets that mention this glyph or clearly refer to it, e.g.:

   > “To us, this mark is a promise. To the old gods, it might be a threat.” — High Priestess Ilaren  

   > “Never carve it without knowing the other letters. It doesn’t forgive mistakes.” — Exiled runesmith Varr

6. **Player Notes (Optional)**

   - If the design allows, players may add their own short notes to a glyph.  
   - This encourages theory-crafting and personal tagging.

---

## 5. Fragments – Half-Words and Broken Texts

The **Fragments** tab focuses on **incomplete sequences**:

- broken inscriptions,
- partial phrases,
- two letters of a three-letter word, etc.

### 5.1. Fragment List

- Shown as a list of **fragment cards**, each representing:
  - a unique fragment pattern (visual),
  - one or more locations where it appears.

### 5.2. Fragment Entry Layout

Each fragment entry may include:

1. **Fragment Visual**

   - A sketch showing how the fragment appears:
     - e.g. `[Glyph A] – [Glyph B] – [missing]`.

2. **Status**

   Example statuses:

   - `PARTIAL` – confirmed to be an incomplete word.  
   - `UNCONFIRMED` – unclear if it’s a full word or just random decoration.  
   - `RESOLVED` – later, if the fragment gets matched to a full word (optional link to Runic Library).

3. **Locations**

   - Every wall, monument, tablet or mural where this fragment appears.

4. **Notes & Theories**

   - Narrative comments and characters’ guesses, e.g.:

     > “The old woman in the village insists this fragment is part of an ancient prayer, but she doesn’t remember the end of it.”

5. **Links to Glyphs**

   - A list of glyphs that form the fragment.  
   - Clicking a glyph jumps to that glyph’s entry.

---

## 6. Inscriptions – Context & Places

The **Inscriptions** tab is about **where and how** runes appear in the world.

Each inscription is a **snapshot** of:

- a specific location,
- a set of glyphs and fragments,
- what happened there (if anything).

### 6.1. Inscription List

- Displayed as a list grouped by region:
  - e.g. `Region: Brackenford Road`, `Region: Old Bloodmine`, etc.
- Each entry line may show:
  - location name,
  - a small icon indicating if the inscription includes:
    - glyphs only,
    - a fragment,
    - a full word,
    - or is tied to a puzzle.

### 6.2. Inscription Entry Layout

Each inscription entry includes:

1. **Location Name & Region**

   - e.g. “Roadside Chapel – Brackenford Road”.

2. **Screenshot / Sketch (Optional)**

   - A stylised representation of the object or wall.

3. **Glyphs and Fragments Involved**

   - A row of symbols in the order they appear.  
   - Clicking a symbol opens its Glyph entry.

4. **Player Interaction Result**

   - e.g.:
     - “Touching the glyph had no effect.”  
     - “Rearranging the stones opened a secret passage.”  
     - “Matching the pattern lit all three braziers.”

5. **Narrative Notes**

   - Short description for flavour and memory:

     > “A small, neglected chapel under a leaning oak tree. Someone has recently cleaned the stone around the glyph.”

6. **Puzzle / Quest Flags (If Applicable)**

   - Markers like:
     - `PUZZLE SOLVED`,  
     - `QUEST-RELATED`,  
     - `INCOMPLETE` (if there is still something to do here).

---

## 7. Knowledge Progression & States

The Journal should reflect that **knowledge evolves**.

### 7.1. Glyph Knowledge States (Example Model)

- `UNKNOWN` – (no entry; player has never seen the symbol).  
- `SEEN` – symbol recorded from environment, no context yet.  
- `MENTIONED` – NPC talked about it, but with vague or conflicting info.  
- `INTERPRETED` – game judges that the player has enough aligned hints to show a rough summary (still not a full “this equals X buff”).  
- `CONFLICTING` – multiple sources disagree strongly (flagged so the player sees the ambiguity).

### 7.2. Automatic Updates

The Journal should:

- Automatically update when:
  - a new location shows the same glyph,
  - an NPC line about that glyph is heard,
  - a puzzle connected to that glyph is solved.
- Never **retroactively “fix” the past**:
  - conflicting notes remain; they’re part of the world’s fractured knowledge.

---

## 8. Interaction with the Runic Library

The Journal and the Library are **sister systems**:

- **Runic Journal**
  - Tracks:
    - glyphs,
    - fragments,
    - inscriptions,
    - NPC commentary.
  - Is about:
    - **lore, clues, and patterns**.

- **Runic Library**
  - Tracks:
    - fully confirmed rune words,
    - successful letter combinations,
    - their mechanical effects.
  - Is about:
    - **usable magic** and **crafting recipes**.

### Example Flow

1. Player sees a glyph on a chapel →  
   `Glyph entry created in Journal (SEEN)`.

2. Player hears a priest name and describe the symbol →  
   `Glyph state updates to MENTIONED, NPC quote added`.

3. Player later discovers a full rune word that uses this glyph and successfully crafts it →  
   - Runic Library:
     - adds a new word entry with effect.  
   - Journal:
     - may add a hint that this glyph “appears in at least one confirmed rune of protection”.

The Journal **never** shows raw numbers or full mechanical breakdown.  
Those belong to the Library.

---

## 9. UX Guidelines

To keep the Journal fun and not overwhelming:

1. **No spoilers**
   - Do not display glyphs or fragments the player hasn’t actually discovered.

2. **Lightweight readability**
   - Entries should be short and focused.  
   - The Journal is not a novel; it’s a reference tool.

3. **Strong location linking**
   - At least one click from:
     - Glyph → where seen.  
     - Inscription → glyphs involved.

4. **Search & filters (optional but useful)**
   - Filter by:
     - region,
     - knowledge state,
     - involvement in puzzles.

5. **Visual clarity**
   - Glyph icons must be readable and distinct even in small sizes.  
   - Use consistent colour coding for states and types.

---

## 10. Summary

The **Runic Journal**:

- records **what the player has learned about the alphabet**,  
- organises:
  - glyphs,
  - fragments,
  - inscriptions,
  - NPC hints,
- supports a feeling that:
  - **the entire world is filled with pieces of a broken language**,
- lets players revisit and connect clues without:
  - giving them a solved alphabet or full rune recipes.

It is the **investigation layer** of the runic system.  
For crafting and confirmed rune words, players turn to the **Runic Library**.
