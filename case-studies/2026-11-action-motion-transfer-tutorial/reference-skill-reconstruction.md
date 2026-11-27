---
name: h3-dance-video-reconstruction
version: 1.0.0
description: Reverse-engineer dance and performance videos into faithful, character-aware, timestamped H3 prompts with explicit reference authority, movement mechanics, camera behavior, and segment continuity.
---

# H3 Dance Video Reconstruction Skill

## 1. Purpose

Turn a supplied dance/performance video into two deliverables:

1. **A grounded choreography breakdown** that explains what each performer actually does, when they do it, how their bodies move, how they relate to one another, and how the camera behaves.
2. **Complete, independently usable H3 segment prompts** that reconstruct the source performance while applying the user's designated character, appearance, environment, and audio references.

The task is reverse-engineering, not free-form choreography invention. The source video is the evidence. Preserve its distinctive movement structure, timing, asymmetry, interactions, spatial changes, and ending instead of replacing them with generic dance language.

## 2. When to use

Use this skill when the user asks to:

- Analyze,拆解,反推,复刻,迁移, or reconstruct dance/action from a supplied video.
- Replace people or mannequins in a video with characters from one or more reference images.
- Produce H3 prompts from a dance reference, including segmented prompts.
- Preserve a video's choreography while changing character identity, art style, clothing, or background according to references.

If the user asks only for a prompt rewrite and no video analysis is needed, do not run the full analysis workflow.

## 3. Non-negotiable principles

### 3.1 Observe first; write second

- Inspect the actual supplied video before describing its choreography.
- Never infer a complete sequence from the opening frame, thumbnail, filename, or a few disconnected frames.
- Use a broad timeline scan first, then inspect denser samples around movement changes, turns, crossings, accents, and segment boundaries.
- If a movement is unclear or occluded, describe only what can be supported. Mark uncertainty rather than inventing an exact limb path.
- Do not claim exact BPM, beat positions, frame rate, duration, or camera movement unless measured or visibly supported.

### 3.2 Preserve source choreography

- Treat the source as the authority for action order, timing, movement direction, body orientation, footwork, gesture pathways, interaction, formation, and ending.
- Do not simplify a complex phrase into “wave arms,” “turn around,” “step,” or “dance energetically.” Explain the actual movement sequence and body mechanics.
- Do not add jumps, spins, kicks, travelling paths, props, interactions, facial acting, or camera moves that are not present in the source.
- Do not force mirrored choreography when the source performers are asynchronous or use different movements.
- Preserve delays, counter-movements, individual variations, and deliberately asymmetrical ending poses.

### 3.3 Separate reference responsibilities

State the authority of every supplied reference explicitly. The default arrangement is:

- `<Picture 1>`: character identity and appearance; also the environment/background when the user says the picture is the scene master or asks to preserve its background.
- `<Video 1>`: choreography, body mechanics, movement trajectory, interaction, timing, shot composition, and camera behavior.
- `<Audio 1>`: audio content and timing authority when the user supplies audio for synchronization or retiming.

Do not copy unwanted elements from a motion reference. For example, when `<Video 1>` contains white mannequins or a grey studio, these are motion references only if the user has specified that the characters and/or background must come from `<Picture 1>`.

If the user assigns different authority, follow the user's explicit assignment instead of this default.

### 3.4 Preserve identity mapping

When replacing multiple performers:

- Define each replacement identity explicitly, such as original left performer → left character in `<Picture 1>` and original right performer → right character in `<Picture 1>`.
- Keep identity attached to the performer throughout the video, including when the performers turn, overlap, cross, or move to different screen positions.
- Never swap faces, clothing, hairstyles, or identities; never merge or duplicate performers.
- Distinguish **identity correspondence** from **current screen position**. A character moving across the frame does not become the other character.
- If the source has more performers than the references can identify, state the unresolved mapping instead of silently inventing it.

### 3.5 Respect established H3 syntax

Use native reference tags with angle brackets and spaces:

- `<Picture 1>`
- `<Video 1>`
- `<Audio 1>`
- `<Subject 1>`

