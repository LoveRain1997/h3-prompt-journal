# BATCH7 续产单文件版 · E 组 7 片（D048/D049/D050/D051/D054/D055/D056）

> 整片档案制续产（D/E/F 串行组的 E 组）：每片七件套，规格同 D 组。反推全程未切割；BPM 全部 onset_probe 实测+置信分层，散板/无网格/禁用片拒写数值；AIGC 三档判定附帧证据，证据不足者登记为无法判定；动作编号 `Dxxx-Ayy` 只进索引表不进提示词正文。
> 本文件为续产第二批（E 组），F 组 10 片待续。

---

# D048 反推档案

- **档案号**：D048（源 v33）
- **短标题 ↔ 原片名**：窗边纱裙光影写真 ↔ 窗边的下午｜30 秒日系胶片感写真片段.mp4
- **时长**：30.00s（30fps）
- **画幅**：1280×714 横屏（电影感裁切）
- **音轨**：有（氛围配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 1280×714 横屏 / 30.00s |
| 镜头形态 | 单一连续镜头，固定机位；室内窗边（白色窗帘/窗台暖气片/三脚架可见），一名女生在窗光下做写真姿态（站姿回眸→撩发→坐地/床上躺姿）；全片无切点 |
| 运镜 | 固定机位，无推拉摇移变焦 |
| 剪辑层 | 无剪辑；日系胶片调色滤镜 |
| **ABC 结论** | **A 一镜到底**（固定机位，光影写真） |

## ② 场景与人物档案

**场景**：室内窗边，白色半透窗帘、窗台暖气片、摄影三脚架（可见于画面左侧，说明为自拍/拍摄现场）；午后强侧光透入，日系胶片暖调。

**人物 1（主体）**：年轻东亚女性，黑色长直发；浅粉/裸色轻薄纱质吊带裙（居家/睡衣风格）。姿态为写真摆拍：站立回眸、撩发、抬手遮面、坐于地面及躺于床上。
**内容处理说明**：素材为日常写真，档案只登记动作与构图，不做露骨细节描述。

**道具**：三脚架、窗台、床/地面。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-6.0 | 窗边站立，背对转回眸，长发垂落；抬手撩发至脑后 | 固定横屏中景，窗光逆侧 |
| 6.0-12.0 | 侧身抬手做遮面/扶发手势，身体微倾，看向镜头 | 同上 |
| 12.0-20.0 | 转为坐姿（地面/床边），手臂支撑，头部后仰或侧转 | 同上 |
| 20.0-26.0 | 躺姿，手抚腹部/头发，身体舒展 | 同上 |
| 26.0-30.0 | 起身/侧坐收势，回望窗光 | 同上 |

**末三分之一倒查**：末帧为侧坐/站起过渡姿态；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 184.6 BPM（不可采信）
- 强 onset 分布稀疏且不规则，为氛围配乐/环境音，无稳定打击网格。
- 判定：**无稳定节拍（禁写 BPM 数值）**；写真摆拍动作依时间码锚点，不依赖节拍。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中置信）**
- 证据：窗光与窗帘褶皱、三脚架结构在帧间稳定；发丝与纱裙运动连续；胶片颗粒为统一后期层。
- 反证检查：未见肢体融合/背景重排。

## ⑥ 剪辑特效层

- 切点：无（0 切镜）。
- 特效/叠加：日系胶片调色与颗粒、柔光；无水印（原片）。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action cinematic horizontal footage in a sunlit room by a window with white sheer curtains, a windowsill radiator and a visible camera tripod. A young East Asian woman with long straight black hair wears a light pink sheer slip dress in a home/loungewear style, posing in the afternoon backlight with a Japanese film-grain look. From 0.0 to 6.0 seconds she stands by the window, turns from a back view to look over her shoulder and sweeps her hair back with one hand. From 6.0 to 12.0 seconds she tilts her body and raises a hand to shade or touch her face, looking toward the camera. From 12.0 to 20.0 seconds she moves into a seated pose on the floor or bed edge, supporting herself with an arm and tilting or turning her head. From 20.0 to 26.0 seconds she reclines, one hand resting on her hair or torso, body relaxed. From 26.0 to 30.0 seconds she rises or shifts to a side-seated pose, glancing back toward the window light. Warm backlit window light, soft film grain and gentle color grading throughout.

