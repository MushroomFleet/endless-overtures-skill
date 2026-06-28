# Lyria 3.1 Prompt Craft

How to turn one invented work into a prompt that actually generates well on Gemini Lyria 3.1.

## How Lyria 3.1 reads a prompt

- **It reads description, not notation.** Lyria does not parse a catalogue number, an opus number, or a literal key signature. So the title is flavor; the prompt is the instruction. Everything you want to hear must be *described*, not *named*.
- **The named key is a promise the prompt must keep.** Because Lyria won't honor "in D-flat major" literally, you translate the key into its mood and write *that* into the prompt (see the cheat-sheet below). This is what keeps the fiction and the sound in agreement.
- **Keep it instrumental.** Lyria can drift toward adding voices. End every prompt by ruling out vocals so it stays on the intended instrument.

## The levers that move Lyria

Pull all of these in each prompt and the output stops sounding generic:

1. **Instrumentation** — "solo piano", "solo harpsichord", "solo piano and orchestra", "string quartet".
2. **Era / style anchor** — "early-Romantic salon tradition", "French impressionist", "high-Baroque keyboard", "late-Romantic Russian".
3. **Tempo + rubato** — "slow and unhurried, flexible rubato"; "brisk and even, strict tempo"; "andante, gentle give-and-take".
4. **Melodic character** — "a warm singing high melody"; "a grieving vocal line in the middle register"; "a clipped, dancing motif".
5. **Accompaniment texture** — "a gently rocking widely-spaced left hand"; "softly pulsing repeated chords"; "a flowing harp-like figuration"; "an even walking bass".
6. **Emotional image** — one concrete picture: "the colour of a candle burning low", "snow falling without wind", "an empty ballroom at dawn".
7. **Dynamic arc** — say where it stays quiet and where it lifts: "mostly pianissimo with a single aching climax that withdraws".
8. **Ornamentation** — "delicate filigree runs", "trills and turns", "no ornament, plain and bare".
9. **Recording character** (optional, adds realism) — "intimate close-miked felt piano with a little room", "resonant concert grand", "dry harpsichord, very present".

## The prompt skeleton

Fill every slot. Aim for roughly 45–70 words.

```
Solo [instrument] [form] in the [era/style] tradition. [tempo + amount of rubato]. [melodic character] over [accompaniment texture]. [one emotional image]. [dynamic arc — where it stays soft, where it lifts]. [ornamentation]. [recording character]. Instrumental only, no vocals.
```

## Two rules of thumb

1. **Name the texture, not just the feeling.** "A singing high melody over a rocking widely-spaced left hand" beats "beautiful and sad." Lyria can act on the first; the second it has to guess.
2. **Give it an arc, not a state.** Tell it where to stay quiet and where to lift, or it tends to drift along evenly with no shape.

## Key → mood cheat-sheet

The named key in the title must agree with the mood in the prompt. Use this mapping (it follows the broad Romantic-era associations; adjust to taste):

| Key | Mood to write into the prompt |
|---|---|
| D-flat / G-flat major | velvety, intimate, warm, close |
| A-flat major | noble, tender, nostalgic |
| F / B-flat major | sunlit, songful, open |
| C / G major | plain, candid, untroubled |
| E / A major | serene, radiant, calm |
| F-sharp major | luminous, ecstatic, shimmering |
| B major | glowing, transcendent, weightless |
| D / G minor | grave, plaintive, archaic |
| C / F minor | tragic, dark, passionate |
| E / A minor | melancholy, faded, wistful |
| C-sharp / G-sharp minor | restless, grieving, nocturnal |
| B-flat / E-flat minor | turbulent, shadowy, stormy |

## One worked example

Title: **Nocturne No. 2,604 in B-Flat Minor, Op. 911 No. 1 — "The Storm Returns"**
B-flat minor → "turbulent, shadowy, stormy", so the prompt delivers exactly that:

```
Solo piano nocturne, dark and restless. Opens brooding and quiet with a mournful cantabile theme over a low murmuring accompaniment, then builds into an agitated, stormy middle section with surging arpeggios and dramatic dynamic swells, before sinking back into shadow. Turbulent, passionate, deeply Romantic. Heavy rubato throughout. Resonant grand piano, intimate but powerful. Instrumental only, no vocals.
```
