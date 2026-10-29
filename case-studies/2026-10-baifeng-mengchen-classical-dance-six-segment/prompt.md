# 《白凤蒙尘》可直接套用的提示词模板 + 六段完整提示词

> 输入只有 `<Picture 1>`（人物身份、脸、发型、发饰、服装、比例、色彩、光线、完整环境的唯一视觉权威）和当前段裁剪音频 `<Audio 1>`。9:16 竖屏真人古风舞蹈 MV，舞者全程无声表演（不唱歌、不说话、不做口型、无字幕）。六段总时长 **79.882 秒**，105.25 BPM。

## 音乐时间网格

| 项 | 值 |
|---|---|
| 全曲总长 | 79.882 s |
| BPM | 105.25 |
| 单拍 beat | 0.5701 s |
| 半拍 half-beat | 0.285 s |
| 单小节 bar | 2.2803 s |
| 乐句 phrase | 4.5606 s |

## 六段总览（全曲窗口 / 段内时长 / 动作机制）

| 段 | 全曲窗口 | 段内时长 | 主动作机制 |
|---|---|---:|---|
| SEG01 白凤凌霜 | 00:00.000–13.166 | 13.166 s | 穿掌背转前 → 背身腰圈扫弧 → 半脚尖平衡 → 遮面露眼 → 碎步后踢 |
| SEG02 暗网坠谷 | 13.166–26.958 | 13.792 s | 拧倾出胯 → 圆场碎步 → 低位扫弧腰圈 → 沉跪即起（转失败被截） |
| SEG03-A 仙姿蒙尘·进入 | 26.958–33.916 | 6.958 s | 交叠前臂螺旋下沉 → 掌心承重低位跪坐 → 甩发露眼 → 坐姿扭转 |
| SEG03-B 仙姿蒙尘·恢复 | 33.916–39.413 | 5.497 s | 撑脚起身 → 紧凑半转 → 交叉脚落地制动 → 半跪起身受阻 |
| SEG04 强撑仙姿 | 39.413–52.166 | 12.753 s | 横向八字臂线 → 半转甩发 → 半脚尖平衡 → 拧倾出胯（仪态重建） |
| SEG05 被迫校正 | 52.166–65.750 | 13.584 s | 跪位撩臂起身 → 沉跪即起 → 关节链反向截断 → 起到一半被打断 |
| SEG06 傲骨未折 | 65.750–79.882 | 14.132 s | 呼吸提沉 → 背身双臂渐升 → 立圆胸腰展开 → 空手致意 → 冷静终止 |

---

# 0. 通用可套用模板（H3 古风舞蹈 self-contained 骨架）

> 把 `<...>` 占位替换为本段内容即可。SEG02 起的每一段都要在开头写 `CONTINUITY IN`（承接上一段结尾的同一局部特写），不重新摆回图 1 静态姿势。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman shown in <Picture 1>. <Picture 1> is the sole authority for her identity, face, hair, existing hair ornaments, costume, proportions, palette, lighting, and complete environment. She is the only dancer. Keep the supplied scene and clothing unchanged; no damage, extra prop, captor, or second person appears.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, exactly <DURATION> seconds long, using only <Picture 1> and this cut of <Audio 1>. [CONTINUITY IN: open on the exact <HAND/EYE/FOOT detail> that ended the previous segment, at the same frame position, focal distance, and direction of movement; continue it before widening.] Begin <this segment's unique texture: which body levels, support points, rotation axes, and movement quality change>. The low/standing work has clear support points and controlled weight transfer; it is not random motion. The soundtrack retains its original voice, but Song Yu does not speak, sing, or synchronize mouth movement. No text appears on screen.

Continuous layer: <one support point is always loaded before the next body part moves; the spine unfolds in sections; the head and hair arrive after the torso; costume follows gravity and momentum>.

[Shot 1 | <start–end> | <framing, e.g. front three-quarter, camera lowers with body>]
<beat range>: <force source → path → peak → result; name the supporting hand/foot and the order of wrist/elbow/shoulder/ribs>.
...

