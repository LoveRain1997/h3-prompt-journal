# Case Study 012 — 台灯五章节奏 · 高定时尚大片 A/B 双版（Editorial Lamp-Rhythm Fashion Film, Dark-Luxury vs Cute）

> 一支 15 秒、**完全由音乐时间轴驱动**的高定 editorial 时尚大片，同一套「台灯五章 + 10 个互不重复身体架构 + 离散时尚机位」骨架，做出两个可直接生成的版本：**p83 暗奢·双手猛撩裙摆** 与 **p84 可爱·双手高举后折脚跳跃**。机制不变，只换调性、配器与结尾 Hero。单图锁定人物与房间，正文零外貌；台灯是踩在 downbeat 上的节奏视觉锚。

## Inputs（输入）

- **`<Picture 1>`（单图，唯一视觉权威）**：成年主角 + 完整物理环境——身份 / 脸 / 发型 / 体型 / 肤色、整套服装 / 鞋 / 配饰、**裙摆结构与裙内不透明贴身舞蹈安全裤**、现场台灯及其位置、房间几何 / 家具 / 地板 / 墙面 / 陈设、灯光方向 / 曝光 / 调色 / 对比 / 写实质感。
- **AUDIO**：提示词内自建 `non_diegetic_music`（无外部音频文件），BPM 124 / 4/4，两版仅调性与配器不同。
- 目标：不是常规舞蹈片，而是「一张张会动的时尚照片」拼成的 premium 广告；提示词全英文，正文不描写外貌。
- 两份逐字成品：
  - [`p83-dark-luxury-skirt-throw.txt`](./p83-dark-luxury-skirt-throw.txt) — 暗奢 E minor，结尾 **MASSIVE SKIRT THROW / HERO BULLET-TIME**
  - [`p84-cute-backfolded-jump.txt`](./p84-cute-backfolded-jump.txt) — 可爱 A major（NEW CUTE VERSION），结尾 **TWO-HAND HIGH JUMP / BACK-FOLDED FEET HERO**

## The problem（问题：要换调性，却不能推翻已经跑通的节奏骨架）

p83 暗奢版已经把「音乐—灯光—动作—机位」咬合得很死，但成片气质偏性感、结尾靠双手撩裙摆露安全裤。想要一支**更轻、更可爱、更贵气俏皮**的版本时，最容易犯的错是从头重写——结果把已经验证有效的灯点、moment 边界、相机纪律全部弄丢。

真正的需求是一次**受控变奏（controlled variation）**：保留可复用的机制（Creative DNA），只替换表层的情绪、音色和结尾那个最大动作。这个案例展示了如何让两版共享同一副骨架、只在三个指定层面分叉，从而低成本产出气质迥异但节奏同样精准的成片。

## The breakthrough（突破：固定骨架，只在三层分叉）

两版**逐字相同**的骨架：

1. **单图全锁、零外貌文字**：人物、服装、台灯、房间一律由 `<Picture 1>` 承担，配一大段 `Preserve exactly …` 与 `Do not redesign / relocate / add / remove`；正文 token 全部投给时间轴、身体力学与机位。
2. **台灯 = 踩 downbeat 的节奏视觉锚**：五次开关严格落在小节线，无渐变 / 闪烁 / 变色 / 新光源，房间物理上保持同一间。
3. **10 个 MOMENT 身体架构互不重复**：每个动作都走 `INITIATION → TRAVEL → ACCENT → BRAKE → RELEASE`，动作之间不许回中性站姿、不许重复 contrapposto / 摆胯 / 撩发 / 走向镜头 / 原地转。
4. **离散时尚机位（非一条连续运镜）**：压缩长焦、中肖像、中全景、短跟拍、rack focus、肩部遮挡、发丝擦镜、短 arc、受控 ROLL、hard brake、末段 rapid pullback。
5. **优先级链**：`BGM 结构 → 音乐 accent → 身体发起 → 身体力学 → 独特 pose 架构 → 相机响应 → 选择性 ROLL → 相机 brake → 台灯状态 → 剪辑过渡 → 下一个音乐事件`。音乐永远是第一驱动。

