# H3 Motion Transfer — Subject-First Reconstruction (动作迁移 · 人物优先重建)

> 案例展示视频: [result-video.mp4](./result-video.mp4) — 9.4s · 928×1664 · 图1 人物+世界 × 目标视频动作 × 音频1 时序, 一镜合成。
> **工作流**: [H3动作迁移工作流.json](https://github.com/LoveRain1997/h3-prompt-journal) (ComfyUI, MiniMax H3 Ref2VA 双通道)。

## 这是什么

H3 动作迁移: 输入**图1**（人物+世界的唯一权威）、**视频1**（动作与镜头参考）、**音频1**（时序权威），输出一段"图1的人在图1的世界里，跳视频1的舞、踩音频1的点"的新实拍表演。展示视频即实测结果：目标视频是黑裙绣花抹胸裙室内踢腿小舞，迁移后成为青绿仙裙湖边石上的同构编舞——人物、服装、环境全部来自图1，动作机制、镜头几何逐拍对应，时长 9.4s。

## 硬约束：H3 动作迁移最长 8–9 秒

> ⚠️ **H3 单次动作迁移生成上限约 8–9 秒。** 目标视频超过 9s 必须先剪辑截取，或将编舞按乐句拆成 8–9s 的段分别迁移再拼接。本案例 9.4s 已接近上限（工作流 Duration=9s, 124 帧 @24fps）。超过上限会导致动作漂移、身份崩坏或尾部截断。

## 提示词全文（可直接粘贴）

```text
# MULTIMODAL RECONSTRUCTION
# SUBJECT-FIRST RECONSTRUCTION WITH FIRST-FRAME CAMERA ALIGNMENT

Create ONE coherent live-action performance video from:

<Picture 1>
<Video 1>
<Audio 1>

These references have STRICTLY SEPARATED responsibilities.

The most important rule is:

<Picture 1> owns the FINAL PERSON and FINAL WORLD.

<Video 1> does NOT own the final person.

<Video 1> does NOT own the final environment.

<Video 1> does NOT own the final background.

<Video 1> does NOT own the final clothing.

<Video 1> does NOT own the final lighting.

Video 1 provides only transferable BODY MOVEMENT and CAMERA BEHAVIOR.

<Audio 1> controls FINAL TIMING.


# ABSOLUTE SUBJECT IDENTITY RULE

The final performer MUST be Subject 1 from <Picture 1>.

This is an absolute identity constraint.

At every frame of the final video:

Subject 1's face, facial structure, hair, body appearance, body proportions, clothing, accessories and recognizable physical identity must remain derived from <Picture 1>.

NEVER use the person appearing in <Video 1> as the final performer.

NEVER preserve the Video 1 person's:

* face
* facial structure
* hair
* hairstyle
* body
* body proportions
* clothing
* costume
* accessories
* makeup
* skin appearance
* physical identity

The person in Video 1 exists ONLY as a source of motion information.

The person in Video 1 is NOT a second subject.

The person in Video 1 is NOT a visual identity reference.

The person in Video 1 MUST be completely replaced by Subject 1 from Picture 1.


# ABSOLUTE ENVIRONMENT RULE

The final environment MUST come from <Picture 1>.

The final background MUST come from <Picture 1>.

The final architecture MUST come from <Picture 1>.

The final spatial world MUST come from <Picture 1>.

NEVER use Video 1's:

* background
* room
* building
* street
* stage
* studio
* landscape
* walls
* floor
* ceiling
* architecture
* decorative objects
* environmental objects
* production design
* scenery

as the final environment.

The Video 1 environment is completely discarded.

The final video must physically exist inside the world of Picture 1.


# CRITICAL FIRST-FRAME RULE

The first frame of Video 1 is NOT a complete visual template.

Do NOT copy the first frame of Video 1.

Do NOT reproduce the first frame of Video 1 as an image.

Do NOT transfer the person from the first frame.

Do NOT transfer the background from the first frame.

Do NOT transfer the lighting from the first frame.

Do NOT transfer the environment from the first frame.

Do NOT transfer the clothing from the first frame.

Do NOT transfer the production design from the first frame.

Only extract the following NON-VISUAL-IDENTITY information from the first frame:

* camera-to-subject distance
* camera height
* camera orientation
* camera angle
* shot size
* framing geometry
* subject scale within frame
* visible body region
* headroom
* side margins
* approximate subject position in frame
* subject-facing direction
* opening body orientation
* opening pose mechanics

Everything else in the first frame is discarded.


# FIRST FRAME = CAMERA GEOMETRY ONLY

Interpret the first frame of Video 1 as a CAMERA GEOMETRY REFERENCE.

It answers only:

"How is the camera positioned relative to the performer at 0.00 seconds?"

It does NOT answer:

"Who is the performer?"

It does NOT answer:

"Where is the performer?"

It does NOT answer:

"What does the environment look like?"

It does NOT answer:

"What does the performer wear?"

It does NOT answer:

"What lighting does the scene use?"

Those questions are answered exclusively by Picture 1.


# 0.00 SECOND RECONSTRUCTION

At 0.00 seconds, first establish Subject 1 from Picture 1 inside the world of Picture 1.

Then physically position the camera so that Subject 1 has approximately the same:

* shot size
* camera-to-subject distance
* visible body region
* subject scale
* framing
* headroom
* side margins
* camera height
* camera angle
* body orientation

as the performer in Video 1's first frame.

This is a CAMERA REPOSITIONING operation.

It is NOT a PERSON REPLACEMENT inside Video 1.

It is NOT a BACKGROUND REPLACEMENT inside Video 1.

It is NOT a VIDEO-TO-VIDEO FACE SWAP.

It is NOT an IMAGE COMPOSITING operation.

The correct construction is:

Subject 1 from Picture 1
+
World from Picture 1
+
Camera geometry extracted from Video 1's first frame

NOT:

Video 1 first frame
+
Picture 1 background

NOT:

Video 1 first frame
+
Picture 1 face

NOT:

Video 1 first frame
+
Picture 1 character


# SUBJECT-FIRST INITIALIZATION

Before applying any Video 1 information, establish:

1. Subject 1 from Picture 1
2. Picture 1 clothing
3. Picture 1 physical appearance
4. Picture 1 environment
5. Picture 1 background
6. Picture 1 spatial world

Only AFTER these are established may Video 1 camera geometry be applied.

The order is mandatory:

PICTURE 1 SUBJECT
↓
PICTURE 1 WORLD
↓
CAMERA REPOSITIONING
↓
VIDEO 1 OPENING BODY ORIENTATION
↓
MOVEMENT RECONSTRUCTION

Never reverse this order.

Do NOT begin from Video 1 and then attempt to replace its person.

Do NOT begin from Video 1 and then attempt to replace its background.

The final video must be generated from Picture 1 as the base physical world.


# OPENING POSE TRANSFER

The opening pose from Video 1 may be transferred ONLY as BODY MECHANICS.

Transfer:

* limb configuration
* body orientation
* weight distribution
* balance
* arm position
* head orientation
* gaze direction
* preparation state

but reconstruct that pose using Subject 1 from Picture 1.

Do NOT transfer the visual appearance of the Video 1 performer.

If the Video 1 performer is standing in a particular pose:

Subject 1 from Picture 1 performs that pose.

The Video 1 performer must disappear completely from the final result.


# VIDEO 1 IS A MOTION CAPTURE REFERENCE

Treat Video 1 as if it were a motion-capture reference.

Extract:

* preparation
* initiation
* acceleration
* expansion
* contraction
* accent
* recovery
* weight transfer
* foot placement
* pelvis movement
* torso movement
* shoulder movement
* arm pathway
* wrist movement
* hand movement
* head movement
* gaze
* facing direction
* movement amplitude
* movement speed
* transition mechanics

Do NOT treat Video 1 as footage that should be visually reproduced.

The final performer is always Subject 1 from Picture 1.


# VIDEO 1 CAMERA = MOTION-CAMERA REFERENCE

After extracting the body movement, separately extract the physical camera behavior:

* camera position
* camera distance
* camera height
* camera angle
* camera orientation
* camera trajectory
* camera speed
* handheld behavior
* tracking
* push-in
* pull-back
* lateral movement
* orbit
* reframing
* shot-size changes
* visible body-region changes

Reconstruct these camera behaviors inside Picture 1's world.

Do NOT reconstruct the Video 1 environment around the camera.

The camera moves through Picture 1's world, not Video 1's world.


# STRICT REFERENCE SEPARATION

Think of the references as separate channels:

PICTURE 1
= PERSON
= CLOTHING
= IDENTITY
= ENVIRONMENT
= BACKGROUND
= WORLD

VIDEO 1 FIRST FRAME
= CAMERA GEOMETRY
= OPENING BODY ORIENTATION

VIDEO 1 REMAINDER
= MOVEMENT MECHANICS
= TRANSITIONS
= CAMERA BEHAVIOR

AUDIO 1
= TIMING
= RHYTHM
= ACCENTS
= PHRASES
= TRANSITIONS


# NEVER MERGE REFERENCE ROLES

Do NOT let Video 1 provide identity.

Do NOT let Video 1 provide environment.

Do NOT let Video 1 provide clothing.

Do NOT let Video 1 provide lighting design.

Do NOT let Video 1 provide production design.

Do NOT let Picture 1's original camera framing override the camera geometry learned from Video 1.

Do NOT let Video 1's original person override Subject 1.

Do NOT let Video 1's original environment override Picture 1.

Each reference controls only its assigned information.


# AUDIO 1 — FINAL TEMPORAL AUTHORITY

<Audio 1> determines when the reconstructed movement happens.

Do NOT preserve Video 1's original timing.

Do NOT simply replay Video 1.

Do NOT speed up or slow down Video 1 as a whole.

Instead:

reconstruct the movement from Subject 1's opening state according to Audio 1.

Use:

* BPM
* beat duration
* bar duration
* phrase duration
* first downbeat
* musical accents
* musical hits
* phrase boundaries

when provided.

The opening state must develop naturally into the first musical movement phrase.


# MOVEMENT CONTINUITY

Use:

preparation
→ initiation
→ expansion
→ accent
→ recovery
→ transition

Do NOT create:

* disconnected poses
* slow wandering
* idle walking
* arbitrary repositioning
* frozen pose sequences

When a position change is necessary, use the minimum practical number of steps.

The performer must remain actively performing.


# FINAL PHYSICAL WORLD

The final video must feel like one continuous real-world filming session.

Subject 1 remains the same person from Picture 1.

The world remains the world from Picture 1.

The camera physically exists inside Picture 1's environment.

The movement comes from Video 1's transferable physical mechanics.

The camera language comes from Video 1's transferable cinematography.

The timing comes from Audio 1.


# FINAL VALIDATION

Before final generation, verify:

SUBJECT:

Is every frame's performer Subject 1 from Picture 1?

If NO → reject and reconstruct.

BACKGROUND:

Is every frame's environment derived from Picture 1?

If NO → reject and reconstruct.

OPENING:

Does 0.00 seconds use the camera geometry of Video 1's first frame?

If NO → adjust the physical camera.

VIDEO 1 PERSON:

Has the Video 1 performer been completely discarded?

If NO → reject and reconstruct.

VIDEO 1 BACKGROUND:

Has the Video 1 environment been completely discarded?

If NO → reject and reconstruct.

MOVEMENT:

Is the body movement reconstructed from Video 1 mechanics rather than copied frame-by-frame?

If NO → reconstruct.

TIMING:

Is the movement retimed according to Audio 1?

If NO → reconstruct.

CAMERA:

Is the camera behavior derived from Video 1 while physically existing inside Picture 1?

If NO → reconstruct.


# FINAL TARGET

The intended result is exactly:

PICTURE 1 PERSON
+
PICTURE 1 WORLD
+
VIDEO 1 FIRST-FRAME CAMERA GEOMETRY
+
VIDEO 1 OPENING BODY MECHANICS
+
VIDEO 1 MOVEMENT LANGUAGE
+
VIDEO 1 CAMERA LANGUAGE
+
AUDIO 1 TIMING

→ ONE NEW LIVE-ACTION PERFORMANCE


The result must NOT be:

Video 1 with Picture 1 background.

The result must NOT be:

Video 1 with Picture 1 face.

The result must NOT be:

Video 1 with Picture 1 character pasted onto it.

The result must NOT be:

Picture 1 background with the original Video 1 performer.

The result MUST be:

Subject 1 from Picture 1 performing inside Picture 1's world, beginning from a camera composition derived from Video 1's first frame, then performing a newly reconstructed Audio 1-driven choreography using only the transferable physical movement and camera language of Video 1.
```

## 使用说明

- **输入三件套**: `<Picture 1>` = 人物+世界锚定图（人物外观、服装、环境、光线全部由它定义，提示词零外貌文字）；`<Video 1>` = 目标动作视频（只贡献动作机制+首帧镜头几何+镜头行为）；`<Audio 1>` = 时序权威（BPM/重拍/乐句）。
- **时长上限**: 目标视频剪辑到 **8–9 秒以内**再喂给 H3（工作流 Duration 节点=9）。长舞按乐句拆段，逐段迁移后剪辑拼接。
- **ComfyUI 工作流要点**（H3动作迁移工作流.json）: UNET=`minimax_h3_hybrid_fl2va_ref2va` + Ref2VA turbo LoRA；双通道（20步 simple / 6步 turbo sigma，开关切换）；动态场景 beta-8 + ExtendIntermediateSigmas(2, 0.75)、静态场景 beta-4 + (3, 0.75)；续接段用 ImageAddNoise(0.2–0.5) 缓解油腻，成片剪辑时裁掉加了噪声的前 22 帧；分辨率 1344×768，Duration=9s/124 帧 @24fps。
