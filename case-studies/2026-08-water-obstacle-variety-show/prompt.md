# 水上闯关综艺「剧情锚点」提示词

## 使用方法

只上传 **1 张图片**作为人物参考，即 `<Picture 1>`。

`<Picture 1>` 只负责确定主角的身份与外观，其他角色、场景、障碍、摄影和综艺氛围全部由 H3 根据提示词自行生成。

这个 Prompt 的核心思路不是把每一个动作写死，而是只规定几个**不可改变的剧情锚点**，例如：

**滚筒成功 → Fishbone 摔倒 → 起身继续 → 高墙抓住 → 机关侧面击飞 → 落水 → 湿发表情结尾**

至于具体怎么躲障碍、怎么失衡、镜头怎么切、观众怎么反应，让 H3 自己发挥。

## 分辨率调试技巧

提示词按 **20 秒规格**编写。实际生成时推荐两步走：

**第一步：0.3 分辨率调试**

在 0.3 分辨率下即可生成完整 20 秒视频。分辨率低、生成快，适合反复迭代调试场景编排——剧情锚点是否成立、摔倒是否自然、击飞时机是否准确，都能在低分辨率下快速验证。

**第二步：直接调高分辨率出片**

场景调试满意后，不用动提示词，直接把分辨率改到 **1 或 0.8** 重新生成，即可获得不错的最终效果。

> 分辨率只影响画质，不影响时长与编排。所以提示词一次写好，调试期用 0.3 快速试错，出片期切 1/0.8 一遍过。

---

## Prompt

### subject_definitions

<Subject 1> (S1) is the main contestant, visually derived from <Picture 1>. Preserve her identity and overall appearance from <Picture 1>, including face, hairstyle, hair color, skin tone, apparent age, body proportions, physique, clothing, and any accessories visibly present in the reference. Do not introduce new wearable accessories that are not present in the reference.

### summary

[reference generation] Create a 20-second, 16:9 horizontal, highly realistic live-action Chinese television water-obstacle variety show.

<Subject 1> competes on one large continuous nighttime water-obstacle course above a competition pool. The course is a clearly connected linear track consisting of the starting platform, rolling-cylinder obstacle, Fishbone Reverse, connecting runway, and a giant curved final wall.

<Subject 1> continuously progresses toward the finish.

The obstacle interactions, choreography, camera language, timing, reactions, detailed physical movements, and television production style should be naturally designed by the model for the most convincing and entertaining result while preserving the required story beats.

### retention_analysis

<Subject 1> remains the same person from <Picture 1> throughout the entire video.

The competition takes place in one continuous nighttime arena with one coherent obstacle course and one competition pool. The runway and obstacles remain spatially connected and visually understandable from shot to shot.

Do not add new wearable accessories that are absent from <Picture 1>.

The model has creative freedom over camera placement, editing rhythm, exact body movement, obstacle-avoidance choreography, audience reactions, facial acting, broadcast framing, and detailed physical motion, provided the required story beats remain intact.

### detailed_description

[Shot 1]

Introduce <Subject 1> at the starting platform of the large nighttime water-obstacle course.

Establish the scale and excitement of the Chinese television variety-show environment.

<Subject 1> briefly addresses the camera in a soft, cute, youthful feminine Mandarin voice:

<Subject 1> (S1) says, <d>[Mandarin Chinese] 大家好，我要开始啦！</d>

She then prepares to compete and begins moving toward the course.

Allow the model to naturally determine the opening framing, camera movement, acting details, and broadcast presentation.

[Shot 2]

The competition begins.

<Subject 1> rapidly enters the first rolling-cylinder obstacle and continues forward through it.

The cylinders respond naturally to her weight and movement.

Show convincing momentum, balance adjustments, and physical interaction.

She successfully clears this section and continues toward Fishbone Reverse.

Let the model freely choreograph the detailed crossing and camera movement.

[Shot 3]

<Subject 1> enters Fishbone Reverse and attempts to cross while continuously progressing toward the finish.

The rotating elements create increasing difficulty and require natural real-time reactions.

The model may choose the most convincing combination of ducking, stepping, leaning, jumping, lowering the body, sliding, or other physically plausible evasive movements.

One physical interaction must eventually disrupt her balance and cause a genuine fall onto the obstacle platform.

The fall should feel accidental, believable, and slightly comedic rather than staged.

[Shot 4]

Continue naturally from the fall.

<Subject 1> recovers and immediately resumes the competition, continuing toward the finish.

She clears the remaining Fishbone section and reaches the next connecting part of the same runway.

The model determines the most natural recovery movement and camera transition.

[Shot 5]

<Subject 1> reaches the final curved wall at the end of the same obstacle course.

She makes one determined final attempt.

She successfully runs onto the wall and reaches the top, securing the wall edge with both hands.

For a brief moment, she appears extremely close to completing the challenge.

Audience excitement reaches its peak.

Allow the model to naturally determine the climbing motion, camera angle, pacing, and performance detail.

[Shot 6]

At the moment she appears close to succeeding, a large padded mechanical game-show obstacle unexpectedly swings from the side and physically strikes her upper body.

The impact redirects her laterally away from the wall and causes her to lose her grip.

She is thrown outward from the end of the course.

The exact mechanics and body response should be naturally generated according to realistic momentum and gravity.

[Shot 7]

Continue the same physical event without changing location.

<Subject 1> falls from the end of the course into the competition water beside the final obstacle.

Keep the relationship between the final wall, the end of the runway, and the water visually coherent.

She hits the water with a convincing splash.

[Shot 8]

<Subject 1> resurfaces from the same pool with naturally wet hair.

She looks exhausted and briefly stunned, then reacts toward the broadcast camera with a cute, slightly aggrieved, comedic expression.

She softly says:

<Subject 1> (S1) says, <d>[Mandarin Chinese] 差一点嘛……</d>

End on her reaction.

### overall_soundscape

Authentic Chinese television sports-variety sound design: energetic audience reactions, Mandarin live commentary, footsteps, obstacle mechanics, physical impacts, heavy breathing, water impact, splash, and natural arena ambience.

Let the model determine the exact commentary wording, audience reactions, sound timing, and broadcast intensity according to the visible action.

### non_diegetic_music

Energetic Chinese sports-variety instrumental music with playful competition energy.

The music naturally builds through the challenge, intensifies during the final wall attempt, peaks around the apparent-success moment and sudden mechanical strike, then resolves into a light comedic ending after the water impact.