只在以下三层分叉（见对照表）：**音乐调性与配器、中段若干下身动作、结尾 MOMENT 10 的 Hero 机制**。

## 两版差异对照（A/B）

| 维度 | p83 暗奢版 | p84 可爱版 |
|---|---|---|
| 定位 | sensual editorial attitude film（性感克制） | cute / elegant / mischievous attitude film（俏皮贵气） |
| Genre | dark luxury high-fashion electro | playful luxury electro-pop |
| 调式 / Key | **E minor** | **A major** |
| 鼓与贝斯 | tight gated kick、rounded sub-bass | tight but **soft** kick、rounded **playful** bass |
| 主音色 | dry metallic plucks、percussive clicks、filtered rising noise | bright **mallet plucks、小铃铛 bell、sparkling synth、pizzicato 电子音、tiny claps、playful riser** |
| 明确排除 | lush pads、vocals、lyrics | 暗黑 drone、重 cinematic bass、工业打击、恐怖质感、pads、**vocals/lyrics** |
| MOMENT 05 | **LEG SWEEP**：支撑脚站定，另一腿由胯带动向后划半圆，裙摆延迟拖出弧线 | **LATERAL STEP / TOE POINT**：小侧步、重心侧移、脚尖干净点地（明确不是划腿 / 踢 / 转 / 重复下蹲） |
| MOMENT 06 | ARM / BACK RELEASE：一臂向后上延展、肩背对立轴 | DIAGONAL REACH / **LIGHT BOUNCE**：脚踝膝盖小弹（明文 NOT a jump，脚不离地） |
| MOMENT 07 | KNEE DRIVE / CLOTHING SNAP：单膝向前带过中线、裙摆 fabric snap | QUICK KNEE TAP / SHOULDER ACCENT：紧凑小抬膝 + 双肩前后 sharp accent |
| MOMENT 09（蓄力） | **SIDE-FACING SKIRT PRELOAD**：侧三-quarter，双手握住裙摆两侧、屈胯蓄力、裙不开 | **JUMP PRELOAD / ARM SWING**：双脚站定屈膝、双臂向后摆加载、裙保持自然闭合、手不碰裙 |
| **MOMENT 10（结尾 Hero）** | **MASSIVE SKIRT THROW**：双手在 impact 同时向外猛甩裙摆 → fabric whip → 裙摆最大绽放 → 稳定身体为中轴、裙摆惯性继续 → bullet-time → 安全裤在撩裙峰值清晰露出 | **TWO-HAND HIGH JUMP / BACK-FOLDED FEET**：蹬地双腿起跳 → 双手在头顶高举成 V → **双脚后折并拢成一个紧凑整体**（不分叉、不踢镜头）→ 跳跃惯性自然扬起裙摆、安全裤清晰可见 → 空中 bullet-time → 落地英雄站姿 |
| 安全裤露出方式 | 由「手甩裙摆」造成，强调 forceful throw、非慢开、非手拉暴露 | 由「向上跳跃的物理惯性」造成，强调不手拉裙、不制造透明 / 走光 |
| 收尾画面 | 大开放裙摆 campaign still，硬锁 | 落地后自然 settle 的 premium campaign 照片感，硬锁 |

> 两版 MOMENT 01–04、08 与所有灯点、相机 ROLL 分布、时间边界完全一致；分歧集中在 05/06/07 的下身质感与 09/10 的结尾机制。

## 台灯五章与精确灯点（两版共用，可复算）

BPM 124 → 1 beat = 60/124 = **0.484s**，1 bar（4 拍）= **1.936s**；全片 = **7 个完整小节 + 3 拍结尾** = 7×1.9355 + 3×0.4839 = **15.000s**。

