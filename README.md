# H3 Prompt Journal

A case-study journal of MiniMax H3 prompt engineering experiments. Each entry documents a real attempt, the failure modes encountered, the breakthrough insight, and the final prompt that worked.

## Why a journal

H3 prompt engineering is less about parameter tuning and more about **teaching the model a different way of thinking about transition**.

Most public H3 prompts fail because they describe what should appear in each shot. Successful prompts describe the **continuous physical logic** the camera must follow. This journal collects the prompts that figured out that logic.

## How each entry is laid out

Every case study in `case-studies/` follows the same structure:

```
case-studies/YYYY-MM-short-name/
├── README.md      <- Context, the problem, the breakthrough, the takeaway
└── prompt.md      <- The full final H3 prompt that worked
```

The `prompt.md` files are designed to be pasted directly into H3. The `README.md` is the design rationale.

## Index

| # | Title | Date | Status |
|---|---|---|---|
| [001](./case-studies/2026-08-three-person-orbital-long-take/) | Three-Person Occlusion-Linked Orbital Long Take | 2026-08 | published |
| [002](./case-studies/2026-08-dual-subject-speed-contrast/) | Asymmetric Speed-Ratio Duo Choreography | 2026-08 | published |
| [003](./case-studies/2026-08-single-subject-three-pose/) | Micro-Cam Anchor-Flow Flight | 2026-08 | published |
| [004](./case-studies/2026-08-furina-windsurfing-fashion-mv/) | Layered Reference Architecture with Text-Driven Climax | 2026-08 | published |
| [005](./case-studies/2026-08-water-obstacle-variety-show/) | Beat-Anchored Improvisation Variety Show | 2026-08 | published |
| [006](./case-studies/2026-08-sticker-character-kitchen-comedy/) | Mixed-Media Sticker-in-Reality Comedy | 2026-08 | published |
| [007](./case-studies/2026-08-cinematic-character-reveal-two-part/) | Two-Part Cinematic Character Reveal with Continuous BGM | 2026-08 | published |
| [008](./case-studies/2026-08-first-person-finger-controlled-dance/) | Single-Image First-Person Finger-Controlled Dance | 2026-08 | published |

## Companion

This journal sits next to two other repos in the same workflow:

- [`video-to-h3-prompt`](https://github.com/LoveRain1997/video-to-h3-prompt) — the reusable H3 reverse-engineering skill that produces these prompts
- [`h3-prompt-writing`](https://github.com/MiniMax-AI/MiniMax-H3/tree/main/skills/h3-prompt-writing) — the upstream H3 spec

## License

MIT — see [LICENSE](./LICENSE).
