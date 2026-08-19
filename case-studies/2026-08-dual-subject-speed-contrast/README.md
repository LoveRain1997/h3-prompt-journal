# Case Study 002 — Asymmetric Speed-Ratio Duo Choreography

## Inputs

- `<Picture 1>` — Two characters together: Kokomi (left) and Qiqi (right)
- Single reference image, both identities locked from it
- Target: butterfly-step dance to instrumental BGM (Paradise-style)
- Prompt language: **Chinese**

## The problem

H3 synchronizes dancers to the beat.

Give the model two people and music, and it defaults to mirror-sync: both bodies lock to the same tempo, the same downbeat, the same phrasing. The brief wanted the opposite — Kokomi fast and continuous, Qiqi slow and delayed, a "master leads, student follows with a lag" dynamic. But "fast" and "slow" are adjectives. The model rounded them to "same speed, slightly different."

## The breakthrough

Speed difference is not a feeling. It is a **ratio**.

Instead of describing tempo qualitatively, the prompt gives the model an explicit arithmetic anchor:

> When Kokomi has completed **3 actions**, Qiqi has completed **1**.

This converts an aesthetic tempo gap into a checkable count. The model cannot round "3:1" to "roughly equal." It has to hold the asymmetry or visibly fail the rule.

The second lever is **behavioral motivation**. Qiqi isn't just "slow" — she watches Kokomi, then imitates the action she just saw. This gives the lag a narrative cause rather than an arbitrary speed cap, which makes the desynchronization feel intentional instead of broken.

The technique stack:

| Technique | Role |
|---|---|
| **Count-Ratio Anchor** | 3:1 action count — the concrete rule the model must hold |
| **Watch-Then-Imitate Logic** | Gives the slow subject a reason for the lag |
| **Asymmetric Speed Choreography** | The overall temporal desynchronization pattern |
| **Close-Range Continuous Orbit** | Camera stays tight on both faces throughout |

## The named language

> **Asymmetric Speed-Ratio Duo Choreography**

Naming the pattern as a *ratio* rather than a *feeling* is the key. "One fast, one slow" is subjective. "3:1 count-locked" is a specification.

## 48-hour takeaway

Adjectives don't survive generation. "Fast" becomes "normal." "Slow" becomes "normal." The model's default is convergence toward the beat.

To hold a visible difference, convert the aesthetic intent into a **number the model can track**. A 3:1 action-count ratio is harder to ignore than "one person is faster." And to make the asymmetry feel deliberate rather than defective, give the slower subject a **reason** — she's watching, then copying. Lag with motivation reads as choreography. Lag without motivation reads as a bug.

## The final prompt

See [`prompt.md`](./prompt.md) for the full prompt (Chinese, ~170 lines).

The prompt is organized in this order:

1. **Reference lock** — Picture 1 is the sole reference, both identities frozen
2. **Dance type** — butterfly steps, light footwork, side-to-side
3. **Asymmetric speed rule** — Kokomi fast/continuous, Qiqi slow/one-at-a-time
4. **Count-ratio anchor** — the explicit 3:1 action-count specification
5. **Behavioral logic** — Qiqi watches, then imitates with a delay
6. **Negative constraints** — no sync, no catching up, no sudden acceleration
7. **Camera** — close continuous orbit, waist-to-head framing
8. **Audio** — instrumental BGM only, no vocals

## Result

A duo dance where Kokomi completes roughly 3 butterfly-step actions for every 1 that Qiqi completes, sustained from first second to last, with Qiqi visibly watching and lagging behind throughout.

## Tags

`#H3` `#prompt-engineering` `#choreography` `#asymmetric-speed` `#count-ratio` `#duo-dance` `#desynchronization` `#butterfly-step`