| 时间 | 小节位置 | 台灯 | 章节 |
|---|---|---|---|
| 0.000 | bar 0 | **ON** | A 建立身体节奏（0.000–3.871） |
| 3.871 | bar 2 | **OFF** | B 暗场 / 图形剪影（3.871–7.742） |
| 7.742 | bar 4 | **ON** | C 回亮 / 能量更新（7.742–11.613） |
| 11.613 | bar 6 | **OFF** | D 悬停期待 temporal vacuum（11.613–13.548） |
| 13.548 | bar 7 | **ON** | E 最终 Hero impact（13.548–15.000，3 拍尾） |

> 灯点严格每 2 小节一次（3.871 / 7.742 / 11.613），最终 impact 落在第 7 小节头 13.548。每次开关都与音乐 downbeat 精确同帧，并配一声克制的实体开关 `switch click`（写在 `overall_soundscape`，踩这四个点）。OFF 不是黑场，用房间残余照明自然呈现。

## 10-MOMENT 骨架（两版共用时间边界，★＝两版分歧）

| Moment | 时间 | 身体 / 镜头要点 |
|---|---|---|
| 01 | 0.000–1.300 | 反向重心转移、脚跟轻抬、一臂斜后；中全景三-quarter 侧，短跟拍 + 极短**顺时针 ROLL**，~1.0s 双 hard brake |
| 02 | 1.300–2.600 | 肘起在头侧构图、头反向轻歪；侧颜→三-quarter 前，焦段压缩 + rack focus 前臂→眼，**无 ROLL**，时尚肖像 |
| 03 | 2.600–3.871 | **纯侧面下蹲**、一腿斜伸长腿线、躯干挺直不朝镜头；随胯下降，最低点一次**逆时针 ROLL** 后回正；3.871 灯 OFF |
| 04 | 3.871–5.806 | 支撑脚起身（胯先起）、转**后三-quarter**、回头看镜头；肩部遮挡→rack focus 肩→眼，灯保持 OFF |
| 05 ★ | 5.806–7.742 | p83 后腿**划半圆** / p84 **侧步点地**；toe / sweep accent 上短**顺时针 ROLL**；7.742 灯 ON |
| 06 ★ | 7.742–9.677 | p83 手臂向后上 release / p84 斜上够 + 轻弹；手→前臂→肩→颈→脸的垂直 rise，无 ROLL，直视镜头 |
| 07 ★ | 9.677–11.613 | p83 单膝前带 + 裙摆 snap / p84 小抬膝 + 双肩 accent；下半身跟后快速上摇到脸，最锐 accent 一次短**顺时针 ROLL**；10.645 sub hit、11.129 hi-hat burst；11.613 灯 OFF |
| 08 | 11.613–12.250 | **Temporal vacuum 静止**：音乐抽稀，几乎定格、仅呼吸 / 发丝 / 配饰微动；相机水平、仅极小前向 parallax，无 ROLL / zoom / 慢动作 |
| 09 ★ | 12.250–13.548 | p83 双手抓裙两侧**撩裙 preload** / p84 屈膝摆臂**跳跃 preload**；~13.300 riser 张力最大、定格蓄力；13.548 灯 ON，Moment 10 立刻起 |
| 10 ★ | 13.548–15.0 | 音乐 hit + 灯 ON + 最大动作三合一；rapid pullback 微升 + 短 arc 给全整空中 / 绽放轮廓，峰值 **bullet-time feel（非字面慢动作）**；~13.9 动作到顶开始下落 / 收手，~14.1 落地 / 硬锁，14.1–15.0 近乎全静的 campaign still |

## 相机系统纪律（两版共用）

