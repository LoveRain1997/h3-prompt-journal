# 芙宁娜「帆板写真式音乐 MV」完整制作方案

## H3 三段生成 → 完整视频合成 → 提取完整音频 → Suno 重制配乐

下面这版按照**实际制作流程重新整理**，纠正前面两个关键点：

1. **第三段 H3 生成时不使用图3，纯文字控制运镜与高潮。**
2. **最终配乐不是分别处理每15秒音乐，而是先把完整视频的音频提取出来，再将完整音频交给 Suno 进行重新生成/重制，最后把正式配乐放回完整视频。**

---

# 一、项目整体结构

这次项目不是简单的「角色运动视频」，而是：

> **真人 COS 写真 + Windsurfing 帆板运动 + 电子音乐 + 体育摄影 + 音乐高潮**

最终希望形成一条完整的视觉能量曲线：

```text
人物定妆
↓
进入海面
↓
高速帆板
↓
运动强度提升
↓
更大的浪
↓
最终高潮
↓
巨浪冲浪
↓
帆板腾空
↓
Hero Shot
↓
落水
↓
写真式收尾
```

整体采用：

* **9:16 竖屏**
* 真人写实 COS
* 高质量体育摄影
* 长焦为主
* 近距离拍摄
* 少用远距离全景
* 保证人物占据较大的画面面积
* 让有限的视频像素集中在人物、服装、帆板和关键动作上

---

# 二、这次最重要的 H3 多图经验

## 1. 三张图不是简单“等权参考”

实际工作中，我们把三张图分别定义成：

```text
Picture 1
人物定妆 / 第一帧

Picture 2
人物三视图 + 帆板装备

Picture 3
当前段落的拍摄指导图
```

其中：

### Picture 1

负责：

* 人物身份
* 真人 COS 外貌
* 脸部
* 发型
* 服装
* 色彩
* 第一帧状态

---

### Picture 2

负责：

* 人物正面
* 侧面
* 背面
* 服装结构
* 鞋
* 帆板
* 帆
* 桅杆
* Boom
* 装备结构

必须明确告诉 H3：

> **Picture 2 不是分镜图。**

---

### Picture 3

负责：

* 摄影机位置
* 构图
* 长焦/近景关系
* 运镜方向
* 人物在画面中的位置
* 镜头距离
* 运动摄影语言

而实际经验是：

> **视觉拍摄指导图对运镜构图的约束非常强。**

因此不能只在文字里写：

> “摄影机低机位环绕……”

然后给 H3 一张完全不同构图的指导图。

图和文字应该尽量表达同一个摄影意图。

---

# 三、一个非常重要的例外：最终第三段

这次实际采用的最终方案是：

```text
Picture 1
+
Picture 2
+
纯文字
```

**没有 Picture 3。**

原因不是“上一段的图3会影响下一段”。

三个15秒片段本身是**独立生成**的，不存在跨段视觉记忆。

真正的原因是：

> **第三段需要完全由文字重新定义摄影机运动和高潮过程。**

如果第三段继续给一张具体的运镜指导图，那么这张图本身就会成为非常强的视觉构图约束。

而最终第三段我们希望文字精确控制：

```text
接近巨浪
↓
冲上浪壁
↓
起跳
↓
腾空
↓
音乐高潮
↓
Hero Shot
↓
落水
```

因此最终15秒采用：

```text
图1 = 人物
图2 = 三视图
文字 = 摄影 + 动作 + 节奏
```

这也是这次项目最有价值的实验结果之一。

---

# 四、音乐节奏设计

原始音乐分析得到：

**BPM ≈ 128**

**4/4**

整体属于：

> Chiptune / Synthpop / Electronic

核心律动：

* Four-on-the-floor
* Syncopation
* Kick
* Hi-hat
* Snare / Clap
* Synth Bass
* Lead Synth

视觉上最重要的节点：

```text
0–3s
Build-up

3s
Main Drop

3–10s
高能量段

6–7s
Mini-turnaround

9–10s
最强视觉高潮

10–12s
Release

12–15s
下一乐句
```

所以不能把15秒平均处理。

应该让：

> **音乐的重音决定动作，音乐的释放决定镜头缓和。**

---

# 五、第一段：高速帆板进入状态

## 使用方式

上传：

```text
Picture 1
人物定妆照

Picture 2
人物三视图 + 帆板装备

Picture 3
第一段拍摄指导图
```