overall_soundscape: A soft ambient backing track with quiet indoor room tone; no speech and no distinct sound effects.

non_diegetic_music: A mellow ambient/film-style instrumental with no steady beat grid.
```

## 动作索引表

| 编号 | 名称 | 拍数(无BPM→秒) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D048-A1 | 窗边回眸撩发 | 6s | 0.0-6.0 | 背身站立→回眸+撩发至脑后 | H3: turns from a back view to look over her shoulder and sweeps her hair back |
| D048-A2 | 遮面侧身姿态 | 6s | 6.0-12.0 | 撩发→抬手遮面/扶发侧倾 | H3: tilts her body and raises a hand to shade or touch her face |
| D048-A3 | 坐地支撑仰头 | 8s | 12.0-20.0 | 站姿→坐姿手臂支撑+头部后仰侧转 | H3: moves into a seated pose supporting herself with an arm, head tilted back |
| D048-A4 | 躺姿舒展 | 6s | 20.0-26.0 | 坐姿→躺姿手抚头发/身体舒展 | H3: reclines with one hand resting on her hair, body relaxed |
| D048-A5 | 起身回望收势 | 4s | 26.0-30.0 | 躺姿→起身/侧坐回望窗光 | H3: rises to a side-seated pose, glancing back toward the window light |

<!-- ============ 档案分隔 ============ -->

# D049 反推档案

- **档案号**：D049（源 v34）
- **短标题 ↔ 原片名**：Cosplay高脚凳静态摆拍 ↔ 杨雨潼 搜狐扫楼.mp4
- **时长**：20.44s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 20.44s |
| 镜头形态 | 单一连续镜头，固定机位中景；一名 cosplay 造型女生坐于木质高脚凳上，橙红色墙+珠帘背景；全片无切点，主体几乎静止 |
| 运镜 | 固定机位，无运动 |
| 剪辑层 | 无剪辑/无特效 |
| **ABC 结论** | **A 一镜到底**（固定机位静态摆拍，动作幅度极低） |

## ② 场景与人物档案

**场景**：室内，橙红色墙面、珠帘/亮片挂饰、木质高脚凳、白色桌面（放有道具）；暖色灯光。

**人物 1（主体）**：年轻东亚女性，cosplay 造型——黑紫红色短裙装（带荷叶边/格纹），黑色高跟鞋，头戴发饰；坐于高脚凳，手边有红色道具包。全程保持坐姿摆拍，动作极少（微调手势/转头）。

**平台水印**：左上角小红书号水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-6.0 | 坐于高脚凳，双腿交叠，手扶膝/道具包，正面看向镜头方向 | 固定竖屏中景，人物居中偏左 |
| 6.0-13.0 | 保持坐姿，手部小幅调整（触脸/扶物），头部微动 | 同上 |
| 13.0-20.44 | 坐姿收势，拍手/手势收束，末帧维持坐姿 | 同上 |

**末三分之一倒查**：末帧坐姿稳定；无黑场/新动作。全片以静态摆拍为主，非舞蹈。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 215.3 BPM（不可采信：非舞蹈配乐，onset 稀疏）
- 判定：**无稳定可用节拍（禁写可靠 BPM）**；画面动作非节拍驱动，依时间码锚点。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中置信）**
- 证据：服装荷叶边与格纹、高脚凳木纹、珠帘反光在帧间稳定；主体姿态连续。
- 注：美颜磨皮与滤镜，属后期层。
- 反证检查：未见肢体融合/背景重排。

## ⑥ 剪辑特效层

- 切点：无。
- 特效/叠加：美颜磨皮、暖色滤镜、小红书水印。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 footage of a young East Asian woman in a black-purple-red cosplay costume (ruffled plaid short dress, black high-heeled shoes, hair accessories) seated on a tall wooden stool against an orange-red wall with a bead curtain and a white table holding props. From 0.0 to 6.0 seconds she sits with legs crossed, one hand resting on her knee or a red prop bag, facing toward the camera. From 6.0 to 13.0 seconds she stays seated with only small adjustments of her hands and head, touching her face or the prop. From 13.0 to 20.44 seconds she makes a small clapping or hand gesture and holds the seated pose to the end. The shot is static with no camera movement, warm lighting, beauty smoothing and a Chinese social-media watermark at the top left. The subject is nearly motionless throughout, posed rather than dancing.

overall_soundscape: A soft pop backing track plays; quiet indoor ambience. No speech.

non_diegetic_music: A gentle pop instrumental with no clear beat grid relevant to the static pose.
```

