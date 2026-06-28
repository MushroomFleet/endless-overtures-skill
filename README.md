# Endless Overtures

> A Claude skill that invents phantom catalogues of classical music — works that never existed, numbered into the thousands — and renders each one as a ready-to-paste **Gemini Lyria 3.1** music prompt.

Point it at a composer. Get back a semantically named markdown catalogue of pieces from the timeline where that composer never stopped writing: Chopin's 2,604th nocturne, Debussy's 3,050th prélude, Tchaikovsky's 207th symphony. The impossible catalogue number is the fiction. The prompt underneath is real, and generates.

---

## 🎼 What is this?

**Endless Overtures** is an Agent Skill for Claude. Given a single classical composer, it produces one markdown artifact containing **8–12 invented works**, each with:

- a **fictitious catalogue title** that borrows the composer's real naming grammar (`Nocturne No. 2,604 in B-Flat Minor, Op. 911 No. 1`) but pushes the numbers absurdly high,
- a **one-line program note** — an image or a feeling, not a dry description,
- and a **fenced Lyria 3.1 prompt** written to actually sound like that work when fed to the model.

It's built on one core idea: **the title carries the fiction; the prompt carries the sound.** Lyria 3.1 doesn't read an opus number or a literal key signature, so every prompt is written to *embody* the mood the title only implies.

## ✨ Why

Lyria 3.1 can synthesise convincing instrumental music, but a one-line request ("a sad piano piece") gives it nothing to grip. This skill encodes the craft of writing prompts that work — naming the texture instead of the feeling, giving the model an *arc* instead of a static mood, and matching the named key to the colour the prompt describes — while wrapping the whole thing in a generative conceit that's genuinely fun: an alternate music history where the great catalogues ran on into the thousands.

The result is a reusable, extendable library of prompts in any classical composer's voice — useful for scoring, ambience, study, mood-boards, or simply imagining the music that history didn't get to write.

## 🗂️ What's inside

```
endless-overtures/
├── SKILL.md                              # the orchestrator: workflow + rules
└── references/
    ├── lyria-prompt-craft.md             # how Lyria 3.1 reads prompts; levers, skeleton, key→mood table
    ├── phantom-catalogue-method.md       # the alternate-history conceit + naming grammar per composer
    ├── composer-profiles.md              # a starting library of 10 composer voices (+ a "derive any other" fallback)
    └── example-chopin-nocturnes.md       # a complete, proven example as the gold standard
```

## 🚀 Installation

**Claude.ai / Claude apps:** upload `endless-overtures.skill` in your Claude skill settings (Settings → Capabilities → Skills).

**Claude Code:** place the `endless-overtures/` folder in your skills directory (e.g. `~/.claude/skills/endless-overtures/`).

Once installed, the skill's name and description sit in Claude's context and it triggers automatically when you ask for it.

## 🎹 Usage

Just name a composer:

```
use the endless-overtures skill with Pyotr Ilyich Tchaikovsky
```

or trigger it by intent, without the skill name:

```
invent some Rachmaninoff préludes that never existed, as Lyria prompts
```

Claude loads the composer's voice, writes the catalogue, and saves it as a markdown file named after the conceit — e.g. `tchaikovsky-ballets-that-never-were-lyria-prompts.md`. One composer per run.

### Optional flourishes

You can ask for extras on top of the default catalogue:

- a **fictional performer-editor** ("your timeline's Barenboim") and a phantom publishing house, to thicken the fiction;
- a **themed sub-opus** — a whole run in one key, one mood, or one hour of the night;
- a **late-style set** where the harmony drifts deliberately stranger, as if the composer aged decades past their real death.

## 🎶 Example output

A single entry from a generated catalogue looks like this:

> ### Nocturne No. 2,604 in B-Flat Minor, Op. 911 No. 1 — *"The Storm Returns"*
> > It begins by pretending to be calm.
>
> ```
> Solo piano nocturne, dark and restless. Opens brooding and quiet with a mournful cantabile theme over a low murmuring accompaniment, then builds into an agitated, stormy middle section with surging arpeggios and dramatic dynamic swells, before sinking back into shadow. Turbulent, passionate, deeply Romantic. Heavy rubato throughout. Resonant grand piano, intimate but powerful. Instrumental only, no vocals.
> ```

Copy the fenced prompt straight into Lyria 3.1.

## 🎻 Supported composers

A starting library of ten profiled voices ships in `references/composer-profiles.md`:

**Chopin · Debussy · Satie · Liszt · Bach · Scarlatti · Beethoven · Rachmaninoff · Ravel · Schubert**

The list is **not closed.** Name any composer — Scriabin, Brahms, Fauré, Albéniz, Mompou — and the skill derives the same fields (signature forms, instrumentation, textures, moods, keys, catalogue abbreviation) from Claude's own knowledge of their style, then proceeds identically.

## 🧠 How the conceit works

Each work borrows the composer's **real cataloguing system** and pushes only the numbers:

```
[Form] No. [running count, into the thousands] in [Key], [Cat.] [number] No. [within-set] — "[evocative title]"
```

The catalogue token matches the composer — `Op.` for Chopin and Tchaikovsky, `BWV` for Bach, `L.` for Debussy, `D.` for Schubert, `K.` for Scarlatti, `S.` for Liszt, `M.` for Ravel — so the invented work sits exactly one absurd digit away from the truth. Satie, who never numbered by opus, gets a bare sequence instead. The skill matches each composer's habits down to small details (Debussy's titles printed in parentheses *after* the music; Bach's bare catalogue lines with no titles at all).

## ⚙️ Notes on Gemini Lyria 3.1

- Prompts are **instrumental-only** by design — each ends by ruling out vocals so the model stays on the intended instrument.
- The named **key is a promise the prompt keeps**, not an instruction Lyria parses; the prompt translates it into mood via the key→mood cheat-sheet in `references/lyria-prompt-craft.md`.
- Prompts **name texture and arc** (where it stays quiet, where it lifts) rather than just a feeling, because that's what the model can actually act on.

---

## 📚 Citation

### Academic Citation

If you use this codebase in your research or project, please cite:

```bibtex
@software{endless_overtures,
  title = {Endless Overtures: Phantom Classical Catalogues as Gemini Lyria 3.1 Music Prompts},
  author = {Drift Johnson},
  year = {2026},
  url = {https://github.com/MushroomFleet/endless-overtures-skill},
  version = {1.0.0}
}
```

### Donate:

[![Ko-Fi](https://cdn.ko-fi.com/cdn/kofi3.png?v=3)](https://ko-fi.com/driftjohnson)