第一段的任务：

> **让观众进入这个世界。**

不是一开始就把最大的浪拿出来。

视觉：

```text
海面
↓
人物
↓
帆板
↓
加速
↓
水花
↓
高速跟拍
```

---

## 第一段完整 H3 提示词

```text
H3 Ref2VA Prompt — Furina Windsurfing Fashion MV — Segment 1

REFERENCE ROLES:

<Picture 1> is the FIRST FRAME VISUAL ANCHOR.

Begin directly from the visual state shown in Picture 1.

Preserve the same adult realistic female cosplayer, facial identity, hairstyle, blue eyes, realistic skin, navy decorative crown, navy-and-white Fontaine-inspired costume, gold ornamental details, blue ribbons and translucent blue-white flowing fabric.

<Picture 2> is the CHARACTER AND WINDSURFING EQUIPMENT REFERENCE.

Use Picture 2 only to preserve the character construction, costume structure, footwear, windsurf board, mast, boom, transparent blue sail and rigging.

Do not treat Picture 2 as a storyboard.
Do not reproduce the turnaround-sheet layout.

<Picture 3> is the CINEMATOGRAPHY REFERENCE for this 15-second segment.

Use Picture 3 to guide the camera position, framing, lens language, camera movement, subject scale and general composition.

Do not literally reproduce graphic arrows from the guide image.

VIDEO:

Create a 15-second vertical 9:16 realistic cinematic fashion music video.

The visual style combines realistic professional windsurfing sports photography with elegant fashion editorial photography.

Use predominantly close and medium telephoto compositions.

Keep the character large and highly detailed in frame.

Avoid distant establishing shots.

The ocean should remain recognizable but secondary to the character.

MUSIC STRUCTURE:

Approximately 128 BPM.
4/4 electronic chiptune / synthpop.

0–3 seconds:
BUILD-UP.

3–10 seconds:
MAIN DROP.

6–7 seconds:
MINI-TURNAROUND.

10–12 seconds:
RELEASE.

12–15 seconds:
TRANSITION.

TIMELINE:

0–1s:

Begin directly from Picture 1.

Maintain the character's appearance and visual identity.

<Subject 1> is already windsurfing naturally.

The board moves smoothly across the ocean.

Hair, ribbons and translucent fabric react naturally to the wind.

Use a close telephoto composition.

1–2s:

The camera begins tracking alongside her.

The board accelerates slightly.

Use natural water movement and subtle spray.

Keep her face clearly visible.

2–3s:

The musical build-up increases.

Lower the camera slightly toward water level.

Increase tracking speed.

Water spray becomes more visible.

Prepare for the drop.

3s — MAIN DROP:

Immediately increase camera energy.

Use a fast close telephoto tracking shot.

<Subject 1> accelerates across the water.

The board cuts through the surface.

White spray enters the foreground.

The transparent blue sail forms a strong diagonal.

3–5s:

Maintain high-speed side tracking.

Keep the subject large in frame.

The camera moves smoothly parallel to the board.

Her body remains naturally balanced against the wind.

Hair and fabric react realistically.

5–6s:

Shift gradually toward a three-quarter frontal telephoto view.

The camera moves backward while the subject advances.

Keep her face and costume highly detailed.

6–7s — MINI-TURNAROUND:

Use the musical turnaround as a subtle camera-direction change.

Briefly reduce forward camera movement.

Then smoothly transition from side-front tracking to side-rear tracking.

Maintain continuity of motion.

7–9s:

Return to strong forward motion.

Use low water-level telephoto tracking.

Increase water spray.

The sail and body create strong diagonal lines.

The character remains the visual focus.

9–10s:

Reach the strongest visual energy of this segment.

Use a controlled close curved tracking movement consistent with Picture 3.

Do not pull far away.

Keep the character large.

10–12s:

Music releases.

Reduce camera movement.

Transition into a stable close telephoto fashion shot.

<Subject 1> continues windsurfing naturally.

12–15s:

The next phrase begins.

Resume smooth side tracking.

The character continues moving forward.

Do not introduce the final giant wave yet.

End with clear forward motion leading naturally into Segment 2.

PHYSICAL REALISM:

Maintain believable windsurfing mechanics.

Hands remain correctly connected to the boom.

Feet remain plausibly positioned on the board.

The sail reacts naturally to wind.

The board remains physically connected to the character.

No distorted hands.
No distorted feet.
No detached sail.
No malformed mast.
No floating board.
No impossible body positions.
```