## 动作索引表

| 编号 | 名称 | 拍数(无BPM→秒) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D049-A1 | 高脚凳交叠坐姿 | 6s | 0.0-6.0 | 坐下→双腿交叠手扶膝/道具 | H3: sits on the stool with legs crossed, one hand on her knee or a prop bag |
| D049-A2 | 手部微调 | 7s | 6.0-13.0 | 坐姿→手部小幅调整触脸/扶物 | H3: stays seated with small adjustments of her hands and head |
| D049-A3 | 手势收势 | 7.44s | 13.0-20.44 | 微调→小幅拍手手势→坐姿定格 | H3: makes a small hand gesture and holds the seated pose to the end |

<!-- ============ 档案分隔 ============ -->

# D050 反推档案

- **档案号**：D050（源 v35）
- **短标题 ↔ 原片名**：多造型写真快剪 ↔ 看看舞蹈生.mp4
- **时长**：64.45s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 覆盖全片 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 64.45s |
| 镜头形态 | 多场景多造型写真快剪：户外街拍（白裙/黑裙/灰背心牛仔裤）与室内（白衬衫黑丝）多段，各段硬切；主体疑为同一女生多套造型 |
| 运镜 | 各段机位固定，段间硬切 |
| 剪辑层 | 大量切点（≈每2-4s），卡点剪辑；无定格/转场特效 |
| **ABC 结论** | **C 多镜快剪**（写真拼贴型） |

## ② 场景与人物档案

**场景（多段）**：①户外林荫道（秋日阳光、树木、街道）；②暗调街景（红墙/霓虹）；③街边（灰背心+牛仔短裤）；④室内（白衬衫+黑丝，室内桌柜背景）。

**人物**：年轻东亚女性（红棕色长发），多套造型：白色抹胸长裙、黑色亮面抹胸短裙、灰色背心+牛仔短裤、白衬衫+黑色过膝袜。姿态为写真摆拍（回眸、托腮、蹲姿、扶墙）。

**平台水印**：左上角小红书号水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-12.0 | 户外白裙造型：站立回眸、撩发、扶肩，阳光逆侧 | 竖屏中景硬切 |
| 12.0-26.0 | 黑色亮面短裙造型：街边蹲姿、扶墙、侧身抬腿，暗调霓虹 | 竖屏多段硬切 |
| 26.0-44.0 | 灰背心+牛仔裤造型：街头站立、叉腰、拨发、蹲姿 | 竖屏街拍硬切 |
| 44.0-64.45 | 室内白衬衫造型：桌面支撑、跪坐、侧身摆拍，收势于造型 | 竖屏室内近景 |

**末三分之一倒查**：末帧室内摆拍造型；全片为独立写真镜头拼接，无连续动作链。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 99.4 BPM
- 强 onset 分布随配乐乐句，切点密度≈2-4s/切。
- 判定：**固定节拍参考（弱-中置信）**，写真快剪随乐句切换；不写强 BPM 定论，提示词以时间码/场景段为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中置信）**
- 证据：各段服装/发型稳定可辨；街景与室内背景透视一致；蹲姿/抬腿动作连续。
- 注：美颜磨皮与多套滤镜，属后期层。
- 反证检查：未见明显肢体融合/背景重排。

## ⑥ 剪辑特效层