overall_soundscape:
<Audio 1> is the only soundtrack, with original voice and instruments unchanged. No speech, singing, mouth-sync, visible text, or generated sound effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. Main local anchors: <list>. Follow the waveform if it differs from the estimates.
```

> 纪律：① 每段独立生成、时间从 00:00 起算，段头标注全曲窗口；② 段内 `[Shot N]` 是动作章节，切点必须有动作/遮挡/焦点理由；③ 局部特写约 0.25–0.55 s，提供新信息并回到舞蹈；④ 全片最多一次完整旋转，其余用半转/轴线扭转/急停；⑤ 低机位不是裙底视角，窥视感靠遮挡、视差、距离与焦点。

---

# SEG01｜白凤凌霜｜13.166 s（全曲 00:00–13.166）

动作机制：C16 穿掌·背转前 → C17 背身腰圈扫弧（空手版）→ C12 半脚尖平衡 → C4 遮面露眼 → C18 碎步后踢行进。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman shown in <Picture 1>. <Picture 1> is the sole authority for her identity, face, hairstyle, existing hair ornaments, costume, proportions, palette, lighting, and complete environment. She is the only dancer. All visual details come directly from the picture. No new character or prop appears; the camera remains outside the image.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, exactly 13.166 seconds long, using only <Picture 1> and this cut of <Audio 1>. Begin from the exact visible state of <Picture 1>, but make motion already alive on the first frame: continue the existing weight, wrist tension, or torso direction rather than resetting into a new pose. Song Yu moves with the assured precision of a highly trained peak master. Keep the mouth naturally relaxed and silent; the original vocal is only part of the soundtrack. Do not generate speech, singing, mouth-sync, or on-screen text.

Continuous layer: breath-led rise and sink passes from ankles through knees, pelvis, ribs, and head. The supporting foot is always clear. The head and fingertips finish slightly after the torso. Her hair and clothing follow the body's momentum with natural delay. Use varied body planes, traveling footwork, and one short balance, not repeated arm circles.

[Shot 1 | 0.000–1.625s | medium-full, front three-quarter]
0.000–0.570s: press through the ball and outer edge of the supporting foot; the free toe draws a short diagonal hook across the floor.
0.570–1.140s: let the pelvis follow the hook while the sternum counter-rotates the other way; the rear heel swivels and the knees absorb the torque. Inside this interval, insert a 0.285-second close-up of the supporting heel and hooked toe pressing and releasing against the floor; follow the toe's diagonal path, then match-cut back to the waist as the pelvis starts its counter-rotation. The close-up reveals the source of the turn rather than interrupting it.
1.140–1.625s: the leading hand unfurls finger by finger, wrist turns inward, elbow cuts a short diagonal toward the opposite side of the chest. The camera slides laterally in the same direction as the toe hook and keeps both feet visible.

[Shot 2 | 1.625–3.916s | traveling front-to-side track]
1.625–2.195s: cross the left foot behind the right and pass the right palm across the face-line without touching it.
2.195–2.765s: thread that palm under the opposite elbow; rotate the wrist over and let the fingers complete the path last.
2.765–3.335s: the left foot covers across the centerline, the rear heel pivots, and the pelvis begins a back-to-front turn while the ribs remain counter-facing.
3.335–3.916s: the head spots the front direction, both forearms cross briefly at the sternum, then sink and separate into unequal high-low diagonals. Let the crossing forearm fill the frame for a fraction of a second; use that moving sleeve edge as a motivated wipe into the next rear three-quarter view, preserving the same direction of torso rotation. The camera tracks with the foot crossing and reveals the next composition only after the crossed line resolves.

[Shot 3 | 3.916–6.208s | medium-full, side/rear three-quarter]
3.916–4.486s: flick both elbows outward and rotate the shoulders away from the lens; take one compact cross-behind step.
4.486–5.056s: the pelvis draws a right-to-down-to-left waist circle as the chest holds a small counter-twist.
5.056–5.626s: one empty hand sweeps in a long shallow arc just above the floor; the other arm crosses the ribs and opens above shoulder level, creating two different planes.
5.626–6.208s: the rear heel swivels, the torso spirals back toward front, and the trailing hand continues a fraction after the chest arrives. A short whip-pan follows the shoulder turn, then resolves on the low hand arc; camera and dancer turn together rather than orbiting separately.

[Shot 4 | 6.208–8.500s | chest-height camera, stable for the balance]
6.208–6.778s: press through the supporting ankle and rise onto demi-pointe; draw the free knee upward into a compact front attitude.
6.778–7.348s: cross the forearms above the crown, keeping the elbows curved and the neck long.
7.348–7.918s: hold the balance for one clear beat; only the gaze and fingertips continue moving.
7.918–8.500s: separate the arms sharply into one high diagonal and one low diagonal, lower the free foot toe-first, and transfer weight sideways before the heel touches. The camera stays planted during the balance and resumes motion on the landing, so the accent reads cleanly.

[Shot 5 | 8.500–10.833s | intrusive shoulder-side view]
8.500–9.070s: pass the right hand in front of the eyes, briefly veiling one side of the face; the other hand curves behind the head.
9.070–9.640s: hold the veil for one beat while weight remains over the back leg and the front toe points diagonally behind.
9.640–10.210s: peel the hand outward to reveal the eyes; begin on a tight eye-and-fingertip close-up, rack focus from the fingertips to her eyes as the hand clears the face, then widen just enough to catch the head turning first and the shoulders and pelvis following into a quarter-turn.
10.210–10.833s: finish with a small toe pivot and an offset arm line. The camera peers from just behind the near shoulder, a thin edge of existing sleeve naturally occluding one frame edge; push closer as the eyes appear, then slide with the turn.

[Shot 6 | 10.833–13.166s | low side tracking view, full body readable]
10.833–11.403s: take a light traveling step diagonally away, the back foot flicking up behind after push-off.
11.403–11.973s: cross the next step and flick the opposite lower leg backward, arms expanding into an asymmetric wing shape.
11.973–12.543s: step through and pivot the supporting heel, allowing hair and costume to sweep through their own delayed arc.
12.543–12.880s: let the far arm trail behind the waist while the high arm continues upward; take one more traveling cross-step and pivot the supporting heel, keeping the body in rear three-quarter motion.
12.880–13.166s: move into a tight close-up of the raised wrist and softly curled fingertips while the arm continues the same upward-forward curve. End on the wrist at the upper-right edge of the frame, fingers angled diagonally down and inward, with the shoulder and torso movement still implied behind it. This is the exact visual bridge into SEG02; do not finish on a full-body pose or stop the hand.

Micro-expression layer: calm discernment; a single brief glance into the lens during the eye reveal, then gaze follows the traveling hand. The mouth remains relaxed and silent.

overall_soundscape:
<Audio 1> is the complete original soundtrack, including the recorded voice and instruments. No additional speech, singing, lip-sync, on-screen text, or generated sound effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. Main local movement anchors: 1.625s, 3.916s, 6.208s, 8.500s, 10.833s. Follow the waveform if it differs from the estimates.
```

---

# SEG02｜暗网坠谷｜13.792 s（全曲 13.166–26.958）

动作机制：C5 拧倾出胯 → C6 圆场碎步 → C19 低位扫弧与腰圈 → C20 沉跪即起。压迫感来自舞步第一次被截断，身体重心与上身转向失去同步。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman shown in <Picture 1>. <Picture 1> alone controls identity, face, hair, existing hair ornaments, outfit, proportions, palette, lighting, and the full environment. Keep the source world unchanged. She is the only dancer. No captor, second person, new prop, visible restraint, or replacement environment appears.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, exactly 13.792 seconds long, from <Picture 1> and this cut of <Audio 1>. <Picture 1> locks appearance and the original scene; it does not reset the choreography to its still pose. CONTINUITY IN: open on the exact tight close-up that ended SEG01: the same raised wrist in the upper-right frame area, fingers angled diagonally down and inward, with the same rear three-quarter movement direction. At 0.000s the wrist continues its existing curve downward and across; the camera follows the hand for a fraction, then pulls back to reveal the body continuing the traveling cross-step. Do not start a new pose. The first half shows her trained command through asymmetric torso lines and traveling footwork. Then a turn fails to finish, forcing her to catch her balance and redirect the movement. This is an intentional dance phrase with changing dynamics, never random stumbling. The performer remains silent; preserve the original recorded vocal only in the soundtrack, with relaxed lips and no mouth-sync or on-screen text.

Continuous layer: breath still powers the rise and sink, but after the interruption, recoveries become shorter. Every loss of balance has a visible cause in the foot, pelvis, or shoulder chain.

[Shot 1 | 0.000–2.250s | hand close-up pulling back to medium-full front-side]
0.000–0.285s: continue the identical raised-wrist close-up from SEG01. The wrist carries its downward-forward curve; the fingers finish curling inward after the wrist has begun to turn.
0.285–0.516s: the camera tracks down the forearm and pulls back as the rear heel presses into the floor and the front toe draws inward, revealing the pelvis beginning its twist. This single movement unites the detail shot and the body action.
0.516–1.086s: push the hip to one side while keeping the sternum angled toward the lens, producing a clear opposing waist line.
1.086–1.656s: the upper hand cuts diagonally above the shoulder while the lower hand closes near the waist; the head follows the high hand last.
1.656–2.250s: release the hip line through a short heel-toe switch and travel one step sideways. Use a 0.285-second foot insert on the heel-toe switch, then tilt and track upward along the same diagonal into the hip and hand line. The camera moves parallel to the footwork, starting on the release rather than the accent peak.