---

# 六、第二段：大型浪区出现

## 使用方式

重新独立生成。

上传：

```text
Picture 1
同一张人物定妆照

Picture 2
同一张人物三视图 + 帆板装备

Picture 3
第二段专用拍摄指导图
```

第二段的任务不是高潮。

而是：

> **让观众意识到：前面只是开始。**

视觉变化：

```text
普通海浪
↓
更强风
↓
更高速
↓
更大水花
↓
大型涌浪
↓
陡峭浪壁
↓
为最终高潮准备
```

---

## 第二段完整 H3 提示词

```text
H3 Ref2VA Prompt — Furina Windsurfing Fashion MV — Segment 2

REFERENCE ROLES:

<Picture 1> is the FIRST FRAME VISUAL ANCHOR.

Begin from the visual state established by Picture 1.

Preserve the same adult realistic female cosplayer, facial identity, hairstyle, blue eyes, navy decorative crown, navy-and-white costume, gold details, blue ribbons and translucent blue-white fabric.

<Picture 2> is the CHARACTER AND WINDSURFING EQUIPMENT REFERENCE.

Use Picture 2 only to preserve character construction, costume structure, footwear, windsurf board, mast, boom, transparent blue sail and rigging.

Do not treat Picture 2 as a storyboard.

<Picture 3> is the CINEMATOGRAPHY REFERENCE for this segment.

Use Picture 3 to guide camera position, framing, camera movement, lens language and general composition.

Do not literally reproduce graphic arrows.

VIDEO:

Create a 15-second vertical 9:16 realistic cinematic fashion music video.

Continue directly from the visual energy of Segment 1.

This segment must be visibly more intense than Segment 1.

The purpose is to transition from high-speed windsurfing into a much larger wave environment.

Do not perform the final aerial jump yet.

The largest wave should become clearly visible toward the second half.

MUSIC:

Approximately 128 BPM.
4/4 electronic chiptune / synthpop.

0–3s:
BUILD-UP.

3–10s:
MAIN DROP.

6–7s:
MINI-TURNAROUND.

10–12s:
RELEASE.

12–15s:
TRANSITION.

TIMELINE:

0–1s:

Continue naturally.

Use a close three-quarter telephoto composition.

<Subject 1> continues windsurfing at high speed.

1–2s:

Increase wind intensity.

The ocean becomes more active.

The board accelerates.

Use stronger water spray.

2–3s:

The camera lowers toward the water.

Reveal larger swells in the distance.

Build anticipation for the drop.

3s — MAIN DROP:

Cut into a stronger low water-level tracking shot.

<Subject 1> accelerates through larger ocean swell.

Water spray becomes significantly larger.

Keep the subject large in frame.

3–5s:

Use energetic telephoto tracking.

Large rolling swells move through the background.

The character remains clearly readable.

5–6s:

Shift toward a frontal three-quarter tracking angle.

The camera retreats as the character advances.

A much larger swell is visible ahead.

6–7s — MINI-TURNAROUND:

Use the musical turnaround for a brief change in camera direction.

A large burst of spray crosses the foreground.

Momentarily obscure part of the subject.

Then reveal her again.

The larger wave is now becoming the main environmental feature.

7–8s:

Return to high-speed tracking.

The subject moves toward the large wave.

The camera remains relatively close.

8–9s:

Lower the camera.

The wave face rises dramatically.

The board approaches the base of the swell.

The character naturally adjusts body weight and sail angle.

9–10s:

Reach the strongest visual energy of this segment.

The large wave occupies a major portion of the background.

The subject approaches it at high speed.

Do not jump yet.

10–12s:

Music releases.

Slow the camera slightly.

Show the character continuing toward the large wave.

The scale of the ocean should clearly exceed Segment 1.

12–15s:

The next phrase begins.

Follow the character toward the wave.

The wave face becomes steep and clearly surfable.

The character lowers her center of gravity.

She prepares to ride up the wave.

End immediately before the final aerial action.

PHYSICAL REALISM:

The wave must be large but physically surfable.

It must not look like a tsunami.

Maintain realistic windsurfing mechanics.

Hands remain correctly positioned on the boom.

Feet remain connected to the board.

The sail reacts naturally to wind.

The board remains physically connected.

No impossible acrobatics.
```

