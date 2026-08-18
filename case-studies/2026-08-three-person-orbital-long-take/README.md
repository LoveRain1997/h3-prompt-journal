# Case Study 001 — Three-Person Occlusion-Linked Orbital Long Take

## Inputs

- `<Picture 1>` — Person 1 + master environment + master spatial coordinate system
- `<Picture 2>` — Person 2 appearance only
- `<Picture 3>` — Person 3 appearance only
- Target duration: **20 seconds**, single continuous shot

## The problem

H3 kept reading the brief as "the camera flies toward the second person."

Three characters, three full references, one shared room — and the model kept producing literal point-to-point flights. As soon as the brief said "go to Person 2," H3 cut or teleported or crossfaded. The semantic of *transition* was already poisoned by training data.

## The breakthrough

The real transition is not **flight**. It is **linkage**.

Each character owns a complete close-range orbit — feet to head, traveling horizontally through front-side, three-quarter, side, and rear-side. The camera never stops, never cuts. The current subject's body moves extremely close to the lens, forming a **foreground occlusion**. The camera rounds the shoulder, the hair, the back — and the next character suddenly emerges from behind the obstruction as a fresh orbital center.

The technique stack:

| Technique | Role |
|---|---|
| **Foreground Occlusion Transition** | The transition mechanism itself |
| **Motivated Camera Movement** | The camera's path is always physically explainable |
| **Continuous Long Take** | Single 20 s take, no internal cuts |
| **Close-Range Orbital Camera** | Each subject gets a full 360° orbit |

## The named language

> **Occlusion-Linked Orbital Long Take**

Naming the pattern mattered. Once the prompt contained the named language, H3 stopped trying to interpret "go to" and started treating each segment as a separate orbital problem to solve independently.

## 48-hour takeaway

H3 prompt engineering is less about piling constraints and more about **teaching the model a different way of thinking about transition**.

Constraints like "no cut" and "no morph" are necessary but not sufficient. The model needs a generative grammar — a named pattern it can reproduce.

## The final prompt

See [`prompt.md`](./prompt.md) for the full 1413-line prompt that solved this case.

The prompt is organized in this order:

1. **Reference priority** — which picture controls what
2. **Master environment lock** — Picture 1 owns the whole space
3. **Three people, one space** — spatial integration rules
4. **Visibility rule** — only one person visible at a time until the final reveal
5. **Spatial arrangement** — physical distance, occlusion geometry
6. **Identity lock** — exact face / clothing / hairstyle preservation
7. **Per-character orbit specification** — motion logic for each subject
8. **Camera behavior** — close-range orbital, motivated motion
9. **Optical behavior** — realistic perspective, parallax, no fisheye
10. **Absolute negative constraints** — every failure mode enumerated as a prohibition
11. **Final creative intent** — one-sentence physics description of the whole shot

## Result

20-second continuous single-take H3 output:

- Person 1 full orbit (≈6 s) → occlusion reveal
- Person 2 full orbit (≈6 s) → occlusion reveal
- Person 3 full orbit (≈6 s) → short pull-back
- Final close half-body three-person portrait (≈2 s)

All three people visible together for the first and only time in the final frame, proving their physical co-presence throughout.

## Tags

`#H3` `#prompt-engineering` `#camera-language` `#long-take` `#foreground-occlusion` `#orbital` `#three-person` `#occlusion-linked`