[Shot 2 | 2.250–4.584s | lateral tracking, medium-full]
2.250–2.796s: take two tiny gliding steps across the frame, keeping the upper torso level and quiet.
2.796–3.366s: add a quick cross-behind step; the leading shoulder advances as the opposite hip retreats.
3.366–3.936s: the arms travel at different depths: one forearm sweeps behind the waist, the other crosses the chest and turns palm-out.
3.936–4.584s: reverse the direction with a heel swivel and a short diagonal toe placement, so the feet redraw the path instead of walking straight. The camera tracks at the dancer's pace, then briefly overtakes her shoulder line and corrects to center, creating a subtle sense of pursuit.

[Shot 3 | 4.584–6.917s | waist-height to knee-height observer view]
4.584–5.076s: she begins a clean pivot from a planted heel; the pelvis commits to the turn.
5.076–5.646s: the ribs continue rotating a fraction too far while the head spots late, splitting the body into two directions.
5.646–6.216s: the front foot catches with a sharp toe tap; one arm extends outward to counterbalance and the wrist folds before the elbow finishes extending.
6.216–6.917s: the extended arm recoils toward the chest while the rear foot slides behind to rescue balance. Insert a brief close-up of the catching toe skidding a few centimeters, then tilt up along the leg as the arm recoils; finish from a low side position at about knee height, around 1.2m away. A natural sleeve edge crosses the near foreground at the end and motivates the cut into the lunge, while the support foot remains readable.

[Shot 4 | 6.917–9.167s | main Hitchcock dolly zoom]
6.917–7.357s: the failed pivot drops into a deep diagonal lunge, one knee bending while the other leg lengthens outward; the torso tips beyond the support base.
7.357–7.927s: an open palm reaches forward as the rear foot searches for the floor. Begin a real Dolly Zoom: physically track the camera backward while zooming in, holding her apparent upper-body size nearly constant as the unchanged background perspective stretches away.
7.927–8.497s: the rear foot finally catches and the shoulders jerk to a stop; let the arm and hair continue for a small, believable fraction after the feet stabilize. During the catch, briefly rack focus from the reaching palm in the foreground to the tense eyes behind it; keep the real Dolly Zoom active in the background, with no separate digital warp.
8.497–9.167s: the palm turns inward and draws back to the sternum, knees absorb the recoil. End the optical distortion exactly on this catch; no digital background warping.

[Shot 5 | 9.167–11.500s | low lateral track]
9.167–9.637s: keep the same low level and shift weight from the bent front foot toward the rear foot.
9.637–10.207s: draw a right-to-left waist circle; one hand sweeps a broad shallow arc above the floor while the other arm cuts high behind the shoulder.
10.207–10.777s: the chest counter-rotates against the pelvis and the front knee begins to extend, but the rise is checked halfway.
10.777–11.500s: slide the front toe inward, close the low hand to the ribs, and redirect the torso into a side-facing angle. Start tight on the hand being forced back toward the ribs; rack focus from knuckles to eyes only after the reach has been curtailed, then slide laterally until the shoulder briefly occludes the lens and reveals the next kneeling-to-rising composition.

[Shot 6 | 11.500–13.792s | low kneeling-to-rising view]
11.500–11.917s: press through the planted foot and shin to lift the torso toward a tall kneel.
11.917–12.487s: the upper arm rises in a wide arc while the lower arm remains close to the waist; shoulders open in sequence.
12.487–13.057s: before the upper arc can complete, both forearms cross at the chest and the elbows drop unevenly.
13.057–13.342s: the pelvis twists toward front while the feet remain in a narrow base; the shoulders continue a fraction after the legs stop.
13.342–13.792s: the crossed forearms rise into a tight close-up at sternum height; the near wrist lies diagonally over the far forearm, both hands tense but controlled. End on the overlapping wrist line while the torso remains in the low kneeling twist. This exact crossed-forearm image is the bridge into SEG03; the hands must not reset or uncross before the cut.

Micro-expression layer: a quick look follows the missed pivot; after the catch, she looks toward the camera with restrained alarm and a jaw that remains relaxed. No mouth motion follows the voice.

