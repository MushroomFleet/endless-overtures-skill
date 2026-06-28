# The Phantom Catalogue Method

How to build the alternate-history conceit for any composer, consistently.

## The premise

A real composer left a finite catalogue and then stopped — usually because they died. This skill writes from the timeline where they didn't: where the catalogue kept growing, where the same hand (or the school that inherited it) went on numbering night-pieces and études and sonatas **into the thousands**. The works are invented. The grammar of their names is borrowed exactly from the real catalogue, so the fiction sits one absurd digit away from the truth.

> Chopin left 21 nocturnes and died at 39. This is Nocturne No. 2,604.

## The naming grammar

Borrow the composer's **real cataloguing system** and push only the numbers:

```
[Form] No. [running count, into the thousands] in [Key], [Cat.] [number] [No. within-set] — "[evocative title]"
```

- **Form** — the actual form the composer wrote (nocturne, prélude, étude, sonata, gnossienne, prelude & fugue, impromptu…).
- **Running count** — the headline absurdity. Hundreds to tens of thousands. This is what signals the alternate future.
- **Key** — a real key, chosen so its mood matches the prompt (see `lyria-prompt-craft.md`).
- **Cat.** — the composer's own abbreviation, also pushed high:
  - Chopin, Beethoven, Rachmaninoff, Scriabin → **Op.**
  - Bach → **BWV**
  - Schubert → **D.**
  - Debussy → **L.**
  - Liszt → **S.**
  - Scarlatti → **K.** (or **Kk.**)
  - Ravel → **M.**
  - Mozart → **K.**
  - Satie → often untitled by number; use a plain sequence ("Gnossienne No. 47") and drop the catalogue token.
- **Title** — a short evocative name in quotes, when the composer's tradition used them (Debussy, Liszt, Scriabin titled freely; Bach and Scarlatti mostly didn't — for them, a bare catalogue line reads more authentic, and the program note carries the image instead).

## Choosing the forms

For each run, assemble a varied set:

1. **Core set (5–7)** — the composer's signature form, the one a listener pictures first. This is the spine of the catalogue.
2. **Phantom forms (2–3)** — other forms the same composer genuinely wrote, to vary texture and pace (e.g. for Chopin: a prélude, an étude, a ballade alongside the nocturnes).
3. **One phantom large-scale work (optional)** — a single movement of an invented multi-movement work. This is where "a symphony that never existed" can live. Give the composer forces they never used (a full orchestra for Chopin; a concerto for Satie) **only** as a deliberate alternate-timeline flourish, and label it as the hybrid it is. Otherwise keep to their real instrument.

## Keeping the fiction consistent

- **Program notes** — one line each, an image or a feeling, never a dry description. "It begins by pretending to be calm." Not "A piece in ternary form."
- **Internal coherence** — vary keys and moods across the set, but let them feel like one composer's hand. Don't put a ragtime stride into a Satie catalogue.
- **Optional thickeners** (offer, don't impose):
  - A **fictional performer-editor** — "your timeline's Barenboim / Gould / Argerich" — credited as the one who unearthed and recorded the catalogue.
  - A **phantom publishing house** or an editor's preface line.
  - A **themed sub-opus** — a whole run in one key, or all set at one hour of the night.
  - A **late-style drift** — harmony that grows stranger across the set, as if the composer aged decades past their real death.

## How many, and how long

Default **10 works**. Each prompt is one paragraph (~45–70 words). The whole artifact should be scannable: a listener can read a title, read one line, and decide whether to generate it.