Do not write `Picture1`, `Video1`, `Audio1`, or `Subject1` as substitutes for the reference tags.

When the task needs character binding, use `subject_definitions` and `integrated_multimodal_description`. Keep the prompt complete rather than returning isolated patches or fragments.

## 4. Input inspection workflow

### Step 1 — Establish the media facts

Record only facts that can be read or measured:

- Total duration.
- Frame rate and resolution when available.
- Aspect ratio and visible framing.
- Whether audio is present and whether it is relevant to timing.
- Number of performers and their initial screen positions.

Do not make the user repeat information already available in the conversation.

### Step 2 — Build a coarse timeline

- Sample the video across its full duration at a regular interval sufficient to see the overall phrase structure.
- Identify entrances, delayed starts, changes in formation, body-orientation changes, synchronized sections, solo sections, crossings, accents, and the final pose/action.
- Mark approximate timestamps for each meaningful transition.
- Do not divide the video into equal-length segments merely for convenience. Segment boundaries should follow actual phrase or action changes, subject to H3 duration limits.

### Step 3 — Inspect movement transitions closely

For every phrase boundary or complex action, inspect additional frames around:

- The initial body position.
- The action initiation.
- The widest/strongest extension or accent.
- Weight transfer and foot contact.
- The recovery or return path.
- The transition into the next action.

A contact sheet is a navigation aid, not sufficient evidence for every detailed action. Revisit the original video around ambiguous or fast movements.

### Step 4 — Track performers independently

Create a separate movement record for every performer before writing a combined duet description.

For each performer, track:

- Screen position and travel direction.
- Facing direction and torso orientation.
- Supporting foot and weight transfer.
- Step pattern, knee lift, landing, and balance.
- Pelvis and torso tilt/rotation.
- Shoulder action and arm pathway.
- Elbow shape, wrist direction, and hand/finger articulation where visible.
- Head direction and visible facial expression.
- Start delay, synchronization, response, and interaction with the other performer.

Do not let the more active performer erase the less active performer's actions. A performer who waits, watches, prepares, or joins late is still part of the choreography.

### Step 5 — Identify duet structure

Explicitly classify the relationship at each point:

- Solo lead with partner waiting or observing.
- Delayed entry or response.
- Call-and-response.
- Synchronized unison.
- Parallel but non-identical movement.
- Mirrored movement, only when actually mirrored.
- Opposing movement or counterbalance.
- Formation change, approach, retreat, crossing, or separation.
- Asymmetric final gesture or pose.

State whether the performers face the camera, face each other, turn sideways, or turn away. Do not assume both performers always share the same facing direction.

### Step 6 — Analyze camera behavior separately

Record the camera only where the source supports it:

- Shot size and whether the performers remain full-body.
- Physical camera height and viewing direction.
- Camera travel: static, pan, tilt, tracking, orbit, push, pull, or handheld movement.
- Reframing, cuts, and changes of viewpoint.
- Whether the performers move relative to the camera or the camera moves to follow them.

Do not invent camera movement to make the prompt sound cinematic. If the source camera is static, say it is static. If the camera behavior cannot be established, omit unsupported detail.

**No Degree Law:** Do not write numeric camera-angle labels in degrees. Describe physical camera placement, height, distance, viewing direction, subject-ground relationship, and actual camera path instead.

### Step 7 — Use audio only when it is available and relevant

- If `<Audio 1>` is supplied as timing authority, preserve its exact requested slice, local time reset, segment duration, and musical events.
- If BPM, beat, bar, phrase, downbeat, or lyric-event data is supplied, use those values as given.
- If no verified tempo data exists, use source-video timestamps and visible action timing. Do not fabricate BPM or beat numbers.
- Do not add lip-sync to dance-only footage unless requested or clearly present in the source.

## 5. Choreography writing standard

### 5.1 Describe mechanics, not labels

Weak descriptions:

- “The character waves both arms.”
- “They turn and dance together.”
- “They move gracefully and energetically.”
- “The character does a cute pose.”

Required level of description:

- Which arm or leg moves first.
- Where the limb starts and where it travels.
- Whether the arm opens, folds, circles, crosses, rises, or sweeps.
- How the shoulders, elbows, wrists, and hands articulate the movement.
- Which foot supports the body and where the weight transfers.
- Whether the knee bends, lifts, lands, or stabilizes.
- How the torso tilts or rotates in relation to the hips and feet.
- How the movement resolves and leads into the next action.

Use only the detail visible in the source. If hand/finger details are too small to resolve, describe the larger arm pathway without inventing finger choreography.

### 5.2 Use a movement-chain structure

Where the source permits, describe each action chain as:

1. **Preparation** — starting posture, supporting foot, and gathered energy.
2. **Initiation** — the first body part or weight shift that starts the action.
3. **Expansion** — how the movement travels through the body and opens in space.
4. **Accent** — the most distinct extension, lift, tilt, turn, or rhythmic emphasis.
5. **Recovery** — how the body returns or changes support.
6. **Transition** — the physical action that makes the next movement possible.

Do not force all six labels into every sentence. The purpose is to ensure that the complete action chain is represented, not to create repetitive prose.

### 5.3 Preserve rhythm and movement density

- Preserve the source's relative movement density: stillness, preparation, quick accents, sustained movement, and recovery.
- Do not turn every beat into a new action if the source uses continuous movement.
- Do not stretch a brief gesture into a long pose or compress a long phrase into one vague action.
- State meaningful action timing with timestamps or time ranges.

### 5.4 Chibi and stylized-character adaptation

When the destination characters are chibi or use a different body style:

- Preserve the source action's intent, order, direction, rhythm, and spatial relationship.
- Adapt limb reach, balance, knee height, and torso range naturally to the destination character proportions.
- Keep actions readable at the smaller body scale; do not produce broken wrists, twisted joints, disconnected limbs, or impossible balance.
- Preserve the reference character's head, face, hair, clothing, accessories, color design, and defining details.
- Do not enlarge the head further or alter the character design unless asked.
- Clothing may respond naturally to movement, but must not be redesigned or replaced unless the user requests it.

## 6. Segment design rules

### 6.1 Duration and boundaries

- Every H3 generation segment must be **15 seconds or shorter**.
- Preserve the original source timeline; do not silently speed up, slow down, trim, or reorder actions.
- Prefer boundaries at phrase changes, performer entry/exit, formation changes, major turns, or clear action transitions.
- Do not split in the middle of a distinctive movement unless the duration limit makes it unavoidable.
- When a source is longer than 15 seconds, use as many segments as necessary. Do not force a fixed number of segments.
- Display each segment's exact source-time range and duration.

### 6.2 Each segment must be independently usable

Every segment prompt must repeat the reference hierarchy, character definitions/mapping, appearance locks, environment locks, and relevant camera rules. Do not rely on a previous segment's prompt being present in the model's context.

Each segment must specify:

- Its opening body state and facing direction.
- The first visible action and how it begins.
- The complete action sequence in this time range.
- Each performer's separate action and relationship to the partner.
- Footwork, support, weight transfer, torso, arms, and turns where visible.
- The ending action/state and whether it is a transition or final pose.
- Camera behavior for this time range.

Avoid generic statements such as “continue from the previous segment” as the only opening instruction. Explicitly describe the actual opening movement.

### 6.3 Segment-to-segment continuity

For consecutive generated segments:

- Record the final movement state of segment N and the opening movement state of segment N+1.
- Use a physically plausible handoff. Do not require H3 to reproduce an exact held body pose across independently generated clips.
- When compatible with the source camera and choreography, use a local movement anchor (for example, a raised hand, turning shoulder, stepping foot, or flowing sleeve) to bridge the cut: end on a readable movement detail and open the next segment on the same action detail before revealing the next full-body action.
- Do not force a close-up, camera move, match cut, or new angle when the source does not support it or the user has locked the camera.
- Do not insert a freeze, dead pause, or arbitrary hard cut that is absent from the source.
- If an exact visual match is not feasible, preserve direction, facing, momentum, and timing as the continuity bridge.

