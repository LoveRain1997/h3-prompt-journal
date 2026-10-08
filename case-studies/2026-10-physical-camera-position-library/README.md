# System A — Physical Camera Position Library (机位视角案例库 · 25 类)

![system-a](./cover-placeholder.png)

- **Date:** 2026-10
- **Source:** 舞蹈动链H3.md I 章 (用户写法标准全文, Rev.1.0 并入)
- **Prompt:** see [prompt.md](./prompt.md) — 25 类视角物理定义块全文, 可直接复制进任何 H3 提示词

## The problem

H3 treats camera language as **vibes, not geometry**. Write `low angle` and the model averages it into "slightly lower". Write `extreme low angle` and you get a waist-height shot with a bit of tilt. Every named-angle vocabulary word (`low angle / high angle / eye-level / dutch / top-down`) is a label for an effect — and H3 does not execute labels.

## The breakthrough — name the effect vs. define the conditions

> **Don't name the effect. Define the physical conditions that produce it.**

Every one of the 25 position blocks answers the same seven questions in physical terms:

1. **REAL CAMERA OBJECT** — a real physically plausible camera
2. **WHERE IT IS** — floor / waist / knee / above head / directly overhead / behind / beside
3. **HOW HIGH** — `5-15cm above the ground` / `at knee height` / `above her head and shoulders`
4. **RELATIONSHIP TO SUBJECT** — beneath her / beside her / directly behind / diagonal front
5. **LENS POINTS WHERE** — sharply upward / horizontally / steeply downward / perpendicular to the floor
6. **WHAT THIS POSITION PHYSICALLY SEES** — the floor close to the lens, her body rising above the viewpoint, the top surfaces of the shoulders visible, the horizon tilted with the camera roll
7. **ANTI-SIMPLIFICATION** — `NOT an eye-level camera tilted upward / NOT a crop / NOT a digital zoom / NOT a rotation of the finished image`

Once the camera is a **thing in the scene with a position**, it cannot be averaged away.

## Library map (25 classes)

| Class | Position | Signature geometry |
|---|---|---|
| A1 | Eye-level | optical axis horizontal, natural human proportion |
| A2 | Slight low | below chest, lens angled moderately up |
| A3 | Waist-level | floor visible as lower plane, height increase |
| A4 | Knee-level | legs rise from foreground, vertical exaggeration |
| A5 | Floor-level extreme low | lens 5–15cm up, strong foreshortening — the signature shot |
| A6 | Worm's-eye | subject towers, ceiling enters background |
| A7 | High-angle | diagonal down, top surfaces visible, not top-down |
| A8 | Extreme high | steep down-diagonal, height compressed |
| A9 | True top-down | vertical optical axis, perpendicular to floor |
| A10 | Diagonal overhead | above + slightly front, face retained |
| A11 | True side | lateral co-plane with subject |
| A12 | Front three-quarter | 30–45° off frontal axis |
| A13 | Direct rear | same central axis, from behind |
| A14 | Rear three-quarter | back plane + one side |
| A15 | Extreme close | real short distance, real perspective change on micro-movement |
| A16 | Ground-level side | centimeters up, lateral view, legs dominate near field |
| A17 | Close rear tracking | follows her through the environment, no orbit |
| A18 | Human handheld | chest-to-eye height, subtle operator fluctuations |
| A19 | Dutch angle | roll around the optical axis — the whole frame tilts together |
| A20 | Upward tilt | position fixed, lens physically tilted up |
| A21 | Downward tilt | position fixed, lens physically tilted down |
| A22 | Perspective response | her movement changes real distance → real size change |
| A23 | Authenticity lock | universal anti-simplification block |
| A24 | 8-element shot structure | placement → height → distance → axis → relation → result → response → lock |
| A25 | The principle | name the effect vs. define the conditions |

## Takeaway

Write the camera as **a real object occupying real space**, state what that position physically sees, then forbid the lazy approximations by name. Pairs with the movement library (*System B: Camera Movement Discipline*) — position answers "where is the camera", movement answers "how does it travel".
