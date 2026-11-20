# INDEX — Music-Dance Theatre / Solo Stage Performance

**MiniMax H3 Full-Reference Ref2VA · Complete Rebuild Rev.8.3 · 21 independently generated clips**  

**Source audio:** `11月16日.mp3` · **Runtime:** 252.648s · **Segments:** 21 · **Tempo:** 170.15 BPM · **Beat:** 0.3526s · **Bar:** 1.4105s · **Phrase:** 2.821s · **Format:** vertical 9:16.

## 生成素材与执行边界

- **Picture 1：全程唯一人物母版。** 只负责完整人物视觉身份的全程锁定。所有片段都使用同一张 Picture 1。正式 H3 提示词不再用文字复述任何人物外观细节；不得重绘、改变或替换图1中的人物，也不得把场景参考覆盖到人物上。Picture 1 的原背景、光线、姿势和构图不继承。
- **Picture 2：实际上一段最后一帧。** SEG02–SEG21 每次生成时，把紧邻上一段真实导出的最后一帧作为 Picture 2。Picture 2 只锚定开场瞬间的场景、悬浮姿态、运动方向、镜头侧别和仍在场的舞台构件；人物身份与全套设计始终由 Picture 1 覆盖。不要用预想的末帧代替真实生成帧。
- **每次最多两段：** 按 01–02、03–04……19–20 分组生成；每组先生成奇数段，再提取真实末帧作为下一段 Picture 2 生成偶数段。下一组的奇数段继续使用上一偶数段的真实末帧。SEG21 单独作为尾声生成。
- **真正的单人音乐舞台剧：** 只有一位台上表演者。没有工作人员、舞台监督、搬景人员、其他演员、伴舞或乐队成员入镜。所有场景构件由舞台地板内置升降机构直接升起、旋转、下降，不拍工作人员，不出现推车或手动搬运。舞台地板可以存在，但表演者全程以悬浮舞蹈为主，不在地面行走、起跳落地或站桩表演。
- **景别纪律：** 以近景、近中景、中景、人物占画较大的中近全身为主。不要大全景、全舞台远景、观众席远景、人物小到模糊的全身远景。需要读清完整舞姿时用中近全身，保持人物占画面主体并清晰；布景靠人物身后的局部、前景视差和焦点转移表达规模。
- **观众处理：** 画面不展示观众，不出现观众席、观众人形、手臂、剪影或星星棒镜头。原始音轨中已有的现场声浪保留。保留原始 `<Audio 1>` 已有的现场声浪、欢呼与掌声，不生成新观众音轨。
- **情绪而非歌词插画：** 歌词只提供情绪方向和音乐时间窗，不按名词生成场景或道具。不得因为歌词出现 chapel、book、page、bread、star、spell、window 等词而添加教堂、书本、书页、面包、星星道具、魔法物品或窗户。每两段一幕的舞台构件均为抽象情绪舞台美术，不是歌词实体化。
- **舞蹈与悬浮：** 默认头上脚下的竖直悬浮轴，动作由肩胸、脊柱、腰胯、腿部和脚尖共同完成；漂移、半转、肢体波浪、腿部延展和剪式换形组成完整舞句。严禁重复跳起落地、舞台走路填充、横躺式飞行或连续倒飞。全片只有 SEG17 允许一次头朝下垂直下潜，SEG18 只负责从该末态连续恢复竖直；其余 19 段的舞句结尾全部保持头上脚下的竖直或自然三分之四倾斜状态，不得把倒置当成高潮模板或结束姿势。
- **口型：** 只在指定原始歌词窗口进行短时同步：SEG07 的关键情感句、SEG12 的重现句、SEG17 的 “Come on!”、SEG19 的两句致谢。其余原始演唱只作为音轨，人物以表情、眼神、呼吸和舞蹈回应，不全程对口型。
- **H3 正文格式：** 每段使用官方 Ref2VA 六字段顺序：`subject_definitions` → `summary` → `retention_analysis` → `detailed_description` → `overall_soundscape` → `non_diegetic_music`。每段是完整、自包含的英文提示词；每段一个独立 `text` 代码块，方便单段复制。

## Rev.8.2 修订说明｜动作库编舞重建（保留）

- 以 Rev.1.12 动作库为本次编舞的动作来源，替换上一版 21 段完全相同的通用舞蹈段落；每段均有不同的动作链组合、局部时间窗、身体动力路径和出态。
- 导演层只负责情绪弧线、舞台调度、镜头和转场；编舞层优先选择动作库标准链，再针对持续悬浮条件改编受力与支撑方式。
- SEG01–SEG16、SEG19–SEG21：每段仍以头上脚下的直立悬浮或自然三分之四倾斜状态结束；除 SEG06、SEG13 两次完整竖轴旋转外，其他转体只做半转或四分之一转。
- SEG17：保留全片唯一一次头朝下垂直下潜，并在末帧明确保持该动作以供 SEG18 接续。
- SEG18：从真实倒置末帧连续恢复直立；本段结束必须是头上脚下的稳定悬浮，不再重复倒置。
- SEG17 保留全片唯一一次头朝下垂直下潜；SEG18 从实际倒置末态恢复，并在 1.193s 前回到头上脚下。
- 21 段各自的音频、局部时间码、场景构件、单人舞台剧设定、图1人物锁定和 Ref2VA 六字段均保留；本次重建集中在舞蹈动作链及其拍点执行描述。

## 十一幕情绪与舞台美术规划

- **OVERTURE — The performer invites the room into the music：** hesitation opening into an intimate invitation。舞台构件：One slender, freestanding oval stage frame rises vertically from a concealed lift in the stage deck. Its surface is dark satin metal with a narrow warm edge light. It is an abstract scenic frame, not a door, portal, chapel, halo or lyric illustration. It remains fixed during this two-segment scene.

- **ACT I — Curiosity becomes wonder：** curiosity, discovery and a growing sense of possibility。舞台构件：Two slim sculptural stage fins and one shallow curved upper rib rise directly from separate concealed floor lifts. Their surfaces are matte charcoal with subtle pearl reflections. They form an abstract asymmetrical composition, not stained glass, shelves, books, a window or any literal lyric object.

- **ACT II — Inner scale expands：** wonder widening into joyful release。舞台构件：Three translucent vertical planes rise from the stage deck at staggered depths. Each is narrow enough to remain behind the performer in medium framing. The planes have no text, symbols, pages, stars or pictures; they catch layered light and create depth through parallax.

- **ACT III — Vulnerability and acceptance：** the outward spectacle contracts into an intimate emotional truth。舞台构件：The previous planes are fully below the deck. A single low-profile crescent-shaped vertical scenic rib rises behind the performer. It is open, asymmetrical and non-literal; no room, furniture, book or physical symbol appears.

- **ACT IV — Warmth and connection：** loneliness gives way to warmth, companionship and playful joy。舞台构件：Two opposing shallow curved reflectors rise directly from the stage deck, one on either side behind the performer. Their inner faces carry warm diffused light, suggesting an embracing space without depicting another person, table, chair, food or literal lyric object.

- **ACT V — Inner conflict becomes clarity：** a brief inward struggle resolves into calm conviction。舞台构件：Two tall angled fins rise from concealed deck lifts and pivot toward one another, leaving a clear open gap behind the performer. Their faces are dark and non-reflective; light travels across their edges. They are abstract theatrical architecture, not pages, a book or a literal object.

- **ACT VI — A safe emotional center：** uncertainty softens into trust and emotional safety。舞台构件：A single open curved frame rises from the stage deck, with two short vertical side ribs. The shape remains open at the front and above; it never becomes a room, cage, house or literal shelter. No furniture or hand props.

- **ACT VII — The inner world opens outward：** private security expands into confident generosity。舞台构件：Three tall translucent vertical panels rise at separate depths and pivot outward in a shallow fan. Their surfaces remain abstract and unmarked. Their motion is slow, mechanically consistent and clearly driven by integrated stage lifts.

- **ACT VIII — The shared climax：** private wonder becomes a confident invitation to share the moment。舞台构件：A broad but shallow curved frame rises behind the performer, accompanied by two narrow vertical towers. These are real modular scenic pieces driven by concealed floor lifts; no extra performers, literal symbols, audience faces or oversized spectacle objects.

- **ACT IX — Gratitude and the final bow：** exhilaration settles into sincere gratitude and quiet affection。舞台构件：A low, narrow vertical light frame rises behind the performer, much simpler than the climax structure. It is the only remaining scenic unit; all other pieces are below the stage deck.

- **CODA — The last light：** calm afterglow, intimacy and a final connection。舞台构件：All scenic pieces remain below the deck. Only one thin vertical backlight line remains behind the performer, with no additional prop or scenic object.



## 动作库版本与 21 段选链总表｜Rev.1.12（2026-11-17）

动作库正本：<https://raw.githubusercontent.com/LoveRain1997/h3-prompt-journal/main/case-studies/2026-10-dance-motion-chain-library/dance-motion-chain-h3.md>

**本次使用的真实标准链与改编边界：**

| 动作库链 | 原始动作机制 | 本片适配方式 |
|---|---|---|
| A13 | 低位交叉双臂→向两侧展臂 | 保留双臂开合路径；取消提踵／跳落支撑 |
| A15 | 胸前 X 交叉→水平展开 | 原样保留上肢路径，叠加浮空躯干反向配重 |
| B7 | 翻掌邀请＋同侧胯部 accent | 保留掌心翻转，胯部改为小幅反向 counter-tilt |
| B8 | 一臂高、一臂低的错位身体波浪 | 保留肩→胸→肋→腰的连续波浪，腿部加入姿态反向配重 |
| C1 | 呼吸驱动提沉 | 只使用胸廓、脊柱和头部的呼吸传递，不采用跪坐／站起 |
| C2 | 双臂横向连续 figure-eight 云手 | 保留手臂横向环路，重心左右移改为浮空骨盆微反向摆动 |
| C3 | 单臂立圆上举＋上胸腰延展 | 保留立圆与胸椎延展，限制腰椎过度后弯 |
| C5 | 拧腰、出胯、斜向手臂亮相 | 保留躯干扭转和斜线，去除站立支撑假设 |
| C7 | 留头起转、平转、甩发收势 | 适配为绕身体竖轴的受控旋转；全片仅 SEG06、SEG13 各一次完整 360° |
| C12 | 吸腿 attitude 静态平衡 | 取消半脚尖承重，改为无支撑的悬浮 attitude 与 pointed-leg counterline |
| C14 | 轻倾、手至腮边、保持 | 仅用于收束段的微倾与短暂持形 |
| C16 | 云手穿掌、背转前、交叉下沉 | 保留云手和穿掌路径；删掉地面步法，只做受控上身朝向变化 |
| G1 / G2 / G3 / G4 | TURN、LINE、FLIP、Contemporary Spiral / Off-axis Tilt / Fall & Recovery、Hero Lock 与八步 Hero 链 | 按各段需要抽取技术结构；唯一完整倒置只出现在 SEG17，SEG18 专门恢复 |

**21 段选链分配：**

| 段落 | 动作链组合 | 核心编舞任务 |
|---|---|---|
| 01 | C1 → C2 → A15 → C5 / LINE | 呼吸起势、云手、交叉开臂、邀请斜线 |
| 02 | B8 → A13 → C5 → B7 / C12 | 身体波浪、展臂、半转、掌心邀请与 attitude |
| 03 | C1 → C2 / B8 → C12 → LINE | 发现感波浪、attitude 换形、长线条 |
| 04 | C3 → A15 / C5 → C16（适配）→ Off-axis Tilt | 立圆、交叉展开、半转、受控侧倾 |
| 05 | B8 → C12 / LINE → C5 / Spiral → LINE | 波浪、腿线延展、局部转向、回收邀请 |
| 06 | A13 → C12 → C7 / TURN → G3 Hero Lock | 全身释放、腿部组合、第一处完整竖轴旋转 |
| 07 | C1 → Contemporary Contraction / Spiral → Off-axis Tilt / B8 → C2 | 情绪内收、脊柱螺旋、浅倾与安静回流 |
| 08 | C1 → C3 / C2 → C12 → LINE | 呼吸扩张、上下立圆、attitude 与接受性长线 |
| 09 | B7 → C2 / B8 → C12 → A13 / C5 | 邀请掌、云手波浪、交叉腿线、温暖展开 |
| 10 | C2 / A15 → C12 → C5 / Spiral → B7 / LINE | 高低臂环、attitude、四分之一转、确定性开放 |
| 11 | A15 / B8 → Contraction / Spiral → Off-axis Tilt / LINE → Accent Lock | 交叉压缩、螺旋挣扎、对角线释放 |
| 12 | C1 → C2 → C3 → C12 / LINE | 呼吸澄明、云手、立圆、克制平衡 |
| 13 | TURN Prep → C7 / TURN → G3 Hero Lock / C12 → C3 | 第二处也是最后一处完整竖轴旋转、Hero 锁定 |
| 14 | C1 → C2 / A13 → C12 → B7 / LINE | 安全感、展开、attitude、双掌给予 |
| 15 | A15 → C12 / LINE → Spiral / Off-axis Tilt → C16（适配） | 面板扩张对应的快速开合、腿形交换、螺旋与穿掌 |
| 16 | C16（适配）/ A15 → C12 / LINE → C5 / 半转 → LINE / Accent Lock | 全曲最完整的预高潮舞句、半转、Hero 前置线条 |
| 17 | FLIP Prep → Initiation → 单次 head-first vertical dive → 持续下潜 | 全片唯一一次头朝下垂直下潜 |
| 18 | Fall & Recovery → Suspension → C12 → B8 / Hero Lock | 从 SEG17 实际倒置末帧恢复竖直、延伸与定势 |
| 19 | C1 → C2 → B7 / C13（适配）→ LINE | 两段致谢口型期间保持嘴部可见，随后掌心向外 |
| 20 | C1 → A13（适配）→ C14 → C3 / C12 | 小幅谢幕、温和持形、回到竖直尾声 |
| 21 | C14 → C3 → C1 → G3 Hero Lock | 最终亲密手势、呼吸收束、活态定格 |

**全片动作预算：** 两次完整竖轴旋转（SEG06、SEG13）；唯一一次 head-first vertical dive（SEG17）；SEG18 仅负责恢复。其他段落使用半转、四分之一转、躯干螺旋和轴线倾斜，不用连续转圈填充。连续悬浮是持续层，不是让人物横躺或被动漂移。

**选链排除原则：** 不调用依赖深蹲、跪姿、地面滚动、走步或真实跳跃落地的动作原样进入本片，例如 B3、B5、B6、B15、C9、C10、C11、C18、C19、C20、C24；只在有明确改编价值时抽取上身动作路径，并在提示词中写明已移除地面支撑条件。

---

## Rev.8.3 修订说明｜古风式动作落点接力转场（20 个段间切口）

本次只迁移此前古风舞项目中有效的视觉剪辑方法，不迁移古风服装、环境、道具或水雾美术。转场不再采用‘上一段最后全身姿势＝下一段第一帧全身姿势’的姿态接续。采用 **动作峰值／释放中的身体局部落点 → 硬切 → 同一局部近景接住 → 沿身体路径揭示人物 → 回到本段舞蹈覆盖**。