- **离散构图而非一条连续运动**：每个相机状态由不同身体动作触发，靠快速 editorial 过渡连接。
- **ROLL 只在 01 / 03 / 05 / 07 四个点**，且都是绕光轴的极短、受控旋转，绑死具体动作 accent；**每次 roll 后地平线必须回正**；不连续转、不 360°、不绕房间 orbit、不长期歪 horizon。Moment 08、09 保持水平。
- **Hard brake**：每个 pose 到位时相机与身体同时硬刹，形成短暂时尚静止。
- **Bullet-time feel** 只出现在结尾峰值：主观时间密度被拉长，但人物是稳定中轴、头发 / 裙摆 / 衣缘保留真实惯性；明文「不是字面慢动作、不机械冻结」。
- 机位关系反复在 profile / 后三-quarter / 前三-quarter / 局部 / 腿位中全景 / 最终全身之间切换；禁用顶拍、地板广角、鱼眼、无尽 zoom、通用慢推。

## 合规 / 安全设计（值得复用的写法）

- 主角明确为**成年专业时尚表演者**，全程着装（fully clothed）；裙内**不透明贴身舞蹈安全裤**被定义为造型的固定服装层，全程「不消失 / 不变透明 / 不变形 / 不移位 / 不被替换」。
- 结尾露安全裤被反复框定为**完整着装下的时尚造型 reveal，绝非裸露或内衣暴露**；p84 更进一步改为由跳跃惯性自然扬起裙摆，明文不许手拉裙、不许透明面料、不许 wardrobe malfunction。
- 躯干一旦降低，必须是**纯侧面 / 后三-quarter / 强侧三-quarter**，禁止胸部朝镜头的正面下俯、禁止 cleavage 特写与胸部构图；可爱版另加「不幼态、不卡通、不夸张 kawaii」。

## 48-hour takeaway（可复用清单）

1. **A/B 改版只换表层、不重写机制**：把跑通的时间轴 / 灯点 / 机位 / 优先级链原样保留，分叉点集中在调性、配器与结尾 Hero，改完两版节奏天然对齐、可直接对比成片。
2. **让一个道具成为节拍器**：台灯五章把「灯光状态」写进剪辑语言，开关全部钉在 downbeat（本例每 2 小节），并配同点实体音效——音乐、灯光、动作三合一，成片像被音乐剪辑出来。
3. **先算音乐网格再写动作**：BPM→beat/bar 时长→小节线灯点→「7 小节 + 3 拍尾 = 15.0s」，所有 moment 边界与 sub hit（10.645 / 11.129）都挂在网格上。
4. **十个 moment 强制身体架构不重样**：每个动作写明与前一个的区别，并显式排除重复（同款蹲 / 侧步 / 跳互不相似），配 `INITIATION→TRAVEL→ACCENT→BRAKE→RELEASE`。
5. **ROLL 可数、必回正**：只在少数具名时刻出现、绑死动作、用后回正；末段 bullet-time 是「时间密度」不是慢动作。
6. **敏感露出用服装层 + 朝向规则提前锁死**：把安全裤写成不透明造型层、把俯身朝向限定为侧面，结尾 reveal 即合规。

## Assets

| 文件 | 作用 |
|---|---|
| [`p83-dark-luxury-skirt-throw.txt`](./p83-dark-luxury-skirt-throw.txt) | 暗奢 E minor 版完整成品（结尾双手撩裙 Hero），逐字 |
| [`p84-cute-backfolded-jump.txt`](./p84-cute-backfolded-jump.txt) | 可爱 A major 版完整成品（结尾双手高举后折脚跳 Hero），逐字 |

> 两份成品与下载源文件 SHA-256 一致（字节级逐字保存）。生成时需自行提供 `<Picture 1>`（人物 + 含台灯的室内环境参考图）；仓库不含受版权 / 肖像约束的图像、音频与成片。

## Tags

`#H3` `#prompt-engineering` `#high-fashion` `#editorial-film` `#fashion-commercial` `#image-locked` `#zero-appearance-description` `#music-driven` `#beat-sync` `#lamp-rhythm` `#lighting-as-editing` `#discrete-compositions` `#camera-state-machine` `#controlled-roll` `#hard-brake` `#bullet-time` `#hero-frame` `#ab-variation` `#mechanism-migration` `#safety-shorts`
