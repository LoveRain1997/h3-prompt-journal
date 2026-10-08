# Advanced Camera Movement Combinations (物理运镜组合库 · 10 组合 · NO DEGREE VERSION)

- **Date:** 2026-10
- **Source:** 用户提供的 H3 ADVANCED CAMERA MOVEMENT COMBINATIONS (PHYSICAL CAMERA GEOMETRY VERSION)
- **Prompt:** see [prompt.md](./prompt.md) — 14 条 SEGMENT RULES + 13 词词库 + 10 组组合全文, 可直接复制进任何 H3 舞蹈 MV 提示词

## The problem

The most common camera language in H3 prompts — `ARC 40°`, `45° ORBIT`, `camera rotates 60°`, `low angle → high angle` — is a **term plus a number**. H3 cannot execute that unit. It produces either nothing, or a wild swinging orbit that nobody asked for.

## The breakthrough — replace the unit of description

> CAMERA TERM → DEGREES  ❌
> START POSITION → PHYSICAL PATH → SUBJECT TRIGGER → END POSITION → FINAL FRAMING  ✅

Wrong:

> `The camera arcs 45 degrees to her right.`

Right:

> `The camera starts directly in front of her, then the operator physically walks toward her right shoulder while keeping the lens aimed at her face; the camera finishes beside the right shoulder, slightly forward of the arm line.`

Every description now contains **where the operator starts, which side of her body they walk along, what the lens keeps aimed at, and where they finish**. H3 executes people walking in rooms; it does not execute protractor readings.

## The 14 segment rules (the constitution)

The rule set encodes the whole physics: real handheld operation in 3D space (PHYSICAL CAMERA LAW), real distance/height/side placement (POSITION LAW), zero degrees (NO DEGREE LANGUAGE), stated optical-axis targets (OPTICAL-AXIS LAW), distance and height only through real travel (DISTANCE/HEIGHT LAW), readable walking paths when crossing sides (SIDE-CHANGE LAW), and the master rule — **SUBJECT-TRIGGER LAW: the camera changes movement only because a written performer action causes the change**.

Plus the choreography contract: connected dance actions never replaced by walking; the dancer relocates with one or two purposeful steps while the camera does the spatial reframing; HERO LOCK when stopped; TRANSITION HOOK at the end.

## The thirteen-word lexicon

PUSH-IN · PULL-BACK · TRACK · PASS · WRAP · RISE · DROP · FLOOR SLIDE · OCCLUSION · REVEAL · WHIP PAN · RECOIL · HERO LOCK

Each word is defined as a **physical path performed by the operator**, not an effect. WRAP is not "orbit" — it is "walk around one side of the performer while continually redirecting the lens". OCCLUSION is not "a transition" — it is "her arm/sleeve/hair passes close to the lens and temporarily blocks the image while the operator keeps moving".

## The ten combinations

| # | Path | Signature move |
|---|---|---|
| 01 | Front follow → side travel → shoulder pass → front reacquire | the all-purpose single-take dance cover |
| 02 | Side follow → overtake → physical turn → reverse follow | walk-forward sections; camera ends ahead of her |
| 03 | Push-in → right-side reposition → three-quarter reframe | chest phrase into a finished 3/4 pose |
| 04 | Upper-body follow → drop → footwork insert → rise → face | the mirror law: 人蹲机蹲, 人起机起 |
| 05 | Low follow → rise with body → chest → face | grounded phrase rising through the frame |
| 06 | Push-in → arm occlusion → hidden side shift → reveal | her arm is the transition tool |
| 07 | Front follow → operator stop → she crosses → physical turn → follow behind | direction changes; camera stays put then re-acquires |
| 08 | Floor slide → body reveal → rise → upper-body follow | footwork from the floorboards up |
| 09 | Close front → pass one shoulder → body blocks lens → opposite-side reveal | intimate three-quarter finish |
| 10 | Hero lock → micro push → performance trigger → side response | the camera answers, never initiates |

## Takeaway

组合 10 是整库的伦理缩影：**相机先站定（HERO LOCK），只做一次微推进，然后完全由人物的强动作触发侧移响应**。所有十个组合共享同一条纪律——摄影师拿着真实摄影机在场景里怎么走、怎么摆、何时因为舞者的什么动作而改变路径；人物与镜头的关系永远写成空间与路径，从不写成术语与角度。Pairs with *System A: Physical Camera Position* (where the camera is) and *System B: Camera Movement Discipline* (how much it may move).
