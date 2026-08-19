# Case Study 004 — Layered Reference Architecture with Text-Driven Climax

## Inputs

- `<Picture 1>` — Character key visual / first frame (identity, face, hair, costume)
- `<Picture 2>` — Character turnaround + windsurfing equipment reference (board, sail, mast, boom)
- `<Picture 3>` — Segment-specific cinematography guide (used in segments 1 & 2 only)
- Target: **3 × 15-second segments** → 45-second vertical 9:16 fashion-sports music video
- Post-production: full video audio → Suno remix → final music-video sync
- Prompt language: **Chinese** (design doc) + **English** (H3 prompts)

## The problem

H3 treats all reference images as equal-weight visual targets.

Give it three pictures and it tries to reproduce all three simultaneously — the character, the equipment sheet, and the camera angle all become "things to match." The result is a compromised compromise: the character looks like a turnaround model, the camera framing fights the text instructions, and the equipment renders as a flat illustration rather than a 3D prop in motion.

Worse, when the project needs a **cinematic climax** — a windsurfing aerial jump at the musical peak — a cinematography reference image becomes a cage. The model tries to match the guide image's composition instead of executing the dynamic hero-shot timing the text describes.

## The breakthrough

Give each picture a **job title**, and when the job is done, **fire the picture**.

### Layer 1 — Role-segregated reference architecture

Instead of three equal-weight references, each picture gets a specific role:

| Picture | Role | Controls | Does NOT control |
|---|---|---|---|
| **Picture 1** | First Frame Visual Anchor | Identity, face, hair, costume, color, opening frame state | Camera, composition, equipment structure |
| **Picture 2** | Character + Equipment Reference | Body construction, costume structure, footwear, board, sail, mast, boom, rigging | Storyboard, camera, motion |
| **Picture 3** | Cinematography Reference | Camera position, framing, lens language, movement direction, subject scale, composition | Character appearance, equipment |

The prompt explicitly tells H3: *"Picture 2 is not a storyboard. Do not reproduce the turnaround-sheet layout."* This prevents the model from flattening a 3D scene into a 2D character sheet.

### Layer 2 — Text-driven climax (drop Picture 3 for the final segment)

The third segment — the hero moment where the windsurfer launches off a giant wave — uses **only Picture 1 + Picture 2**. No Picture 3.

This is not because of cross-segment visual memory (each 15s clip is independently generated). It's because a cinematography guide image would **over-constrain the camera** during the most complex action sequence:

```
giant wave → ride up wave face → takeoff → airborne → hero shot → landing → fashion ending
```

When the text needs to precisely time camera stops, music peaks, and spray explosions to specific seconds, a guide image fights the text. Removing it lets the text be the sole director.

### Layer 3 — Music-driven timeline structure

The 15-second timeline is not divided evenly. It's divided by **musical function**:

```
0–3s    Build-up
3s      Main Drop
3–10s   High-energy
6–7s    Mini-turnaround
9–10s   Absolute visual peak
10–12s  Release
12–15s  Next phrase
```

The rule: **music's accent decides the action; music's release decides the camera ease.** The 9–10s hero shot must align with the strongest musical accent — camera stops aggressive movement, stabilizes into a low-angle telephoto hero frame, and holds.

### Layer 4 — H3 + Suno split workflow

The final music is not generated per-segment. Instead:

```
H3 generates 3 segments → edit into full video → extract full audio → Suno remixes complete audio → final music placed back → final sync edit
```

This gives Suno the complete musical structure (build-up → drop → development → climax → ending) rather than three disconnected 15-second fragments.

The technique stack:

| Technique | Role |
|---|---|
| **Role-Segregated Reference** | Each picture has a specific job, preventing equal-weight compromise |
| **Text-Driven Climax** | Drop Picture 3 for the final segment; let text be the sole director |
| **Music-Driven Timeline** | BPM-anchored segmentation; accents decide actions |
| **H3 + Suno Split** | H3 owns visual; Suno owns final complete music |
| **Hero Shot Timing Lock** | Camera stops at musical peak; holds the iconic frame |

## The named language

> **Layered Reference Architecture with Text-Driven Climax**

"Layered" tells the model: these images are not equal — each has a role. "Text-Driven Climax" tells the model: when the action peaks, text is the only director. Together they solve the two failure modes — reference-image compromise and climax constraint — in one concept.

## 48-hour takeaway

A reference image is an employee, not a partner. Give it a job title, tell it what it does NOT control, and when its job is done, dismiss it.

The most important experiment in this project was **removing Picture 3 from the final segment**. The instinct is to add more references for more control. But during a climax — when camera, action, music, and spray all need to hit specific marks at specific seconds — a guide image becomes a constraint that fights the text. Less reference input gave more output control.

And for multi-segment music videos: **generate all video first, then remix the complete audio.** Feeding Suno the full 45-second audio structure produces a coherent musical arc; feeding it three isolated 15-second clips produces three unrelated tracks.

## The final prompt

See [`prompt.md`](./prompt.md) for the full production document (~1465 lines, Chinese design doc + three English H3 prompts).

The document is organized in this order:

1. **Project structure** — 9:16 vertical, fashion-sports hybrid, visual energy curve
2. **Multi-image lesson** — role segregation for Pictures 1/2/3
3. **The segment-3 exception** — why Picture 3 is dropped for the climax
4. **Music design** — BPM 128, 4/4, timeline function map
5. **Segment 1 prompt** — high-speed windsurfing entry (Picture 1+2+3)
6. **Segment 2 prompt** — large wave zone approach (Picture 1+2+3)
7. **Segment 3 prompt** — final hero moment, text-only camera control (Picture 1+2, no Picture 3)
8. **Segment comparison table** — reference usage per segment
9. **Why text-only for segment 3** — cinematography language upgrade rationale
10. **Post-production workflow** — H3 → full video → extract audio → Suno → final sync
11. **Music-video sync map** — which visual beat aligns with which musical function
12. **Complete workflow diagram** — end-to-end production flowchart
13. **Four retained lessons** — reference separation, Picture 3 per-segment, music as director, H3+Suno split

## Result

A 45-second vertical fashion-sports music video produced in three independent 15-second H3 segments, with the final climax segment using text-only camera control and the complete soundtrack remixed by Suno from the full video's extracted audio.

The signature frame: Furina cosplayer airborne above a breaking wave, transparent blue sail fully extended, camera frozen at the musical peak in a low-angle telephoto hero composition.

## Tags

`#H3` `#prompt-engineering` `#multi-image` `#layered-reference` `#text-driven-climax` `#music-driven-timeline` `#windsurfing` `#fashion-mv` `#suno` `#vertical-video` `#hero-shot`