---

# 七、第三段：最终英雄时刻

这是整支 MV 最重要的15秒。

## 使用方式

这里是这次实际方案最关键的区别：

### 只上传：

```text
Picture 1
人物定妆照

Picture 2
人物三视图 + 帆板装备
```

### 不上传 Picture 3。

这一段完全由文字控制：

```text
巨浪
↓
冲浪
↓
上浪壁
↓
起跳
↓
腾空
↓
Hero Shot
↓
落水
↓
写真式结束
```

因为第三段的重点不是继续使用之前的拍摄模板，而是让 H3 根据文字完成一套完整的高潮摄影逻辑。

---

## 第三段完整 H3 提示词

```text
H3 Ref2VA Prompt — Furina Windsurfing Fashion MV — Segment 3 FINAL HERO MOMENT

REFERENCE ROLES:

<Picture 1> is the FIRST FRAME VISUAL ANCHOR.

Begin directly from the visual state established by Picture 1.

Preserve the same adult realistic female cosplayer, facial identity, hairstyle, blue eyes, realistic skin, navy decorative crown, navy-and-white Fontaine-inspired costume, gold ornamental details, blue ribbons and translucent blue-white flowing fabric.

<Picture 2> is the CHARACTER AND WINDSURFING EQUIPMENT REFERENCE.

Use Picture 2 only to preserve character construction, costume structure, footwear, windsurf board, mast, boom, transparent blue sail and rigging.

Do not treat Picture 2 as a storyboard.
Do not reproduce the turnaround-sheet layout.

IMPORTANT:

There is NO cinematography reference image for this segment.

All camera movement, framing, lens language, composition, action timing and cinematic progression are controlled by the text below.

VIDEO:

Create a 15-second vertical 9:16 realistic cinematic fashion music video.

This is the FINAL HERO MOMENT.

The visual intensity must be substantially higher than the previous two segments.

Progress naturally from:

large wave
→
high-speed wave riding
→
climbing the steep wave face
→
controlled windsurfing aerial jump
→
board completely leaving the water
→
hero composition
→
musical peak
→
natural landing
→
elegant fashion ending.

This is WINDSURFING.

Do not turn it into conventional surfing.

Do not perform a backflip.

Do not perform a complicated aerial rotation.

Do not spin the character.

The hero action is a clean and controlled windsurfing wave jump.

MUSIC:

Approximately 128 BPM.
4/4 electronic chiptune / synthpop.

0–3 seconds:
BUILD-UP.

3–10 seconds:
MAIN DROP.

6–7 seconds:
MINI-TURNAROUND.

9–10 seconds:
ABSOLUTE VISUAL PEAK.

10–12 seconds:
RELEASE.

12–15 seconds:
NEW PHRASE.

TIMELINE:

0–1s:

Begin directly from Picture 1.

<Subject 1> is approaching the large wave.

Use a close telephoto composition.

The large wave is already visible.

Camera movement is controlled.

1–2s:

Move closer.

The wave face becomes larger.

<Subject 1> accelerates.

She naturally lowers her center of gravity.

Her hands remain correctly positioned on the boom.

2–3s:

The musical fill begins.

Move toward a low water-level camera position.

Reveal the steep wave face and breaking crest.

Increase visual anticipation.

The board begins climbing toward the wave.

3s — MAIN DROP:

<Subject 1> enters the large wave.

The windsurf board accelerates diagonally up the steep wave face.

Large white water spray erupts.

The camera tracks close to the subject.

The transparent blue sail creates a strong diagonal line.

3–4s:

Continue climbing the wave face.

The wave is substantially larger than all previous waves.

Keep the character large in frame.

Keep the face readable.

4–5s:

<Subject 1> approaches the wave lip.

The sail catches the wind strongly.

Hair, ribbons and translucent fabric stream backward.

The camera rises slightly.

5–6s:

The board approaches the crest.

The wave breaks into large white foam.

Frame the character, board, sail and wave crest together.

6–7s — MINI-TURNAROUND:

Use the musical turnaround as a moment of anticipation.

A large burst of spray crosses the foreground.

The subject is briefly partially obscured.

Reveal her again directly at the wave crest.

The board begins to lift.

Do not perform the full jump yet.

7–8s — TAKEOFF:

The music returns strongly.

<Subject 1> drives the windsurf board over the wave crest.

The board completely leaves the water.

The camera rises with her.

Large water spray explodes underneath.

The sail catches the wind.

Hair and translucent fabric move dramatically.

8–9s — AIRBORNE:

The windsurf board is completely airborne.

<Subject 1> is suspended above the breaking wave.

The transparent blue sail is fully visible.

The character, sail and board form a powerful diagonal composition.

The wave breaks below.

Keep the camera close enough to preserve facial detail.

Do not rotate the character.

Do not flip.

Do not deform the board or sail.

9–10s — ABSOLUTE HERO SHOT:

At the strongest musical accent:

STOP the aggressive camera movement.

Stabilize into a powerful low-angle telephoto hero composition.

Present the moment like an iconic professional extreme-sports fashion photograph.

<Subject 1> is fully airborne above the breaking wave.

The board is clearly separated from the water.

The transparent blue sail is fully extended.

Her white-blue hair streams dramatically in the wind.

Her navy-and-white costume and translucent fabric remain clearly visible.

A huge burst of white spray explodes beneath her.

The curling wave forms a dramatic background.

The character, sail and board create one clean diagonal composition.

The character remains the dominant subject.

Hold this hero image long enough to read clearly.

Do not make the character small.

Do not pull far away.

Do not use excessive motion blur.

10–11s:

Begin the release.

The board begins descending naturally.

The camera remains relatively stable.

11–12s:

The board reconnects with the water.

A large realistic burst of spray erupts.

The camera gently moves closer.

<Subject 1> continues riding forward.

12–13s:

The music enters the next phrase.

Transition into a close telephoto fashion portrait.

The giant wave breaks behind her.

The extreme action has ended.

13–14s:

Track gently alongside her.

Hair, ribbons and translucent fabric continue reacting to the wind.

The visual energy becomes elegant again.

14–15s:

End on a close three-quarter hero portrait.

Keep <Subject 1> large in the vertical frame.

The blue sail remains visible behind her.

A distant swell suggests continuation.

Do not introduce another major action.

End with the feeling that the heroic moment has just been completed.

PHYSICAL REALISM:

Maintain realistic windsurfing mechanics.

Hands remain correctly connected to the boom.

Feet remain plausibly positioned on the board.

The sail reacts naturally to wind.

The board remains physically connected to the subject.

The wave is large but physically surfable.

The aerial action is a controlled windsurfing wave jump.

No backflip.
No complicated rotation.
No spinning character.
No detached board.
No detached sail.
No distorted mast.
No malformed hands.
No malformed feet.
No tsunami.
No impossible vertical water wall.

FINAL VISUAL INTENT:

The final musical peak must create one unforgettable image:

An adult realistic Furina cosplayer launches from the crest of a powerful ocean wave while windsurfing.

She and the windsurf board are completely airborne.

Her transparent blue sail is fully extended against the sky.

Her white-blue hair and translucent fabric stream dramatically in the wind.

A massive explosion of white spray and curling ocean foam fills the area beneath her.

At the musical peak, the camera stops its aggressive movement and presents the moment as a powerful low-angle telephoto extreme-sports fashion photograph.

This is the signature final image of the entire music-video sequence.
```