- 切点：大量（多场景硬切拼接）。
- 特效/叠加：美颜磨皮、调色滤镜、小红书水印。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 photo montage of a young East Asian woman with reddish-brown long hair in multiple outfits, cut rapidly between scenes. From 0.0 to 12.0 seconds outdoors on an autumn tree-lined street in a white strapless dress, she stands looking back over her shoulder, sweeps her hair and touches her shoulder in warm backlight. From 12.0 to 26.0 seconds in a black glossy strapless short dress against a dark neon street and red wall, she crouches, leans on a wall and lifts a leg sideways in stylized poses. From 26.0 to 44.0 seconds in a grey sleeveless top and denim shorts on the street, she stands with hand on hip, brushes her hair and crouches. From 44.0 to 64.45 seconds indoors in a white shirt and black over-knee socks, she poses leaning on a desk, kneeling and turning sideways, settling into a final pose. A Chinese social-media watermark is overlaid at the top left. Beauty smoothing and color filters are applied.

overall_soundscape: An upbeat pop track plays over the montage; ambient sound varies by scene but is secondary. No speech.

non_diegetic_music: An upbeat Chinese pop track with phrase changes driving the scene cuts, around 100 BPM (weak-confidence reference).
```

## 动作索引表

| 编号 | 名称 | 拍数(≈99BPM弱) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D050-A1 | 白裙户外回眸撩发 | 8 | 0.0-12.0 | 站立→回眸+撩发+扶肩 | H3: stands looking back over her shoulder, sweeping her hair in warm backlight |
| D050-A2 | 黑裙蹲姿扶墙抬腿 | 10 | 12.0-26.0 | 切镜→蹲姿扶墙+侧抬腿 | H3: in a black dress, crouches, leans on a wall and lifts a leg sideways |
| D050-A3 | 街头叉腰拨发蹲姿 | 12 | 26.0-44.0 | 切镜→站立叉腰+拨发+蹲姿 | H3: stands with hand on hip, brushes her hair and crouches on the street |
| D050-A4 | 室内桌面跪坐摆拍 | 12 | 44.0-64.45 | 切镜→桌面支撑+跪坐侧身→定格 | H3: indoors, poses leaning on a desk and kneeling, settling into a final pose |

<!-- ============ 档案分隔 ============ -->

# D051 反推档案

- **档案号**：D051（源 v36）
- **短标题 ↔ 原片名**：粉色女团舞台群舞 ↔ 录完舞一看微信步数一万八.mp4
- **时长**：85.59s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 覆盖全片 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 85.59s |
| 镜头形态 | 多机位舞台群舞：约 8-10 名女生粉色系蓬蓬裙+双丸子头，粉色舞台带粉色花球装饰；全景/中景/近景多机位切换；长片 |
| 运镜 | 各机位固定，段间硬切（多机位导播切换）；部分段轻微推拉 |
| 剪辑层 | 多切点（机位切换）；无定格/贴纸/变速 |
| **ABC 结论** | **C 多镜切换**（舞台多机位导播切换，群舞） |

## ② 场景与人物档案

**场景**：室内舞台/演出场地，粉白色调背景，地面散落粉色花球/花簇装饰，顶部粉色灯光；整体甜美可爱风格。

**人物**：约 8-10 名年轻东亚女性，统一粉色蓬蓬纱裙 + 白色上衣 + 双丸子头发型 + 白色鞋；为女团齐舞/多人编排，队形有变化（.cluster→散开→两列→聚集）。

**平台水印**：左上角水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-16.0 | 群舞起势：全体蹲姿/摆臂开场，队形聚集居中，双丸子头随动 | 镜1 全景，舞台全貌 |
| 16.0-36.0 | 手臂上举波浪、左右摆动、踏步，队形散开为多列；机位在中景/近景间切换 | 多机位交替 |
| 36.0-60.0 | 副歌段：整齐划一的手臂交叉/上举/跳跃，队形两列对齐，粉色花球前景 | 全景+近景穿插 |
| 60.0-85.59 | 延续齐舞+队形收拢，末段集体造型（蹲/举手组合）收势 | 多机位，末段全景定格 |

**末三分之一倒查**：末帧为集体造型收束；长片机位切换有乐句动机，无叙事断层。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 110.0 BPM
- 强 onset 密集且近似等距，群舞拍点与 onsets 对齐。
- 判定：**固定节拍**，提示词用 "≈110 BPM" 参考；齐舞对拍以时间码锚点为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中-高置信）**
- 证据：多人队形在帧间位置稳定、无个体漂移；蓬蓬裙/丸子头运动模糊连续；舞台花球与背景固定。
- 反证检查：未见人物融合、肢体异常、背景重排。多人场景反而是实拍反证。
- 注：舞台强光+美颜滤镜。

## ⑥ 剪辑特效层

- 切点：多切点（多机位导播切换）。
- 特效/叠加：舞台灯光、美颜滤镜、水印。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 multi-camera footage of a girl-group stage performance with about 8-10 young East Asian women in matching pink fluffy tutu skirts, white tops, twin-bun hairstyles and white shoes, dancing on a pink stage decorated with pink flower pom-poms under pink lighting. From 0.0 to 16.0 seconds the group opens with a crouching pose and arm swings, clustered in the center, buns bouncing. From 16.0 to 36.0 seconds they raise their arms in waves, sway left and right and step in formation as it spreads into several lines, the camera cutting between wide and medium shots. From 36.0 to 60.0 seconds during the chorus they perform synchronized arm crosses, raises and jumps in two aligned lines with pink pom-poms in the foreground. From 60.0 to 85.59 seconds the dance continues with formation changes and then gathers into a final group pose of crouches and raised arms, ending on a wide shot. Multiple fixed camera angles are cut between like a director's live switch. Watermarks and beauty filters are overlaid.

overall_soundscape: An upbeat bright J-pop-style group dance track with strong beats; synchronized footsteps on stage. No speech.

non_diegetic_music: An energetic idol-pop track at approximately 110 BPM with a steady kick and layered synths, edits landing on musical phrases.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈110BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D051-A1 | 蹲姿摆臂开场 | 16 | 0.0-16.0 | 聚集→集体蹲姿+摆臂 | H3: the group opens with a crouching pose and arm swings, clustered in the center |
| D051-A2 | 举臂波浪散队 | 24 | 16.0-36.0 | 聚集→举臂波浪+左右摆+散成多列 | H3: raises arms in waves, sways and steps as the formation spreads into lines |
| D051-A3 | 副歌齐舞跳步 | 28 | 36.0-60.0 | 多列→整齐交叉/上举/跳跃两列对齐 | H3: performs synchronized arm crosses, raises and jumps in two aligned lines |
| D051-A4 | 队形收拢造型 | 28 | 60.0-85.59 | 齐舞→队形收拢→集体蹲/举手造型 | H3: continues with formation changes then gathers into a final group pose |

<!-- ============ 档案分隔 ============ -->

# D054 反推档案

- **档案号**：D054（源 v39）
- **短标题 ↔ 原片名**：草地白背心牛仔短裤单人舞 ↔ 2026112201.mp4
- **时长**：75.86s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 覆盖全片 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 75.86s |
| 镜头形态 | 单一连续镜头，固定机位；户外草地旁小路（绿草坡+土路+树木），一名女生穿白背心+牛仔短裤跳舞；长片无切点 |
| 运镜 | 固定机位，无推拉摇移变焦 |
| 剪辑层 | 无剪辑；无贴纸/变速 |
| **ABC 结论** | **A 一镜到底**（固定机位户外长片舞蹈） |

## ② 场景与人物档案

**场景**：户外草坡旁土路，绿色草地、树木、浅色天空；白天自然光，画面带淡滤镜。

**人物 1（主体）**：年轻东亚女性，黑色长发扎起/散发；白色短背心 + 浅蓝牛仔短裤 + 棕黄色厚底鞋。全程单人舞蹈，动作幅度大（举手/扭胯/踢腿/转身）。

**平台水印**：左上角小红书号水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-16.0 | 起势：双手举头/交叉胸前，踏步与扭胯，站在土路上 | 固定竖屏全身，人物居中 |
| 16.0-36.0 | 连续舞蹈：手臂上举/侧伸/波浪，交替踢腿与侧步，转身 | 同上 |
| 36.0-56.0 | 副歌段：大幅举手、扭腰、单腿抬起平衡，动线小幅前后 | 同上 |
| 56.0-75.86 | 延续舞步组合，末段收势于站立造型 | 同上 |

**末三分之一倒查**：末帧站立造型，动作自然收束；无黑场/新动作。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 66.3 BPM（半速候选）
- 强 onset 网格密集；主候选 ≈132 BPM（二倍速）或 ≈66 BPM 慢速表达，舞蹈动作偏中速。
- 判定：**固定节拍（中速）**，提示词用 "≈66-132 BPM" 参考区间；动作对拍以时间码锚点为准。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中-高置信）**
- 证据：草地纹理与树木在帧间稳定；人物踢腿/转身运动模糊连续；服装随动自然。
- 反证检查：未见肢体融合/背景重排。

## ⑥ 剪辑特效层

- 切点：无（0 切镜）。
- 特效/叠加：淡滤镜、美颜、小红书水印。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 footage on an outdoor dirt path beside a green grassy slope with trees and a pale sky in daylight. A young East Asian woman with dark hair tied back wears a white cropped sleeveless top, light blue denim shorts and tan platform shoes, dancing alone with large movements. From 0.0 to 16.0 seconds she starts with hands raised overhead and crossed at the chest, stepping and swaying her hips on the path. From 16.0 to 36.0 seconds she dances continuously with arms raised, extended sideways and waving, alternating kicks and side steps with turns. From 36.0 to 56.0 seconds during the chorus she makes big arm raises, hip twists and one-leg balances, moving slightly forward and back. From 56.0 to 75.86 seconds she continues the step combinations and settles into a standing pose. A light filter, beauty smoothing and a Chinese social-media watermark are applied.

overall_soundscape: An upbeat dance-pop track drives the choreography; faint outdoor ambience and footsteps on the dirt path. No speech.

non_diegetic_music: A mid-tempo dance-pop track, roughly 66-132 BPM depending on half/double-time reading, with a steady kick.
```

