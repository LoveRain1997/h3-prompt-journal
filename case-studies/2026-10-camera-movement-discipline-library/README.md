# System B — Camera Movement Discipline Library (动态运镜纪律案例库)

- **Date:** 2026-10
- **Source:** 舞蹈动链H3.md E 章 (E1–E10 实测运镜纪律) + 用户 "动作负责舞蹈, 摄影机负责观看" 修订标准
- **Prompt:** see [prompt.md](./prompt.md) — E 章十条运镜纪律 + 十条物理运镜法则 + 词库 + 组合结构全文

## The problem

Two failure modes keep killing H3 dance films:

1. **Camera chases everything** — every chest pulse, every finger accent triggers a camera move. Ten seconds later the frame has jumped six times and the viewer is seasick. The original drafts stuffed `PUSH + DROP + RISE + TRACK + WRAP + ROLL PUNCH` into single segments; the camera had no primary axis, so the result looked like jumping.
2. **Camera language is abstract** — `dynamic tracking`, `camera orbits 40°`, `sweeping camera move`. H3 cannot execute abstractions any more than it can execute `low angle`.

## The breakthrough — 动作负责舞蹈，摄影机负责观看

The camera does NOT react to every small body accent. Each segment has **one primary camera behavior**; a secondary adjustment only when a major level or spatial relationship genuinely changes.

**CAMERA PRIORITY:**
1. establish physical camera position;
2. let the choreography happen inside that frame;
3. move only when the dancer changes level, travels, turns through space, or reveals a new body relationship;
4. settle again.

The real-filming laws this encodes (from E 章): kicks let the camera **plant** and let the choreography hit the lens; formation shifts get a parallel **truck**; floor work mirrors the dancer's level (**人蹲机蹲，人起机起**); the camera starts its move on the **release beat, not the accent peak**.

## The ten physical movement laws

```
POSITION LAW      — placement in real distance/height/side/direction, never abstract terms
NO DEGREE LAW     — no degree measurements; define start and end positions physically
OPTICAL-AXIS LAW  — state what body part the lens aims at during each major move
DISTANCE LAW      — distance changes only through real forward/backward travel
HEIGHT LAW        — height changes only through real rise or descent
SIDE-CHANGE LAW   — crossing sides means physically walking a readable path around her
SUBJECT-TRIGGER   — the camera moves only because a written performer action causes it
DANCE LAW         — continuous connected choreography, never slow walking
POSITION CHANGE   — the dancer relocates with 1-2 purposeful steps; the camera does the reframing
HERO LOCK         — when the camera stops it stays physically stable through the final accent
```

## The thirteen-word lexicon — each one a physical path

| Word | Physical definition |
|---|---|
| PUSH-IN | operator walks toward her along the existing axis |
| PULL-BACK | operator retreats preserving framing |
| TRACK | sideways travel beside her at her speed |
| PASS | travels beyond her previous position into a new side relationship |
| WRAP | walks around one side while keeping her framed |
| RISE | real upward move with her |
| DROP | real descent toward the lower body with her |
| FLOOR SLIDE | lateral travel, lens 5–15cm above the floor |
| OCCLUSION | a real object/body part temporarily blocks the lens |
| REVEAL | operator keeps moving until she is visible again |
| WHIP PAN | one fast physical pan triggered by her action, then stabilization |
| RECOIL | operator backs away a short distance from a strong accent |
| HERO LOCK | operator stops and holds the position physically |
| TIME-CODE SYNC | dance and camera share one absolute timeline — start/peak/recover together, 1:1 |

Every word is a **path with a start position, a trigger, and an end position** — never a vibe.

## The anti-catalog (what killed the old drafts)

```
No camera jumping between positions
No camera movement for every beat
No repeated push-pull / repeated wrap / repeated roll
No orbit unless specifically written
No whip pan unless specifically written
No camera bob synchronized to individual footfalls
No automatic reframing after every body accent
No digital zoom / digital rotation / artificial parallax
```

> The performer generates the movement. The camera observes the movement. The camera moves only for a major spatial reason — and when it moves, it moves **on the same absolute time-code as the choreography**: start with the action, peak with the accent, recover with the release. One timeline, two synchronized motion tracks, one shared set of action peaks.

## The five-part movement block

Every camera block in a modern H3 prompt:

```
CAMERA POSITION:     where the camera is now (real meters)
CAMERA GEOMETRY:     height + distance + side + optical axis + perspective
CAMERA MOVEMENT:     how it travels from here to there (physical path)
MOVEMENT TRIGGER:    which written performer action releases the move
END CAMERA POSITION: where it actually ends up + final framing
```

Zero-movement segments must still write `MOVEMENT: none` and `TRIGGER: none permitted` explicitly — a silent block invites the model to improvise drift.

## Takeaway

真实录舞里，摄影师**先站稳，让舞者在画面里完成动作；只有舞者真的改变空间关系时，才移动一次**。One primary behavior per segment, physical paths with triggers and end positions, and the discipline to leave the camera alone. Pairs with *System A: Physical Camera Position Library* — position answers "where", movement answers "how it travels and why now".
