# Case Study 022 — 13 段古典武侠舞完整 H3 提示词（self-contained 节拍网格 · 音乐连续 hand-off · 参考图/武器状态锁定）

> 一支约 160 秒的**真人古风武侠舞 editorial**，按音乐切分点切成 **13 段独立可生成**的 H3 提示词。每段都是 self-contained：喂**同一张参考图 `<Picture 1>` + 该段对应的裁剪音频 `<Audio 1>`** 即可单独出片；全局时间只用来标注「源歌窗口」，**每段动作时间轴一律从 0.000 重新计时（local time）**。这套打法的核心是：先让舞蹈成立（脚步→重心→身韵→手臂→眼神的完整动力链），再让镜头有理由地运动；同时用**参考图视觉权威 + 武器状态硬保护**，杜绝模型自行换装、添人、画剑、拔剑。
>
> 本案例同时沉淀了一份成体系的中文创作方法论（20 条），见 [`methodology.md`](./methodology.md)，供之后所有古风 / 古风融合舞蹈项目复用。

## Inputs（输入）

- **PICTURE 1（唯一视觉参考）**：单人古风舞者与场景的全部视觉来源——人物身份与外貌、可见配饰与道具、背景、建筑、色彩、灯光。简洁参考图版：只锁图里有的，不引入图中没有的元素。
- **AUDIO 1（每段一段，唯一时间/节奏/重音权威）**：每段喂对应的**裁剪音频**（`seg01 … seg13`），**不要一次喂整曲**；音频保持原样，不加对白、额外演唱、音效或音乐。
- **素材 manifest**：`cuts_manifest(2).json`（给出每段文件名、全局源歌窗口、切分点）。
- 关联封面素材（本地，不随仓库分发）：`d:\Users\Administrator\Downloads\10月19日(3)\10月19日(3).mp4`，45.325s，竖屏 1838×3268，60fps，单人古风舞。
- 逐字提示词：[`prompt.md`](./prompt.md)（13 段 self-contained 英文 prompt + Implementation notes）。
- 方法论：[`methodology.md`](./methodology.md)（20 条导演级创作与自检规则）。

## 音乐时间网格（manifest）

- **BPM 90.5**；标称拍长（beat）**0.663 s**；小节（bar，4 拍）**2.6519 s**；乐句（phrase，2 小节 / 8 拍）**5.3039 s**。
- 音频总时长 **160.496 s**，共 13 段；动作时间戳按段内 local time，重音/乐句作为动作与镜头的切换锚点。
- **第 13 段无歌词事件**：整段 10.270 s 作为**纯器乐尾奏（instrumental coda）**编排，最后的 Hero 收束对齐真实音频尾。

## 13 段结构表

| # | 标题 | 源歌窗口 (s) | 时长 (s) | 段音频 |
|---|---|---|---|---|
| 01 | Cold Mountain Blade-Line | 0.000–13.576 | 13.576 | `seg01_00m00p00s-00m13p58s.mp3` |
| 02 | Rounded Arm Lines, Grounded Footwork | 13.576–24.816 | 11.240 | `seg02_00m13p58s-00m24p82s.mp3` |
| 03 | The Threshold, Footwork to Upper-Body Flow | 24.816–37.500 | 12.684 | `seg03_00m24p82s-00m37p50s.mp3` |
| 04 | Leaving the Old Mountain | 37.500–49.833 | 12.333 | `seg04_00m37p50s-00m49p83s.mp3` |
| 05 | Palace Poise, Moving Before the Lyric | 49.833–62.100 | 12.267 | `seg05_00m49p83s-01m02p10s.mp3` |
| 06 | Light Steps, Unarmed Resolve | 62.100–74.513 | 12.413 | `seg06_01m02p10s-01m14p51s.mp3` |
| 07 | Reprise, More Composed | 74.513–88.133 | 13.620 | `seg07_01m14p51s-01m28p13s.mp3` |
| 08 | Empty Hand, Sheathed Memory | 88.133–101.626 | 13.493 | `seg08_01m28p13s-01m41p63s.mp3` |
| 09 | Old Wind, Warm Hall | 101.626–114.256 | 12.630 | `seg09_01m41p63s-01m54p26s.mp3` |
| 10 | Silence Without Surrender | 114.256–126.893 | 12.637 | `seg10_01m54p26s-02m06p89s.mp3` |
| 11 | Bowing, Then Looking Back | 126.893–138.160 | 11.267 | `seg11_02m06p89s-02m18p16s.mp3` |
| 12 | The Question Returns Twice | 138.160–150.226 | 12.066 | `seg12_02m18p16s-02m30p23s.mp3` |
| 13 | Instrumental Hero Resolution | 150.226–160.496 | 10.270 | `seg13_02m30p23s-02m40p50s.mp3` |

