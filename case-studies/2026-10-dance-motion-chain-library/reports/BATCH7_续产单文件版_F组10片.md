# BATCH7 续产单文件版 · F 组 10 片（D041/D058/D059/D060/D061/D067/D069/D070/D071/D072）

> 整片档案制续产（D/E/F 串行组的 F 组，收官批）：每片七件套，规格同 D/E 组。反推全程未切割；BPM 全部 onset_probe 实测+置信分层，散板/无网格片拒写数值；AIGC 三档判定附帧证据（D041 动画型 AI 高置信；D067 混合/存疑）；动作编号 `Dxxx-Ayy` 只进索引表不进提示词正文。
> 本文件为续产第三批（F 组）；至此 batch7 全部 57 片（首批 30 + D 组 10 + E 组 7 + F 组 10）入库完成。

---

# D041 反推档案

- **档案号**：D041（源 v26）
- **短标题 ↔ 原片名**：AI魔法少女战斗短片 ↔ 《战场魔法少女》成为魔法少女的第一日03【AI全民制作人】.mp4
- **时长**：82.96s（30fps）
- **画幅**：1280×720 横屏
- **音轨**：有（配乐/音效；含中文 AI 生成对白字幕）
- **观察状态**：COMPLETE（scope=visual+audio；接触表 2s/格 覆盖全片 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 1280×720 横屏 / 82.96s |
| 镜头形态 | 多镜头叙事短片：废墟战场、人物特写、变身/魔法特效、对话字幕；大量切镜与镜头运动（电影语言） |
| 运镜 | 多机位、含推拉/跟拍/特写切换 |
| 剪辑层 | 多切镜；含特效（魔法光效/爆炸）、白闪转场；画面带中文字幕（对白/旁白） |
| **ABC 结论** | **C 多镜快剪**（AI 生成叙事短片，非真实舞蹈；按库规则作"动作展示"特例登记） |

## ② 场景与人物档案

**场景（多段）**：废墟城市战场（灰暗天空、倒塌建筑、烟尘）、街道；含魔法光效与爆炸场面。

**人物**：
- 粉发少女（变身形态，粉色花瓣状裙装+花饰），多处战斗/倒地/特写。
- 黑发双马尾少女（深色战斗服），与粉发角色对峙/对话。
- 黑衣机甲/装甲角色（远景）。
- 全片含大量中文对白字幕（AI 生成剧情）。

**内容性质**：AI 生成动画短片（原片名标注「AI全民制作人」），人物为虚拟角色，动作含战斗/魔法/变身，非真人舞蹈。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-6.0 | 废墟中粉发少女倒地/挣扎起身，镜头特写手部；白闪转场 | 近景+特写切换 |
| 6.0-18.0 | 金发角色特写、直升机/街道远景、黑发少女侧脸，对峙铺垫 | 多机位叙事 |
| 18.0-40.0 | 战斗/魔法场面：黑衣装甲角色、粉发少女释放魔法（光片特效）、双方对峙；字幕推进剧情 | 中景+特效镜头 |
| 40.0-62.0 | 粉发少女战斗与倒地交替、双马尾少女表情特写，魔法光效贯穿 | 特写+动作镜头 |
| 62.0-82.96 | 收尾段：角色对话特写、粉色魔法花瓣特效、末帧人物近景 | 近景 |

**末三分之一倒查**：末帧为角色近景；全片为叙事剪辑，无单一动作链；动作时序依剧情与镜头，非节拍驱动。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 215.3 BPM（不可采信：配乐/音效混合，含对白，无舞蹈节拍网格）
- 判定：**无稳定节拍（禁写 BPM 数值）**；叙事短片依剧情时间码，不依赖节拍。

## ⑤ AIGC 判定（帧证据）

**结论：AI 高置信=是（判定：AI 生成动画，高置信）**
- 证据 1：原片名明确标注「AI全民制作人」，为 AI 生成内容平台作品。
- 证据 2：人物面部与服装为典型 AI 二次元风格，帧间存在细节漂移（发饰/服饰纹样在不同镜头不一致）；魔法光效与爆炸为生成式特效。
- 证据 3：中文字幕为 AI 生成对白，叙事逻辑为 AI 短片典型结构。
- 首批评级对照：此类 AI 叙事短片不同于 D019（真人感古风 AI 高置信），本片为**动画型 AI 高置信**，单列登记。

## ⑥ 剪辑特效层

- 切点：大量（多镜头叙事剪辑）。
- 特效/叠加：魔法光效/花瓣粒子/爆炸/白闪转场、中文字幕；全部为 AI 生成画面内元素+后期字幕。
- 变速：含慢镜/特效镜头。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: AI-generated anime-style short film in horizontal 1280x720 format, a dark fantasy battle narrative. In ruined city streets under a grey sky with smoke and collapsed buildings, a pink-haired girl in a flower-petal dress with floral ornaments fights and falls, a black-haired twin-tailed girl in dark combat attire confronts her, and black armored figures appear in the distance. From 0.0 to 6.0 seconds the pink-haired girl collapses and struggles to rise in the ruins with a hand close-up and a white-flash transition. From 6.0 to 18.0 seconds close-ups of a blonde character, a helicopter and street scenes, and the twin-tailed girl's profile build the confrontation. From 18.0 to 40.0 seconds magic effects, light shards and explosions accompany the battle with Chinese dialogue subtitles advancing the story. From 40.0 to 62.0 seconds the pink-haired girl fights and falls alternately, the twin-tailed girl's expressive close-ups intercut with magic light effects. From 62.0 to 82.96 seconds the ending shows character dialogue close-ups and a pink magical petal effect, ending on a character near-shot. This is a generated animated narrative, not live-action dance.