**执行规则：**
- 上一段最后 0.55 秒，摄影机在当前连续镜头内完成一个有动机的局部构图，把最后画面落在指定手、腕、指尖或眼睛上；人物动作仍在进行，不冻结、不摆终止姿势。
- 下一段第一镜必须从同一身体局部的紧特写开始，沿相同动作方向继续约 0.4–0.8 秒，再沿手臂、肩线、视线或躯干路线逐级揭示，最后回到本段需要的近中景或人物占画较大的中近全身。不能一开始就给全身，也不能只拍局部不揭示舞蹈。
- `<Picture 2>` 仍然是上一段真实末帧，负责确认人物实际身体结构、动作相位、运动方向和舞台构件状态；它不再强制复制上一段的全身构图或机位距离。下一段允许以新的近景机位重新构图，但必须接住同一身体局部和运动向量。
- 这是剪辑上的视觉匹配，不是让 H3 生成溶解变形、重影或身体形变。默认直接硬切；每个切口只匹配一个主要身体锚点。舞台构件的升降继续按各段原有设定，不为转场额外增添道具。
- 近景必须是真正有辨识度的手、腕、指尖或眼部局部，不用数字放大五官，不用广角怼脸；镜头随后及时揭示身体动作。

### 20 个切口的视觉落点表

| 切点 | 上一段最后画面落点 | 下一段第一镜局部特写 | 接力方向与揭示路径 |
|---|---|---|---|
| SEG01 → SEG02 | 伸向羽毛飞出方向的右手指尖 | 同一只右手指尖 | 指尖→手腕→前臂→肩胸→错位身体波浪 |
| SEG02 → SEG03 | 胸前打开的掌心 | 同一只胸前掌心 | 掌心→指尖→侧翼光线→双眼与呼吸起势 |
| SEG03 → SEG04 | 追随侧翼光线的双眼 | 同一双眼睛 | 双眼→视线方向→上举手臂→立圆动作 |
| SEG04 → SEG05 | 斜向伸出的手与指尖 | 同一只斜向伸出的手 | 手指→前臂→肩胛→全身波浪 |
| SEG05 → SEG06 | 回到心口的手 | 同一只心口附近的手 | 心口手→腕肘肩→不对称展臂 |
| SEG06 → SEG07 | 高斜线手臂的腕与指尖 | 同一条高斜线手腕 | 腕指→前臂→胸口→眼神与呼吸收缩 |
| SEG07 → SEG08 | 胸前打开的掌心 | 同一只胸前掌心 | 掌心→指尖→双眼→吸气扩胸 |
| SEG08 → SEG09 | 望向画外观众方向的眼神 | 同一双眼睛 | 双眼→眼线→递出手掌→邀请动作 |
| SEG09 → SEG10 | 向外递出的掌心 | 同一只递出掌心 | 掌心→腕部环路→双臂高低交换 |
| SEG10 → SEG11 | 从胸前向外分开的指尖 | 同一组重新打开的指尖 | 指尖→双手外分→眼神与推拉线 |
| SEG11 → SEG12 | 转向舞台中轴的双眼 | 同一双转向中轴的眼睛 | 双眼→面部转向→肩部释放与呼吸 |
| SEG12 → SEG13 | 指向舞台中心的伸出手指 | 同一只指向舞台中心的手 | 指尖→腕肘→躯干反扭→转轴准备 |
| SEG13 → SEG14 | 下降至心口的手腕与指尖 | 同一只下降至心口的手腕 | 腕指→掌心→胸前→柔和眼神 |
| SEG14 → SEG15 | 朝外递出的近侧掌心 | 同一只向外递出的掌心 | 掌心→腕部内旋→胸前交叉→双臂展开 |
| SEG15 → SEG16 | 肩线以上的高位手腕 | 同一只高位手腕 | 高位手腕→头顶弧线→胸前交叉→外展 |
| SEG16 → SEG17 | 从邀请线收回心口的指尖 | 同一只回到心口的手 | 心口指尖→前伸手掌→手臂→直立下潜预备 |
| SEG17 → SEG18 | 倒置下潜中调节速度的伸出手腕 | 同一只倒置中的伸出手腕 | 倒置腕指→前臂→肩胸→倒置身体与恢复起点 |
| SEG18 → SEG19 | 从心口向外打开的掌心 | 同一只向外打开的掌心 | 掌心→前臂→肩线→眼睛与致谢表情 |
| SEG19 → SEG20 | 递向画外空间的打开掌心 | 同一只递向画外的掌心 | 掌心→手腕→心口→上脊柱鞠躬 |
| SEG20 → SEG21 | 转回镜头时聚在心口附近的指尖 | 同一组心口附近的指尖 | 心口指尖→手背/腕部→脸侧→眼睛 |

**分工提醒：** 本表定义段间视觉剪辑和镜头落点；每段 `LOCAL DANCE TIMELINE` 仍是唯一身体动作时序。开场局部特写只是对该动作的近距离摄影覆盖，不增加第二套动作，也不重复上一段刚完成的动作。SEG17→SEG18 特殊处理：局部特写必须保留实际倒置方向，接住同一只正在调节下潜速度的手，再揭示倒置中的恢复；不得提前扶正或重复下潜。
## 21 个独立 H3 提示词

## SEGMENT 01 — Threshold — a private beginning

**原曲区间：** 0.000–12.000s · **时长：** 12.000s · **音频：** `seg01_00m00p00s-00m12p00s.mp3`  
**歌词事件：** Instrumental; no lyric events in this crop.

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

No second reference image is supplied for the opening segment. <Picture 1> remains the sole character reference; construct the stage environment only from the scene directions in this prompt.

<Audio 1> is the exact original crop `seg01_00m00p00s-00m12p00s.mp3` from 0.000s to 12.000s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 12.000 seconds.

summary:

[reference generation + audio reuse] Create an exact 12.000-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: OVERTURE — The performer invites the room into the music. Emotional objective: She begins inward and tentative, then chooses to invite the unseen audience into the performance. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.

<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: OVERTURE — The performer invites the room into the music. The performer's immediate objective is: She begins inward and tentative, then chooses to invite the unseen audience into the performance.
Emotional movement: hesitation opening into an intimate invitation. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
One slender, freestanding oval stage frame rises vertically from a concealed lift in the stage deck. Its surface is dark satin metal with a narrow warm edge light. It is an abstract scenic frame, not a door, portal, chapel, halo or lyric illustration. It remains fixed during this two-segment scene.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
A restrained central soft key and a narrow warm side beam; auditorium remains mostly dark. Keep the face readable and the background low in detail.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
At the first frame she is already vertically suspended near the oval frame; the original feather is present as the sole opening prop.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] A close-medium view holds on her poised hand and attentive eyes. She slowly turns the single feather between her fingertips, pauses, then raises her gaze toward the lens. Her body remains upright in a controlled float; a small shoulder release begins the first movement phrase.
[Shot 2] At 00:02.929, She draws the feather close to her chest, lets the wrist rotate outward, and extends the hand toward the camera. The movement travels from wrist to elbow to shoulder, then gently opens the chest. Her legs pass through one narrow pointed cross and uncross without a jump or landing.
[Shot 3] At 00:05.750, The feather moves into the near foreground and briefly softens focus. She releases it once; it continues on a single natural drift past the lens. The camera tracks a short distance with the feather, then returns focus to her eyes as her free hand opens toward the audience.
[Shot 4] At 00:08.571, She follows the feather with her gaze, then completes a small controlled vertical-axis turn while remaining head-up and feet-down. The oval frame begins its slow descent. End with her right arm extended toward the space the feather has crossed, preserving the same screen direction. During the final 0.55 seconds, make one continuous, physically motivated camera reframe onto her extended right hand. Let the fingertips occupy the dominant part of the frame as they continue along the same reaching path toward the space the feather crossed. Keep the hand moving slightly through the cut; the feather has already left the frame and is not shown or released again.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Breath-led initiation; C2 — Horizontal cloud-arm figure-eight; A15 — X-cross to open line; C5 + G1 LINE — Diagonal invitation.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–02.929s | C1 — Breath-led initiation: Begin with a small chest rounding and release: the sternum softens, ribs follow, then the spine lengthens upward one section at a time. The pelvis remains vertically organized while both pointed legs hang in a narrow crossed line; this is a breath cue, not a takeoff.
02.929–05.750s | C2 — Horizontal cloud-arm figure-eight: The left arm rises as the right sinks, then they exchange levels to trace one continuous horizontal figure-eight in front of the chest. Let the rib cage and pelvis make a restrained counter-sway beneath the arm path; fingers finish each loop rather than fluttering independently.
05.750–08.571s | A15 — X-cross to open line: Bring both forearms into one clean chest-level X, then separate them horizontally into a wide open line. At the same time, uncross the lower legs into one narrow pointed scissor and recross once, keeping the torso upright.
08.571–12.000s | C5 + G1 LINE — Diagonal invitation: Turn the torso into a small three-quarter twist led by the ribs, counter-rotate the pelvis, and extend the reaching arm along a diagonal. The free leg lengthens below with a pointed foot; hold the line just long enough for the gaze to arrive, then let the wrist soften into the outgoing reach.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): Instrumental; no lyric events in this crop.
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. She follows the feather with her gaze, then completes a small controlled vertical-axis turn while remaining head-up and feet-down. The oval frame begins its slow descent. End with her right arm extended toward the space the feather has crossed, preserving the same screen direction. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG01 releases the feather once. SEG02 begins on the actual feather trajectory and never replays the release. At the end of SEG02 the oval frame begins descending; SEG03 opens on that same frame already below its former height as the new fins rise.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 12.000 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.108s, 2.929s, 5.750s, 8.571s, 11.392s. Local downbeats: 1.519s, 4.340s, 7.161s, 9.982s. Detected high-confidence drum accents: 6.595s kick; 10.495s snare; 10.867s snare; 11.239s snare. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 02 — The invitation — the stage answers

**原曲区间：** 12.000–24.000s · **时长：** 12.000s · **音频：** `seg02_00m12p00s-00m24p00s.mp3`  
**歌词事件：** Instrumental; no lyric events in this crop.

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg02_00m12p00s-00m24p00s.mp3` from 12.000s to 24.000s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 12.000 seconds.

summary:

[reference generation + audio reuse] Create an exact 12.000-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: OVERTURE — The performer invites the room into the music. Emotional objective: She accepts the audience connection and lets the performance become more open and rhythmic. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: OVERTURE — The performer invites the room into the music. The performer's immediate objective is: She accepts the audience connection and lets the performance become more open and rhythmic.
Emotional movement: hesitation opening into an intimate invitation. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
One slender, freestanding oval stage frame rises vertically from a concealed lift in the stage deck. Its surface is dark satin metal with a narrow warm edge light. It is an abstract scenic frame, not a door, portal, chapel, halo or lyric illustration. It remains fixed during this two-segment scene.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
A restrained central soft key and a narrow warm side beam; auditorium remains mostly dark. Keep the face readable and the background low in detail.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue from the actual last frame of SEG01: the feather has already passed out of frame; only the extended hand and its reaching direction remain as the visual cue. Do not show the feather again or recreate its release.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Start on a tight local close-up of the same right fingertips and extended hand from <Picture 2>. The fingers continue the same forward-reaching motion and soften once; do not show the feather again. Track backward along the wrist and forearm, then open to a close-medium view as the shoulder and torso carry the first staggered body wave. Reach the broader dance composition only after the hand-to-shoulder movement is readable. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:02.213, She leads a connected phrase from shoulder blades into chest, ribs and waist, then lets both forearms sweep outward on alternating musical accents. Her knees fold into a small crossed attitude and lengthen again; the feet remain pointed and unsupported.
[Shot 3] At 00:05.034, A short side-track passes across the oval frame, creating parallax while she performs one measured half-turn and returns to a three-quarter front orientation. Her expression shifts from shy curiosity to a warm, confident smile.
[Shot 4] At 00:07.855, The camera holds close enough to keep her full vertical figure readable as the oval begins lowering into the deck. She finishes the phrase with one palm open and the other hand near her sternum. End in a controlled upright float; no feather is retrieved. In the final 0.55 seconds, let the camera settle on the open palm held near her sternum. The fingers extend and the palm turns a few degrees outward, leaving that small wrist rotation unfinished at the cut.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: B8 — Staggered body wave; A13 — Low cross to broad port de bras; C5 — Counter-twist half-turn; B7 + C12 — Offering palm into suspended attitude.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–02.213s | B8 — Staggered body wave: Start the wave at one shoulder with one arm high and the other low. Let the ripple travel through sternum, ribs, waist and pelvis in sequence; the two arms lag at different speeds so the body wave reads as one connected four-count phrase.
02.213–05.034s | A13 — Low cross to broad port de bras: Cross the forearms low in front of the torso, then sweep both arms outward in two broad arcs. The chest opens after the elbows, and the pointed legs pass through a compact crossed attitude before lengthening again; no foot touches the deck.
05.034–07.855s | C5 — Counter-twist half-turn: Draw one elbow toward the ribs to preload the torso, rotate the rib cage and shoulders through a measured half-turn, and let the pelvis follow slightly later. The head spots last and returns to a three-quarter front orientation; the legs remain compact and pointed throughout.
07.855–12.000s | B7 + C12 — Offering palm into suspended attitude: Flip the leading palm upward as the same-side hip shifts into a subtle counter-tilt. Fold one knee into a compact attitude while the opposite leg extends below, then reopen the palm toward the room and settle into a clean vertical line.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): Instrumental; no lyric events in this crop.
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
During the final phrase, the oval frame begins to descend vertically into its integrated stage lift. It does not fall, fold into another object or move by a visible person. It is almost below the deck by the final frame, leaving a dark, clean transition area.
Pair-level transition rule: SEG01 releases the feather once. SEG02 begins on the actual feather trajectory and never replays the release. At the end of SEG02 the oval frame begins descending; SEG03 opens on that same frame already below its former height as the new fins rise.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 12.000 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 2.213s, 5.034s, 7.855s, 10.676s. Local downbeats: 0.803s, 3.624s, 6.445s, 9.266s. Detected high-confidence drum accents: 5.903s hihat; 6.646s snare; 10.338s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 03 — First wonder — a new scale appears

**原曲区间：** 24.000–36.020s · **时长：** 12.020s · **音频：** `seg03_00m24p00s-00m36p02s.mp3`  
**歌词事件：** 6.333–9.000s Morning spills through chapel glass; 9.125–12.000s Golden dust goes drifting past

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg03_00m24p00s-00m36p02s.mp3` from 24.000s to 36.020s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 12.020 seconds.

summary:

[reference generation + audio reuse] Create an exact 12.020-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT I — Curiosity becomes wonder. Emotional objective: She reacts to the first expansion of the stage with curiosity rather than literal surprise acting. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT I — Curiosity becomes wonder. The performer's immediate objective is: She reacts to the first expansion of the stage with curiosity rather than literal surprise acting.
Emotional movement: curiosity, discovery and a growing sense of possibility. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Two slim sculptural stage fins and one shallow curved upper rib rise directly from separate concealed floor lifts. Their surfaces are matte charcoal with subtle pearl reflections. They form an abstract asymmetrical composition, not stained glass, shelves, books, a window or any literal lyric object.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Cool neutral side light gradually receives a restrained champagne highlight; maintain the soft face key. The fins catch moving light only when the camera angle changes.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The oval frame from the prior scene has lowered out of view; the first two vertical fins are rising behind her. She is still drifting slightly toward camera-left from SEG02.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Open on a tight close-up of that same open palm near the sternum. Continue the unfinished wrist rotation so the palm turns outward; let the fingertips lead the movement. Rack focus from the palm to the first rising scenic fin behind her shoulder, then tilt to her eyes as she registers the change. Do not begin with a medium-full view. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:01.497, The camera makes a short lateral slider move, letting the second fin cross behind her in parallax. She opens one arm sideways, then lets the opposite arm follow in a delayed wave. Her torso makes a gentle side spiral while the pelvis keeps the vertical axis stable.
[Shot 3] At 00:04.318, She draws one knee upward into a compact attitude, extends the lower leg diagonally, then returns to a long pointed line. Her arms counterbalance at different heights. The fins catch a pale moving highlight but do not display pictures or symbols.
[Shot 4] At 00:07.139, The camera moves from three-quarter to a clean frontal medium-full view. She completes the movement with a quiet open-chest extension as the upper rib settles into place. End with her eyes following the light across the fins. For the final 0.5 seconds, let the camera travel from the medium-full composition into a close detail of her eyes. Her gaze continues tracking the moving fin light in one clear screen direction; keep the eye movement active through the final frame.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Breath-led noticing; C2 + B8 — Figure-eight arms with a staggered torso ripple; C12 — Suspended attitude exchange; G1 LINE — Full extension and gaze lock.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–01.497s | C1 — Breath-led noticing: A small inhale lifts the sternum and lengthens the neck; the head turns only after the eyes register the rising scenic fin. The lower body stays in a long, pointed vertical line, preserving the existing suspended state.
01.497–04.318s | C2 + B8 — Figure-eight arms with a staggered torso ripple: One arm sweeps high while the other travels low, then both pass through a horizontal figure-eight. The ripple travels from shoulders through ribs to waist; the pelvis counterbalances rather than following the arms as a rigid block.
04.318–07.139s | C12 — Suspended attitude exchange: Draw one knee into a compact front attitude, extend its lower leg diagonally, then fold it back as the opposite leg lengthens beneath the pelvis. The arms stay at unequal heights to counterbalance the leg change; this is an unsupported floating balance, not a demi-pointe stand.
07.139–12.020s | G1 LINE — Full extension and gaze lock: Lengthen one arm laterally and the opposite leg downward into a clear opposing diagonal. Extend through the spine and ribs without arching the lower back; the head and eyes complete the line last, then the chest settles into the outgoing open shape.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 6.333–9.000s Morning spills through chapel glass; 9.125–12.000s Golden dust goes drifting past
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. The camera moves from three-quarter to a clean frontal medium-full view. She completes the movement with a quiet open-chest extension as the upper rib settles into place. End with her eyes following the light across the fins. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG03 and SEG04 share the same two fins and upper rib. SEG04 ends with them rotating edge-on and descending; SEG05 opens on their last visible edge while the three translucent planes rise from the deck.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 12.020 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 1.497s, 4.318s, 7.139s, 9.960s. Local downbeats: 0.087s, 2.908s, 5.729s, 8.550s, 11.371s. Detected high-confidence drum accents: 2.030s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 04 — The world opens — controlled release

**原曲区间：** 36.020–47.332s · **时长：** 11.312s · **音频：** `seg04_00m36p02s-00m47p33s.mp3`  
**歌词事件：** 0.021–2.563s Every book's a secret door; 2.771–5.313s Every page reveals one more; 5.313–10.563s And the whole wide sky begins to sing

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg04_00m36p02s-00m47p33s.mp3` from 36.020s to 47.332s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 11.312 seconds.

summary:

[reference generation + audio reuse] Create an exact 11.312-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT I — Curiosity becomes wonder. Emotional objective: Curiosity expands into an expressive, unguarded release. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT I — Curiosity becomes wonder. The performer's immediate objective is: Curiosity expands into an expressive, unguarded release.
Emotional movement: curiosity, discovery and a growing sense of possibility. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Two slim sculptural stage fins and one shallow curved upper rib rise directly from separate concealed floor lifts. Their surfaces are matte charcoal with subtle pearl reflections. They form an abstract asymmetrical composition, not stained glass, shelves, books, a window or any literal lyric object.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Cool neutral side light gradually receives a restrained champagne highlight; maintain the soft face key. The fins catch moving light only when the camera angle changes.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue from SEG03 with the same front-facing axis, one arm still open and the eyes following the fin light. The stage fins remain in the same positions.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Cut directly into a close-up of the same eyes and continuing gaze direction from <Picture 2>. Hold the eye-line for a brief instant, then follow it with a controlled pan toward the raised hand as it begins the vertical-circle pathway. Reveal the hand, shoulder and upper chest in sequence; the opening arm circle is already in progress, not a new pose. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.583, She folds the raised arm across her chest, rotates through the ribs, and opens the other arm in the opposite direction. One leg lengthens to the side in a controlled développé and returns through a pointed cross. Her torso remains mostly upright.
[Shot 3] At 00:06.404, A short counter-track moves against her arm sweep, giving the fins visible parallax without rotating the camera around a static performer. She completes a smooth vertical-axis half-turn, head spotting late, then re-finds the lens.
[Shot 4] At 00:09.225, The fins rotate edge-on and begin lowering. She lets both arms descend in a controlled release while her gaze follows the narrowing light. End on a softly open chest and one hand extended, with the next scenic lift only beginning to appear. In the final 0.55 seconds, follow the extended hand until its diagonal fingertips become the clear visual landing point. Keep the fingers reaching along the same diagonal while the fins continue their edge-on descent behind her.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C3 — Vertical circle and upper-chest lift; A15 + C5 — Cross, open, and counter-twist; C16 adaptation — Back-to-front upper-body passage; G2 Off-axis Tilt + G1 LINE — Controlled side inclination.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.583s | C3 — Vertical circle and upper-chest lift: One arm draws a continuous vertical circle from in front of the torso to above the crown. The sternum lifts and the upper back extends gently as the head follows the raised hand; keep the movement distributed through the upper spine, not a deep lumbar backbend.
03.583–06.404s | A15 + C5 — Cross, open, and counter-twist: Cross the forearms once across the chest and open them sharply to opposing sides. As the arms separate, rotate the ribs one way and the pelvis the other, creating a clear spiral through the waist while one pointed leg extends laterally.
06.404–09.225s | C16 adaptation — Back-to-front upper-body passage: Carry the leading hand across the face line, thread the opposite palm beneath it, and rotate the shoulders through a controlled half-turn. Adapt only the arm pathway and upper-body facing change from C16; omit its floor-supported cover step and do not add a second turn.
09.225–11.312s | G2 Off-axis Tilt + G1 LINE — Controlled side inclination: Incline the torso slightly away from the extended leg while the pelvis counterbalances beneath the ribs. The lower body remains vertical and pointed; recover through the waist and chest into a long, open diagonal as the scenic fins lower.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.021–2.563s Every book's a secret door; 2.771–5.313s Every page reveals one more; 5.313–10.563s And the whole wide sky begins to sing
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The two fins and upper rib begin lowering into their individual floor lifts on the final musical phrase. Their reflections narrow to two thin vertical lines before disappearing.
Pair-level transition rule: SEG03 and SEG04 share the same two fins and upper rib. SEG04 ends with them rotating edge-on and descending; SEG05 opens on their last visible edge while the three translucent planes rise from the deck.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 11.312 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.762s, 3.583s, 6.404s, 9.225s. Local downbeats: 2.172s, 4.993s, 7.814s, 10.635s. Detected high-confidence drum accents: No high-confidence isolated drum accent specified; use only the supplied phrase/downbeat grid.. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 05 — Awe — the performance blooms

**原曲区间：** 47.332–61.333s · **时长：** 14.001s · **音频：** `seg05_00m47p33s-01m01p33s.mp3`  
**歌词事件：** 0.126–2.668s Ancient voices call to me; 2.668–4.876s like starlight through the air; 5.459–7.459s The heavens smile; 7.459–10.543s a thousand colors bloom everywhere; 11.334–12.709s I see a thousand lights; 12.709–14.001s Inside the words they tried to hide

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg05_00m47p33s-01m01p33s.mp3` from 47.332s to 61.333s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 14.001 seconds.

summary:

[reference generation + audio reuse] Create an exact 14.001-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT II — Inner scale expands. Emotional objective: She moves from wonder into exhilaration as the stage gains depth and color. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT II — Inner scale expands. The performer's immediate objective is: She moves from wonder into exhilaration as the stage gains depth and color.
Emotional movement: wonder widening into joyful release. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Three translucent vertical planes rise from the stage deck at staggered depths. Each is narrow enough to remain behind the performer in medium framing. The planes have no text, symbols, pages, stars or pictures; they catch layered light and create depth through parallax.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Soft pearl-white front fill with controlled amber and pale blue edge separation. The planes brighten in sequence, not all at once.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The previous fins have descended; three translucent planes rise at staggered depth. Her extended hand from SEG04 is still moving outward.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Begin with a tight close-up of the same extended hand and diagonal fingertips. Continue the outward reach for a fraction of a second, then let the camera trace backward along the forearm to the shoulder blades as the full torso wave begins. Open into a subject-dominant medium-full frame only after the wave has visibly passed through the upper body. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.555, She performs a linked leg phrase: one knee lifts into attitude, the lower leg unfolds into a pointed diagonal, then the other leg crosses beneath in a soft scissor exchange. Arms travel through a high-low port de bras, never repeating the same curve twice.
[Shot 3] At 00:06.376, The camera slides between the visual edges of the planes while keeping her face and torso unobstructed. She pivots around her vertical axis, opening the arms to decelerate; the translucent surfaces brighten in sequence, creating layered depth rather than literal images.
[Shot 4] At 00:09.197, On the final phrase she reaches into the space between the planes, then pulls the hand back toward her heart. End in a strong but relaxed three-quarter orientation, with the planes still rising in the background. During the final 0.55 seconds, reframe onto the hand she has drawn back toward her heart. The palm remains close to the sternum; the fingers begin to uncurl as the body holds its three-quarter line. Cut before the hand fully releases.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: B8 — Full torso wave; C12 + G1 LINE — Attitude to long diagonal; C5 + G2 Spiral — Spiral pivot and open brake; G1 LINE — Reach, recoil, and heart line.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.555s | B8 — Full torso wave: Initiate at the shoulder blades, ripple through sternum and ribs, then carry the wave to the waist and pelvis. Let the arms follow in an asymmetrical high-low pattern, with the second arm arriving a half-count later rather than repeating the first curve.
03.555–06.376s | C12 + G1 LINE — Attitude to long diagonal: Lift one knee into a compact attitude, lengthen the lower leg into a pointed diagonal, then draw the opposite leg through a narrow cross beneath the pelvis. The arms make a high-low counterline; finish with a fully extended leg line and a steady head-up axis.
06.376–09.197s | C5 + G2 Spiral — Spiral pivot and open brake: Preload through the ribs, spiral the chest into a small three-quarter orientation, and let the pelvis follow with delayed counter-rotation. Open the arms asymmetrically to decelerate; keep this a partial pivot, not a full spin.
09.197–14.001s | G1 LINE — Reach, recoil, and heart line: Extend one hand into the space between the scenic planes, then draw the elbow back toward the sternum while the opposite arm lengthens behind. The chest remains lifted and the feet stay pointed below; hold the three-quarter line as the planes continue rising.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.126–2.668s Ancient voices call to me; 2.668–4.876s like starlight through the air; 5.459–7.459s The heavens smile; 7.459–10.543s a thousand colors bloom everywhere; 11.334–12.709s I see a thousand lights; 12.709–14.001s Inside the words they tried to hide
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. On the final phrase she reaches into the space between the planes, then pulls the hand back toward her heart. End in a strong but relaxed three-quarter orientation, with the planes still rising in the background. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG05 and SEG06 share the same three planes. SEG06 ends with the planes turning edge-on and descending; SEG07 opens with the crescent frame rising into the newly cleared background.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 14.001 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.734s, 3.555s, 6.376s, 9.197s, 12.018s. Local downbeats: 2.144s, 4.965s, 7.786s, 10.607s, 13.428s. Detected high-confidence drum accents: 10.764s hihat; 11.113s snare; 12.181s hihat; 12.715s hihat; 13.597s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 06 — Joy — full-body release

**原曲区间：** 61.333–76.269s · **时长：** 14.936s · **音频：** `seg06_01m01p33s-01m16p27s.mp3`  
**歌词事件：** 0.000–2.708s A hundred thousand tales unfold; 2.708–5.583s Each page a universe of gold; 5.583–7.875s I see a thousand lights; 8.292–11.250s They turn the darkest night to day; 11.250–14.375s I've read a thousand spells

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg06_01m01p33s-01m16p27s.mp3` from 61.333s to 76.269s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 14.936 seconds.

summary:

[reference generation + audio reuse] Create an exact 14.936-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT II — Inner scale expands. Emotional objective: Awe becomes joyful certainty and the dance takes over the scene. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT II — Inner scale expands. The performer's immediate objective is: Awe becomes joyful certainty and the dance takes over the scene.
Emotional movement: wonder widening into joyful release. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Three translucent vertical planes rise from the stage deck at staggered depths. Each is narrow enough to remain behind the performer in medium framing. The planes have no text, symbols, pages, stars or pictures; they catch layered light and create depth through parallax.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Soft pearl-white front fill with controlled amber and pale blue edge separation. The planes brighten in sequence, not all at once.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue the three-quarter orientation and hand-to-heart motion from SEG05; all three panels are already fully raised.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Start on a tight close-up of the same hand at the heart. The fingers uncurl and the hand leaves the chest along the same path, becoming the first visible motion of the open-arm release. Track from hand to wrist to elbow and shoulder, then reveal the expanding chest and the full suspended arm line. Do not restart from a full-body pose. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.659, She executes a clear aerial leg sequence: right knee lifts, lower leg lengthens to the side, the leg folds through attitude, then extends downward into a long pointed line. The opposite leg counterbalances; there is no jump or contact with the stage deck.
[Shot 3] At 00:06.480, She completes one clean upright-axis turn, using compact crossed legs to gather speed and opening both arms to slow. The camera counters with a short opposite-side move, but does not perform an independent orbit or roll.
[Shot 4] At 00:09.301, The planes begin turning edge-on as she finishes in a high diagonal arm line. She lets the wrists release and the shoulders soften while the set lowers. End with one arm still extended, carrying its direction into SEG07. For the final 0.55 seconds, follow the wrist of the still-extended high diagonal arm. Let the fingers complete one soft release while the arm remains lifted; land the final frame on the hand rather than the full-body silhouette.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: A13 — Open-arm release; C12 — Attitude, extension, and scissor recovery; G1 TURN + C7 — One complete upright-axis turn; G3 Hero Lock + G1 LINE — High diagonal release.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.659s | A13 — Open-arm release: Begin from the inherited hand-near-chest state. Cross the forearms low for one beat, then sweep them outward into a broad, unequal port de bras; the sternum rises first and the waist follows with a delayed spiral.
03.659–06.480s | C12 — Attitude, extension, and scissor recovery: Lift the right knee into a clear attitude, extend the lower leg sideways, fold it back through attitude, then lengthen it downward into a pointed line. The opposite leg counterbalances and passes through one controlled scissor exchange; do not add a hop or landing.
06.480–09.301s | G1 TURN + C7 — One complete upright-axis turn: Gather the legs into a compact crossed line and draw the elbows slightly inward to establish one vertical body axis. Initiate the single 360-degree pivot from the torso and pelvis as both arms open to regulate angular momentum; spot the head once, complete the turn facing the established front direction, then widen the arms to brake. This is the first of only two complete turns in the full performance.
09.301–14.936s | G3 Hero Lock + G1 LINE — High diagonal release: Let the rotation's remaining momentum travel into one high diagonal arm line and one long pointed leg line. Lock the chest and gaze on the musical accent, then release only the wrists and shoulders as the scenic planes begin turning edge-on.
Rotation budget: this is one of the two and only two complete upright-axis rotations in the full performance. Complete the single turn once, decelerate visibly and leave the body on the specified outgoing line.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.000–2.708s A hundred thousand tales unfold; 2.708–5.583s Each page a universe of gold; 5.583–7.875s I see a thousand lights; 8.292–11.250s They turn the darkest night to day; 11.250–14.375s I've read a thousand spells
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The three vertical planes rotate slightly edge-on and descend together, leaving their light traces to fade before the next act.
Pair-level transition rule: SEG05 and SEG06 share the same three planes. SEG06 ends with the planes turning edge-on and descending; SEG07 opens with the crescent frame rising into the newly cleared background.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 14.936 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.838s, 3.659s, 6.480s, 9.301s, 12.122s. Local downbeats: 2.248s, 5.069s, 7.890s, 10.712s, 13.533s. Detected high-confidence drum accents: 0.130s hihat; 1.013s hihat; 2.406s hihat; 3.822s hihat; 4.356s hihat; 5.239s hihat; 6.655s hihat; 8.420s hihat; 11.415s hihat; 12.297s hihat; 14.062s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 07 — Vulnerability — the outward motion quiets

**原曲区间：** 76.269–86.525s · **时长：** 10.256s · **音频：** `seg07_01m16p27s-01m26p53s.mp3`  
**歌词事件：** 0.522–5.731s But love's the one no book can tell

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg07_01m16p27s-01m26p53s.mp3` from 76.269s to 86.525s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 10.256 seconds.

