# Case Study 003 — Micro-Cam Anchor-Flow Flight

## Inputs

- `<Picture 1>` — The same person, pose 1 (first anchor)
- `<Picture 2>` — The same person, pose 2 (second anchor)
- `<Picture 3>` — The same person, pose 3 (final anchor)
- Target duration: **15 seconds**, single continuous shot
- All three images show the **same person** — poses are waypoints, not separate identities

## The problem

H3 treats reference images as destinations.

Give it three poses of one person, and it produces a slideshow: hold Pose 1 → crossfade → hold Pose 2 → crossfade → hold Pose 3. Or worse, a slow elegant orbit around a frozen body, treating the poses as static portraits to admire. The energy dies. The reference images become endpoints to *reach and hold*, not anchors to *flow through*.

## The breakthrough

Invert the agency.

The **person moves normally** and does not avoid the camera. The **camera is the agile one** — an extremely small invisible flying point that predicts body movement and dodges at high speed. The person is gigantic relative to the camera. The camera sweeps past feet, legs, torso, shoulders, hair — constantly redirecting around the moving body without ever slowing down.

The three reference poses are not destinations. They are **anchors** — waypoints in a continuous high-density flight. Between each anchor, the person performs multiple intermediate movements (weight transfer, torso rotation, limb reposition, head turn) that naturally lead toward the next pose. The camera never stops. The person never freezes.

The technique stack:

| Technique | Role |
|---|---|
| **Anchor-Flow Pose Structure** | Three poses as waypoints, not endpoints |
| **High-Speed Body Avoidance** | Camera dodges moving body parts at speed |
| **Tiny Invisible Camera** | Scale inversion — person gigantic, camera tiny |
| **Dual Action Density** | Both camera AND person must move frequently |
| **Motivated Camera Movement** | Every dodge is physically explainable |

## The named language

> **Micro-Cam Anchor-Flow Flight**

Two ideas in one name. "Anchor-Flow" tells the model: poses are passed through, not landed on. "Micro-Cam" tells the model: the camera is a tiny agile flyer, not a cinematic crane. Together they break the two default failure modes — static slideshow and slow orbit — in a single concept.

## 48-hour takeaway

Reference images aren't destinations — they're waypoints.

The model freezes when it thinks "reach pose and hold." It needs a **continuous flight grammar** where poses are milestones along a moving path, not stopping points. And the energy comes from **inverted agency**: instead of a static camera watching a posing model, make the camera the active agent that dodges and redirects around a naturally moving person.

The 15-second timeline structure also matters. Breaking the shot into seven micro-segments (0–2.5s, 2.5–5s, 5–7.5s, 7.5–9.5s, 9.5–11.8s, 11.8–13.5s, 13.5–15s) with a specific camera trajectory for each gives the model a beat sheet it can follow, rather than a vague "make it dynamic."

## The final prompt

See [`prompt.md`](./prompt.md) for the full ~880-line prompt.

The prompt is organized in this order:

1. **Reference priority** — three pictures, same person, poses as anchors
2. **Visual appearance lock** — reference images control appearance only
3. **Identity lock** — exact face/hair/clothing preservation throughout
4. **Core concept** — tiny invisible flying camera, person gigantic
5. **Critical speed requirement** — camera must move fast, no slow floating
6. **Critical action density** — person must also move frequently, no frozen poses
7. **Who moves and who avoids** — person moves normally, camera dodges
8. **High-speed camera avoidance** — specific dodge patterns per body part
9. **15-second structure** — seven micro-segments with camera trajectories
10. **Physical camera logic** — real 3D point, momentum, no teleportation
11. **Optical behavior** — realistic perspective, motion blur, no fisheye
12. **Absolute negative constraints** — every failure mode enumerated
13. **Final creative intent** — one-paragraph physics description of the whole shot

## Result

15-second continuous single-take H3 output:

- 0–2.5s: Picture 1 anchor + rapid lower-body flight
- 2.5–5s: fast transition → Picture 2 anchor
- 5–7.5s: rapid ascending orbit around Picture 2
- 7.5–9.5s: fast transition → Picture 3 anchor
- 9.5–11.8s: high-speed upper-body / head orbit
- 11.8–13.5s: rapid face approach + direction change
- 13.5–15s: extreme fast pull-back → Picture 3 half-body hero frame → hold

The camera never stops. The person never freezes. Three reference poses flow into each other through a continuous high-speed flight.

## Tags

`#H3` `#prompt-engineering` `#camera-language` `#micro-cam` `#anchor-flow` `#body-avoidance` `#three-pose` `#high-speed-flight` `#single-subject`