---

# 八、三段最终使用表

| 段落      | Picture 1 | Picture 2 | Picture 3 | 运镜控制    |
| ------- | --------- | --------- | --------- | ------- |
| **第一段** | 人物定妆      | 三视图+帆板    | 第一段指导图    | 图3 + 文字 |
| **第二段** | 人物定妆      | 三视图+帆板    | 第二段指导图    | 图3 + 文字 |
| **第三段** | 人物定妆      | 三视图+帆板    | **无**     | **纯文字** |

三个片段都是**独立生成**。

---

# 九、为什么第三段要纯文字

这里不是因为“之前的图会影响下一段”。

而是因为第三段需要的是：

> **从摄影语言层面彻底升级。**

前两段的拍摄核心是：

```text
人物
+
高速运动
+
长焦
+
近距离跟拍
```

第三段则是：

```text
巨浪
+
上浪壁
+
起跳
+
腾空
+
低机位
+
英雄构图
+
稳定定格
```

所以第三段不再需要一张拍摄指导图去约束摄影机，而是让 H3 根据完整文字时间轴自行完成。

---

# 十、三个15秒片段生成之后

生成完成后：

```text
Segment 1
       ↓
Segment 2
       ↓
Segment 3
       ↓
完整视频
```

先把三个片段按照音乐节奏剪成**完整的视频版本**。