## 动作索引表

| 编号 | 名称 | 拍数(≈132BPM) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D054-A1 | 举臂交叉踏步起势 | 20 | 0.0-16.0 | 站立→双手举头/胸前交叉+踏步扭胯 | H3: starts with hands raised overhead and crossed at the chest, stepping and swaying her hips |
| D054-A2 | 举臂侧伸踢腿转身 | 24 | 16.0-36.0 | 踏步→举臂侧伸波浪+交替踢腿转身 | H3: dances with arms raised and waving, alternating kicks and side steps with turns |
| D054-A3 | 大幅举手扭胯平衡 | 24 | 36.0-56.0 | 踢腿→大幅举手+扭腰+单腿平衡 | H3: makes big arm raises, hip twists and one-leg balances, moving slightly forward |
| D054-A4 | 舞步收势站立 | 24 | 56.0-75.86 | 平衡→延续舞步→站立造型定格 | H3: continues the step combinations and settles into a standing pose |

<!-- ============ 档案分隔 ============ -->

# D055 反推档案

- **档案号**：D055（源 v40）
- **短标题 ↔ 原片名**：毛茸茸白外套街头写真 ↔ 穿搭｜阳光下毛茸茸的氛围感拉满🍂.mp4
- **时长**：12.59s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：COMPLETE（scope=visual+audio-rhythm；接触表 2s/格 + onset 实测）
- **复述确认门**：批量流水线任务，waived

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 12.59s |
| 镜头形态 | 多段街头写真快剪：秋日阳光街道（树影/石墙/街景），女生穿白色毛茸茸外套多姿态；段间硬切 |
| 运镜 | 各段固定机位，段间硬切 |
| 剪辑层 | 多切点（≈每2s一切），卡点写真剪辑 |
| **ABC 结论** | **C 多镜快剪**（写真拼贴型） |