summary:

[reference generation + audio reuse] Create an exact 10.256-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT III — Vulnerability and acceptance. Emotional objective: She stops performing outwardly for a moment and acknowledges the emotional limit of certainty. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT III — Vulnerability and acceptance. The performer's immediate objective is: She stops performing outwardly for a moment and acknowledges the emotional limit of certainty.
Emotional movement: the outward spectacle contracts into an intimate emotional truth. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
The previous planes are fully below the deck. A single low-profile crescent-shaped vertical scenic rib rises behind the performer. It is open, asymmetrical and non-literal; no room, furniture, book or physical symbol appears.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
A narrow warm follow beam surrounds the performer while the rest of the stage falls into deep charcoal. The beam softens rather than spotlighting a hard circle on the floor.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The planes have lowered; the open crescent frame rises behind her. The extended arm from SEG06 remains lifted and starts to soften.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Open in a tight close-up of that same raised wrist and fingertips. Continue the small finger release, then let the hand descend along the same path. The camera follows the forearm toward the chest and settles on her face as the breath-led contraction begins. Preserve the restrained energy; do not cut straight to a full-body view. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:02.828, During the selected lyric window, she performs only the chosen line with precise, restrained mouth movement: <Subject 1> (S1) sings <d>[English] But love's the one no book can tell</d>. Keep the mouth unobstructed and the face stable; do not continue lip-sync outside this window.
[Shot 3] At 00:05.649, As the phrase resolves, her palm rests over the heart area, then slides away into an open hand. One shoulder turns inward, followed by a small rib contraction and a gradual release. The camera makes a very slow lateral drift, not a push-in that changes face size abruptly.
[Shot 4] At 00:08.470, She lifts her gaze and opens the free arm toward the side, still restrained. The crescent's warm edge dims, leaving a soft central key. End with her palm open at chest height and a calm, vulnerable expression. In the final 0.55 seconds, let the camera land on the open palm at chest height. The fingertips relax and the palm turns subtly toward the viewer, leaving the gesture alive rather than frozen.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Breath contraction; G4 Contemporary / Contraction to Spiral; G2 Off-axis Tilt + B8 — Shallow inclination and ripple release; C2 — Quiet cloud-arm continuation.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–02.828s | C1 — Breath contraction: Let the chest soften inward on the exhale; the head follows with a small downward inclination, then the spine lengthens again on the next inhale. Keep the motion private and restrained, with the lower body suspended and stable.
02.828–05.649s | G4 Contemporary / Contraction to Spiral: Fold one forearm across the ribs as the sternum contracts, then let the elbow lead a gradual spiral through the chest and waist. The pelvis follows a fraction later and the free arm lengthens away, creating visible push-pull tension without a floor drop.
05.649–08.470s | G2 Off-axis Tilt + B8 — Shallow inclination and ripple release: Allow the torso to incline slightly off its vertical axis while the pelvis and extended leg counterbalance. Reverse the motion through a small shoulder-to-rib wave, allowing the open palm to drift away from the heart; do not let the body become horizontal.
08.470–10.256s | C2 — Quiet cloud-arm continuation: Trace one small horizontal figure-eight close to the chest, one arm rising as the other lowers. Reduce the arm radius and let the final loop resolve into an open palm at chest height, with the head upright and gaze lifted.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.522–5.731s But love's the one no book can tell
Selected lip-sync only: 00:00.522–00:05.731, <Subject 1> (S1) sings <d>[English] But love's the one no book can tell</d>. Mouth movement ends with the source phrase; no lip-sync outside this window.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. She lifts her gaze and opens the free arm toward the side, still restrained. The crescent's warm edge dims, leaving a soft central key. End with her palm open at chest height and a calm, vulnerable expression. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG07 and SEG08 share the crescent frame and intimate light. SEG08 ends as the crescent lowers and the curved reflectors begin to appear; SEG09 opens on those reflectors continuing upward.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 10.256 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.007s, 2.828s, 5.649s, 8.470s. Local downbeats: 1.418s, 4.239s, 7.060s, 9.881s. Detected high-confidence drum accents: 0.171s other; 0.705s other; 3.352s hihat; 3.700s hihat; 5.117s snare; 6.185s snare; 7.230s snare; 8.995s hihat; 9.529s hihat; 9.877s hihat; 10.063s snare. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 08 — Acceptance — emotion turns into light

**原曲区间：** 86.525–98.146s · **时长：** 11.621s · **音频：** `seg08_01m26p53s-01m38p15s.mp3`  
**歌词事件：** 0.016–1.100s Ah —; 6.016–7.308s All the secrets in my mind; 7.308–9.016s Still leave wonders left to find; 9.183–11.516s Even tears can turn to light

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg08_01m26p53s-01m38p15s.mp3` from 86.525s to 98.146s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 11.621 seconds.

summary:

[reference generation + audio reuse] Create an exact 11.621-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT III — Vulnerability and acceptance. Emotional objective: The vulnerability becomes acceptance without melodramatic crying or literal visual metaphors. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT III — Vulnerability and acceptance. The performer's immediate objective is: The vulnerability becomes acceptance without melodramatic crying or literal visual metaphors.
Emotional movement: the outward spectacle contracts into an intimate emotional truth. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
The previous planes are fully below the deck. A single low-profile crescent-shaped vertical scenic rib rises behind the performer. It is open, asymmetrical and non-literal; no room, furniture, book or physical symbol appears.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
A narrow warm follow beam surrounds the performer while the rest of the stage falls into deep charcoal. The beam softens rather than spotlighting a hard circle on the floor.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue with the palm open at chest height and the same intimate light; the crescent frame is still present.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Begin with a close-up of the same open palm at chest height. Continue the slight outward turn; the fingers lengthen naturally, not into a new symbol. Rack focus from the fingertips to her eyes as the measured inhale begins, then ease into a close-medium portrait that keeps the hand and face connected. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.856, The camera eases sideways to reveal her shoulder line as both arms make a flowing low-to-high port de bras. The chest opens, the ribs follow, and the waist creates a small counter-spiral. Her legs remain in a vertical crossed line with pointed feet.
[Shot 3] At 00:06.677, She raises one knee, extends the foot outward, then returns it through a smooth attitude transition. The opposite arm lengthens to counterbalance. A small warm reflection travels along the crescent frame in response to the movement; no particles or lyric objects appear.
[Shot 4] At 00:09.498, The stage crescent lowers into the deck. She lets both arms widen and turns her eyes toward the unseen audience, shifting from inward reflection to a warmer connection. End with shoulders open and the movement still flowing. For the final 0.5 seconds, reframe to a close detail of her eyes as they turn toward the unseen audience. Keep the gaze traveling gently across the same side of frame; do not show an audience insert.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Inhale and chest expansion; C3 + C2 — Vertical circle into horizontal cloud hands; C12 — Attitude to outward extension; G1 LINE — Wide acceptance line.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.856s | C1 — Inhale and chest expansion: Begin with a measured inhalation: sternum rises, ribs widen, and the spine lengthens without an exaggerated back arch. The eyes soften first; the arms remain relaxed, preserving the intimate start.
03.856–06.677s | C3 + C2 — Vertical circle into horizontal cloud hands: Sweep one arm upward through a vertical circle, then let the other join in a flowing horizontal figure-eight. The chest opens after the hands pass overhead; the waist makes a small counter-spiral and both legs stay in a narrow pointed cross.
06.677–09.498s | C12 — Attitude to outward extension: Raise one knee into a compact attitude, extend the foot outward along a diagonal, then return through the same controlled path. The opposite arm reaches away to counterbalance; do not add a jump, landing or abrupt leg kick.
09.498–11.621s | G1 LINE — Wide acceptance line: Open both arms to unequal heights and lengthen one leg below the pelvis. The sternum stays lifted, the head turns toward the unseen room only after the arms reach their endpoint, and the body finishes in a clear upright line.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.016–1.100s Ah —; 6.016–7.308s All the secrets in my mind; 7.308–9.016s Still leave wonders left to find; 9.183–11.516s Even tears can turn to light
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The crescent rib retracts into the deck. A pair of small curved reflectors begins to rise at the back edge, visible only as a slim highlight in the outgoing frame.
Pair-level transition rule: SEG07 and SEG08 share the crescent frame and intimate light. SEG08 ends as the crescent lowers and the curved reflectors begin to appear; SEG09 opens on those reflectors continuing upward.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 11.621 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 1.035s, 3.856s, 6.677s, 9.498s. Local downbeats: 2.446s, 5.267s, 8.088s, 10.909s. Detected high-confidence drum accents: 0.155s snare; 1.571s snare; 2.616s snare; 3.336s snare; 4.219s hihat; 4.404s snare; 5.449s hihat; 5.983s hihat; 6.866s hihat; 8.793s other; 9.513s kick; 9.675s other. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 09 — Warmth — an unseen connection

**原曲区间：** 98.146–109.273s · **时长：** 11.127s · **音频：** `seg09_01m38p15s-01m49p27s.mp3`  
**歌词事件：** 0.020–1.479s When a friend is by my side; 1.479–4.854s Warm bread and laughter make the world feel right; 5.729–8.312s Ancient voices call to me; 8.312–10.562s like starlight through the air

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg09_01m38p15s-01m49p27s.mp3` from 98.146s to 109.273s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 11.127 seconds.

summary:

[reference generation + audio reuse] Create an exact 11.127-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT IV — Warmth and connection. Emotional objective: She performs as if sharing a moment with someone just beyond the camera, without creating or showing a second character. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT IV — Warmth and connection. The performer's immediate objective is: She performs as if sharing a moment with someone just beyond the camera, without creating or showing a second character.
Emotional movement: loneliness gives way to warmth, companionship and playful joy. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Two opposing shallow curved reflectors rise directly from the stage deck, one on either side behind the performer. Their inner faces carry warm diffused light, suggesting an embracing space without depicting another person, table, chair, food or literal lyric object.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Warm amber and soft ivory blend around the performer, with the original soft frontal key kept stable. The two reflectors glow in response to her open gestures.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The crescent is down; two curved reflectors are rising. Her arms are already open from SEG08 and her gaze is directed just beside the lens.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Cut to a tight close-up of the same eyes and continuing outward eyeline. Let the gaze finish its small sideward travel, then pan down along that line to the near hand as it turns palm-up in the invitation gesture. Reveal the shoulders and torso after the hand has become the next visual target; no audience faces or silhouettes appear. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.519, The camera tracks across the warm reflector edge while she makes a connected shoulder-to-wrist wave. Her torso remains vertically suspended; the pelvis subtly counter-rotates as one knee folds and the opposite foot lengthens below.
[Shot 3] At 00:06.340, She performs a buoyant but controlled two-part leg phrase: a pointed cross, a small knee lift, and a long release into an extended diagonal. The arms open at different levels to avoid a symmetrical repeated gesture. Warm light slowly fills the scene.
[Shot 4] At 00:09.162, She gives a brief genuine smile toward the unseen audience, then turns her head back to center. End with one hand extended and the other near the heart; the reflectors remain in their established positions. During the final 0.55 seconds, favor the extended offering hand. Let the palm remain open while the wrist starts a small circular turn; keep the other hand near the heart in the softer background.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: B7 — Invitation palm; C2 + B8 — Cloud hands with shoulder-to-waist wave; C12 — Cross, attitude, and long pointed release; A13 + C5 — Open embrace and gentle torso twist.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.519s | B7 — Invitation palm: Turn the near hand palm-up and let the same-side hip shift subtly in the opposite direction. The other arm stays long and low; the head follows the open palm, creating a direct but gentle offering gesture.
03.519–06.340s | C2 + B8 — Cloud hands with shoulder-to-waist wave: The arms trace a horizontal figure-eight at chest height, one rising as the other sinks. Carry a single staggered ripple through shoulders, ribs and waist; keep the pelvis counter-rotating rather than swaying as a block.
06.340–09.162s | C12 — Cross, attitude, and long pointed release: Pass one pointed foot across the other, lift the free knee into attitude, then lengthen the leg into a clean diagonal below the pelvis. The arms open at different levels to frame the leg line without becoming another symmetrical gesture.
09.162–11.127s | A13 + C5 — Open embrace and gentle torso twist: Cross the arms low once, sweep them outward, and turn the ribs a small amount toward the offering hand while the pelvis counterbalances. Return the head to center and preserve one hand extended with the other near the heart.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.020–1.479s When a friend is by my side; 1.479–4.854s Warm bread and laughter make the world feel right; 5.729–8.312s Ancient voices call to me; 8.312–10.562s like starlight through the air
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. She gives a brief genuine smile toward the unseen audience, then turns her head back to center. End with one hand extended and the other near the heart; the reflectors remain in their established positions. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG09 and SEG10 share the two warm curved reflectors. SEG10 ends as they descend and the two angled fins emerge; SEG11 opens with the fins continuing their rise.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 11.127 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.698s, 3.519s, 6.340s, 9.162s. Local downbeats: 2.109s, 4.930s, 7.751s, 10.572s. Detected high-confidence drum accents: 0.005s kick; 0.701s kick; 0.887s hihat; 1.421s kick; 1.584s kick; 1.932s kick; 2.280s hihat; 3.348s kick; 3.697s hihat; 4.417s hihat; 5.113s hihat; 6.530s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 10 — Shared joy — a brighter dance phrase