### 6.4 Preserve the real ending

The final segment must reproduce the source ending, including any difference between performers. Do not replace a distinctive asymmetric ending with a synchronized generic pose. Specify the final body positions and the final hold only when the source actually holds.

## 7. H3 prompt construction contract

### 7.1 Required top-level structure

For character replacement or multi-character transfer, use this structure:

```text
subject_definitions:

<Subject 1>:
[Exact identity and appearance assignment from the designated picture reference.]

<Subject 2>:
[Exact identity and appearance assignment from the designated picture reference.]

integrated_multimodal_description:

REFERENCE AUTHORITY:
[Explicitly define what each Picture, Video, and Audio reference controls.]

CHARACTER MAPPING:
[Explicit left/right or named identity mapping. State that identity never swaps.]

APPEARANCE AND ENVIRONMENT LOCK:
[Specify exactly what stays from the image reference and what must not be inherited from the motion video.]

CHOREOGRAPHY — SOURCE TIMING [START–END]:
[Timestamped, performer-specific action chain with mechanics and duet relationship.]

CAMERA:
[Only source-supported framing, camera placement, and movement.]

SEGMENT ENDING / TRANSITION:
[Concrete ending state and handoff to the next segment, if applicable.]
```

This is a structure guide, not a reason to include irrelevant headings. If the user asks for a single performer or no character replacement, omit unnecessary character-mapping sections while retaining the relevant reference authority.

### 7.2 Prompt language and completeness

- Default to **Chinese analysis + English H3 prompts**, unless the user requests another language.
- Provide complete prompts for every requested segment, not patch-only edits.
- Put every required reference tag directly in the prompt using its exact native syntax.
- Make each prompt executable as a standalone H3 input.
- Use concrete imperative instructions and explicit source authority.
- Avoid unsupported numerical camera angles, invented BPM, invented props, and vague cinematic filler.

### 7.3 Character and scene locks

Use positive, explicit locks:

- “The character retains the exact identity and appearance from `<Picture 1>`.”
- “The original live-action environment from `<Picture 1>` remains unchanged.”
- “Only the performers are replaced; the motion and camera behavior are transferred from `<Video 1>`.”

Do not overdescribe an environment that must be copied exactly from a reference image. Name the background lock and identify its source. Do not accidentally invite a background redraw by writing a new scenic description that conflicts with the reference.

### 7.4 No unwanted additions

Unless the user asks for them, do not add:

- New props, furniture, accessories, people, animals, or scenery.
- New costume elements or redesigned clothes.
- Extra choreography, extra turns, jumps, kicks, or dance breaks.
- Unrequested lip-sync, dialogue, or facial acting.
- Unobserved camera moves, lighting changes, visual effects, or cuts.
- Additional backgrounds or alternate locations.

## 8. Output contract — what the response must contain

When the user requests a **complete dance breakdown and segmented H3 prompts**, deliver the following in order.

### A. Short analysis preface

State:

- Source video identity (use the supplied filename when available).
- Verified duration.
- Number of performers.
- The overall choreography structure in one or two sentences.

Do not use generic praise or unsupported evaluation.

### B. Timestamped choreography breakdown

Provide a compact table with these columns:

| Source time | Left performer | Right performer | Duet / formation / facing | Camera |
|---|---|---|---|---|

Rules:

- Every row must describe a distinct action phrase or meaningful transition.
- Keep the left and right performers separate.
- Include waiting, delayed entry, response, synchronization, and asymmetry where present.
- Include facing direction and spatial changes where relevant.
- Include camera information only if observed; otherwise write “fixed” only when the source visibly confirms it, or omit the camera detail.
- Use timestamp precision appropriate to the inspection. Do not imply frame-perfect accuracy from coarse sampling.

### C. Complete H3 prompts for every segment

For each segment, provide:

1. Segment number and exact source-time range.
2. A short Chinese title that describes its actual choreography function.
3. The complete English H3 prompt in a separate fenced code block.
4. Explicit character identity mapping and reference authority.
5. Performer-specific action mechanics and timing.
6. Camera and environment constraints.
7. A concrete segment ending/transition.