## ② 场景与人物档案

**场景（多段）**：秋日户外街道——阳光透过树叶洒下、石墙、街边店铺、长椅；暖色调。

**人物**：年轻东亚女性，深棕长卷发；白色毛茸茸/羽毛质感外套 + 内搭，白色下装；姿态为写真摆拍（正面走近、侧身回眸、手部动作、仰望）。

**平台水印**：左上角水印。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-4.0 | 街头正面走近，手抬至面部/胸前，阳光洒在毛发外套上 | 竖屏中景，街景背景 |
| 4.0-8.0 | 侧身回眸、手部比划/托腮，转身展示外套轮廓 | 竖屏多段硬切 |
| 8.0-12.59 | 仰望/闭眼侧脸特写、抬手拨发，收势于造型 | 竖屏近景 |

**末三分之一倒查**：末帧侧脸/造型定格；全片为独立写真镜头拼接。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 166.7 BPM（参考值）
- 强 onset 随配乐乐句，切点密度≈2s/切。
- 判定：**固定节拍参考（弱置信）**；写真快剪随乐句切换，动作依时间码。

## ⑤ AIGC 判定（帧证据）

**结论：实拍（AI 高置信=否，判定=实拍，中置信）**
- 证据：毛发外套纤维质感、树叶光斑、石墙纹理在帧间稳定；发丝与动作连续。
- 注：美颜磨皮与暖调滤镜，属后期层。
- 反证检查：未见明显肢体融合/背景重排。