**原曲区间：** 109.273–120.816s · **时长：** 11.543s · **音频：** `seg10_01m49p27s-02m00p82s.mp3`  
**歌词事件：** 0.018–1.977s The heavens smile; 1.977–5.060s a thousand colors bloom everywhere; 5.102–5.852s Ah —; 5.852–7.060s I see a thousand lights; 7.060–8.477s Inside the words they tried to hide; 8.477–11.518s A hundred thousand tales unfold

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg10_01m49p27s-02m00p82s.mp3` from 109.273s to 120.816s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 11.543 seconds.

summary:

[reference generation + audio reuse] Create an exact 11.543-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT IV — Warmth and connection. Emotional objective: Warmth becomes playful confidence and a more expansive dance performance. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT IV — Warmth and connection. The performer's immediate objective is: Warmth becomes playful confidence and a more expansive dance performance.
Emotional movement: loneliness gives way to warmth, companionship and playful joy. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Two opposing shallow curved reflectors rise directly from the stage deck, one on either side behind the performer. Their inner faces carry warm diffused light, suggesting an embracing space without depicting another person, table, chair, food or literal lyric object.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Warm amber and soft ivory blend around the performer, with the original soft frontal key kept stable. The two reflectors glow in response to her open gestures.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue the outward hand line and centered gaze from SEG09; both curved reflectors remain raised.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Open on a tight local close-up of the same extended offering hand and palm. Continue the wrist circle, then track the hand as it joins the opposite arm in the high-low figure-eight. Let the second arm enter the frame naturally and widen to the upper body as the two arm pathways exchange levels. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.677, She draws both legs into a compact crossed line, opens one knee into attitude, then lengthens the other leg into a pointed side extension. The torso counterbalances with a smooth S-shaped curve while remaining predominantly upright.
[Shot 3] At 00:06.498, A brief foreground pass of the nearest reflector creates a soft wipe without hiding her face. She rotates a quarter turn, lets the existing flowing elements respond with delayed buoyancy, then returns to front three-quarter. The camera settles as her arms reach their widest expressive line.
[Shot 4] At 00:09.319, The reflectors begin descending. She closes the phrase by drawing both hands toward the chest and opening them again, now with a more grounded emotional certainty. End with a lifted gaze and a clean three-quarter body line. In the final 0.55 seconds, move into a close insert of the fingertips as both hands reopen from the chest. The near fingertips separate and travel outward; preserve the lifted gaze just beyond the top edge of the detail.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C2 + A15 — High-low arm figure-eight into X-open; C12 — Crossed-leg to attitude line; C5 + G2 Spiral — Quarter pivot with torso spiral; B7 + G1 LINE — Certain open-palmed finish.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.677s | C2 + A15 — High-low arm figure-eight into X-open: Sweep one arm above the chest while the other circles low, exchanging levels through a continuous figure-eight. Bring the forearms together once into a chest-level X, then release into a wide horizontal opening; keep the shoulders and ribs involved, not only the wrists.
03.677–06.498s | C12 — Crossed-leg to attitude line: Gather both legs into a narrow pointed cross, lift one knee into attitude, then lengthen the opposite leg sideways into a pointed extension. The rib cage inclines subtly away from the extended leg to create a balanced S-line.
06.498–09.319s | C5 + G2 Spiral — Quarter pivot with torso spiral: Turn the rib cage through a small quarter orientation while the pelvis counter-rotates, then unwind toward front three-quarter. The arms widen to their largest line as the spiral resolves; do not add a complete spin.
09.319–11.543s | B7 + G1 LINE — Certain open-palmed finish: Draw both hands toward the sternum, then send one palm outward and the other along a high diagonal. Extend one pointed leg beneath the pelvis and hold the lifted gaze as the reflectors descend.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.018–1.977s The heavens smile; 1.977–5.060s a thousand colors bloom everywhere; 5.102–5.852s Ah —; 5.852–7.060s I see a thousand lights; 7.060–8.477s Inside the words they tried to hide; 8.477–11.518s A hundred thousand tales unfold
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The curved reflectors slowly lower into the deck while the warm light narrows. A pair of tall angled fins begins to emerge behind them.
Pair-level transition rule: SEG09 and SEG10 share the two warm curved reflectors. SEG10 ends as they descend and the two angled fins emerge; SEG11 opens with the fins continuing their rise.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 11.543 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.856s, 3.677s, 6.498s, 9.319s. Local downbeats: 2.266s, 5.087s, 7.908s, 10.729s. Detected high-confidence drum accents: 1.045s hihat; 2.461s hihat; 2.995s kick; 3.158s hihat; 4.574s hihat; 6.688s hihat; 10.031s other. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 11 — Inner conflict — light and shadow meet

**原曲区间：** 120.816–132.763s · **时长：** 11.947s · **音频：** `seg11_02m00p82s-02m12p76s.mp3`  
**歌词事件：** 1.142–5.600s Each page a universe of gold; 5.600–6.850s I see a thousand lights; 6.850–8.184s They turn the darkest night to day; 8.184–10.642s I've read a thousand spells

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg11_02m00p82s-02m12p76s.mp3` from 120.816s to 132.763s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 11.947 seconds.

summary:

[reference generation + audio reuse] Create an exact 11.947-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT V — Inner conflict becomes clarity. Emotional objective: Her confidence is tested by an inward hesitation, then she chooses to continue. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT V — Inner conflict becomes clarity. The performer's immediate objective is: Her confidence is tested by an inward hesitation, then she chooses to continue.
Emotional movement: a brief inward struggle resolves into calm conviction. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Two tall angled fins rise from concealed deck lifts and pivot toward one another, leaving a clear open gap behind the performer. Their faces are dark and non-reflective; light travels across their edges. They are abstract theatrical architecture, not pages, a book or a literal object.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Begin with a cool/warm split across the background, then gradually converge into one balanced warm-white field while keeping the performer clearly separated.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The warm reflectors are lowering; two angled fins emerge. Her hands are opening from the chest as the previous phrase continues.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Start in a tight close-up of the same fingertips and hands continuing to separate from the chest. Follow the near hand outward, then rack focus to her eyes as one arm advances and the other remains closer to the body, revealing the push-pull line. The X-to-open dance phrase continues; no fresh arm cross is added. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.418, She contracts through the ribs, folds one forearm across the torso, and turns her shoulder away. After a short held beat, she releases the elbow and rotates the chest back toward camera. Keep the emotion internal; no literal struggle or pantomime.
[Shot 3] At 00:06.239, The camera slides across the narrow gap between the fins while she extends one leg into a long diagonal and draws it back through a pointed cross. Her arms separate to either side, making the body line visibly larger.
[Shot 4] At 00:09.060, The fins open outward as the lighting converges into a balanced warm-white state. She completes the phrase with both arms extended at unequal heights, gaze steady. End with the torso already turning toward the central axis. For the final 0.5 seconds, carry the camera into a close detail of her eyes as the torso turns toward the central axis. Let the gaze complete the same inward travel while the unequal arm line remains in motion outside the tight frame.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: A15 + B8 — Crossed tension into staggered wave; G4 Contemporary / Contraction to Spiral; G2 Off-axis Tilt + G1 LINE — Diagonal extension; G3 Accent Lock — Asymmetric open line.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.418s | A15 + B8 — Crossed tension into staggered wave: Bring the forearms into one firm chest-level X, then separate them unevenly—one arm high, one low. A single body wave travels from the shoulder girdle through sternum and ribs into the waist, with no repeated rocking.
03.418–06.239s | G4 Contemporary / Contraction to Spiral: Contract the ribs and draw one forearm across the torso; rotate the chest away from camera, then release the elbow and spiral the sternum back toward the lens. The pelvis follows with a delayed counter-turn, preserving the internal conflict without mimed struggle.
06.239–09.060s | G2 Off-axis Tilt + G1 LINE — Diagonal extension: Extend one leg into a long diagonal and incline the torso slightly away from it. The opposite arm reaches outward to counterbalance; the waist and shoulder line lengthen before the body returns toward vertical.
09.060–11.947s | G3 Accent Lock — Asymmetric open line: Open both arms at unequal heights and stop the chest cleanly on the accent. Let only the wrists retain a trace of motion while the gaze settles; the torso already begins a small turn toward the central axis for the next segment.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 1.142–5.600s Each page a universe of gold; 5.600–6.850s I see a thousand lights; 6.850–8.184s They turn the darkest night to day; 8.184–10.642s I've read a thousand spells
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. The fins open outward as the lighting converges into a balanced warm-white state. She completes the phrase with both arms extended at unequal heights, gaze steady. End with the torso already turning toward the central axis. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG11 and SEG12 share the two angled fins. SEG12 ends as they pivot outward and descend; SEG13 opens on the single open curved frame continuing up from the deck.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 11.947 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.597s, 3.418s, 6.239s, 9.060s, 11.881s. Local downbeats: 2.007s, 4.828s, 7.649s, 10.470s. Detected high-confidence drum accents: 0.787s other; 3.596s other; 4.131s other; 5.013s other; 5.361s other; 8.357s other; 9.239s other; 10.655s other. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 12 — Clarity — a quiet declaration

**原曲区间：** 132.763–145.000s · **时长：** 12.237s · **音频：** `seg12_02m12p76s-02m25p00s.mp3`  
**歌词事件：** 0.487–5.653s But love's the one no book can tell

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg12_02m12p76s-02m25p00s.mp3` from 132.763s to 145.000s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 12.237 seconds.

summary:

[reference generation + audio reuse] Create an exact 12.237-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT V — Inner conflict becomes clarity. Emotional objective: The inner debate resolves into a simple, emotionally clear decision. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT V — Inner conflict becomes clarity. The performer's immediate objective is: The inner debate resolves into a simple, emotionally clear decision.
Emotional movement: a brief inward struggle resolves into calm conviction. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Two tall angled fins rise from concealed deck lifts and pivot toward one another, leaving a clear open gap behind the performer. Their faces are dark and non-reflective; light travels across their edges. They are abstract theatrical architecture, not pages, a book or a literal object.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Begin with a cool/warm split across the background, then gradually converge into one balanced warm-white field while keeping the performer clearly separated.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue the torso turn from SEG11; the angled fins are now held open and the warm-white light has settled.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Open on a close-up of the same eyes in three-quarter profile. Continue the gaze toward center; the camera glides across the face toward a frontal three-quarter view, then reveals the shoulder release and quiet breath alignment. Keep the face sharp and unobstructed; do not begin at medium distance. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:02.755, During 00:00.487–00:05.653, she performs only the chosen vocal phrase with restrained, readable lip-sync: <Subject 1> (S1) sings <d>[English] But love's the one no book can tell</d>. Do not add mouth movement before or after the exact window; let the remaining vocal tail play over her stillness and eye-line.
[Shot 3] At 00:05.576, After the vocal phrase, she turns her palm upward and lets the wrist roll open. The movement passes from shoulder through elbow, wrist and fingers, while the opposite arm slowly extends behind as a counterline. The camera tracks a short arc outside her shoulder without crossing the established axis.
[Shot 4] At 00:08.397, The fins pivot away and descend. She makes a small vertical-axis turn and returns to a calm front three-quarter line, both feet pointed in a narrow stagger. As her attention moves toward the center of the stage, let one arm lengthen in the same direction and lead with the fingertips. In the final 0.55 seconds, bring the camera onto those reaching fingertips; they travel inward by a small amount, leaving the reach unfinished at the cut.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Quiet breath-led alignment; C2 — Restrained cloud-arm phrase; C3 — Vertical arm circle and chest lift; C12 + G1 LINE — Floating balance into front three-quarter.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–02.755s | C1 — Quiet breath-led alignment: Let the chest round slightly on the exhale and lengthen one vertebra at a time on the inhale. Keep the neck and face relaxed; the body remains in its narrow head-up floating axis.
02.755–05.576s | C2 — Restrained cloud-arm phrase: Trace a compact horizontal figure-eight near chest height, alternating one arm high and one low. During the selected sung phrase, keep both hands away from the mouth and let the chest movement remain small so the lip-sync remains readable.
05.576–08.397s | C3 — Vertical arm circle and chest lift: After the lyric phrase, carry one palm upward through a vertical circle; the shoulder initiates, the elbow follows, and the wrist completes the arc. The sternum lifts gently and the opposite arm extends behind as a counterline.
08.397–12.237s | C12 + G1 LINE — Floating balance into front three-quarter: Gather the legs into a narrow stagger, let one knee fold briefly into attitude, then lengthen both pointed feet beneath the pelvis. Rotate only a small quarter-turn through the ribs and shoulders and settle into a calm front three-quarter line. During the final 0.55 seconds, lengthen one arm toward stage center with the fingertips leading, then keep that reach unfinished for the outgoing visual handoff.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.487–5.653s But love's the one no book can tell
Selected lip-sync only: 00:00.487–00:05.653, <Subject 1> (S1) sings <d>[English] But love's the one no book can tell</d>. Mouth movement ends with the source phrase; no lip-sync outside this window.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The fins pivot outward and descend. A low open arc starts to rise at center back, preparing the next more intimate scene.
Pair-level transition rule: SEG11 and SEG12 share the two angled fins. SEG12 ends as they pivot outward and descend; SEG13 opens on the single open curved frame continuing up from the deck.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 12.237 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 2.755s, 5.576s, 8.397s, 11.218s. Local downbeats: 1.344s, 4.165s, 6.986s, 9.808s. Detected high-confidence drum accents: 0.636s other; 6.278s other; 7.160s other; 11.386s other. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 13 — Instrumental transformation — a new center

**原曲区间：** 145.000–157.436s · **时长：** 12.436s · **音频：** `seg13_02m25p00s-02m37p44s.mp3`  
**歌词事件：** Instrumental; no lyric events in this crop.

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg13_02m25p00s-02m37p44s.mp3` from 145.000s to 157.436s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 12.436 seconds.

summary:

[reference generation + audio reuse] Create an exact 12.436-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT VI — A safe emotional center. Emotional objective: During the instrumental passage, she reclaims the stage and re-enters the dance with a decisive but graceful phrase. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT VI — A safe emotional center. The performer's immediate objective is: During the instrumental passage, she reclaims the stage and re-enters the dance with a decisive but graceful phrase.
Emotional movement: uncertainty softens into trust and emotional safety. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
A single open curved frame rises from the stage deck, with two short vertical side ribs. The shape remains open at the front and above; it never becomes a room, cage, house or literal shelter. No furniture or hand props.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Soft warm-white front light with a subtle amber inner edge. Keep the surrounding stage restrained and uncluttered.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The angled fins have disappeared; a single open curved frame rises. Her gaze and torso are already turning toward stage center.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Begin on a tight close-up of the same reaching fingertips directed toward stage center. Continue their inward travel, then follow the hand toward the wrist and elbow as both elbows draw inward at different heights. Tilt and track into the torso counter-twist, revealing the compact crossed-leg axis preparation for the turn. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:01.802, She completes one full upright-axis turn, keeping the head above the torso and feet below. The legs remain compact and crossed to control the rotation; the camera performs a short counter-arc from outside the turn so the body rotation remains unmistakable.
[Shot 3] At 00:04.623, As the turn resolves, she opens both arms asymmetrically to decelerate and extends one leg into an elegant attitude line. The camera moves with her recovery and stops when the movement peaks; do not add a second turn or any inversion.
[Shot 4] At 00:07.444, The curved frame reaches its final height. She carries the extended arm into a soft overhead line, then lowers the wrist toward the heart. End in an upright, stable float with the frame clearly established behind her. During the final 0.55 seconds, follow the extended arm as its wrist lowers toward the heart. Finish on the fingertips just before they reach the chest; keep the movement continuous and head-up.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: G1 TURN — Axis preparation; C7 + G1 TURN — One complete 360-degree pivot; G3 Technical Peak / Hero Lock + C12; C3 — Overhead vertical circle into soft finish.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–01.802s | G1 TURN — Axis preparation: Draw the elbows inward at different heights and bring the pointed legs into a compact crossed line. The torso counter-twists against the pelvis to preload one clean vertical-axis rotation; the body remains suspended with no floor push.
01.802–04.623s | C7 + G1 TURN — One complete 360-degree pivot: Initiate one continuous full turn from the rib cage and pelvis around the established vertical axis. Keep the legs compact and crossed to control the radius; the head spots once and returns to the front as the rotation completes. Open the arms only after the rotation has passed its midpoint to control deceleration. This is the second and final complete turn of the full performance.
04.623–07.444s | G3 Technical Peak / Hero Lock + C12: As the turn resolves, widen both arms asymmetrically and fold one knee into a suspended attitude line. Reach the technical peak on the phrase accent, hold a brief clean Hero Lock with the eyes fixed, and let the foot and fingertips retain a small delayed inertia.
07.444–12.436s | C3 — Overhead vertical circle into soft finish: Carry the extended arm through a smaller vertical circle overhead, then lower the wrist toward the heart while the opposite leg lengthens below. Finish with a stable upright axis and the curved scenic frame clearly behind her.
Rotation budget: this is one of the two and only two complete upright-axis rotations in the full performance. Complete the single turn once, decelerate visibly and leave the body on the specified outgoing line.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): Instrumental; no lyric events in this crop.
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. The curved frame reaches its final height. She carries the extended arm into a soft overhead line, then lowers the wrist toward the heart. End in an upright, stable float with the frame clearly established behind her. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG13 and SEG14 share the open curved frame. SEG14 ends with its open shape beginning to retract; SEG15 opens with the three vertical panels already rising.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 12.436 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 1.802s, 4.623s, 7.444s, 10.265s. Local downbeats: 0.392s, 3.213s, 6.034s, 8.855s, 11.676s. Detected high-confidence drum accents: 1.959s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 14 — Safety — the space holds her