overall_soundscape:
<Audio 1> supplies the complete unmodified soundtrack. The performer is silent; no additional dialogue, singing, lip-sync, on-screen text, or generated effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. Main local anchors: 2.250s, 4.584s, 6.917s, 9.167s, 11.500s. The primary Hitchcock dolly zoom is limited to 6.917–9.167s.
```

---

# SEG03-A｜仙姿蒙尘·低位进入与视觉揭示｜6.958 s（全曲 26.958–33.916）

> 双提示词之 **A**。喂 `<Picture 1>` + 全曲 26.958–33.916 音频。强调身体从站姿进入地面的完整路径，建立局部特写、头发遮挡与镜头揭示；结尾停在 hand-led wipe（手扫向镜头完全遮挡），作为与 B 段的剪辑接缝。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman shown in <Picture 1>. The picture is the sole authority for identity, face, hair, existing ornaments, costume, proportions, palette, lighting, and complete environment. She is the only dancer. Keep the supplied scene and clothing unchanged; no damage, extra prop, captor, or second person appears.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, 6.958 seconds long (the first half of a 12.455-second floor-level segment), using only <Picture 1> and this cut of <Audio 1>. <Picture 1> locks identity and the existing visual world; it does not reset the pose. CONTINUITY IN: open on the same tight close-up of the crossed forearms at sternum height that ended SEG02, with the near wrist diagonal over the far forearm. At 0.000s the fingers release first, the wrists uncross in the same plane, and the camera widens as the elbows separate; this continuing release leads directly into the floor-level descent. No new opening pose. This half's texture is floor-level spiralling, supported rotation, a single hair-driven reveal, and lateral seated torsion. The low work has clear support points and controlled weight transfer; it is not random rolling. Song Yu does not speak, sing, or synchronize mouth movement. No text appears on screen.

Continuous layer: even at floor level, one support point is always loaded before the next body part moves. The spine unfolds in sections; the head and hair arrive after the torso; the costume follows gravity and momentum.

[Shot 1 | 0.000–2.333s | crossed-forearm close-up opening into floor-level spiral]
0.000–0.285s: continue the identical crossed-forearm close-up from SEG02. The top wrist rolls inward; the fingers release in sequence, and the two forearms separate without changing the torso's low kneeling twist.
0.285–0.570s: pull back to reveal the elbows opening at different heights as the pelvis shifts toward the support side.
0.570–1.140s: slide one foot outward and fold the nearer knee; the ribs spiral down against the pelvis, carrying the body toward the floor rather than repeating a standing cross-step.
1.140–1.710s: plant one palm to accept weight while the free leg extends along a diagonal. Insert a short close-up of the palm spreading and loading against the floor, fingers accepting weight one after another; track from the hand toward the extended toe, then return to the low full-body line before the descent completes.
1.710–2.333s: use the planted palm and bent knee to guide the body into a compact low seated-kneel. The camera descends in parallel with the body's center and keeps the planted hand and extended leg visible.

[Shot 2 | 2.333–4.625s | low close-to-medium, hair reveal]
2.333–2.903s: from the low seat, press both palms into the floor and spiral the sternum upward; the head remains bowed.
2.903–3.473s: long hair falls naturally across part of the face as the chest turns toward the side; the nearer hand passes across the face-line without touching the hair.
3.473–4.043s: the head sweeps once from left to right; hair follows with delayed horizontal inertia and clears the eyes.
4.043–4.625s: she fixes a sharp side glance, pushes through the supporting palm, and rotates the ribs toward the lens. Use a tight eye close-up exactly as the hair clears; rack focus from a loose strand crossing the near foreground to the iris, then cut on the first clear eye contact. The camera moves from over-shoulder to low frontal, with the hair itself providing the wipe.

[Shot 3 | 4.625–6.958s | seated torsion, sideways frame]
4.625–5.195s: remain at the low level and rotate the pelvis toward the supporting side while the sternum twists the opposite way.
5.195–5.765s: both arms swing laterally across different planes, the near hand sweeping low and the far elbow carving behind the ribs.
5.765–6.335s: extend the free leg along the floor, point the toes, and reach one hand diagonally forward; let the torso lean over the grounded hip rather than lifting the leg high.
6.335–6.958s: recoil through wrist, elbow, shoulder, and ribs, then draw the extended leg inward along a curved path. Insert a brief close-up of the pointed toe dragging inward along the floor; rack focus from toe to the reaching hand as it retreats. The camera tracks sideways across the seated waist twist and ends with the near hand and sleeve edge passing close across the lens until they fully occlude the frame — a hand-led wipe that hands the cut to the half-turn in SEG03-B. Hold the fully occluded frame to the end; do not reveal the body again before the cut.

Micro-expression layer: the eyes reappear after the hair sweep, then settle into a hard inward focus. Mouth relaxed and silent.

overall_soundscape:
<Audio 1> as the only soundtrack, with original voice and instruments unchanged. No speech, singing, mouth-sync, visible text, or generated sound effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. A-half local anchors: 2.333s, 4.625s, 6.958s. This A-half covers full-song 26.958–33.916; the hand-led wipe lands at full-song 33.916.
```

---

# SEG03-B｜仙姿蒙尘·低位反转与恢复受阻｜5.497 s（全曲 33.916–39.413）

> 双提示词之 **B**。喂 `<Picture 1>` + 全曲 33.916–39.413 音频。**B 段 local 时间从 0 起算（B local 0.000 = 全曲 33.916 = SEG03 时间轴 6.958）**。开场从 A 段手部遮挡之后继续，身体撑脚起身、半转、交叉脚制动，再半跪起身却在最后停住。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman shown in <Picture 1>. The picture is the sole authority for identity, face, hair, existing ornaments, costume, proportions, palette, lighting, and complete environment. She is the only dancer. Keep the supplied scene and clothing unchanged; no damage, extra prop, captor, or second person appears.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, 5.497 seconds long (the second half of a 12.455-second floor-level segment; B-local 0.000 = full-song 33.916), using only <Picture 1> and this cut of <Audio 1>. <Picture 1> locks identity and the visual world; it does not reset the pose. CONTINUITY IN: open a fraction after the hand-led wipe — the near hand and sleeve edge still cross the lens as partial occlusion while Song Yu remains at the low seated level; the hand clears the lens as the body rises, revealing the half-turn already underway. No new opening pose. This half's texture is a compact half-turn, crossed-foot landing and toe braking, then a supported low rise that catches halfway and cannot complete its recovery. Rotational inertia and the stalled recovery are the visual contrast; it is choreographic, not random. Song Yu does not speak, sing, or synchronize mouth movement. No text appears on screen.

Continuous layer: one support point is always loaded before the next part moves; the head spots the return and hair follows a fraction late; the costume settles after the body stops.

[Shot 1 | 0.000–2.250s | one compact half-turn]
0.000–0.285s: from the residual wipe, the near hand and sleeve clear the lens as Song Yu plants the supporting foot and presses through its ball to lift from the floor into a low crouch.
0.285–0.570s: begin one compact traveling half-turn; pelvis and shoulders rotate first, head spots the return direction, and hair snaps across a fraction later.
0.570–1.140s: continue the half-turn at one consistent height; the free arm trails the rotation and the ribs follow the pelvis.
1.140–1.710s: land with feet crossed and knees soft, immediately slide the rear toe out to stop the turn's remaining momentum.
1.710–2.250s: the arms cut in opposite diagonals, one elbow forward and the opposite wrist trailing, then reverse levels during the landing. The camera follows a fraction late and catches up with a lateral move; preserve rotational direction across the landing.

[Shot 2 | 2.250–4.917s | supported low rise]
2.250–2.820s: place one palm on the floor and fold the nearer knee under the torso while the other leg lengthens backward.
2.820–3.390s: shift the pelvis above the planted palm, twist the ribs away, and draw the extended leg back in a curved line.
3.390–3.960s: push through the palm and sole to lift into a half-kneel, one arm unfolding from near the floor to above shoulder height.
3.960–4.530s: the other hand stays close to the ribs; the spine rises only halfway and then catches, as if the body cannot yet complete its recovery. Start this beat on a tight detail of the planted palm tightening, then tilt up the forearm into the arrested shoulder and eyes; let the arm occupy the near foreground.
4.530–4.917s: settle the supporting knee and keep the reaching arm suspended for a short fraction. The camera tilts up from the support hand to her eyes exactly as the rise stops.

[Shot 3 | 4.917–5.497s | near-static held beat]
4.917–5.202s: hold the low level with the supporting palm and knee still planted; only the fingertips ease their tension as the torso breathes through the arrested rise.
5.202–5.497s: the eyes tighten during the stalled rise, then settle into a hard inward focus toward the camera. Hair and fabric complete their natural residual movement. The camera holds still for the same beat, making the pause deliberate and heavy. End on the arrested half-kneel with the reaching arm suspended; this is the bridge into SEG04, where the same weight-bearing palm continues pressing to carry her upward.

