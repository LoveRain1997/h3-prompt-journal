# 用手指控制 AI 跳性感卡点舞｜H3 单图手势控舞教程

## 使用说明

**只输入图片 1**，然后直接导入下面整段提示词。

* 图片 1：唯一视觉参考，负责人物外貌、服装、环境、光照、构图和原图摄影视角。
* 不需要输入第二张动作图或手部参考图。
* 可以直接修改提示词里的 **DANCE STYLE** 和动作顺序，自定义舞蹈。
* 但不要破坏核心控制关系：**手指向上/下 → 人物上下变化；手指向左/右 → 人物左右晃动。**
* 想换成其他舞蹈，只修改舞蹈描述，不要删除手势控制和同步规则。

## 完整提示词

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] A continuous live-action first-person smartphone recording based entirely on <Picture 1>. <Picture 1> is the only visual reference for the adult female dancer's appearance, face, hairstyle, hair color, costume, body proportions, environment, room layout, wall, floor, lighting, color and initial spatial composition. Preserve the original visual identity and environment of <Picture 1>.

The camera closely reproduces the distinctive perspective of <Picture 1>: a strong high-angle first-person smartphone POV looking substantially downward at the woman. The camera is clearly above her eye level. The top of her head, shoulders and upper body are visibly seen from above. Keep substantial ceiling visible in the upper part of the frame. Do not use an eye-level view, third-person view, orbiting camera or cuts.

A single adult arm belonging to the camera operator enters naturally from the lower-right foreground. Show a connected forearm, wrist, palm and fingers. The hand is a moderate-size foreground element, not a giant object. Keep the hand primarily within the lower-right quadrant, occupying approximately 10–18% of the image area. The hand must never extend across the center, cover the woman's face or cover her torso. The woman remains the primary visual subject and the hand is only the foreground controller.

Keep the woman physically close to the smartphone, approximately 1.0–1.2 meters away. Her full body occupies approximately 70–80% of the vertical frame. Do not pull the camera backward, do not place her deep in the room and do not progressively make her smaller.

The foreground index finger directly controls the woman's dance movement. The woman does not independently freestyle. The hand is the visible movement cue and the woman's body immediately follows it.

Maintain these exact control relationships throughout the entire video:

UP → WOMAN RISES.
DOWN → WOMAN LOWERS.
LEFT → WOMAN MOVES LEFT.
RIGHT → WOMAN MOVES RIGHT.

For UP, the index finger moves clearly upward and the woman's body immediately rises. Her torso extends upward, her posture becomes taller, her arms naturally rise and her center of gravity moves upward.

For DOWN, the index finger moves clearly downward and the woman's body immediately lowers. Her knees bend slightly, hips lower, center of gravity drops and torso lowers into a controlled dance position.

For LEFT, the index finger moves toward screen-left and the woman's body immediately shifts and sways toward screen-left. Her weight, torso and hips follow the same direction. The entire body movement must be clearly visible.

For RIGHT, the index finger moves toward screen-right and the woman's body immediately shifts and sways toward screen-right. Her weight, torso and hips follow the same direction. The entire body movement must be clearly visible.

LEFT and RIGHT must not become tiny hip twitches. The woman's body must visibly move from side to side. Keep the horizontal movement simple so the connection between finger direction and body direction remains unmistakable.

The hand gesture and corresponding body movement are tightly synchronized. The woman's movement begins as the corresponding finger gesture begins and develops within the same musical beat. No noticeable reaction delay, no one-beat delay, no anticipation and no independent movement.

The dance is a confident, sexy viral short-form influencer dance: energetic rhythmic hip movement, controlled waist isolation, subtle torso waves, attractive shoulder movement, pronounced but tasteful hip accents, confident posture, playful facial expression, direct eye contact and natural hair movement. The dance should feel like a polished viral social-media dance challenge. Make the movement sexy, stylish, rhythmic and visually captivating while keeping it non-explicit.

During LEFT and RIGHT movements, maintain the direct horizontal hand control while adding sensual hip accents. During UP and DOWN movements, maintain the direct vertical hand control while adding smooth waist and body movement. Never sacrifice hand-to-body control for complicated choreography.

Use a fast modern viral dance rhythm with strong clear beats.

Command sequence:
UP → DOWN → LEFT → RIGHT → LEFT → RIGHT → UP → DOWN → LEFT → RIGHT.

Each command produces one clearly visible corresponding body movement. Do not add unrelated freestyle movements, spins, walking or complicated footwork.

The index finger moves with strong, deliberate gestures. The wrist and forearm naturally follow the finger. Use short, clear upward, downward, leftward and rightward gestures. Do not use weak floating gestures. Keep the hand in the lower-right foreground and never allow it to dominate the center of the frame.

Maintain one continuous handheld smartphone recording with subtle natural camera instability. Preserve the strong high-angle perspective and close composition throughout the entire shot. Do not zoom out, pull backward, lower the camera or lose either the hand or the woman's full body.

At the end, use LEFT → RIGHT → UP. The woman performs a left body movement with a sensual hip accent, a right body movement with a sensual hip accent, then rises into a confident final dance pose. The hand remains in the lower-right foreground and does not move into the center. Hold the final pose briefly.

overall_soundscape: Natural indoor room ambience, subtle foot movement, fabric movement and quiet smartphone handling sounds, preserving the acoustic character of <Picture 1>.

non_diegetic_music: A modern viral short-form dance track with strong punchy beats, crisp percussion and clear rhythmic accents. Each major beat provides a timing point for the hand gesture and its corresponding dance movement.
```
