# Case Study 008 — Single-Image First-Person Finger-Controlled Dance

> **用手指控制 AI 跳性感卡点舞｜H3 单图手势控舞教程**

## Inputs

- `<Picture 1>` — The ONLY visual reference. Locks dancer's appearance, face, hairstyle, costume, environment, lighting, and the original high-angle smartphone perspective
- Target: vertical 9:16 first-person smartphone recording, continuous single shot
- Prompt language: **English** (descriptive blocks + literal command clauses)
- Output: short-form viral dance video controlled by a foreground finger

## Media files

| File | Role |
|---|---|
| [`reference-dance-demo.mp4`](./reference-dance-demo.mp4) | Original AnimateDiff补帧 demo clip used as the visual reference source |

## What this prompt solves

A solo dancer + a controlling hand in the same frame, and the hand must visibly *cause* the dance.

Two problems collide here. **First**, the model's prior for "dance" is to freelance — once a dancer is on screen, the model improvises choreography it considers aesthetically pleasing, ignoring any external cue. **Second**, a hand in the foreground is almost always a problem: H3 will either grow it to dominate the frame, slide it across the center to cover the face, or shrink it to a barely visible background element. None of these work when the hand is supposed to be the puppeteer.

The third hidden problem: most prompt authors would write a list of dance moves (hip sway, arm wave, hair flip) and let the model sequence them. That fails because the model doesn't *see* a connection between the hand in the foreground and the dancer's body, so the two drift out of sync, or the hand disappears during the most important beat.

## The breakthrough

State the control relationship as a literal mapping, then forbid alternatives.

The prompt establishes an explicit, one-to-one control grammar at the top:

```
UP → WOMAN RISES.
DOWN → WOMAN LOWERS.
LEFT → WOMAN MOVES LEFT.
RIGHT → WOMAN MOVES RIGHT.
```

Each direction is then given a paragraph defining exactly how the body responds (torso extension for UP, hip drop for DOWN, full-body weight shift for LEFT/RIGHT) and — crucially — a negative clause: `LEFT and RIGHT must not become tiny hip twitches`. Without this, the model would interpret "left/right movement" as subtle hip sways. The prompt forces a *visible full-body shift*.

The same anti-drift logic applies to the hand itself:

- A connected forearm / wrist / palm / fingers chain (no floating phantom hand)
- Lower-right quadrant only, 10–18% of image area (not a giant, not a sliver)
- Hand never extends across the center, never covers the face or torso

The dance description is intentionally generic — `confident, sexy viral short-form influencer dance` — because the prompt's purpose is the *control contract*, not the choreography. The usage note at the top of the article tells the user: swap the dance style freely, swap the command sequence freely, but never break the finger-to-body mapping.

The technique stack:

| Technique | Role |
|---|---|
| **Literal Control Mapping** | UP/DOWN/LEFT/RIGHT as one-to-one body-direction commands |
| **Directional Anti-Twitch Clause** | Forbids subtle hip-sway interpretation of LEFT/RIGHT |
| **Foreground Element Quota** | 10–18% image area, lower-right quadrant only |
| **No-Drift Composition Locks** | Camera distance 1.0–1.2m, body 70–80% of frame, no zoom-out |
| **Sync-Within-Beat Rule** | No reaction delay, no one-beat lag, no anticipation |
| **Command Sequence Table** | Pre-defined 10-beat sequence (UP→DOWN→L→R→L→R→UP→DOWN→L→R) |
| **Modular Dance Section** | Dance style is a swappable description, not a hard-coded choreo |
| **Closing Triplet Pose** | L→R→UP with a held final pose as the resolution |

## The named language

> **Finger-Controlled First-Person Dance**

The name encodes the three things that make this prompt work: the hand is the *controller* (not a prop), the camera is *first-person* (not a third-party observer), and the dancer is *in the shot* (not a stock figure pasted in). Lose any of these and the prompt collapses into either an unconstrained dance video or a hand-in-foreground demo with no relationship between them.

## 48-hour takeaway

When a prompt has two visible actors, name their *relationship* explicitly.

Most prompt authors describe each actor's appearance and actions separately and hope the model connects them. It doesn't. A dancer description and a hand description, written in isolation, become two independent scenes that happen to share a frame. The connection only appears if the prompt *itself* contains the connection — and the simplest way to write a connection is a literal mapping: hand goes up, body goes up; hand goes left, body goes left.

Three reinforcing rules make this stick:

**1. Define each direction with a body response, not just a label.** "LEFT means the body moves left" is too abstract. Specify the body parts that move: weight, torso, hips — and how. The model will follow mechanics more reliably than abstract directions.

**2. Negate the cheap interpretation.** "LEFT/RIGHT must not become tiny hip twitches" prevents the model from satisfying the prompt with the easiest possible interpretation. Always include the wrong-but-allowed version in the negative list.

**3. Quota the foreground element.** A 10–18% area constraint for the hand prevents both the "giant hand" failure (model inflates the controller) and the "barely visible hand" failure (model shrinks it). Specifying the range is much more reliable than saying "natural size."

## The final prompt

See [`prompt.md`](./prompt.md) for the full usage notes + ready-to-paste prompt.

The prompt file is organized as:

1. **Usage notes** (Chinese) — single-Picture workflow, swappable dance style, unbreakable control rules
2. **integrated_multimodal_description** — Picture 1 reference scope, high-angle POV, hand placement quota, body distance lock
3. **Control grammar** — UP/DOWN/LEFT/RIGHT with body-response definitions
4. **Anti-twitch / anti-drift clauses** — for body and hand separately
5. **Dance style description** — generic viral-dance vocabulary, swappable
6. **Command sequence** — 10-beat hard-coded sequence
7. **Closing triplet** — L → R → UP final pose
8. **Soundscape + music** — indoor ambience + viral dance track

## Result

A continuous first-person smartphone recording, locked to the high-angle perspective of Picture 1:

- A hand in the lower-right foreground issuing clear UP/DOWN/LEFT/RIGHT gestures
- The dancer immediately following each gesture with full-body movement (rise, drop, side-shift, side-shift)
- No phantom hand, no floating fingers, no hand covering the face, no distant dancer
- Ten gesture-movement pairs on rhythm, ending in a held confident pose
- Music: viral dance track with punchy beats synchronized to the gesture timing

## Tags

`#H3` `#prompt-engineering` `#first-person-pov` `#finger-control` `#dance` `#short-form` `#single-image` `#control-mapping` `#anti-drift` `#viral-dance` `#chinese-tutorial`