Micro-expression layer: eyes tighten during the stalled rise, then settle into a hard inward focus. Mouth relaxed and silent.

overall_soundscape:
<Audio 1> as the only soundtrack, with original voice and instruments unchanged. No speech, singing, mouth-sync, visible text, or generated sound effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. B-half local anchors: 2.250s, 4.917s. This B-half covers full-song 33.916–39.413; the final 0.580s is one deliberate held beat.
```

---

# SEG03 第三段·双提示词手动剪辑时间点流程

> 复杂动作不交给一条长提示词一次完成：A、B 两条提示词分别生成源片，再在剪辑软件里选动作最匹配的画格完成衔接。

| 步骤 | 全曲时间 | 对应素材 | 操作 |
|---|---|---|---|
| 1. 生成 A 源片 | 26.958–33.916（6.958 s） | SEG03-A | 若平台单次时长受限，可生成更长源片，最终只取前 6.958 s |
| 2. 生成 B 源片 | 33.916–39.413（5.497 s） | SEG03-B | 同上，B-local 0 = 全曲 33.916；只取需要的动作区间 |
| 3. 定位剪辑点 | **全曲 33.916（SEG03 时间轴 6.958）** | A 结尾 / B 开头 | A 结尾是 hand-led wipe：近手与袖缘扫向镜头直到**完全遮挡**；B 开头从遮挡后手袖离开、撑脚起身 |
| 4. 遮挡接缝 | 33.916 前后 1–3 帧 | 两源片 | 在 A「完全遮挡帧」与 B「仍被遮挡帧」之间硬切；接缝被手/袖盖住，观众看不到跳变 |
| 5. 匹配核对 | 剪辑点 ±0.1 s | 两源片 | 手的运动方向（扫向镜头→向侧离开）、身体低位、摄影机运动（A 横移收尾 / B 跟随起身）趋势一致；不一致则换一帧或重抽 B |
| 6. 音画核对 | 全曲 33.916 | 拼接结果 | 该点音乐不重启、不跳帧；A、B 都用同一条连续音乐的对应窗口，接缝落在音乐气口 |

关键：不是把两段视频简单拼起来，而是在**身体姿态、运动方向、手部轨迹、摄影机运动**上找共同相位；优先用 hand-led wipe 的完全遮挡帧隐藏接缝。若 B 段开头与 A 段遮挡对不齐，可让 B 源片多生成 1–2 s，从中挑出手部离开镜头、身体开始撑脚起身的那一帧作为 B 的入点。

---

# SEG04｜强撑仙姿｜12.753 s（全曲 39.413–52.166）

动作机制：C2 横向八字臂线 → C7 单次半转甩发 → C12 半脚尖平衡 → C5 拧倾出胯与肩胯反线。以站立中轴、失去对齐、重建仪态为主。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman from <Picture 1>. The image exclusively controls her identity, face, hair, existing ornaments, clothes, proportions, colors, lighting, and entire scene. Preserve all existing visual information. She is the only dancer; add no captor, prop, or new setting.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, exactly 12.753 seconds long, using only <Picture 1> and this cut of <Audio 1>. <Picture 1> remains the identity and environment authority, not a pose reset. CONTINUITY IN: start on the exact close-up of the weight-bearing palm that ended SEG03-B; the same finger pads remain pressed and the wrist keeps the same diagonal. Let the palm press further into the floor, transfer force through wrist, elbow and shoulder, draw one knee beneath the pelvis, plant the foot, and rise through a compact low crouch into standing during the opening second. The camera tilts up and pulls back along the same arm so the rise is one continuous action, not a cut to an already-standing pose. The choreographic signature is a formal upright line that repeatedly bends sideways and must be rebuilt through ankle, knee, pelvis, ribs, and head — not by returning to the same symmetrical pose. Song Yu is silent, with relaxed lips and no synchronization to the recording; do not display any text.

Continuous layer: a subtle breath-led rise and sink continues, with active weight transfers beneath the upper-body lines. Arms do not mirror each other; the head arrives after the shoulders, and fabric settles after each change in direction.

[Shot 1 | 0.000–1.045s | palm macro tilt-up into low side observer view]
0.000–0.285s: continue SEG03's identical palm close-up; the finger pads press harder and the wrist transfers weight toward the heel of the hand.
0.285–0.570s: travel up the forearm as the elbow bends and the near knee tucks under the pelvis; the free foot finds the floor.
0.570–1.045s: press through the planted foot and hand to lift the pelvis, then release the hand from the floor as the spine stacks upward into a compact standing line. One arm forms a narrow high line while the other hand remains near the lower ribs; the free toe taps outward to initiate the next route. The camera rises with the body's center and pulls back to retain both feet, making the kneeling-to-standing transition continuous and legible.

[Shot 2 | 1.045–3.670s | parallel lateral track]
1.045–1.632s: the high arm descends through center as the low arm rises, their wrists passing at different depths.
1.632–2.202s: the feet cross behind, open to the side, then swivel on the heel; the pelvis makes a small horizontal loop while the sternum counters it. Insert a quick detail of the wrists passing at different depths, then pull focus through the gap between the forearms to the opposing shoulder and hip line; this makes the counter-rotation legible before the camera returns to the lateral track.
2.202–2.772s: the near elbow slices across the face-line and the wrist rotates outward; the far hand travels close behind the waist.
2.772–3.342s: uncross the foot and shift weight to the opposite side, changing the level of the arms without opening them symmetrically.
3.342–3.670s: the head catches up last and the hip stays offset, creating a formal but unstable diagonal. Track parallel to the feet and rise toward waist height only as the arms cross.

[Shot 3 | 3.670–5.753s | compact half-turn, Hitchcock pressure]
3.670–3.912s: the planted heel initiates a compact half-turn; pelvis turns first.
3.912–4.482s: shoulders and ribs follow while the head spots a fixed direction; hair continues briefly after the torso checks.
4.482–5.053s: the rear foot crosses behind and the front toe pivots inward, sharply arresting the remaining rotation.
5.053–5.623s: the torso appears to continue a fraction while the feet are already stopped, producing a taut corkscrew line. Use a controlled Hitchcock dolly zoom here: physically track backward while zooming in, keeping the upper body roughly the same size as the unchanged background perspective stretches away.
5.623–5.753s: stop the optical distortion on the toe check and let the body take over again. Preserve full-body legibility; this is the only strong zoom in this segment.

[Shot 4 | 5.753–8.295s | still framing on high balance]
5.753–6.193s: press through the ankle and rise onto demi-pointe, drawing the free knee into a controlled front attitude.
6.193–6.763s: cross both forearms above the head with curved elbows and lifted sternum.
6.763–7.333s: hold one exact beat; insert a 0.285-second close-up of the raised supporting heel and flexed toes gripping the floor, then cut back to the full-body balance before the beat ends. The fingers and gaze continue moving slightly while the torso remains balanced.
7.333–7.903s: separate the arms into unequal diagonals, one high and one low; the lifted knee opens outward slightly.
7.903–8.295s: lower toe-first and transfer weight sideways before the heel settles. The camera remains planted during the balance and dips with the descent.

[Shot 5 | 8.295–10.462s | side-front, close parallax]
8.295–8.473s: initiate a backward cross-step, pelvis turning away while the sternum stays toward the lens.
8.473–9.043s: wrists cross near the face, elbows peel in opposite directions, and the chest rotates into a corkscrew.
9.043–9.613s: the trailing foot drags laterally to contain the turn; one hand folds toward the sternum while the other reaches behind the hip.
9.613–10.183s: the feet stop first, then shoulders, then head; the head turns toward camera last, revealing that she has noticed the observer without immediately yielding.
10.183–10.462s: the gaze lands. Start with a tight close-up framed through the near forearm; rack focus from the forearm edge to her eyes, then slide sideways behind the arm so it wipes across the lens into the next vertical-line shot. The horizon levels as the eyes meet the lens.

[Shot 6 | 10.462–12.753s | reconstructing the vertical line]
10.462–10.753s: straighten the supporting knee and stack pelvis under ribs.
10.753–11.323s: release the shoulder blades and let one hand trace a narrow vertical curve beside the head.
11.323–11.893s: extend the free leg behind with a pointed toe while the other hand stays firm and low near the waist.
11.893–12.463s: rotate the torso only a quarter toward the lens, restoring the long neck and lifted sternum.
12.463–12.753s: keep the tall diagonal, with the lower hand folded inward beside the ribs and its wrist visibly bent while the upper arm remains extended. Move into a tight close-up of that lower wrist and tense fingertips; end as the wrist begins a small outward roll. This is the exact bridge into SEG05, which continues the same wrist action rather than restarting from a full-body stance.

Micro-expression layer: eyes are composed during the rise, narrow briefly during the interrupted turn, and return to direct, controlled contact after the balance. Lips remain relaxed and silent.

overall_soundscape:
<Audio 1> remains the full original soundtrack. No added dialogue, singing, mouth-sync, visible text, or generated sound effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. Main local anchors: 1.045s, 3.670s, 5.753s, 8.295s, 10.462s. Dolly zoom occurs only during the half-turn at 3.670–5.753s.
```