## ⑥ 剪辑特效层

- 切点：多切点（多段硬切）。
- 特效/叠加：暖调滤镜、阳光光斑、美颜、水印。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 photo montage on an autumn sunlit street with tree shadows, a stone wall and shopfronts. A young East Asian woman with dark brown wavy long hair wears a fluffy white feather-textured coat with light-colored inner layers and bottoms, posing in several shots. From 0.0 to 4.0 seconds she walks toward the camera on the street, raising a hand toward her face or chest as sunlight falls on the fluffy coat. From 4.0 to 8.0 seconds she turns sideways and looks back, makes small hand gestures or rests her cheek on her hand, turning to show the coat's silhouette. From 8.0 to 12.59 seconds she looks up or closes her eyes in a side-profile close-up, brushing her hair with a hand and settling into a final pose. The shots cut about every two seconds, with warm grading, sunlight dapples, beauty smoothing and a watermark.

overall_soundscape: A warm upbeat pop track plays; street ambience is secondary. No speech.

non_diegetic_music: A light upbeat pop track with phrase changes driving the cuts, around 167 BPM (weak-confidence reference).
```

## 动作索引表

| 编号 | 名称 | 拍数(≈167BPM弱) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D055-A1 | 街头走近抬手 | 5 | 0.0-4.0 | 远处走近→手抬至面部/胸前 | H3: walks toward the camera, raising a hand toward her face in sunlight |
| D055-A2 | 侧身回眸转身 | 6 | 4.0-8.0 | 抬手→侧身回眸+手势+转身展示外套 | H3: turns sideways and looks back, turning to show the coat's silhouette |
| D055-A3 | 仰望拨发收势 | 7 | 8.0-12.59 | 转身→仰望侧脸+拨发定格 | H3: looks up in a side-profile close-up, brushing her hair and settling into a pose |

<!-- ============ 档案分隔 ============ -->

# D056 反推档案

- **档案号**：D056（源 v41）
- **短标题 ↔ 原片名**：海滩拍摄花絮远景 ↔ 更新一个小花絮！今晚更新正片！.mp4
- **时长**：15.35s（30fps）
- **画幅**：720×1280 竖屏 9:16
- **音轨**：有（配乐；无对白转录）
- **观察状态**：PARTIAL（scope=visual；**证据缺口**：主体被大面积树叶前景遮挡且距离远，无法精确还原动作细节，仅登记可见运动轮廓）
- **复述确认门**：批量流水线任务，waived；证据缺口照常登记

---

## ① 片型分流

| 项 | 判定 |
|---|---|
| 画幅/时长 | 720×1280 竖屏 / 15.35s |
| 镜头形态 | 单一连续镜头，固定机位远景；前景为大面积绿叶（虚化/遮挡），透过树叶间隙可见远处沙滩上一名人物在活动；疑似拍摄花絮 |
| 运镜 | 固定机位，无运动 |
| 剪辑层 | 无剪辑 |
| **ABC 结论** | **A 一镜到底**（固定远景花絮，主体严重遮挡） |

## ② 场景与人物档案

**场景**：海滩远景——浅色沙滩、海水边缘、岸边木桩/支架；大面积绿叶前景占据画面大部分（近景树叶虚化），视线透过树叶间隙看向沙滩。

**人物 1（主体，远处）**：一名人物（疑为女性，浅色服装）在沙滩/水边活动，因距离远+遮挡，形体细节不可辨；可见其在画面中部小幅移动/摆臂。

**证据缺口登记**：
- 无法判定具体动作类型（舞蹈/走位/拍摄摆姿）、手势、服装细节、面部。
- 无法判定是否实拍/AIGC（远景+遮挡不足以取帧证据）。
- 提示词仅描述可确认的构图与运动轮廓，不臆造动作细节。

## ③ 全程时间轴

| 时间码 | 主体动作（因果链） | 机位/构图 |
|---|---|---|
| 0.0-5.0 | 透过树叶间隙，远处沙滩人物站立/小幅移动 | 固定远景，树叶前景遮挡 |
| 5.0-10.0 | 人物在沙滩上移动位置、手臂轮廓有摆动 | 同上 |
| 10.0-15.35 | 人物继续小幅活动，末帧维持远景 | 同上 |

**末三分之一倒查**：末帧远景人物仍在活动；无黑场/切镜。

## ④ BPM 实测（onset_probe.py，sr=22050）

- ref_tempo（autocorr）= 191.4 BPM（不可采信：花絮配乐，画面动作与节拍无可靠对应）
- 判定：**无稳定可用节拍（禁写可靠 BPM）**；画面依时间码锚点。

## ⑤ AIGC 判定（帧证据）

**结论：无法判定（证据不足）**
- 原因：主体距离远且被树叶大面积遮挡，无有效帧证据可取；叶影与沙滩在帧间看似稳定，但不足以支撑实拍/生成结论。
- 登记为"证据不足，待补"，不强行归入实拍或生成档。

## ⑥ 剪辑特效层

- 切点：无。
- 特效/叠加：疑似调色滤镜；无水印（原片视角）。
- 变速：无。

## ⑦ 完整提示词（T2VA，可直接粘贴）

```text
integrated_multimodal_description: Live-action vertical 9:16 far-shot behind-the-scenes footage of a beach, framed through large out-of-focus green leaves in the foreground that occupy most of the frame. Through gaps in the leaves, a small distant figure in light clothing can be seen moving near the shoreline and the sandy beach, with wooden posts or a stand along the shore. From 0.0 to 5.0 seconds the distant figure stands and shifts slightly on the sand. From 5.0 to 10.0 seconds the figure moves position with slight arm motion visible at this distance. From 10.0 to 15.35 seconds the figure continues small movements and the shot holds to the end. The subject is heavily occluded by foliage and too distant for fine detail; only the general composition and motion outline are described.

overall_soundscape: A light backing track plays; distant beach ambience is indistinct. No intelligible speech.

non_diegetic_music: A light instrumental/pop track with no reliable beat correspondence to the heavily occluded distant figure.
```

## 动作索引表

| 编号 | 名称 | 拍数(无BPM→秒) | 源时间窗 | 入态→出态 | H3 一句话 |
|---|---|---|---|---|---|
| D056-A1 | 远景站立微动 | 5s | 0.0-5.0 | 站立→小幅移动（遮挡） | H3: a distant figure stands and shifts slightly on the sand through the leaves |
| D056-A2 | 沙滩位置移动 | 5s | 5.0-10.0 | 微动→改变位置伴手臂轮廓摆动 | H3: the distant figure moves position with slight arm motion visible |
| D056-A3 | 远景活动延续 | 5.35s | 10.0-15.35 | 移动→继续小幅活动至末帧 | H3: the figure continues small movements as the far shot holds to the end |