**原曲区间：** 157.436–171.033s · **时长：** 13.597s · **音频：** `seg14_02m37p44s-02m51p03s.mp3`  
**歌词事件：** 2.772–5.272s All the worlds I hold inside; 5.564–8.314s Still need somewhere safe to shine; 8.355–10.939s Every star and spell above; 11.147–12.772s Can't replace the warmth of love

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg14_02m37p44s-02m51p03s.mp3` from 157.436s to 171.033s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 13.597 seconds.

summary:

[reference generation + audio reuse] Create an exact 13.597-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT VI — A safe emotional center. Emotional objective: She discovers a sense of belonging and emotional safety without depicting a literal house or room. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT VI — A safe emotional center. The performer's immediate objective is: She discovers a sense of belonging and emotional safety without depicting a literal house or room.
Emotional movement: uncertainty softens into trust and emotional safety. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
A single open curved frame rises from the stage deck, with two short vertical side ribs. The shape remains open at the front and above; it never becomes a room, cage, house or literal shelter. No furniture or hand props.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Soft warm-white front light with a subtle amber inner edge. Keep the surrounding stage restrained and uncluttered.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue from SEG13 with the wrist descending toward the heart; the open curved frame is now stationary.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Cut to a tight close-up of the same wrist and fingertips arriving at the heart area. Let the fingertips complete the final small travel, then follow the palm as it rests near the sternum. Tilt to her softened eyes as they turn toward the open side of the frame; the breath-led alignment continues without a reset. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.471, The camera passes close to the frame edge, then reveals her in medium-full composition. She opens one arm through a smooth port de bras while the other hand remains briefly near the chest; the torso expands and the pelvis follows with a slight delay.
[Shot 3] At 00:06.292, She extends one knee outward into a controlled développé, then folds it into attitude and crosses the pointed feet again. Her shoulders and arms counterbalance so the vertical suspended axis remains clear. The curved frame stays open, never enclosing her.
[Shot 4] At 00:09.113, She looks outward, releases the hand from her chest and offers both palms to the room. End with a gentle, confident open shape; the frame begins to retract for the next expansion. For the final 0.55 seconds, select the nearer of the two offered palms as the visual landing point. The palm stays open, then begins to rotate inward toward her torso; keep its fingers crisp in the final frame.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Warm breath and heart anchor; C2 + A13 — Cloud hands opening into port de bras; C12 — Développé to attitude and crossed line; B7 + G1 LINE — Two-palm offering.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.471s | C1 — Warm breath and heart anchor: Allow one soft inhale to lift the sternum while the hand rests near the heart. The shoulders release outward and the gaze moves toward the open side of the frame; keep the lower body long and quietly suspended.
03.471–06.292s | C2 + A13 — Cloud hands opening into port de bras: Trace one smooth horizontal figure-eight, then cross the forearms low and sweep them outward into a full open arc. The chest expands after the arms, and the pelvis follows with a slight delayed counter-shift.
06.292–09.113s | C12 — Développé to attitude and crossed line: Extend one knee outward through a controlled développé, fold it back into attitude, then pass the pointed feet into a narrow cross. Arms stay at unequal heights to counterbalance; no ground-supported ballet stance.
09.113–13.597s | B7 + G1 LINE — Two-palm offering: Turn both palms outward and upward, then let the arms settle into an asymmetrical open line. Lengthen one pointed leg below the pelvis and hold a warm outward gaze as the curved frame retracts.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 2.772–5.272s All the worlds I hold inside; 5.564–8.314s Still need somewhere safe to shine; 8.355–10.939s Every star and spell above; 11.147–12.772s Can't replace the warmth of love
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The open frame lowers smoothly into the deck. Three slim vertical panels begin rising behind the performer for the next expansion.
Pair-level transition rule: SEG13 and SEG14 share the open curved frame. SEG14 ends with its open shape beginning to retract; SEG15 opens with the three vertical panels already rising.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 13.597 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.650s, 3.471s, 6.292s, 9.113s, 11.934s. Local downbeats: 2.061s, 4.882s, 7.703s, 10.524s, 13.345s. Detected high-confidence drum accents: No high-confidence isolated drum accent specified; use only the supplied phrase/downbeat grid.. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 15 — Expansion — the world responds

**原曲区间：** 171.033–183.916s · **时长：** 12.883s · **音频：** `seg15_02m51p03s-03m03p92s.mp3`  
**歌词事件：** 0.383–2.883s All the worlds I hold inside; 3.175–5.883s Still need somewhere safe to shine; 5.967–8.508s Every star and spell above; 8.717–10.758s Can't replace the warmth of love; 11.592–12.883s I see a thousand lights

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg15_02m51p03s-03m03p92s.mp3` from 171.033s to 183.916s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 12.883 seconds.

summary:

[reference generation + audio reuse] Create an exact 12.883-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT VII — The inner world opens outward. Emotional objective: Her inner confidence expands into a larger, more colorful performance without literal lyric illustration. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT VII — The inner world opens outward. The performer's immediate objective is: Her inner confidence expands into a larger, more colorful performance without literal lyric illustration.
Emotional movement: private security expands into confident generosity. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Three tall translucent vertical panels rise at separate depths and pivot outward in a shallow fan. Their surfaces remain abstract and unmarked. Their motion is slow, mechanically consistent and clearly driven by integrated stage lifts.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Pearl-white and restrained champagne highlights expand across the panels; subtle color shifts stay in the background and never repaint the performer.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The curved frame is retracting; three vertical panels rise. She is already facing outward with both palms offered.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Start on a tight close-up of that same nearer open palm. Continue the inward wrist rotation and let the hand travel across the torso into the single chest-level X-cross. Track the crossing hand, then allow the opposing arm to enter and open outward as the camera reveals the shoulder and upper body. Do not begin on the full-body panels. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:01.158, She performs a linked aerial phrase: one knee lifts into attitude, the foot extends outward, the leg folds and crosses beneath, then the other leg lengthens down. Her arms exchange high and low levels; the movement remains continuous and never becomes a jump or landing.
[Shot 3] At 00:03.979, A close-medium cut catches the chest and shoulder spiral as she turns her head late toward the camera. She opens the arms into a wide diagonal, then narrows them to regulate the next movement. Colored reflections move only across the panels, not across her face in a way that changes her appearance.
[Shot 4] At 00:06.801, The panels fan outward. She glides laterally through the space between their visual edges and finishes in a strong three-quarter line, one arm high and one low. End with the movement accelerating into SEG16. In the final 0.55 seconds, follow the high hand of the unequal arm line. Let its wrist fold and begin the arc toward the crown; finish with the hand moving across the upper edge of frame, not with a completed pose.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: A15 — Fast chest cross and opening; C12 + G1 LINE — Attitude exchange and leg extension; G2 Spiral + Off-axis Tilt; C16 adaptation — Thread-palm and cloud-arm release.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–01.158s | A15 — Fast chest cross and opening: From the opening arm line, cross the forearms once across the torso and split them into opposing diagonals. The shoulders lead the separation; the ribs rotate a fraction later, making the action read as a single sharp phrase rather than two repeated arm waves.
01.158–03.979s | C12 + G1 LINE — Attitude exchange and leg extension: Lift one knee into attitude, extend the lower leg outward, fold through a narrow cross, then lengthen the opposite leg down. Exchange the arms from high to low to counterbalance the leg path; the body stays vertical and unsupported.
03.979–06.801s | G2 Spiral + Off-axis Tilt: Let the sternum spiral toward the camera while the pelvis counters, then incline the torso modestly away from the extended leg. Recover by unwinding through the ribs, not by swinging the entire body horizontally.
06.801–12.883s | C16 adaptation — Thread-palm and cloud-arm release: Thread one palm beneath the opposite forearm and carry both arms through a layered cloud-arm sweep. Keep the facing change to a small three-quarter adjustment; omit C16's step-based turn and let the hands open into one high-low diagonal as the lateral float accelerates.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.383–2.883s All the worlds I hold inside; 3.175–5.883s Still need somewhere safe to shine; 5.967–8.508s Every star and spell above; 8.717–10.758s Can't replace the warmth of love; 11.592–12.883s I see a thousand lights
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. The panels fan outward. She glides laterally through the space between their visual edges and finishes in a strong three-quarter line, one arm high and one low. End with the movement accelerating into SEG16. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG15 and SEG16 share the three translucent panels. SEG16 ends as they close toward a line and descend; SEG17 opens with the broad curved frame and two slim towers continuing to rise.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 12.883 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 1.158s, 3.979s, 6.801s, 9.622s, 12.443s. Local downbeats: 2.569s, 5.390s, 8.211s, 11.032s. Detected high-confidence drum accents: 0.493s kick; 1.213s kick; 2.606s kick; 5.415s kick; 6.112s kick; 6.460s kick; 6.809s kick; 7.157s kick; 7.505s kick; 7.854s kick; 8.225s kick; 8.573s kick. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 16 — Full expression — the dance takes the stage

**原曲区间：** 183.916–194.958s · **时长：** 11.042s · **音频：** `seg16_03m03p92s-03m14p96s.mp3`  
**歌词事件：** 0.000–1.250s Inside the words they tried to hide; 1.250–3.959s A hundred thousand tales unfold; 3.959–6.542s Each page a universe of gold; 6.542–11.042s I see a thousand lights

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg16_03m03p92s-03m14p96s.mp3` from 183.916s to 194.958s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 11.042 seconds.

summary:

[reference generation + audio reuse] Create an exact 11.042-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT VII — The inner world opens outward. Emotional objective: She reaches the fullest expression of the show’s solo dance vocabulary and prepares the climax. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT VII — The inner world opens outward. The performer's immediate objective is: She reaches the fullest expression of the show’s solo dance vocabulary and prepares the climax.
Emotional movement: private security expands into confident generosity. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
Three tall translucent vertical panels rise at separate depths and pivot outward in a shallow fan. Their surfaces remain abstract and unmarked. Their motion is slow, mechanically consistent and clearly driven by integrated stage lifts.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Pearl-white and restrained champagne highlights expand across the panels; subtle color shifts stay in the background and never repaint the performer.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue the lateral glide and unequal arm line from SEG15; the three panels are fully opened.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Open on a tight close-up of the same high hand and wrist as it continues across the crown. Track the hand through the broad cloud-arm pathway and the opposite palm threading beneath it; then reveal the chest-level X and the outward split through a close-medium view. The camera must not start with the full figure already centered. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:02.381, Her legs pass through a controlled scissor exchange: one knee folds, the other lengthens, then both pass through a narrow crossed line. She unfolds one leg into a long arabesque-like diagonal while the torso stays mostly upright, then returns to vertical alignment.
[Shot 3] At 00:05.202, She performs a quick shoulder-led spiral into a compact half-turn, then opens both arms sharply on the next phrase accent. The panels pivot outward and catch a brighter back edge. Keep the motion crisp but elegant, not frantic or mechanically beat-by-beat.
[Shot 4] At 00:08.023, She completes the phrase by extending one arm toward the audience, then draws it back into the chest as the panels begin to lower. End with a clear invitation gesture and the body already carrying forward. During the final 0.55 seconds, bring the camera to the fingertips as the extended invitation hand returns to the chest. Let the fingertips arrive but do not let the hand become motionless; carry a small inward movement through the cut.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C16 adaptation + A15 — Thread-palm into X-open; C12 + G1 LINE — Scissor exchange into arabesque-like diagonal; C5 + C7 half-pivot variant — Spiral and half-turn; G1 LINE + G3 Accent Lock — Pre-climax invitation.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–02.381s | C16 adaptation + A15 — Thread-palm into X-open: Lead with a broad cloud-arm sweep across the face line, thread the opposite palm beneath it, then bring the forearms into one chest-level X and split them sharply outward. This is an upper-body pathway adaptation only; no step-based turn.
02.381–05.202s | C12 + G1 LINE — Scissor exchange into arabesque-like diagonal: Fold one knee while the opposite leg lengthens, pass through one narrow pointed scissor, then extend the free leg behind and below into a long arabesque-like diagonal. The torso counterbalances but stays predominantly upright; the head remains above the pelvis.
05.202–08.023s | C5 + C7 half-pivot variant — Spiral and half-turn: Rotate through the ribs and shoulders into one compact half-turn while the pelvis follows late; the arms open on the accent to brake the movement. Do not complete a full rotation here; the full-turn budget is already reserved for SEG06 and SEG13.
08.023–11.042s | G1 LINE + G3 Accent Lock — Pre-climax invitation: Extend one arm toward the room and the opposite leg into a clean pointed line, then draw the reaching elbow toward the sternum without collapsing the chest. Hold a clear asymmetric accent and let the body momentum continue forward into SEG17.
Rotation budget: this segment uses only the specified compact half-turn; do not extend it into a complete rotation.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.000–1.250s Inside the words they tried to hide; 1.250–3.959s A hundred thousand tales unfold; 3.959–6.542s Each page a universe of gold; 6.542–11.042s I see a thousand lights
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The three panels begin to close toward a single central line and lower. A larger curved frame and two narrow side towers start emerging from the deck.
Pair-level transition rule: SEG15 and SEG16 share the three translucent panels. SEG16 ends as they close toward a line and descend; SEG17 opens with the broad curved frame and two slim towers continuing to rise.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 11.042 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 2.381s, 5.202s, 8.023s, 10.844s. Local downbeats: 0.970s, 3.791s, 6.612s, 9.433s. Detected high-confidence drum accents: 7.672s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 17 — The call — one decisive vertical dive

**原曲区间：** 194.958–207.672s · **时长：** 12.714s · **音频：** `seg17_03m14p96s-03m27p67s.mp3`  
**歌词事件：** 0.000–1.375s They turn the darkest night to day; 1.375–4.083s I've read a thousand spells; 4.083–6.375s But love's the one no book can tell; 6.500–7.292s Come on!; 9.875–12.417s All the worlds I hold inside

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg17_03m14p96s-03m27p67s.mp3` from 194.958s to 207.672s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 12.714 seconds.

summary:

[reference generation + audio reuse] Create an exact 12.714-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT VIII — The shared climax. Emotional objective: The performer turns the emotional invitation into the show’s single climactic aerial action. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT VIII — The shared climax. The performer's immediate objective is: The performer turns the emotional invitation into the show’s single climactic aerial action.
Emotional movement: private wonder becomes a confident invitation to share the moment. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
A broad but shallow curved frame rises behind the performer, accompanied by two narrow vertical towers. These are real modular scenic pieces driven by concealed floor lifts; no extra performers, literal symbols, audience faces or oversized spectacle objects.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
The most expansive light state so far: layered front and side beams, controlled warm-white pulses, and a brighter back edge. Keep the face correctly exposed and do not blow out the character.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The three panels are lowering; the broad curved frame and two slim towers rise. Her arm remains extended from SEG16, carrying the invitation forward.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Begin with a tight close-up of the same fingertips at the chest. Continue the inward motion, then let the palm release forward toward the viewer as the camera tracks along the arm. Gradually reveal the upright suspended body and the continuous vertical travel preparation; the head-first dive does not begin in this opening close-up and remains the single later technical event. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:02.623, She draws both arms inward and lifts through the sternum, then sends one arm upward as the torso begins a controlled forward pitch. The camera shifts to a clear side-front medium-full angle to establish the real body axis before the aerial action.
[Shot 3] At 00:05.444, She completes the single head-first vertical dive of the entire performance. The head turns downward, the shoulders and chest follow, then the pelvis and pointed legs pass overhead; she travels vertically through the frame in one controlled continuous motion. The existing character design responds with buoyant delayed inertia and remains unchanged. The camera tracks alongside the same vertical path; it does not roll to fake the inversion.
[Shot 4] At 00:08.265, The camera holds her actual inverted orientation as she continues the downward passage, arms extending to regulate speed. End while the same dive is still in motion, head leading and legs above, with no landing, platform contact or second rotation. SEG18 must receive this exact inverted movement state. For the final 0.55 seconds, keep the actual inverted body orientation and land the camera on the outstretched hand nearest the edge of frame. Its wrist and fingers remain extended to regulate the ongoing head-first descent. Cut while the same downward motion is still active.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: G1 FLIP / user-mandated single-dive preparation; G1 FLIP — Initiation and forward pitch; G1 FLIP — Single inverted technical passage; G3 Hero-in-motion / outgoing inverted state.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–02.623s | G1 FLIP / user-mandated single-dive preparation: Begin from the inherited upright floating line. Draw both arms inward, lift through the sternum, and establish one continuous vertical travel path. The preparation is visible in the ribs and pelvis; there is no floor push, jump or takeoff.
02.623–05.444s | G1 FLIP — Initiation and forward pitch: The upper chest inclines forward first, followed sequentially by shoulders, rib cage and pelvis. The head leads the vertical path while both legs stay long and joined; the body begins the one planned head-first dive as a single continuous movement, not as repeated tumbling.
05.444–08.265s | G1 FLIP — Single inverted technical passage: Complete the one continuous head-first vertical inversion: shoulders and chest pass below the pelvis, the pelvis follows overhead, and the pointed legs travel above the body. Keep the movement on one vertical route with no extra somersault, no second dive and no lateral cartwheel. The camera tracks beside the same path.
08.265–12.714s | G3 Hero-in-motion / outgoing inverted state: Continue the same uninterrupted downward passage while the arms open to regulate speed. Do not resolve or restart the movement inside this segment; the final frame remains in the actual head-down, legs-above state so SEG18 can recover from the exported frame.
Special climax boundary: this segment alone performs the single planned head-first vertical dive. It is one continuous action with a defined outgoing inverted state for SEG18; do not add any extra flip or repeat.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.000–1.375s They turn the darkest night to day; 1.375–4.083s I've read a thousand spells; 4.083–6.375s But love's the one no book can tell; 6.500–7.292s Come on!; 9.875–12.417s All the worlds I hold inside
Selected lip-sync only: 00:06.500–00:07.292, <Subject 1> (S1) sings <d>[English] Come on!</d>. The brief call is clear and natural; no continuous mouth movement before or after.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. The camera holds her actual inverted orientation as she continues the downward passage, arms extending to regulate speed. End while the same dive is still in motion, head leading and legs above, with no landing, platform contact or second rotation. SEG18 must receive this exact inverted movement state. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG17 and SEG18 share the broad curved frame and towers. SEG17 ends during the one head-first vertical dive; SEG18 begins from that exact inverted movement state and completes the recovery. The frame then descends toward the gratitude scene.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 12.714 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 2.623s, 5.444s, 8.265s, 11.086s. Local downbeats: 1.212s, 4.033s, 6.854s, 9.675s, 12.496s. Detected high-confidence drum accents: No high-confidence isolated drum accent specified; use only the supplied phrase/downbeat grid.. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 18 — Recovery — the climax resolves into connection

**原曲区间：** 207.672–218.571s · **时长：** 10.899s · **音频：** `seg18_03m27p67s-03m38p57s.mp3`  
**歌词事件：** 0.036–2.661s Still need somewhere safe to shine; 2.828–5.328s Every star and spell above; 5.578–7.578s Can't replace the warmth of love

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg18_03m27p67s-03m38p57s.mp3` from 207.672s to 218.571s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 10.899 seconds.

summary:

[reference generation + audio reuse] Create an exact 10.899-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT VIII — The shared climax. Emotional objective: She completes the single inversion and transforms its force into a return to upright freedom. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT VIII — The shared climax. The performer's immediate objective is: She completes the single inversion and transforms its force into a return to upright freedom.
Emotional movement: private wonder becomes a confident invitation to share the moment. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
A broad but shallow curved frame rises behind the performer, accompanied by two narrow vertical towers. These are real modular scenic pieces driven by concealed floor lifts; no extra performers, literal symbols, audience faces or oversized spectacle objects.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
The most expansive light state so far: layered front and side beams, controlled warm-white pulses, and a brighter back edge. Keep the face correctly exposed and do not blow out the character.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue the same head-first vertical movement from SEG17, with the same screen direction and momentum; do not begin a new dive or repeat the inversion.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Open on a tight close-up of that same outstretched hand and wrist, preserving the inverted orientation visible in <Picture 2>. The fingers spread slightly to regulate the same descent; track along the forearm to the shoulder and torso, then widen enough to reveal the actual inverted body and the beginning of recovery. Do not create a second dive, a new rotation or an upright reset. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:01.193, She returns to a clear head-up, feet-down vertical float. One knee folds into attitude while the opposite leg lengthens below; the arms sweep from wide to a soft diagonal. The camera moves from side-front toward a readable frontal medium-full composition without crossing the action axis.
[Shot 3] At 00:04.014, She performs a continuous chest-to-waist wave, then extends both arms outward as the curved frame and towers reach their full height. If the original track swells, let the light intensity respond subtly while the camera remains on the solo performer; do not show the audience.
[Shot 4] At 00:06.835, She turns her gaze toward the audience and brings one hand briefly to the heart before opening it outward. End upright and facing front three-quarter, with the set beginning its slow descent toward the gratitude scene. In the final 0.55 seconds, follow the hand as it leaves the heart and opens outward. Finish on the open palm with the upright body axis already restored; keep the palm moving gently toward the room.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: G2 Contemporary Fall & Recovery — inherited inverted state; G4 Contemporary / Recovery to Suspension; C12 adaptation — Suspended attitude and counterline; B8 + G3 Hero Lock — Upright recovery phrase.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–01.193s | G2 Contemporary Fall & Recovery — inherited inverted state: Begin from the actual inverted final frame of SEG17, not from an upright reset. Open the arms laterally to create drag and decelerate the existing vertical descent; the torso and pelvis continue along the same path.
01.193–04.014s | G4 Contemporary / Recovery to Suspension: The head and shoulders lead the return toward upright, followed in order by the rib cage, pelvis and legs. Use the existing angular momentum to roll the body back into a head-up, feet-down axis by the end of this window; this is the recovery from the one preceding dive, not a new inversion.
04.014–06.835s | C12 adaptation — Suspended attitude and counterline: Once upright, fold one knee into attitude while the opposite leg lengthens below the pelvis. Sweep the arms from a wide open line into a soft diagonal; maintain the head-up axis and do not repeat the dive or begin another tumble.
06.835–10.899s | B8 + G3 Hero Lock — Upright recovery phrase: Carry one controlled chest-to-waist wave through the torso, then open both arms outward as the legs settle into a long pointed vertical line. Hold the recovered upright shape cleanly on the accent; the set rises behind her while the performer remains fully readable.
Recovery boundary: the opening body state is the actual exported inverted end-frame of SEG17. Restore the head-up, feet-down axis by 1.193s and remain upright for the rest of this segment.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.036–2.661s Still need somewhere safe to shine; 2.828–5.328s Every star and spell above; 5.578–7.578s Can't replace the warmth of love
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The curved frame and side towers lower gradually as the show enters its gratitude section. The light resolves into a warm intimate state.
Pair-level transition rule: SEG17 and SEG18 share the broad curved frame and towers. SEG17 ends during the one head-first vertical dive; SEG18 begins from that exact inverted movement state and completes the recovery. The frame then descends toward the gratitude scene.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 10.899 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 1.193s, 4.014s, 6.835s, 9.656s. Local downbeats: 2.603s, 5.425s, 8.246s. Detected high-confidence drum accents: No high-confidence isolated drum accent specified; use only the supplied phrase/downbeat grid.. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 19 — Gratitude — speak to the room

**原曲区间：** 218.571–232.316s · **时长：** 13.745s · **音频：** `seg19_03m38p57s-03m52p32s.mp3`  
**歌词事件：** 0.220–1.054s Ah —; 6.095–7.387s Thank you, everyone!; 8.429–11.345s Thank you for sharing this wonderful night with me!

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg19_03m38p57s-03m52p32s.mp3` from 218.571s to 232.316s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 13.745 seconds.

summary:

[reference generation + audio reuse] Create an exact 13.745-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT IX — Gratitude and the final bow. Emotional objective: She acknowledges the audience personally, shifting from spectacle to sincere thanks. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT IX — Gratitude and the final bow. The performer's immediate objective is: She acknowledges the audience personally, shifting from spectacle to sincere thanks.
Emotional movement: exhilaration settles into sincere gratitude and quiet affection. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
A low, narrow vertical light frame rises behind the performer, much simpler than the climax structure. It is the only remaining scenic unit; all other pieces are below the stage deck.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Warm soft key, gentle side fill and a restrained back edge. No sweeping laser effects or crowd close-ups. The audience remains entirely off-screen.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The climax frame is lowering; the stage has returned to a warm, uncluttered setting. She is upright, facing front three-quarter, one hand just leaving her heart.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Start with a tight close-up of the same outward-opening palm. Continue its gentle extension, then trace back along the forearm to the shoulder and face. Rack focus to her eyes as the hand begins to lower; keep the mouth and face unobstructed before the selected gratitude lines begin. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:01.578, During 00:06.095–00:07.387, she lip-syncs only the exact phrase <d>[English] Thank you, everyone!</d>. Her mouth returns to a relaxed natural expression immediately after the phrase. Keep the framing medium close and the face clear.
[Shot 3] At 00:04.399, During 00:08.429–00:11.345, she performs the second selected phrase <d>[English] Thank you for sharing this wonderful night with me!</d>. The camera makes only a restrained lateral slide; she speaks warmly toward the lens and then lets her eyes move briefly toward the unseen audience.
[Shot 4] At 00:07.220, As the vocal window ends, she gives a small graceful upper-body bow while remaining suspended and never touching the stage deck. She rises back to upright, opens one palm toward the room, and holds the gratitude in her eyes. End with a warm, calm expression. For the final 0.55 seconds, let the camera settle on the open palm offered toward the unseen room. The fingers soften and begin to lower, leaving the hand in gentle motion at the cut; do not show audience inserts.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Breath and heart anchor; C2 — Small cloud-arm phrase; B7 + C13 adaptation — Spoken gratitude into offering; G1 LINE — Open gratitude finish.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–01.578s | C1 — Breath and heart anchor: Keep the upper body quiet as the hand rests briefly over the heart. A small inhale lifts the sternum and the shoulders relax; the face remains open and unobstructed for the selected spoken lines.
01.578–04.399s | C2 — Small cloud-arm phrase: Move one forearm across the chest while the other traces a low horizontal arc; exchange their levels once in a restrained figure-eight. Keep the movement below the mouth and let it settle before the first thank-you line.
04.399–07.220s | B7 + C13 adaptation — Spoken gratitude into offering: During the selected phrase, keep the mouth clear and the torso nearly still; let only the eyes and a small hand-to-heart response carry the emotion. After the line, turn one palm upward and extend it toward the room, adapting C13's soft hand-to-face expressivity without covering the lips.
07.220–13.745s | G1 LINE — Open gratitude finish: Lengthen the free arm outward and let the other hand return near the heart. The chest stays lifted and the feet point below; finish with a gentle upper-body bow initiation that flows into SEG20.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): 0.220–1.054s Ah —; 6.095–7.387s Thank you, everyone!; 8.429–11.345s Thank you for sharing this wonderful night with me!
Selected lip-sync only: 00:06.095–00:07.387, <Subject 1> (S1) sings <d>[English] Thank you, everyone!</d>; then 00:08.429–00:11.345, <Subject 1> (S1) sings <d>[English] Thank you for sharing this wonderful night with me!</d>. Keep the two phrases separate and stop phoneme-matched mouth movement at each exact end.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
End-state for the next segment in this same scene: preserve the current scenic module at exactly its described height and orientation. As the vocal window ends, she gives a small graceful upper-body bow while remaining suspended and never touching the stage deck. She rises back to upright, opens one palm toward the room, and holds the gratitude in her eyes. End with a warm, calm expression. The next clip begins from the actual exported final frame and continues the same emotional action; no scene reset or prop reappearance.
Pair-level transition rule: SEG19 and SEG20 share the narrow warm vertical frame. SEG20 ends as the frame fully descends; SEG21 opens on the clean deck and single thin backlight line. SEG21 is the final coda.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 13.745 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 1.578s, 4.399s, 7.220s, 10.041s, 12.862s. Local downbeats: 0.168s, 2.989s, 5.810s, 8.631s, 11.452s. Detected high-confidence drum accents: 13.048s snare. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 20 — The bow — applause without spectacle

**原曲区间：** 232.316–242.316s · **时长：** 10.000s · **音频：** `seg20_03m52p32s-04m02p32s.mp3`  
**歌词事件：** Instrumental; no lyric events in this crop.

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg20_03m52p32s-04m02p32s.mp3` from 232.316s to 242.316s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 10.000 seconds.

summary:

[reference generation + audio reuse] Create an exact 10.000-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: ACT IX — Gratitude and the final bow. Emotional objective: The performance settles into a real theatrical acknowledgment, not another dance climax. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: ACT IX — Gratitude and the final bow. The performer's immediate objective is: The performance settles into a real theatrical acknowledgment, not another dance climax.
Emotional movement: exhilaration settles into sincere gratitude and quiet affection. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
A low, narrow vertical light frame rises behind the performer, much simpler than the climax structure. It is the only remaining scenic unit; all other pieces are below the stage deck.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
Warm soft key, gentle side fill and a restrained back edge. No sweeping laser effects or crowd close-ups. The audience remains entirely off-screen.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Treat it as the truth for the body's actual configuration, movement phase, screen direction and scenic state, but do not copy its full-frame composition: open on the local body-part close-up specified for this cut in the Rev.8.3 visual-relay table. Continue the upright recovery from SEG19; the hand is still open toward the unseen room and the narrow scenic frame remains behind her.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Open on a tight close-up of the same open palm. Continue the fingers softening and the hand lowering; follow the wrist toward the chest, then tilt to the upper spine as the small bow begins. Pull back only to a close-medium or subject-dominant medium-full view once the bow mechanics are readable. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:01.938, The camera glides sideways through a soft foreground edge of the narrow frame. She draws both arms inward, then opens them in a modest final presentation gesture. The motion is slower than the preceding dance, allowing the original concert sound to breathe.
[Shot 3] At 00:04.759, A close-medium reaction shot catches her eyes and restrained smile as she looks toward different areas of the unseen audience. Do not show the audience or auditorium; keep the camera on the solo performer.
[Shot 4] At 00:07.580, The narrow frame descends into the deck. She turns gently back toward the lens and lets her hands settle near the chest. End in a calm upright float, ready for the coda, without a hard freeze or end card. During the final 0.55 seconds, let the camera land on the fingertips gathered near the heart as she turns gently back toward the lens. The fingers begin to separate with the breath; end while the movement is still alive.
CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C1 — Breath-led bow preparation; A13 adaptation — Modest open-arm presentation; C14 — Soft side inclination and cheek line; C3 + C12 — Small vertical circle into upright coda line.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–01.938s | C1 — Breath-led bow preparation: Let the shoulders soften and the sternum release slightly on the exhale. Begin a small bow from the upper spine while preserving the unsupported vertical body axis; this is a theatrical acknowledgment, not a deep floor-directed fold.
01.938–04.759s | A13 adaptation — Modest open-arm presentation: Bring the forearms briefly toward one another in front of the chest, then sweep them outward into a modest presentation arc. The elbows lead and the hands finish, with the feet remaining pointed beneath the pelvis.
04.759–07.580s | C14 — Soft side inclination and cheek line: Incline the torso gently to one side while one hand floats beside the cheek; hold the expression for a brief count, then let the head return to neutral. Keep the shape intimate, not coy or exaggerated.
07.580–10.000s | C3 + C12 — Small vertical circle into upright coda line: Carry one hand through a compact vertical circle and lower it toward the chest as the other arm softens. Draw the legs into a neat pointed stagger and hold a stable upright float while the narrow frame descends.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): Instrumental; no lyric events in this crop.
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
The narrow frame descends fully below the deck. The final coda begins with a clean stage and one very thin vertical backlight line.
Pair-level transition rule: SEG19 and SEG20 share the narrow warm vertical frame. SEG20 ends as the frame fully descends; SEG21 opens on the clean deck and single thin backlight line. SEG21 is the final coda.
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 10.000 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 1.938s, 4.759s, 7.580s. Local downbeats: 0.528s, 3.349s, 6.170s, 8.991s. Detected high-confidence drum accents: 9.171s hihat. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```