---

# SEG05｜被迫校正｜13.584 s（全曲 52.166–65.750）

动作机制：C10 跪位撩臂起身 → C20 沉跪即起 → 反向截断关节链 → C28 起身路径改成"起到一半被打断"。从站立到单膝、再试图站起，突出动作主导权被夺走。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman shown in <Picture 1>. Use <Picture 1> as the only authority for identity, face, hairstyle, existing hair ornaments, outfit, proportions, colors, lighting, and the full environment. Keep the scene unchanged. She is the only dancer. The opposing force stays off-screen and is implied only through redirected movement and camera placement; no visible captor, extra hand, rope, cage, or added object appears.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, exactly 13.584 seconds long, using only <Picture 1> and the current <Audio 1> cut. <Picture 1> locks identity and environment; it does not reset the choreography. CONTINUITY IN: open on the same tight close-up of the lower wrist beside the ribs that ended SEG04, fingers tense and wrist beginning an outward roll. Continue that roll for the first instant, let the hand travel outward, then interrupt it at the wrist and pull back along the same path as the camera widens to reveal the body. Do not begin with a newly arranged standing pose. The action signature is a vertical rise-and-drop phrase whose extensions are interrupted midway through the joint chain. Every redirection starts somewhere specific — wrist, elbow, shoulder, ribs, pelvis, then feet — and changes the original movement pathway. The result is oppressive and choreographic, not shaking or generic struggling. Song Yu remains silent with relaxed lips; no vocal performance, mouth-sync, or on-screen text.

Continuous layer: quiet breathing and small foot adjustments continue even in the tension gaps. A hold must be a deliberate, readable beat — not frozen motion across the whole phrase.

[Shot 1 | 0.000–2.125s | wrist macro widening to medium-full side-front]
0.000–0.281s: continue the identical lower-wrist close-up from SEG04; the wrist rolls outward and the hand begins to reach away from the ribs.
0.281–0.851s: the wrist is cut off midway; the fingers remain extended as the hand recoils back toward the chest. The camera tracks along the forearm and pulls back, revealing the torso and feet as the supporting heel presses into the floor.
0.851–1.421s: the feet perform a tight cross-behind, side-open, toe-close pattern while the pelvis counter-rotates against the sternum.
1.421–1.991s: the leading hand reaches outward, but its wrist turns back before the elbow reaches full extension; the opposite shoulder remains forward. Cut briefly to a close-up of the wrist reversing direction; follow the recoil backward through the forearm to the shoulder, then return to the medium-full frame as the knees begin to lower. The near hand fills the edge of frame and becomes a visual wipe into the kneeling phrase.
1.991–2.125s: catch the interrupted arm shape without freezing the lower-body pulse. The camera makes a close lateral slide on the wrist reversal and ends on the split hand levels.

[Shot 2 | 2.125–4.542s | one controlled level drop]
2.125–2.561s: bend both knees and lower onto one knee in a sharp but controlled descent; the opposite foot remains planted to absorb weight.
2.561–3.131s: both arms sweep outward from the lower ribs in broad unequal arcs; the chest rises and the chin lifts.
3.131–3.701s: bring the body to a tall kneel, one arm reaching high while the other follows a low path around the waist.
3.701–4.271s: the high wrist folds and the elbow drops before the arm completes its arc, pulling one shoulder inward.
4.271–4.542s: the head stays proud as the torso absorbs the failed extension. Hold a close-up on the tightening eyes and the hand arrested at the end of its path, then widen as the camera rises to tall-kneeling height. The near forearm passes across the lens, carrying the cut into the next view; no separate person or restraint is shown.

[Shot 3 | 4.542–7.042s | kneeling torsion, camera presses then retreats]
4.542–4.841s: rotate the pelvis sideways while the knees remain grounded and stable.
4.841–5.411s: let the sternum counter-rotate; one hand reaches past the head while the other stays close to the ribs.
5.411–5.981s: the reaching wrist abruptly recoils toward the chest, followed by elbow, shoulder, and ribs in sequence; the pelvis continues a fraction farther. Use a close-up insert that tracks the wrist-to-elbow recoil, then rack focus to her face as the torso catches up; the delay between lower body and shoulder remains visible when the camera widens.
5.981–6.551s: correct the twist by repositioning one knee and shifting the weight through the shin, not by flailing the arms.
6.551–7.042s: try to send the hand outward once more; stop it at midline with the fingers still extended. The camera pushes in about 20cm as the hand reaches and retreats the same distance when pulled back. Use the brief 7.000–7.042s gap as an exact fingertip stop, then redirect.