这里不要先急着分别处理音乐。

---

# 十一、真正的配乐制作流程

你这次实际采用的是：

> **先完成完整视频，再提取完整视频的音频，然后交给 Suno 重新生成正式配乐。**

完整流程应该写成：

```text
H3
↓
生成第一段
↓
生成第二段
↓
生成第三段
↓
剪辑成完整视频
↓
提取完整视频中的原始音频
↓
将“完整音频”作为 Suno 的参考
↓
Suno 重新生成完整配乐
↓
得到正式音乐
↓
将正式音乐替换回完整视频
↓
最终调节音画同步
```

**不是：**

```text
15秒音乐
↓
Suno

15秒音乐
↓
Suno

15秒音乐
↓
Suno
```

而是：

```text
完整视频
↓
完整音频
↓
Suno
↓
完整正式配乐
```

这样最大的优势是：

### Suno面对的是完整的音乐结构

它可以理解：

```text
Build-up
↓
Drop
↓
中段发展
↓
第二次发展
↓
最终高潮
↓
结尾
```

而不是把三个15秒音乐段落分别当成互相独立的音乐。

---

# 十二、最终音乐与视频的关系

最终应该让音乐重新对应已经完成的视频：

```text
音乐
          视频

Build-up → 人物进入海面

Drop     → 高速帆板

发展     → 更大浪

高潮准备 → 冲向浪峰

Peak     → 帆板腾空

Hero     → 空中英雄定格

Release  → 落水

尾奏     → 写真式收尾
```

尤其最终高潮：

```text
音乐最强重音
        ↓
芙宁娜腾空
        ↓
帆完全展开
        ↓
帆板脱离水面
        ↓
巨大浪花
        ↓
摄影机停止激烈运动
        ↓
Hero Shot
```

这就是整支 MV 最重要的**音乐—动作—摄影三者同步点**。

---

# 十三、最终完整工作流

最后把这套经验压缩成一张流程图：

```text
                 芙宁娜真人 COS
                       │
                       ↓
              ┌─────────────────┐
              │ Picture 1       │
              │ 人物定妆 / 第一帧 │
              └────────┬────────┘
                       │
                       ↓
              ┌─────────────────┐
              │ Picture 2       │
              │ 三视图 + 帆板装备 │
              └────────┬────────┘
                       │
          ┌────────────┼────────────┐
          ↓            ↓            ↓
       第一段         第二段        第三段
          │            │            │
       图3①           图3②       无图3
          │            │            │
       高速运动       大浪逼近      纯文字高潮
          │            │            │
          └────────────┼────────────┘
                       ↓
                  完整视频
                       │
                       ↓
               提取完整视频音频
                       │
                       ↓
                  Suno 重制
                       │
                       ↓
                 完整正式配乐
                       │
                       ↓
                  最终音画剪辑
                       │
                       ↓
               9:16 帆板写真 MV
```

---

# 十四、这次项目最值得保留的经验

最终可以沉淀成四条规则：

### ① 人物参考和摄影参考分开

```text
图1
人物是谁

图2
人物和装备是什么

图3
这一段怎么拍
```

---

### ② 图3必须服务于当前段落

第一段图3：

> 高速运动。

第二段图3：

> 强化运动 + 大浪。

第三段：

> **不使用图3，纯文字控制最终高潮。**

---

### ③ 音乐不是单纯背景

音乐直接决定：

```text
什么时候加速
什么时候切镜头
什么时候转向
什么时候起跳
什么时候定格
什么时候释放
```

尤其：

> **9–10秒的最终 Hero Shot 必须与音乐最强视觉重音对应。**

---

### ④ H3负责视觉，Suno负责最终完整音乐

```text
H3
负责视频运动与临时音乐节奏参考

↓

完整视频

↓

提取完整音频

↓

Suno
负责完整正式配乐重制

↓

最终剪辑
```

这样这套流程就不再只是一次性的“芙宁娜帆板视频”，而是一套可以继续复用于**冲浪、滑雪、滑板、赛车、摩托、水上运动等“角色写真 + 体育运动 + 音乐 MV”项目**的制作方法。
