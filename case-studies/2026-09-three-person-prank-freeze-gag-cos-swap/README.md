# Case Study 009 — Reverse-Engineered Three-Person Prank with Freeze-Frame Gags + Skin-Only Cos Swap

## Inputs

- **No reference image** — pure **T2VA** rebuild
- Source: a 15-second real UGC vertical prank clip (9:16), reverse-engineered frame-by-frame
- Target: **~15 seconds**, vertical **9:16 / 24fps**, photorealistic live-action (real human cosplayers, NOT anime)
- Two characters reskinned to *Detective Conan* cosplay: Girl A = Hagiwara Chihaya (traffic-police cos), Girl B = Elena Miyano (scientist cos)
- Prompt language: **English** structured sections with two short spoken **Japanese** exclamations
- Result render: [`result-video.mp4`](./result-video.mp4) (0.8-resolution, with audio)

## The problem

This is the journal's first **reverse-engineering** entry — the prompt was not designed from scratch, it had to be recovered from an existing clip. Three failure modes appeared on the first naive pass:

1. **The invisible third actor.** The camera-holder is also the prankster, but only a green sleeve, a green scooter fairing and an occasional hand ever enter frame. A sparse frame walk reads those as clutter and treats the camera as a neutral observer — which inverts the whole plot.
2. **The one-to-many inverse problem.** Different scripts produce near-identical frames. At low sampling rate, "she sprays herself" and "an off-camera hand turns her head so she sprays her friend" look the same; the 3–5-frame helmet-grab that decides between them disappears entirely.
3. **Freeze frames mistaken for acting.** The three half-second shock holds are *post-production*, not people freezing on set. Writing them as action freezes the characters instead of the edit.

## The breakthrough

**Five-channel forensics + a frozen causal skeleton.**

Dense 4–8fps extraction over each ambiguous window adjudicated between competing plot hypotheses instead of confirming the most common one; a 0.5s RMS envelope located three energy peaks, and every peak was reconciled with a picture cause; a BPM false-detection guard (onset regularity + spectrogram kick grid) correctly ruled that the track has **no music — pure field audio**. What emerged is a strict THREE-BEAT loop:

```
rider provokes → girl charges a mouthful → rider physically sabotages →
backfire lands → FREEZE-FRAME shock gag   (×3, escalating)
```

The edit layer was then separated cleanly: one unbroken handheld take with exactly three ~0.5s freeze holds, each marked by a micro punch-in + one-frame white flash + a record-scratch→impact→vacuum post-SFX.

The **cos swap** was done last, under a "skin-only" contract: timestamps, actions, camera, freeze points and sound structure are frozen; only appearance, costume, and the wet-hair/fabric physics they touch are rewritten. A compatibility check handled the one real dependency — the flip-up visor the gags rely on — and character-specific props (lab gear, drawn duty equipment) were explicitly barred from frame so the setting never changes.

| Technique | Role |
|---|---|
| **Dense discriminative sampling** | 4–8fps on ambiguous windows to choose between candidate plots |
| **Audio-visual reconciliation** | each RMS peak must have a visible cause; BPM false-positive guard |
| **Off-camera actor tracking** | sleeve / hand / fairing merged into one real agent (Subject 3) |
| **Layer separation** | live action / camera / edit-effects / sound written into different fields |
| **N-Beat escalation** | the same sabotage loop repeated three times, escalating, in `editing` |
| **Freeze-frame four-tuple** | in-point, duration, overlay, snap-back — never "the actor stops" |
| **Skin-only reskin** | freeze the causal skeleton; rewrite appearance + touched physics only |

## The named language

> **Freeze-Gag Causal Loop with Skin-Only Reskin**

The deliverable is not a description of frames but an executable cause→effect chain a different cast can wear. Once the loop (provoke → charge → sabotage → backfire → freeze) is locked, swapping two original girls for two cosplayers touches `subject_definitions`, `costume_hair_physics`, and the handful of costume words an action physically reaches — and nothing else.

## 48-hour takeaway

When reversing footage, **sampling density is a discriminator, not a quality dial**: sparse frames are for building candidate hypotheses, dense frames are for killing the wrong ones. And treat the camera as a *potential actor* until proven otherwise — a purposeful moving object in frame (a hand, a sleeve, a fairing) always has a controller.

When reskinning, freeze the mechanism and rewrite the surface; the moment a costume change starts moving timestamps or beats, it has stopped being a reskin. A replacement table (appearance before/after, plus every carried-over change) is what keeps that boundary honest.

This entry is the worked example produced by the companion skill [`video-to-h3-prompt`](https://github.com/LoveRain1997/video-to-h3-prompt) — its five-channel pipeline, freeze-frame recipe and skin-only replacement SOP are documented there.

## The final prompt

See [`prompt.md`](./prompt.md) for the full paste-ready prompt: short Chinese usage notes followed by the complete English 14-field prompt.

Field order:

1. **subject_definitions** — three subjects; Subject 3 is the never-fully-shown rider/saboteur
2. **environment_definition** / **lighting_definition** — night residential alley, cool frontal phone fill
3. **integrated_multimodal_description** — `[Shot 1]` + strictly increasing timestamps, three-beat loop with embedded diegetic sound
4. **camera_direction** — handheld first-person POV, sabotage-motivated jolts, freeze punch-ins
5. **editing** — one take + exactly three white-flash freeze gags
6. **performance** / **body_mechanics** / **costume_hair_physics**
7. **negative_constraints** / **overall_soundscape** / **non_diegetic_music** (explicit silence)

## Result

A ~15-second single-take-feel vertical prank clip:

- Rider pours water on A's boot; A charges a mouthful, has her visor slapped down, is interrupted and sprays her own visor — **freeze 1**
- A recharges, has her helmet twisted toward B and accidentally sprays B's face/glasses — **freeze 2**
- B chugs to retaliate, is blocked mid-attack and chokes — **freeze 3**
- Both dissolve into laughter and link arms to camera; no music, only field audio and the three comedic SFX hits

## Assets

| File | Role |
|---|---|
| [`prompt.md`](./prompt.md) | Full final T2VA prompt (paste-ready) |
| [`result-video.mp4`](./result-video.mp4) | Generated result video, 9:16, ~15s, with audio |

## Tags

`#H3` `#prompt-engineering` `#reverse-engineering` `#video-to-prompt` `#first-person` `#off-camera-actor` `#three-beat` `#freeze-frame` `#comedy-timing` `#cos-reskin` `#field-audio` `#vertical-video` `#T2VA`