[Shot 4 | 7.042–9.250s | rise interrupted by main Dolly Zoom]
7.042–7.121s: plant the front foot firmly under the pelvis and begin pressing up from the kneel.
7.121–7.691s: the torso rises; one arm travels from chest height toward overhead while the other palm presses forward.
7.691–8.262s: just before the elbow reaches its endpoint, it buckles inward; the shoulder follows, the ribs twist, and the rear heel slides to save balance.
8.262–8.832s: execute the main Hitchcock dolly zoom: physically track the camera forward while zooming wider, keeping her apparent size near constant as the unchanged background perspective compresses. The effect peaks exactly at the failed arm extension.
8.832–9.250s: the rear heel catches, knees soften, and the camera stops its optical move. Finish the pressure effect with a brief eye close-up framed past the hand held near the chest, then pull back to show she remains standing but slightly off-axis; the following lateral move is motivated by her head turning, not by an arbitrary camera reset.

[Shot 5 | 9.250–11.542s | standing pivot and late reacquisition]
9.250–9.402s: the head spots toward front before the body moves.
9.402–9.972s: take a compact quarter-turn with one cross-step, elbows held close to the ribs.
9.972–10.542s: shoulders arrive late; one forearm cuts horizontally across the chest while the other hand drops behind the hip.
10.542–11.112s: make a sharp heel change and reverse the torso direction without completing another full turn.
11.112–11.542s: the feet stop, then shoulders, then head. Let a passing forearm briefly cover the frame; behind it, the camera reacts slightly late, overshoots the shoulder line, slides back, and reacquires the eyes in a tight insert before widening to the asymmetric body line. This is a controlled imperfect observer movement, not random shake.

[Shot 6 | 11.542–13.584s | asymmetric final resistance]
11.542–11.682s: initiate a high reach from the sternum.
11.682–12.252s: open the forearms into an uneven V while the supporting knee remains flexed.
12.252–12.822s: one hand stays high; the other is pulled back toward the ribs, sending a visible recoil through shoulder and chest.
12.822–13.299s: try to release the lower arm outward again, but stop the elbow halfway and turn the palm inward.
13.299–13.584s: keep one toe lightly touching the floor and the hands at different heights, but let the camera move into a tight close-up of her eyes. Her gaze lands directly on the lens and stays fixed; a tiny shift in focus across the eyes is the only motion at the cut. End on this precise eye line, which SEG06 must continue without changing gaze direction or expression at its first frame.

Micro-expression layer: keep her face controlled through the drop; eyes flick toward the lens at the failed extension; the final gaze is sharper but not melodramatic. Mouth relaxed and silent.

