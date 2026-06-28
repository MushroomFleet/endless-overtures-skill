---
name: endless-overtures
description: Generate a semantically named markdown artifact full of ready-to-paste Gemini Lyria 3.1 music prompts that invent an "endless" phantom catalogue for a chosen classical composer — works that never existed, catalogued into the thousands, as if the composer's output continued in a future that never happened. Use this skill whenever the user says "use the endless-overtures skill", or asks to invent, imagine, or generate fictional / never-written pieces, nocturnes, préludes, études, sonatas, movements, or symphonies in the style of a specific classical artist (Chopin, Debussy, Satie, Liszt, Bach, Rachmaninoff, and so on) as Lyria or Lyria 3.1 music-generation prompts. Also trigger when the user names a classical composer and wants AI music prompts, an alternate-history catalogue, or "pieces that never were" in that composer's voice, even if they don't say the skill name. Targets one composer per run and outputs the catalogue as a markdown file.
---

# Endless Overtures

Invent a phantom catalogue of classical works that never existed — written for one chosen composer, catalogued into the thousands, as if their output continued in a future that never happened — and render each invented work as a ready-to-paste Gemini Lyria 3.1 music prompt.

The guiding idea: **the title carries the fiction; the prompt carries the sound.** The impossibly high catalogue number is the alternate-history conceit. The prompt underneath is what actually drives the model, because Lyria does not read a catalogue number or honor a literal key signature.

## What you produce

A single markdown artifact saved to `/mnt/user-data/outputs/`, semantically named after the conceit and the composer — for example `debussy-preludes-that-never-were-lyria-prompts.md`. It contains **8–12 invented works (default 10)**, each with a fictitious catalogue title, a one-line program note, and a fenced Lyria 3.1 prompt — plus a short method note and an "author your own" template so the user can keep extending the catalogue themselves.

## Workflow

### 1. Identify the target composer
The user names a classical composer or artist (e.g. "use endless-overtures for Rachmaninoff"). If none is named, ask which composer before doing anything else — the whole artifact hinges on it. Target **one** composer per run.

### 2. Load the composer's voice
Read `references/composer-profiles.md` and find the composer. Use their signature forms, instrumentation, characteristic textures, signature moods, typical keys, and their **real-world catalogue abbreviation** (Op., BWV, D., L., K., S., M. …). If the composer isn't profiled, derive the same fields from your own knowledge of their style — the profiles are a starting set, not a closed list.

### 3. Load the craft and the conceit
Read both, every run:
- `references/phantom-catalogue-method.md` — how to extend the naming grammar into the thousands, choose which forms to include, and keep the fiction internally consistent.
- `references/lyria-prompt-craft.md` — how Lyria 3.1 reads a prompt, the levers to pull, the prompt skeleton, and the key→mood cheat-sheet that makes the named key and the written sound agree.

### 4. Choose the contents
Default shape (adapt to the composer):
- **Core set (5–7):** the composer's signature form — Chopin → nocturnes, Debussy → préludes, Satie → gnossiennes, Bach → preludes & fugues, Scarlatti → sonatas — numbered absurdly high.
- **Phantom forms (2–3):** other forms the same composer actually wrote, for variety of mood and texture.
- **One phantom large-scale work (optional, encouraged):** a single movement of an invented sonata, suite, or symphony — this honors the "movements or symphonies that never existed" idea. Only hand the composer an orchestra if it belongs in their world; otherwise keep it to their real instrument.

### 5. Write each entry
Match the exact per-entry format shown in `references/example-chopin-nocturnes.md`: an H3 catalogue title, a one-line blockquote program note, then the Lyria 3.1 prompt in its own fenced code block.

Four rules make the set feel real:
- **Match the key to the mood.** Lyria won't honor a literal key signature, so the named key is a promise the prompt must keep — use the key→mood cheat-sheet.
- **Use the composer's real catalogue abbreviation**, pushed into impossible numbers. That mismatch — exact grammar, absurd count — is where the alternate future lives.
- **Vary the works.** Spread moods, tempos, and keys across the set so Lyria produces genuinely different outputs, not ten versions of one piece.
- **Keep every prompt instrumental.** End each prompt by ruling out vocals so the model stays on the intended instrument.

### 6. Assemble and name the file
Assemble in this order:
1. A title and a short concept paragraph (the alternate-timeline framing for this composer).
2. A "How this catalogue works" note — three bullets adapted from `lyria-prompt-craft.md`.
3. The core set.
4. The phantom forms.
5. The phantom large-scale work (if included).
6. An "Author your own" section: the naming grammar, the prompt skeleton, and the key→mood table.

Save to `/mnt/user-data/outputs/[composer-slug]-[form]s-that-never-were-lyria-prompts.md` and present it with `present_files`.

## Optional flourishes
Offer these when they fit, or honor them on request:
- A **fictional performer-editor** ("your timeline's Barenboim") and a phantom publishing house, to thicken the conceit.
- A **themed sub-opus** — a whole run in one key, or one mood, or one time of night.
- A **late-style set** where the harmony drifts deliberately stranger, as if the composer aged decades further than they actually did.

## Style reference
`references/example-chopin-nocturnes.md` is a complete, proven example — the gold standard for tone, density, and prompt quality. Read it when you want a model to match. Don't reuse its specific works; invent fresh ones for the requested composer.