> 段与段首尾相接（上段结束时间 = 下段开始时间），无重叠、无空档。

## 核心方法：每段 self-contained + 局部时间 + 音乐连续

长片切 13 段后最容易出错的是「时间越界」和「音乐重启」。本案例的纪律：

1. **每段独立可复制**：各自声明 `Picture 1` / `Audio 1` / 段时长 / 段内时间轴，单段即可生成、不依赖上下文。
2. **段内时间从 0.000 起算**：所有动作时间戳是 local time，全局时间只出现在段首「源歌窗口」说明里，避免模型把段内秒数误当全片时间。
3. **只喂该段裁剪音频**：`Audio 1` 对应本片段窗，音乐天然连续；提示词强调不重启、不加声音。
4. **段末写 hand-off 状态**：每段结束的身体/镜头状态是下段开场可自然承接的起点；相邻段不硬切归零。

## 参考图视觉权威与武器状态硬保护

- `Picture 1` 是人物与场景的**唯一**视觉来源；文字只负责新设计的动作与镜头，不复述外貌、不把歌词意象自动变成画面实体（不据歌词擅自换装、添道具、加人、改场景）。
- **武器纪律**：不重新设计、不复制、不画（凭空生成）、不入鞘、不拔剑、不移除、不改动任何武器；**图中无武器则双手始终为空**；图中有武器则保持其既有状态、形制、鞘、朝向与位置。
- 禁止出现第二人、帮忙的手、形似他人的倒影或重复的舞者。

## 动作与镜头的写法（与方法论 20 条呼应）

- **先舞后镜**：去掉摄影机文字，动作本身仍要是完整的舞；镜头每次运动都要有身体动机。
- **身体动力链**：脚步 → 重心 → 身韵 → 手臂 → 眼神；动作写清发力源、承重链、关节线条、头眼位置，逐拍标注 Beat/强弱/local。
- **动作主题贯穿**：13 段复用、变奏、回收同一动作母题（Cold Mountain Blade-Line → 多次 Reprise → Question Returns Twice → Hero Resolution），不是一段一套互不相干的动作。
- **景别也是编舞**：镜头几何写真实空间关系（机位、透视、视差、运动路径），不堆角度名词。
- **负面要给正向替代**：不写「不要普通走路」，而规定位移由交叉步、重心转移、支撑脚转向与回弹组成。

## 最值得迁移的几条

1. **节拍网格显式化**：给出 BPM / beat / bar / phrase 的秒数，让动作与镜头都可落到拍、可核对；散板才不写 BPM。
2. **13 段统一模板**：段首三要素（Picture 权威 / Audio 权威 / 段窗与 local time）→ 段内动作计划 → 镜头设计 → 声音规则 → 负面；每段结构一致，便于批量生成与质检。
3. **简洁参考图版**：外貌完全交给图，文字把字符预算全部用于动作因果、镜头动机与硬约束。
4. **器乐尾奏照样编舞**：无歌词段不「空站」，用音乐 phrasing 把整段设计成器乐 coda，结尾收在真实音频尾。

## Assets

| 文件 | 作用 |
|---|---|
| [`prompt.md`](./prompt.md) | 13 段 self-contained 英文成品提示词 + Implementation notes（按原文分节排版） |
| [`methodology.md`](./methodology.md) | 古风舞蹈 H3 创作方法论 20 条（动作动链 / 导演级运镜 / 分段纪律 / 自检清单） |

> 相关成片与封面素材为本地文件，**真人成片、图像、音频不随公开仓库分发**（肖像 / 版权考量），仅在此留名备查；如需随仓保存可另行放入 `assets/` 或走 Releases 附件。

## Tags

`#H3` `#MINIMAXH3` `#prompt-engineering` `#classical-chinese-dance` `#wuxia` `#guofeng` `#multi-segment` `#self-contained-prompts` `#beat-grid` `#music-driven` `#hand-off` `#image-locked` `#zero-appearance-description` `#weapon-state-lock` `#kinetic-chain` `#camera-motivation` `#promptshare` `#提示词分析` `#ai教程`