## SEGMENT 21 — Last light — the soloist remains

**原曲区间：** 242.316–252.648s · **时长：** 10.332s · **音频：** `seg21_04m02p32s-04m12p65s.mp3`  
**歌词事件：** Instrumental; no lyric events in this crop.

```text
subject_definitions:

<Subject 1> (S1) is the single performer shown in <Picture 1>. <Picture 1> is the permanent and exclusive authority for the complete character image throughout every segment. Preserve it exactly as referenced. Do not write any textual reconstruction of the person's appearance or redesign, restyle, recolor or replace the referenced image. <Picture 1> does not define the stage, background, pose, camera composition or lighting for this production.

<Picture 2> is the actual final frame exported from the immediately preceding generated segment. Use it only as the opening continuity anchor for stage layout, current scenic-unit height and orientation, performer pose and movement phase, camera side, focus relationship and any prop that remains visible. It does not redefine the character image or design; <Picture 1> remains the permanent and exclusive character authority. Continue the next instant of the recorded action rather than recreating it.

<Audio 1> is the exact original crop `seg21_04m02p32s-04m12p65s.mp3` from 242.316s to 252.648s of `11月16日.mp3`. Reuse this entire crop once, unchanged, as the complete soundtrack for exactly 10.332 seconds.

summary:

[reference generation + audio reuse] Create an exact 10.332-second vertical 9:16 premium 3DCG solo music-dance-theatre segment, using <Picture 1> for the character alone and this segment's <Audio 1> as the unchanged soundtrack. Dramatic unit: CODA — The last light. Emotional objective: After the applause, she gives one final intimate gesture and lets the performance disappear. The stage is a real, intimate concert-theatre performance space with abstract scenic architecture that rises directly from integrated lifts in the stage deck. Keep the performer close, large and sharply readable; this is a solo performance, not a literal illustration of the lyrics.

retention_analysis:

<Subject 1> (S1, appears throughout): fully_preserved — the same complete character image is used in every frame, controlled only by <Picture 1>. No text-based appearance reconstruction.
<Picture 1> (all segments): fully_preserved as the sole character reference; its background, pose, lighting and composition are not copied.
<Picture 2> (opening continuity anchor): fully_preserved for the actual preceding frame state only; it does not override <Picture 1> as the character reference.
<Audio 1>: fully_copy — reuse the entire supplied crop 1:1 as the final soundtrack, preserving its original vocals, recorded audience/stadium ambience if present, instrumental mix and dynamics.

detailed_description:

The target is a single-performer concert-theatre piece with emotional dance storytelling. Use the same stylized 3DCG character defined by <Picture 1>; keep the character image stable without textual appearance reconstruction. The stage has a visible dark deck and a compact proscenium-scale performance area. The performer remains the visual center and stays large in frame. Use close, close-medium, medium and subject-dominant medium-full shots only; never use an auditorium-wide, whole-stage or distant full-body establishing shot. When full-body dance needs to read, use a medium-full frame close enough to keep the face, hands and feet crisp. The camera must never pull far away merely to reveal scenery.

SCENE / EMOTIONAL PLAY:
Dramatic unit: CODA — The last light. The performer's immediate objective is: After the applause, she gives one final intimate gesture and lets the performance disappear.
Emotional movement: calm afterglow, intimacy and a final connection. Treat the original lyrics as emotional subtext and timing cues only; do not turn their nouns into literal objects, props, architecture, signs, illustrations or mime. The stage responds to the emotional shift through light, negative space and one abstract scenic construction, not through lyric illustration.

STAGE DESIGN / SCENIC MECHANICS:
All scenic pieces remain below the deck. Only one thin vertical backlight line remains behind the performer, with no additional prop or scenic object.
All scenic pieces emerge directly upward from concealed integrated lifts in the stage deck, stop at their defined height, pivot only when described, and descend vertically back into their own lift slots. Their movement is smooth, mechanically plausible and consistent in direction and timing. No visible stagehands, crew, technicians, performers, carts, cables, trusses or manual scenic handling. No extra actor, dancer, singer, band member or human silhouette enters the stage. No literal object is added because it appears in a lyric. Preserve only the scenic units described for this pair; do not invent extra furniture, books, food, windows, religious architecture, magical props or decorative clutter.

LIGHT / VISUAL HIERARCHY:
The warm frontal key remains long enough to preserve facial readability, then gradually softens as the single backlight line fades.
Keep a stable soft frontal key on the performer's face in every shot. Scenic light shapes the background and edges; it must not recolor the character or overpower facial readability. Each shot has one primary viewing target: face/eyes for emotional turns, complete body for major dance phrases, or one stage element when its rise or rotation is the story event. Avoid equal-brightness everywhere, constant beams, full-frame haze or excessive particles. The mood can become larger through layered lighting and parallax without changing to a wide shot.

OPENING CONTINUITY:
The previous segment's actual final frame is supplied as <Picture 2>. Preserve its actual body configuration, movement phase and scenic state, while deliberately recomposing to the Rev.8.3 local body-part close-up for this cut; continue any incoming scenic lift already in motion. The narrow frame from SEG20 has fully descended; the deck is visually clean and only the thin vertical backlight remains. She stays upright in the same floating axis.

TIMED SHOT SEQUENCE — LOCAL TIME FROM THE START OF THIS AUDIO CROP:
[Shot 1] Begin in a tight close-up of the same fingertips near the heart. Continue their small separation and let one hand rise along the chest line toward the cheek. Track the hand upward, then tilt to her relaxed eyes as the final breath releases. Resolve into a close portrait only after the hand-to-face pathway is complete. The camera remains close, physically plausible and steady enough for the body-part detail to read; this opening is a visual relay, not a new choreographic phrase. Complete the local-detail opening and reveal the performer’s upper-body action within the first 0.8 seconds of this clip; use a close-medium or subject-dominant medium-full view afterward. Keep natural perspective and body proportions; no digital zoom, wide-angle facial distortion or oversized hands.
[Shot 2] At 00:03.223, The camera moves in a very small lateral arc while she raises one hand from the heart and opens the palm toward the viewer. The movement is simple and sincere, with no new prop or scenic object.
[Shot 3] At 00:06.044, She lets the arm descend slowly while the shoulders and chest settle. The camera shifts focus from the open hand back to her eyes, retaining a stable medium close composition and a clean dark background.
[Shot 4] At 00:08.865, The last light line fades gradually. She remains vertically suspended and gives one tiny final nod, then holds a quiet, living expression until the exact end of the audio. No landing, no walk-off, no fade-generated extra scene, no title card.

CAMERA / EDITING:
Use physically motivated close-range camera routes: short lateral slider, shoulder-height counter-track, slight pedestal, controlled foreground pass, shallow arc outside the performer's action axis, measured focus handoff, and brief stable portrait holds. Vary the camera behavior across shots; do not default to orbit-push-orbit. Preserve the active screen direction and camera side within continuous action. No numeric camera-angle labels, no digital zoom, no lens warping, no random shake, no camera roll used to fake body rotation, and no impossible teleporting. A new [Shot N] is a genuine cut; continuous re-framing and focus movement remain inside the current shot. Internal cuts within this segment preserve the ongoing action phase. At a segment boundary, use the specific local-body-part visual relay defined in the Rev.8.3 transition table: the previous segment lands on that detail, and this segment opens on a tight close-up of the same detail before revealing the continuing dance. Match the movement vector, not the previous full-frame composition.

PERFORMANCE / FLOATING DANCE — ACTION-LIBRARY CHOREOGRAPHY:
This segment uses the named Dance Motion Chain Library source chains below. The chain IDs identify source material; they are not H3 control tokens. The four timed windows are the authoritative body-movement score and align to this segment’s existing shot boundaries. The shot sequence above supplies visual coverage, gaze, prop and scenic timing for these same actions; it must not trigger a second performance or repeat a chain.
Continuous movement layer: remain continuously suspended, with no floor-supported balance, standing, walking, takeoff or landing. The vertical body axis is maintained through coordinated rib-cage, spinal and pelvic counterbalance; both legs and pointed feet remain active as genuine dance lines, not passive dangling. Arms use full shoulder-to-fingertip pathways. Give each chain a clear preparation, initiation, expansion, accent, inertia and recovery; let the exit state become the next chain’s entry state.
Selected source chains: C14 — Quiet cheek-line opening; C3 — Small vertical arm circle; C1 — Breath release and settling wave; G3 Hero Lock — Living final tableau.
LOCAL DANCE TIMELINE (all times are local to this <Audio 1> crop):
00.000–03.223s | C14 — Quiet cheek-line opening: From the relaxed suspended state, incline the head and upper torso slightly toward the raised hand, then let the hand hover beside the cheek for one calm count. Keep the expression natural and the body axis upright.
03.223–06.044s | C3 — Small vertical arm circle: Raise one hand through a restrained vertical circle and open the palm toward the viewer. The shoulder initiates, the elbow follows and the wrist completes the path; the chest lifts gently without turning into a backbend.
06.044–08.865s | C1 — Breath release and settling wave: Allow a final breath to travel from the sternum through the ribs into the shoulders, then lower the arm with a delayed wrist release. The legs remain elongated and pointed beneath the pelvis; no new dance phrase is introduced.
08.865–10.332s | G3 Hero Lock — Living final tableau: Resolve into a calm, head-up floating line with one hand relaxed near the heart and the other lowered. Keep a trace of breath and fingertip life through the final audio sample rather than freezing early; the backlight fades without changing the body axis.
End-axis: finish with the head above the pelvis and the legs below, either vertical or in a natural three-quarter inclination. Complete the segment’s partial facing change before its final frame.

VOCAL / LIP-SYNC:
Exact lyric events in this crop (emotional timing reference): Instrumental; no lyric events in this crop.
No lip-sync in this crop. Preserve the original vocal track, but let the performer express its emotion through eyes, breath, facial reaction and dance; do not animate continuous syllable-shaped mouth movement.

OUTGOING STATE / NEXT SEGMENT HANDOFF:
Final state: the performer remains upright and suspended, hand lowering after the last open-palm gesture, eyes calmly held toward the lens. The stage stays clean; only the thin backlight line fades. The picture remains alive through the exact final audio sample.
Pair-level transition rule: 
The next segment must use the actual rendered final frame of this segment as <Picture 2>. The written outgoing state is a target for generation and editorial review, not a substitute for the actual exported frame. If the generated final frame differs, the next segment must follow the actual frame and update its opening action accordingly.

CONTINUITY / QUALITY:
Keep the exact same character image from <Picture 1> throughout, without textual appearance description. Keep one performer, one coherent stage, one consistent camera axis per continuous scene, stable scenic-unit count and physically possible lift motion. No duplicate body parts, no body morphing, no prop duplication, no staff, no audience or visible crowd, no extra performers, no literal lyric props, no subtitles, no lyric captions, no logos, no watermarks and no end card. Maintain the original character's vertical floating performance, clear full-body mechanics and crisp subject focus. Avoid wide shots and distant character scale.


overall_soundscape:

Preserve only the sound already present in <Audio 1>, including its original live-concert vocal energy and any recorded crowd swells or applause. Add no new audience track, no dialogue, no stage-worker voices, no footsteps, no scenic machinery foley and no extra sound effects. The original music remains dominant.

non_diegetic_music:

Reuse <Audio 1> once, unchanged, as the complete soundtrack for exactly 10.332 seconds. Preserve its original tempo of 170.15 BPM, beat interval 0.3526s, bar 1.4105s and phrase 2.821s. Local phrase anchors: 0.401s, 3.223s, 6.044s, 8.865s. Local downbeats: 1.812s, 4.633s, 7.454s, 10.275s. Detected high-confidence drum accents: 0.100s snare; 1.122s hihat; 6.370s kick; 7.415s snare. Synchronize movement peaks and shot changes to these actual phrase/downbeat accents, but do not invent drum hits or put a new action on every beat. No restart, loop, time-stretch, retime, remix, replacement, added score, added crowd audio, silence padding or early fade. End on the exact final sample of the supplied crop.
```


## 两段一组的实际生成顺序


- **第 1 组：SEG01 → SEG02。** 先用 Picture 1 + Audio 1 生成 SEG01；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG02 的 Audio 1 生成第二段。

- **第 2 组：SEG03 → SEG04。** 先用 Picture 1 + Audio 1 生成 SEG03；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG04 的 Audio 1 生成第二段。

- **第 3 组：SEG05 → SEG06。** 先用 Picture 1 + Audio 1 生成 SEG05；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG06 的 Audio 1 生成第二段。

- **第 4 组：SEG07 → SEG08。** 先用 Picture 1 + Audio 1 生成 SEG07；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG08 的 Audio 1 生成第二段。

- **第 5 组：SEG09 → SEG10。** 先用 Picture 1 + Audio 1 生成 SEG09；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG10 的 Audio 1 生成第二段。

- **第 6 组：SEG11 → SEG12。** 先用 Picture 1 + Audio 1 生成 SEG11；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG12 的 Audio 1 生成第二段。

- **第 7 组：SEG13 → SEG14。** 先用 Picture 1 + Audio 1 生成 SEG13；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG14 的 Audio 1 生成第二段。

- **第 8 组：SEG15 → SEG16。** 先用 Picture 1 + Audio 1 生成 SEG15；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG16 的 Audio 1 生成第二段。

- **第 9 组：SEG17 → SEG18。** 先用 Picture 1 + Audio 1 生成 SEG17；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG18 的 Audio 1 生成第二段。

- **第 10 组：SEG19 → SEG20。** 先用 Picture 1 + Audio 1 生成 SEG19；导出真实最后一帧，再以 Picture 1 + 该末帧作为 Picture 2 + SEG20 的 Audio 1 生成第二段。

- **尾声：SEG21。** 使用 Picture 1 + SEG20 的实际最后一帧作为 Picture 2 + SEG21 Audio 1。


## 交付核对


- 21 段；原曲总时长 252.648s；BPM 170.15；单段长度范围 10.000–14.936s。

- 每段六字段 Ref2VA；每段一个独立复制代码块；每段有明确的开场承接与末态；没有新增员工、第二表演者、观众正脸或歌词实体道具。