overall_soundscape: Cinematic orchestral and electronic score with battle sound effects (explosions, magic whooshes) and AI-generated Chinese dialogue carried by subtitles.

non_diegetic_music: A dramatic cinematic score with percussive battle cues; no steady dance beat grid.
```

## 动作索引表

| 编号 | 名称 | 拍数(无BPM→秒) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D041-A1 | 废墟倒地挣扎 | 6s | 0.0-6.0 | 倒地→挣扎起身+手部特写+白闪 | H3: the pink-haired girl collapses and struggles to rise in the ruins with a hand close-up |
| D041-A2 | 角色对峙铺垫 | 12s | 6.0-18.0 | 特写→多角色/街景对峙 | H3: close-ups and street scenes build the confrontation between the characters |
| D041-A3 | 魔法战斗爆发 | 22s | 18.0-40.0 | 对峙→魔法光效+爆炸+战斗 | H3: magic effects and explosions accompany the battle with dialogue subtitles |
| D041-A4 | 战斗倒地交替 | 22s | 40.0-62.0 | 战斗→粉发少女倒地/双马尾特写交替 | H3: the pink-haired girl fights and falls alternately, intercut with the twin-tailed girl's close-ups |
| D041-A5 | 对话花瓣收尾 | 21s | 62.0-82.96 | 交替→对话特写+花瓣特效→角色近景 | H3: the ending shows dialogue close-ups and a pink magical petal effect |

<!-- ============ 档案分隔 ============ -->

# D058 反推档案

- **档案号**：D058（源 v43）
- **短标题 ↔ 原片名**：米白毛衣室内舞蹈 ↔ 软呼呼～被这件毛衣拿捏住了.mp4
- **时长**：41.05s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 覆盖全片 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 41.05s |
| 镜头形态 | 单一连续镜头，固定机位全身；室内（深色沙发/白墙），女生穿米白麻花毛衣+浅黄短裙+白色腿套+厚底鞋跳舞；无切点 |
| 运镜 | 固定机位；无推拉变焦 |
| 剪辑层 | 无剪辑；无贴纸/变速 |
| **ABC 结论** | **A 一镜到底**（固定机位室内舞蹈） |

## ② 场景与人物档案

**场景**：室内，深色布艺沙发、白色墙面、浅色地板；自然室内光。

**人物 1（主体）**：年轻东亚女性，长发（部分帧扎起）；米白色麻花针织毛衣 + 浅黄色短裙 + 白色过膝腿套 + 米色厚底鞋。单人舞蹈，动作轻快。

**平台水印**：左上角水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-10.0 | 起势：从侧身走入/转身，双手交替摆动、踏步 | 固定竖屏全身，人物居中 |
| 10.0-22.0 | 双臂上举/交叉摆动，扭胯踏步，裙摆与毛衣随动 | 同上 |
| 22.0-32.0 | 手部在胸前做组合动作，配合踢腿/侧点步 | 同上 |
| 32.0-41.05 | 延续摆臂踏步，末段收势于站立造型 | 同上 |

**末三分之一倒查**：末帧站立造型，动作自然收束；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 99.4 BPM
- 强 onset 网格与舞蹈踏步对齐。
- 判定：**固定节拍**，提示词用 "≈99 BPM" 参考；精确对拍以时间码为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中-高置信）**
- 证据：麻花毛衣纹理、沙发缝线、腿套褶皱在帧间稳定；动作运动模糊连续。
- 反证检查：未见肢体融合/背景重排。注：有美颜磨皮。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：美颜、水印。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 footage in a room with a dark sofa and white walls. A young East Asian woman with long hair wears a cream cable-knit sweater, a pale yellow short skirt, white over-knee leg warmers and beige platform shoes, dancing alone. From 0.0 to 10.0 seconds she turns into frame and starts with alternating arm swings and stepping. From 10.0 to 22.0 seconds she raises and crosses her arms, swaying her hips and stepping as the skirt and sweater move. From 22.0 to 32.0 seconds she makes hand combinations at chest height with kicks and side steps. From 32.0 to 41.05 seconds she continues arm swings and steps, settling into a standing pose. Beauty smoothing and a watermark are applied.

overall_soundscape: An upbeat pop track drives the dance; quiet indoor ambience. No speech.

non_diegetic_music: An upbeat Chinese pop track at approximately 99 BPM with a steady kick.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈99BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D058-A1 | 转身摆臂踏步 | 12 | 0.0-10.0 | 侧身→转身+交替摆臂踏步 | H3: turns into frame and starts with alternating arm swings and steps |
| D058-A2 | 举臂交叉扭胯 | 14 | 10.0-22.0 | 摆臂→举臂交叉+扭胯踏步 | H3: raises and crosses her arms, swaying her hips and stepping |
| D058-A3 | 胸前手势踢腿 | 14 | 22.0-32.0 | 交叉臂→胸前手势+踢腿侧点 | H3: makes hand combinations at chest height with kicks and side steps |
| D058-A4 | 摆臂收势 | 12 | 32.0-41.05 | 踢腿→摆臂踏步→站立定格 | H3: continues arm swings and steps, settling into a standing pose |

<!-- ============ 档案分隔 ============ -->

# D059 反推档案

- **档案号**：D059（源 v44）
- **短标题 ↔ 原片名**：姐妹户外同步舞 ↔ 依旧姐妹同步率99.95%.mp4
- **时长**：10.97s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 10.97s |
| 镜头形态 | 单一连续镜头，固定机位全身；户外（绿篱/树墙背景），两名女生穿运动短装做同步舞蹈；无切点 |
| 运镜 | 固定机位；无运动 |
| 剪辑层 | 无剪辑/无特效 |
| **ABC 结论** | **A 一镜到底**（固定机位双人同步舞） |

## ② 场景与人物档案

**场景**：户外，绿色树篱/灌木墙背景，浅色地面（操场/步道），白天自然光。

**人物 1、2（双人）**：两名年轻东亚女性，长发扎起；白色/浅色运动短上衣 + 牛仔短裤 + 中筒袜 + 白色运动鞋；动作高度同步（镜像/齐舞），含举手、踢腿、扭胯、下蹲。

**平台水印**：左上角水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-2.5 | 两人并排站立起势，双臂上举做心形/V字 | 固定竖屏全身，两人居中 |
| 2.5-6.0 | 同步踢腿（交替侧抬腿）+ 手臂上举/侧伸 | 同上 |
| 6.0-9.0 | 同步扭胯、下蹲、手臂交叉组合 | 同上 |
| 9.0-10.97 | 收势于同步站姿/手势定格 | 同上 |

**末三分之一倒查**：末帧双人同步站姿；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 132.5 BPM
- 强 onset 网格与踢腿/下蹲重拍对齐。
- 判定：**固定节拍**，提示词用 "≈132 BPM" 参考。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中-高置信）**
- 证据：双人同步动作位置稳定、无个体漂移；树篱纹理与短裤/袜褶皱连续。
- 反证检查：未见肢体融合/背景重排。注：有美颜。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：美颜、水印。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 footage outdoors in front of a green hedge wall on a light paved ground. Two young East Asian women with tied-back hair wear matching light sports crop tops, denim shorts, mid-calf socks and white sneakers, dancing in high synchronization. From 0.0 to 2.5 seconds they stand side by side raising both arms into a heart or V shape. From 2.5 to 6.0 seconds they kick alternating legs sideways with arms raised or extended in unison. From 6.0 to 9.0 seconds they sway their hips, crouch and cross their arms in matched combinations. From 9.0 to 10.97 seconds they settle into a synchronized standing pose with a hand gesture. Beauty smoothing and a watermark are applied.

overall_soundscape: An upbeat dance-pop track drives the synchronized moves; outdoor ambience. No speech.

non_diegetic_music: An energetic pop track at approximately 132 BPM with a clear kick grid.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈132BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D059-A1 | 并举手臂起势 | 6 | 0.0-2.5 | 并排站立→双臂心形/V字 | H3: stand side by side raising both arms into a heart or V shape |
| D059-A2 | 同步侧踢举臂 | 8 | 2.5-6.0 | 举臂→交替侧踢+手臂升降 | H3: kick alternating legs sideways with arms raised in unison |
| D059-A3 | 扭胯下蹲交叉臂 | 8 | 6.0-9.0 | 踢腿→扭胯下蹲+交叉臂 | H3: sway their hips, crouch and cross their arms in matched combinations |
| D059-A4 | 同步收势 | 4 | 9.0-10.97 | 交叉臂→同步站姿手势定格 | H3: settle into a synchronized standing pose with a hand gesture |

<!-- ============ 档案分隔 ============ -->

# D060 反推档案

- **档案号**：D060（源 v45）
- **短标题 ↔ 原片名**：银杏林白裙恋爱循环舞 ↔ 仿佛回到了2010年的温暖…？『恋爱循环竖屏』.mp4
- **时长**：90.07s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 覆盖全片 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 90.07s |
| 镜头形态 | 单一连续镜头，固定机位全身；户外金黄色银杏林（秋日暖光），女生穿白色上衣+蓬蓬纱裙跳舞；长片无切点 |
| 运镜 | 固定机位；无推拉变焦 |
| 剪辑层 | 无剪辑；暖色梦幻滤镜 |
| **ABC 结论** | **A 一镜到底**（固定机位秋景长片舞蹈） |

## ② 场景与人物档案

**场景**：户外银杏林/林荫道，满树金黄银杏叶与落叶，暖色逆光，画面带梦幻暖调滤镜与光斑。

**人物 1（主体）**：年轻东亚女性，金色/浅棕长发；白色上衣 + 白色蓬蓬纱裙 + 白色鞋袜。单人舞蹈，动作为举手、旋转、踢腿、裙摆展示，节奏轻快。

**平台水印**：左上角水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-18.0 | 起势：站立双手展开/侧举，旋转展示裙摆，暖光穿过银杏叶 | 固定竖屏全身，人物居中 |
| 18.0-40.0 | 连续舞蹈：手臂上举波浪、交替踢腿、侧步转身，裙摆飞起 | 同上 |
| 40.0-64.0 | 副歌段：大幅举臂、跳跃、旋转组合，动作幅度最大 | 同上 |
| 64.0-90.07 | 延续舞蹈并逐渐收束，末段站立/举臂造型收势 | 同上 |

**末三分之一倒查**：末帧站立造型，动作自然收束；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 60.1 BPM（半速候选）
- 强 onset 密集且近似等距；主候选 ≈120 BPM（二倍速网格）。
- 判定：**固定节拍（中速）**，提示词用 "≈120 BPM" 参考；对拍以时间码为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中置信）**
- 证据：银杏叶/树干纹理在帧间稳定；裙摆与头发运动模糊连续；光斑为自然逆光+后期叠加。
- 反证检查：未见明显肢体融合/背景重排。注：暖调梦幻滤镜降低细节可核性。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：暖色梦幻滤镜、光斑、美颜、水印。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 footage in a golden ginkgo grove in autumn with yellow leaves and warm backlight, a dreamy warm filter and light flares. A young East Asian woman with golden-light brown long hair wears a white top, a white fluffy tutu skirt and white shoes, dancing alone. From 0.0 to 18.0 seconds she starts standing with arms opening and extending sideways, spinning to show the skirt as warm light filters through the ginkgo leaves. From 18.0 to 40.0 seconds she dances continuously with arms raised in waves, alternating kicks, side steps and turns, the skirt flying with the motion. From 40.0 to 64.0 seconds during the chorus she makes large arm raises, jumps and spins with the biggest movement amplitude. From 64.0 to 90.07 seconds she continues and gradually winds down, ending in a standing or arm-raised pose. Beauty smoothing, a warm filter and a watermark are applied.

overall_soundscape: An upbeat nostalgic J-pop dance track drives the choreography; soft outdoor ambience. No speech.

non_diegetic_music: A bright J-pop style dance track at approximately 120 BPM with a steady kick.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈120BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D060-A1 | 展臂旋转展裙 | 24 | 0.0-18.0 | 站立→双臂展开侧举+旋转展裙 | H3: opens her arms sideways and spins to show the skirt in warm backlight |
| D060-A2 | 举臂波浪踢腿 | 30 | 18.0-40.0 | 旋转→举臂波浪+交替踢腿侧步转身 | H3: dances with arm waves, alternating kicks, side steps and turns |
| D060-A3 | 副歌大幅举跳旋 | 32 | 40.0-64.0 | 踢腿→大幅举臂+跳跃+旋转 | H3: makes large arm raises, jumps and spins during the chorus |
| D060-A4 | 舞步收势造型 | 34 | 64.0-90.07 | 旋转→延续舞步→站立/举臂收势 | H3: continues dancing and winds down into a standing or arm-raised pose |

<!-- ============ 档案分隔 ============ -->

# D061 反推档案

- **档案号**：D061（源 v46）
- **短标题 ↔ 原片名**：商场舞台路演直拍 ↔ 开头转身美得我忍不住嚎哭起来…….mp4
- **时长**：137.58s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（现场音乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 覆盖全片 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 137.58s |
| 镜头形态 | 多机位舞台直拍：商场中庭舞台（LED 背景屏、品牌展台），蓝白女团服女生领舞+伴舞；全景/中景/近景/侧机位切换；长片 |
| 运镜 | 各机位固定+部分手持跟随；段间硬切（多机位导播） |
| 剪辑层 | 多切点（机位切换）；含现场屏幕画面、观众入镜；无变速 |
| **ABC 结论** | **C 多镜切换**（舞台多机位直拍，长片） |

## ② 场景与人物档案

**场景**：商场中庭活动舞台，蓝紫色 LED 背景屏（显示品牌/活动字样）、绿色展台、台下观众与工作人员；舞台灯光。

**人物 1（主体）**：年轻东亚女性，长发扎马尾；蓝白色女团打歌服（短上衣+短裙+长靴/白鞋）；开场即转身亮相，领舞。
**伴舞**：多名女生（部分帧可见 1-2 名），服装相近。

**平台水印**：左上角水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-16.0 | 开场转身亮相：背对转身面向观众，走步、叉腰、定点 pose（对应片名"开头转身"） | 镜1 中景，舞台 |
| 16.0-40.0 | 群舞第一段：手臂上举/交叉、扭胯、踏步，队形小范围移动；机位切换至近景/侧机位 | 多机位交替 |
| 40.0-80.0 | 副歌段：整齐的举手、挥摆、踢腿、下蹲组合，伴舞同框，LED 屏变化 | 全景+近景穿插 |
| 80.0-115.0 | 延续齐舞与走位，队形变化（散开/聚拢），表情管理 | 多机位 |
| 115.0-137.58 | 末段收势：集体造型（举手/定点 pose），镜头定格于主体 | 近景/全景收尾 |

**末三分之一倒查**：末帧集体造型收束；长片机位切换有乐句动机，无叙事断层。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 64.6 BPM（半速候选）
- 强 onset 密集（720 个），主候选 ≈129 BPM（二倍速）；现场音乐节拍网格成立。
- 判定：**固定节拍**，提示词用 "≈129 BPM" 参考；齐舞对拍以时间码为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，高置信）**
- 证据：现场观众、LED 屏内容、舞台结构在帧间稳定；多人舞蹈位置连续无漂移；转身与裙摆运动模糊真实。
- 反证检查：未见人物融合/背景重排。现场直拍为强实拍证据。

## ⑥ 剪辑特效层

- 切点：多切点（多机位导播切换）。
- 特效/叠加：舞台灯光、LED 屏、水印；无额外贴纸特效。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 multi-camera fancam of a mall stage performance. A young East Asian woman with a high ponytail wears a blue-and-white idol stage outfit (crop top, short skirt, long boots) leading a dance with backup dancers on a stage with a blue-purple LED screen and green event booth, an audience and staff visible around. From 0.0 to 16.0 seconds she makes a signature opening turn from back to front, walking and striking a hand-on-hip pose. From 16.0 to 40.0 seconds the first dance section has raised and crossed arms, hip sways and steps with small formation shifts, the camera switching among wide, close and side angles. From 40.0 to 80.0 seconds the chorus features synchronized arm raises, waves, kicks and crouches with the dancers, the LED screen changing. From 80.0 to 115.0 seconds the dance and formation changes continue with expressive facials. From 115.0 to 137.58 seconds the group settles into a final pose with raised arms, ending on a close or wide shot of the leader. Multiple fixed and handheld cameras are cut like a director's switch. A watermark is applied.

overall_soundscape: Live K-pop performance music with strong beats and the muffled sound of the audience; no intelligible speech.

non_diegetic_music: An energetic K-pop idol track at approximately 129 BPM with a steady kick and synth hooks, cuts synced to musical phrases.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈129BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D061-A1 | 开场转身亮相 | 20 | 0.0-16.0 | 背对→转身面向观众+走步叉腰定点 | H3: makes a signature opening turn from back to front, walking and striking a hand-on-hip pose |
| D061-A2 | 群舞第一段 | 30 | 16.0-40.0 | 亮相→举臂交叉+扭胯踏步 | H3: performs raised and crossed arms, hip sways and steps with small formation shifts |
| D061-A3 | 副歌齐舞下蹲 | 48 | 40.0-80.0 | 踏步→整齐举手挥摆+踢腿下蹲 | H3: the chorus features synchronized arm raises, waves, kicks and crouches with the dancers |
| D061-A4 | 走位队形变化 | 44 | 80.0-115.0 | 齐舞→走位聚散+表情管理 | H3: continues the dance with formation changes and expressive facials |
| D061-A5 | 集体造型收势 | 30 | 115.0-137.58 | 走位→集体举手造型定格 | H3: the group settles into a final pose with raised arms, ending on the leader |

<!-- ============ 档案分隔 ============ -->

# D067 反推档案

- **档案号**：D067（源 v52）
- **短标题 ↔ 原片名**：绿裙银发角色坐姿手势 ↔ 9bcc6779-dd02-4ac6-98f3-93d69f7a569d.mp4
- **时长**：9.87s（30fps）
- **画幅**：1080×1920 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 1080×1920 竖屏 / 9.87s |
| 镜头形态 | 单一连续镜头，固定机位中景；室内（浅色墙面/金属架），银发绿裙"角色扮演"形象坐于椅上做手指手势；无切点 |
| 运镜 | 固定机位；无运动 |
| 剪辑层 | 无剪辑 |
| **ABC 结论** | **A 一镜到底**（固定机位坐姿手势） |

## ② 场景与人物档案

**场景**：室内，浅灰白墙面、金属架/器械（似健身房或室内布景），冷色调。

**人物 1（主体）**：银白/浅色短发的游戏/动漫角色造型（疑为 cosplay 或 3D 渲染角色），绿色抹胸上衣配红白披挂、白色裙装；坐于椅上，双手在胸前/头侧做手指比划手势。
**AIGC 注**：人物皮肤与发丝质感高度平滑、边缘过于干净，疑为 3D 渲染或 AI 生成角色叠加实拍场景。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-3.0 | 坐姿，双手在头侧/胸前做爪式/比划手势 | 固定竖屏中景，人物居中 |
| 3.0-7.0 | 手指交替比划、轻微摆头，手势重复 | 同上 |
| 7.0-9.87 | 收势于坐姿手势定格 | 同上 |

**末三分之一倒查**：末帧坐姿手势稳定；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 136.0 BPM（参考）
- 强 onset 稀疏；手势与节拍对应弱。
- 判定：**固定节拍参考（弱置信）**，提示词以时间码为准。

## ⑤ AIGC 判定（帧证据）

**结论：混合/存疑（真人场景 + 疑似 3D/AI 角色；AI 高置信=否，判定=混合，中置信）**
- 证据 1：角色皮肤/发丝过度平滑、服饰纹样精细但缺物理褶皱，与背景的运动视差关系不自然。
- 证据 2：背景金属架/墙面为实拍质感，前景角色为渲染/生成质感，两者光照方向不完全一致。
- 反证检查：未见大面积背景重排；手势连贯。登记为混合档，待逐帧复核。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：冷调滤镜；疑似角色渲染/叠加层。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 fixed-camera shot in a cool-toned indoor room with a pale wall and metal rack. A silver-haired game/anime character figure in a green strapless top with red-and-white drapes and a white skirt sits on a chair, making claw-like and counting hand gestures near her head and chest. From 0.0 to 3.0 seconds she sits making hand gestures at head height and at her chest. From 3.0 to 7.0 seconds her fingers alternate in small gesturing motions with slight head movement. From 7.0 to 9.87 seconds she settles into a seated hand-gesture pose. The character has unusually smooth skin and hair and clean edges, appearing rendered or composited over the live-action background. A cool filter is applied.

overall_soundscape: A light backing track plays; quiet indoor ambience. No speech.

non_diegetic_music: A light pop instrument track around 136 BPM (weak-confidence reference), with no strong beat correspondence to the gestures.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈136BPM弱) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D067-A1 | 坐姿头侧爪手 | 4 | 0.0-3.0 | 坐定→双手头侧/胸前爪式手势 | H3: sits making claw-like hand gestures near her head and chest |
| D067-A2 | 手指交替比划 | 6 | 3.0-7.0 | 爪手→手指交替比划+微摆头 | H3: her fingers alternate in small gesturing motions with slight head movement |
| D067-A3 | 坐姿手势收势 | 4 | 7.0-9.87 | 比划→坐姿手势定格 | H3: settles into a seated hand-gesture pose |

<!-- ============ 档案分隔 ============ -->

# D069 反推档案

- **档案号**：D069（源 v54）
- **短标题 ↔ 原片名**：白T恤室内随性舞 ↔ 下载 (3).mp4
- **时长**：10.91s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 10.91s |
| 镜头形态 | 单一连续镜头，固定机位全身；室内（白墙/门/镜面/家居），女生穿白T恤+短裤+彩色运动鞋跳舞；无切点 |
| 运镜 | 固定机位；无运动 |
| 剪辑层 | 无剪辑；画面底部有中文字幕条（配乐歌词/说明） |
| **ABC 结论** | **A 一镜到底**（固定机位室内随性舞） |

## ② 场景与人物档案

**场景**：室内居家/宿舍，白色墙面、门、镜面柜、置物台（有瓶罐）；自然室内光。

**人物 1（主体）**：年轻东亚女性，长发扎起；白色短袖T恤 + 浅色短裤 + 彩色运动鞋。随性舞动，动作幅度较大（挥臂、扭身、踢腿、下蹲）。

**叠加**：画面底部中文字幕条。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-3.0 | 站立，双手在面前挥摆、扭身 | 固定竖屏全身，人物居中 |
| 3.0-7.0 | 手臂上举/挥动，交替踢腿与侧身摆动，动作随性有力 | 同上 |
| 7.0-10.91 | 下蹲/侧摆组合后起身，收势于站姿 | 同上 |

**末三分之一倒查**：末帧站姿，动作自然收束；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 143.6 BPM
- 强 onset 网格较快，随性舞步与重拍大致对齐。
- 判定：**固定节拍（偏快）**，提示词用 "≈143 BPM" 参考；精确对拍以时间码为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中-高置信）**
- 证据：T恤褶皱、短裤与运动鞋细节、门/镜面/瓶罐在帧间稳定；踢腿/下蹲运动模糊连续。
- 反证检查：未见肢体融合/背景重排。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：底部中文字幕条、美颜。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 footage in a bright home or dorm room with white walls, a door, a mirrored cabinet and a shelf with bottles. A young East Asian woman with tied-back hair wears a white short-sleeve T-shirt, light shorts and colorful sneakers, dancing casually and energetically. From 0.0 to 3.0 seconds she stands swinging both hands in front of her and twisting her body. From 3.0 to 7.0 seconds she raises and waves her arms, alternating kicks and side sways with loose, forceful movements. From 7.0 to 10.91 seconds she crouches and sways sideways then rises, settling into a standing pose. A Chinese subtitle strip runs along the bottom and beauty smoothing is applied.

overall_soundscape: An upbeat pop track drives the casual dance; quiet indoor ambience. No intelligible speech.

non_diegetic_music: A fast upbeat pop track at approximately 143 BPM with a clear kick.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈143BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D069-A1 | 面前挥摆扭身 | 7 | 0.0-3.0 | 站立→双手面前挥摆+扭身 | H3: stands swinging both hands in front of her and twisting her body |
| D069-A2 | 举臂交替踢腿 | 10 | 3.0-7.0 | 扭身→举臂挥动+交替踢腿侧摆 | H3: raises and waves her arms, alternating kicks and side sways |
| D069-A3 | 下蹲侧摆收势 | 7 | 7.0-10.91 | 踢腿→下蹲侧摆→起身站姿 | H3: crouches and sways sideways then rises into a standing pose |

<!-- ============ 档案分隔 ============ -->

# D070 反推档案

- **档案号**：D070（源 v55）
- **短标题 ↔ 原片名**：米色针织上衣卡点摆拍 ↔ dDYYLQSA_UG0JYAO.mp4
- **时长**：14.00s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 14.00s |
| 镜头形态 | 单一连续镜头，固定机位中景；室内纯浅色背景墙，女生穿米色针织无袖上衣+棕褐短裙做卡点摆拍手势；无切点 |
| 运镜 | 固定机位；无运动 |
| 剪辑层 | 无剪辑 |
| **ABC 结论** | **A 一镜到底**（固定机位卡点摆拍） |

## ② 场景与人物档案

**场景**：室内，纯米白/浅色背景墙，简洁布景，柔光。

**人物 1（主体）**：年轻东亚女性，深棕长卷发；米色针织无袖上衣 + 棕褐色包臀短裙。动作以手部卡点手势为主（触脸、举V、比划、扶裙、托腮），配合头部摆动与身体律动。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-4.0 | 双手在头侧/脸旁做比划手势（V字/爪式），卡点切换 | 固定竖屏中景，人物居中 |
| 4.0-9.0 | 手臂上举/放下交替，单手扶裙、侧身摆胯 | 同上 |
| 9.0-14.00 | 托腮/触脸手势与点头律动，收势于造型 | 同上 |

**末三分之一倒查**：末帧造型定格；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 58.7 BPM（半速候选，主候选 ≈117 BPM 二倍速）
- 强 onset 与卡点手势切换对齐。
- 判定：**固定节拍（中速）**，提示词用 "≈117 BPM" 参考。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中置信）**
- 证据：针织纹理、短裙褶皱、发丝在帧间稳定；手势切换连续。
- 注：美颜磨皮与柔光明显，属后期层。
- 反证检查：未见明显肢体融合/背景重排。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：美颜、柔光滤镜。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 fixed-camera footage against a plain light-colored studio wall with soft lighting. A young East Asian woman with dark brown wavy long hair wears a beige knit sleeveless top and a brown fitted short skirt, performing beat-synced gesture poses. From 0.0 to 4.0 seconds she makes V-sign and claw-like hand gestures near her head and face, switching on the beat. From 4.0 to 9.0 seconds she raises and lowers her arms alternately, rests a hand on her skirt and sways her hips sideways. From 9.0 to 14.00 seconds she rests her cheek on a hand, touches her face and nods to the rhythm, settling into a final pose. Beauty smoothing and a soft glow filter are applied.

overall_soundscape: A mid-tempo pop track with a clear beat drives the gesture changes; quiet indoor ambience. No speech.

non_diegetic_music: A mid-tempo pop track at approximately 117 BPM with crisp beats.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈117BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D070-A1 | 头侧V字爪手卡点 | 8 | 0.0-4.0 | 站立→头侧V字/爪手卡点切换 | H3: makes V-sign and claw hand gestures near her head on the beat |
| D070-A2 | 举臂扶裙摆胯 | 10 | 4.0-9.0 | 手势→举臂交替+扶裙+侧摆胯 | H3: raises and lowers her arms, rests a hand on her skirt and sways her hips |
| D070-A3 | 托腮触脸收势 | 9 | 9.0-14.00 | 摆胯→托腮触脸+点头→造型定格 | H3: rests her cheek on a hand, touches her face and nods, settling into a final pose |

<!-- ============ 档案分隔 ============ -->

# D071 反推档案

- **档案号**：D071（源 v56）
- **短标题 ↔ 原片名**：粉开衫木门前舞蹈 ↔ cmaMiAyYkVjTc8Vr.mp4
- **时长**：17.55s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 17.55s |
| 镜头形态 | 单一连续镜头，固定机位中景；木门/木质背景前（阳光斑驳），女生穿粉色开衫+牛仔短裙跳舞；无切点 |
| 运镜 | 固定机位；无运动 |
| 剪辑层 | 无剪辑 |
| **ABC 结论** | **A 一镜到底**（固定机位舞蹈） |

## ② 场景与人物档案

**场景**：户外/半户外木门前，深棕色木门与墙面，阳光透过树叶投下斑驳光点；左下有一只白色小狗入镜（部分帧）。

**人物 1（主体）**：年轻东亚女性，长发偏分；粉色针织开衫 + 浅蓝/牛仔短裙 + 白色鞋。单人舞蹈，动作含举手、扭身、扶开衫、摆胯。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-5.0 | 站于木门前，双手在胸前/头侧摆动、扭身 | 固定竖屏中景，人物居中 |
| 5.0-11.0 | 手臂上举/侧展，扶开衫衣襟，摆胯踏步 | 同上 |
| 11.0-17.55 | 手势组合与转身，收势于站姿造型 | 同上 |

**末三分之一倒查**：末帧站姿造型；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 63.8 BPM（半速候选，主候选 ≈128 BPM）
- 判定：**固定节拍（中速）**，提示词用 "≈128 BPM" 参考；以时间码为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中置信）**
- 证据：木门纹理、光斑、开衫针织与短裙在帧间稳定；小狗入镜帧进一步佐证实拍场景；动作连续。
- 反证检查：未见肢体融合/背景重排。注：美颜滤镜。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：美颜、暖调滤镜。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 fixed-camera footage in front of a dark wooden door and wall with dappled sunlight through leaves, a small white dog appearing in the lower left in some frames. A young East Asian woman with side-parted long hair wears a pink knit cardigan, a light blue denim skirt and white shoes, dancing alone. From 0.0 to 5.0 seconds she stands in front of the door swinging her hands at chest and head height and twisting her body. From 5.0 to 11.0 seconds she raises and extends her arms, adjusts the cardigan opening and steps with hip sways. From 11.0 to 17.55 seconds she makes hand combinations and turns, settling into a standing pose. Beauty smoothing and a warm filter are applied.

overall_soundscape: An upbeat pop track drives the dance; soft outdoor ambience with faint bird or street sounds. No speech.

non_diegetic_music: A mid-tempo upbeat pop track at approximately 128 BPM with a steady kick.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈128BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D071-A1 | 胸前头侧摆手扭身 | 11 | 0.0-5.0 | 站立→双手胸前/头侧摆动+扭身 | H3: stands swinging her hands at chest and head height and twisting her body |
| D071-A2 | 举臂扶襟摆胯 | 13 | 5.0-11.0 | 摆手→举臂侧展+扶开衫+摆胯踏步 | H3: raises and extends her arms, adjusts the cardigan and steps with hip sways |
| D071-A3 | 手势转身收势 | 13 | 11.0-17.55 | 摆胯→手势组合+转身→站姿定格 | H3: makes hand combinations and turns, settling into a standing pose |

<!-- ============ 档案分隔 ============ -->

# D072 反推档案

- **档案号**：D072（源 v57）
- **短标题 ↔ 原片名**：酒店大堂白裙舞蹈 ↔ e2ddcd6c-0fd6-4ddf-b033-9c3b3386909b.mp4
- **时长**：17.41s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 17.41s |
| 镜头形态 | 单一连续镜头，固定机位全身；酒店大堂（金色圆形栏杆/金属立柱/沙发/镜面反射），女生穿白色蓬蓬短裙跳舞；无切点 |
| 运镜 | 固定机位；无运动 |
| 剪辑层 | 无剪辑 |
| **ABC 结论** | **A 一镜到底**（固定机位大堂舞蹈） |

## ② 场景与人物档案

**场景**：酒店大堂/高档室内，金色圆形金属栏杆与圆柱、深色沙发、镜面墙（反射出第二人影/拍摄者）；暖色灯光。

**人物 1（主体）**：年轻东亚女性，红棕色长发扎起；白色蓬蓬短裙+白色上衣（娃娃裙风格）+白色鞋；单人舞蹈，动作含展臂、举臂、扭身、踢腿、比V手势。
**镜中反射**：画面右侧镜面可见第二人影（疑似拍摄者或同伴），不构成第二舞蹈主体。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-5.0 | 站于栏杆前，双臂展开/侧举，扭身摆动 | 固定竖屏全身，人物居中，镜面反射在侧 |
| 5.0-11.0 | 双臂上举做V字/波浪手势，交替踢腿与转身 | 同上 |
| 11.0-17.41 | 手势组合（比V/托举）+扭胯，收势于站姿造型 | 同上 |

**末三分之一倒查**：末帧站姿造型；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 129.2 BPM
- 强 onset 网格与踢腿/举臂重拍对齐。
- 判定：**固定节拍**，提示词用 "≈129 BPM" 参考。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中-高置信）**
- 证据：金色栏杆金属反光、沙发、镜面反射在帧间稳定；裙摆与头发运动连续；镜中反射人影为真实光学反射。
- 反证检查：未见肢体融合/背景重排。注：有美颜滤镜。

## ⑥ 剪辑特效层

- 切点：无。特效/叠加：美颜、暖调滤镜。变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 fixed-camera full-body footage in a hotel lobby with a golden circular metal railing and column, a dark sofa and mirrored walls reflecting a second figure. A young East Asian woman with reddish-brown tied-up hair wears a white fluffy doll-style short dress with a white top and white shoes, dancing alone. From 0.0 to 5.0 seconds she stands in front of the railing opening and extending her arms sideways, twisting and swaying. From 5.0 to 11.0 seconds she raises both arms into a V and waves, alternating kicks and turns. From 11.0 to 17.41 seconds she makes V-sign and lifting hand combinations with hip sways, settling into a standing pose. A second figure is visible in the mirror reflection but does not dance. Beauty smoothing and a warm filter are applied.

overall_soundscape: An upbeat pop track drives the dance; quiet indoor lobby ambience. No speech.

non_diegetic_music: An upbeat pop track at approximately 129 BPM with a steady kick and bright synths.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈129BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D072-A1 | 展臂侧举扭身 | 8 | 0.0-5.0 | 站立→双臂展开侧举+扭身摆动 | H3: opens and extends her arms sideways, twisting and swaying |
| D072-A2 | V字举臂踢腿转身 | 10 | 5.0-11.0 | 侧举→双臂V字波浪+交替踢腿转身 | H3: raises both arms into a V and waves, alternating kicks and turns |
| D072-A3 | V手势扭胯收势 | 10 | 11.0-17.41 | 踢腿→V手势组合+扭胯→站姿定格 | H3: makes V-sign and lifting hand combinations with hip sways, settling into a standing pose |