Do not provide only a summary, action list, or one master prompt when the user asked for segmented prompts.

### D. Brief execution notes

End with only the most consequential risks or continuity requirements, such as:

- A delayed performer entry that must not be lost.
- A required back-facing or front-facing transition.
- A crossing that must not swap identities.
- A distinctive asymmetric final pose.

Do not repeat the entire analysis in the notes.

## 9. Quality gates before responding

Check every item before finalizing:

### Evidence and timing
- [ ] The full source video was inspected, not just a still or filename.
- [ ] Duration and timeline are supported by the source.
- [ ] Major action phrases and transitions are represented in order.
- [ ] No invented actions, props, timing, BPM, or camera moves appear.

### Performer fidelity
- [ ] Each performer has an independent action description.
- [ ] Delayed entries and moments of waiting are preserved.
- [ ] Synchronization is used only where the source is synchronized.
- [ ] Asymmetric actions and the original ending are preserved.
- [ ] Identity mapping remains stable throughout the video.

### Movement detail
- [ ] Descriptions include concrete limb pathways and body mechanics.
- [ ] Weight transfer, supporting foot, steps, knee lifts, and landings are included where visible.
- [ ] Torso, shoulder, elbow, wrist, and hand details are included to the level supported by the footage.
- [ ] Every phrase has a clear transition into the next phrase.

### H3 usability
- [ ] Native tags use angle brackets and spaces: `<Picture 1>`, `<Video 1>`, `<Audio 1>`, `<Subject 1>`.
- [ ] Every segment is no longer than 15 seconds.
- [ ] Every segment prompt is complete and independently usable.
- [ ] Each segment has an explicit opening action and ending state.
- [ ] Segment continuity does not rely on an impossible exact pose handoff.
- [ ] Character appearance and background locks are explicit and do not conflict with motion-reference instructions.
- [ ] English H3 prompt blocks are complete; no patch-only fragments.

If any item cannot be verified, do not pretend that it has passed. State the limitation briefly and write only what the evidence supports.

## 10. Failure patterns to avoid

Do not produce these common low-quality outputs:

- **Generic dance prose:** repeated use of “elegant,” “energetic,” “flowing,” or “playful” without physical action detail.
- **Merged performers:** describing a duet as one combined body instead of tracking each performer separately.
- **False synchronization:** making both performers do the same thing because they are dancing together.
- **Lost negative space:** omitting a performer who is waiting, watching, or preparing to enter.
- **Timeline flattening:** describing a 20-second video as one undifferentiated routine.
- **Invented choreography:** adding spins, jumps, poses, travel, or gestures to make the prompt appear richer.
- **Reference leakage:** copying the motion video's mannequin, clothing, studio, or background when those are not the desired output.
- **Identity drift:** allowing left/right characters to swap identities when they turn or cross.
- **Camera invention:** adding orbit, zoom, push-in, or angle changes without source evidence.
- **Continuity by slogan:** writing only “continue from the previous segment” without specifying the opening action.
- **Incomplete prompt delivery:** giving a master prompt or fragments instead of every requested standalone segment.
- **Overconfident precision:** presenting approximate visual timestamps as frame-perfect measurements.

## 11. Recommended response skeleton

Use this order and keep the wording direct:

```markdown
已检查《[filename]》，视频时长约 [duration]，共有 [performer count] 位表演者。
[One or two sentences describing the actual choreography arc.]

## 一、舞蹈动作拆解
[Timestamped left/right/relationship/camera table]

## 二、H3 分段提示词
[Reference authority and character mapping]

### SEG01｜[start–end]｜[actual phrase title]
[Complete standalone English H3 prompt]

### SEG02｜[start–end]｜[actual phrase title]
[Complete standalone English H3 prompt]

[Continue until the full source timeline is covered.]

## 三、执行时的关键约束
[Only the few highest-impact fidelity risks]
```

If the user asks for only the skill, do not execute a new video analysis. If the user asks for an edit to one segment, preserve all unaffected segment content and return the complete revised segment rather than rewriting the entire work unnecessarily.