overall_soundscape:
<Audio 1> is used unchanged. No new dialogue, singing, mouth-sync, visible text, or added sound effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. Main local anchors: 2.125s, 4.542s, 7.042s, 9.250s, 11.542s. One main Dolly Zoom only, at 7.042–9.250s.
```

---

# SEG06｜傲骨未折｜14.132 s（全曲 65.750–79.882）

动作机制：C1 呼吸提沉 → C34 背身双臂渐升 → C3 立圆与胸腰展开 → C30 空手致意与收回 → C14 收势改成冷静正面终止式。恢复自主路径，不变成胜利庆典，也不重复低位挣扎。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

subject_definitions:
<Subject 1> is Song Yu, the same adult woman shown in <Picture 1>. <Picture 1> exclusively controls her identity, face, hair, existing ornaments, clothing, proportions, color, lighting, and complete environment. Keep all source visual information fixed. She is the only dancer. Do not introduce a captor, additional character, prop, or different setting.

integrated_multimodal_description:
Create a vertical 9:16 live-action Chinese classical dance MV, exactly 14.132 seconds long, using only <Picture 1> and this cut of <Audio 1>. <Picture 1> remains the identity and environment authority, not an opening-pose reset. CONTINUITY IN: begin on the exact eye close-up that ended SEG05, with her gaze fixed on the lens and the same direction of light and facial angle. Preserve that look for the first fraction; then let the eyes shift toward the hand below frame, rack focus to the fingers as they loosen, and pull back to reveal the same arrested body line with one toe lightly touching the floor. The breath releases and the next step continues from that held tension. The choreography changes from a constricted range into self-directed pathways: spine, feet, and hands begin completing their own routes again. The ending is dignified and clear, not a smiley pose montage and not a collapse. The original vocal remains only in the audio; Song Yu dances silently, with relaxed lips, no mouth-sync, and no visible text.

Continuous layer: breath-led spine undulation connects the phrases. The feet keep making purposeful small adjustments; hands do not freeze between actions. One beat of deliberate stillness is reserved for the final close.

[Shot 1 | 0.000–2.458s | eye close-up pulling back into rear three-quarter tracking]
0.000–0.378s: continue SEG05's exact eye close-up. Keep the same gaze direction and facial angle; a small eye movement shifts toward the lower hand while the eyelids remain naturally open.
0.378–0.948s: rack focus from the eyes to the loosening fingertips near the lower edge of frame and pull back along that hand to reveal the same arrested body line, including the lightly touching toe. The shoulders round on an exhale while the supporting heel presses firmly into the floor; this breath starts the recovery rather than resetting her stance.
0.948–1.518s: cross one foot behind on a narrow diagonal and let the pelvis follow the foot while the sternum resists it.
1.518–2.088s: the hands open at different levels near the ribs, fingers uncurling from little finger to index finger. Insert a short close-up as the fingers unfurl in sequence, then pull focus through the opening between the hands to the shoulder line; the hands separate in opposite directions and guide the camera back to the rear three-quarter composition.
2.088–2.458s: unwind the waist just enough to redirect toward a rear three-quarter angle. Move the camera laterally with the cross-step; keep the body fully readable and do not force an instant frontal pose.

[Shot 2 | 2.458–4.541s | back view rising to side-front]
2.458–2.659s: while still facing away, begin lifting one arm from shoulder height.
2.659–3.229s: the other arm follows on a narrower path behind the head; both wrists rise at different speeds.
3.229–3.799s: cross the wrists overhead for a brief accent, shoulders releasing downward beneath the raised arms.
3.799–4.369s: turn the head toward the camera first, then ribs and pelvis follow into a quarter-turn; no complete spin. Let the nearer raised forearm cross the frame as the head turns; whip-pan in the same direction and resolve through the arm's trailing edge on the side-front view. The cut follows the head's lead rather than arriving before the movement.
4.369–4.541s: settle the turn on a toe pivot while the high hands begin to separate. The camera rises toward chest height during the arm ascent and starts a short lateral slide only when the head turns.

[Shot 3 | 4.541–7.125s | side-front, vertical arm circle]
4.541–4.939s: uncross the wrists through a clear palm turnover, one palm rotating outward and the other downward.
4.939–5.509s: the leading arm traces a vertical circle from in front of the chest to overhead, elbow leading then wrist then fingertips. Briefly follow the wrist in close-up through the lower half of the circle, rack focus to the fingertips at the top, then tilt down and widen as the other hand completes its counter-curve; the vertical circle becomes a visual guide rather than an isolated insert.
5.509–6.079s: let the upper back open vertebra by vertebra and lift the sternum; the head follows the raised hand without throwing backward abruptly.
6.079–6.649s: the lower hand travels in a counter-curve close to the waist while the rear foot slides outward to widen the support base.
6.649–7.125s: pivot the front toe inward and return to a long diagonal line, arms now on separate high and low planes. The camera arcs only from profile to front three-quarter, then stops as the chest reaches its extension.

[Shot 4 | 7.125–9.083s | forward acknowledgment, then withdrawal]
7.125–7.219s: shift weight toward the front foot and let the eyes arrive at the lens first.
7.219–7.789s: take one deliberate step forward; the near hand opens toward the viewer at chest height, palm angled slightly upward like a restrained formal acknowledgment.
7.789–8.359s: rotate the wrist outward and extend the fingers sequentially; the other arm remains behind the waist to counterbalance. Let the open palm approach close to the lens until it fills the foreground; focus on the palm lines for a fraction, then follow the same hand backward toward the sternum, revealing her face behind it. This hand-led push-in and withdrawal is the visual transition, not a new prop or magical effect.
8.359–8.929s: draw the open hand back along the same path toward the sternum while the pelvis pivots a quarter away from camera.
8.929–9.083s: the hand closes softly and the foot completes its weight transfer. The camera advances slightly during the offering gesture, then stops while the hand withdraws, making the movement feel chosen rather than forced.

[Shot 5 | 9.083–12.291s | traveling diagonal and body-line return]
9.083–9.499s: take a measured toe-led step on a diagonal; the shoulders stay calm while the hips steer the change of direction.
9.499–10.069s: cross the second step behind and let the sternum counter-rotate, producing a corkscrew through the waist.
10.069–10.640s: the near elbow folds beside the cheek while the opposite arm reaches behind the hip; the head tracks the leading wrist. The camera briefly tightens to the wrist passing beside the cheek, then rack-focuses to her eyes as the hand leaves the foreground; follow her head turn into the next diagonal step.
10.640–11.210s: uncross into a side placement and roll the leading wrist outward, allowing the hand to open only after the elbow has reached its endpoint.
11.210–11.780s: pivot the supporting heel and bring the torso back toward the front three-quarter line; hair follows the turn after a short delay.
11.780–12.291s: both arms release into an asymmetric low-high line and the chest settles above the pelvis. Use a controlled whip-pan motivated by the head turn, resolving exactly on the planted foot; do not use a new background or visual effect.

[Shot 6 | 12.291–14.132s | final calm frontal three-quarter]
12.291–12.350s: let the eyes arrive at the lens while the body finishes its last small weight transfer.
12.350–12.920s: straighten the supporting knee, stack the pelvis beneath the ribs, and release the shoulders downward.
12.920–13.490s: one hand floats beside the cheek with gently curved fingers, then rotates outward and descends diagonally; the other hand opens at waist height. Start on a tight three-quarter close-up through the fingers, holding sharp focus on the eyes; as the hand descends, pull back smoothly to medium-full so the grounded feet and restored vertical line are visible before the final held beat.
13.490–14.060s: hold one exact beat with both feet grounded and the spine upright; only the gaze and fingertips continue moving subtly.
14.060–14.132s: allow the remaining fabric motion to settle naturally as the clip ends, without a sudden freeze or fade.
The camera becomes level and steady at chest height in a medium-full front three-quarter composition. It no longer crowds her; the last frame feels like composure reclaimed rather than triumph declared.

Micro-expression layer: the gaze rises only after the spine and shoulders have restacked. The final expression is proud, lucid, and restrained. Lips remain relaxed and still.

overall_soundscape:
<Audio 1> supplies the complete original soundtrack. The performance is silent; no speech, singing, mouth-sync, on-screen text, or generated sound effects.

non_diegetic_music:
<Audio 1> only. Timing reference: 105.25 BPM, beat 0.5701s, half-beat 0.285s, bar 2.2803s, phrase 4.5606s. Main local anchors: 2.458s, 4.541s, 7.125s, 9.083s, 12.291s. Final stillness occupies one beat only; subtle eye and fingertip motion remains.
```

---

# 段间匹配剪辑｜逐边界核对

| 边界 | 上一段最后画面 | 下一段第一画面 | 连贯动作 |
|---|---|---|---|
| SEG01 → SEG02 | 高举手腕与微卷指尖特写，手仍沿上前方曲线运动 | 同一只手腕、同一画面位置与焦距，接着向下前方运行，再拉开到身体 | 手臂曲线连续，脚步与骨盆扭转随后显露 |
| SEG02 → SEG03-A | 胸前交叠前臂特写，低位扭身状态不变 | 同一交叠角度与前后关系，手指先松、手腕再解开 | 交叠释放直接带动身体下降和手掌承重 |
| SEG03-A → SEG03-B | 全曲 33.916：hand-led wipe 手/袖完全遮挡镜头 | 遮挡后手袖离开，撑脚起身进入半转 | 遮挡接缝，身体低位与手的方向连续 |
| SEG03-B → SEG04 | 压地承重手掌特写（半跪受阻） | 同一手掌、同一腕部斜线与焦点，继续推地 | 手掌→前臂→肩→骨盆受力链把低位带到站立 |
| SEG04 → SEG05 | 胸侧低手腕部特写，手腕开始外旋 | 同一腕部继续外旋、向外伸展，然后在腕部被截断 | 手臂伸展与回收连成受阻动作链 |
| SEG05 → SEG06 | 直视镜头的双眼特写，视线稳定 | 同一眼线和脸部角度，先转动视线，再拉焦到指尖并拉开 | 眼神由受制凝视转向手部，带动恢复自主 |

每个边界的局部特写属于匹配剪辑点，不是段落情绪重置：在同一手部/眼部动作相位上硬切，下一段开头继续前一段最后的运动方向、焦点和遮挡关系；禁止每段回到图 1 静态姿势，也不用黑场、淡入或重新起势代替衔接。
