<div align="center">

<img src="docs/images/banner.jpg" width="720" alt="H3 Prompt Journal Banner">

# 🎬 H3 Prompt Journal

**MiniMax H3 视频/舞蹈提示词案例日记 —— 18 篇真实反推与实测，每篇附可直接粘贴的完整提示词。**

[![Cases](https://img.shields.io/badge/case_studies-19-blue)](./case-studies)
[![Platform](https://img.shields.io/badge/model-MiniMax_H3-red)](https://github.com/MiniMax-AI/MiniMax-H3)
[![Results](https://img.shields.io/badge/🎬_成片演示-X_文章页-1DA1F2)](https://x.com/LoveUolanda/articles)

</div>

---

## 这是什么

H3 提示词工程的难点不在调参数，而在**教会模型一种关于"转场与连续性"的思维方式**。

大多数公开 H3 提示词只描述"每个镜头里该出现什么"，所以生成出来是支离破碎的片段；能跑通的提示词描述的是**镜头必须遵循的连续物理逻辑**——人物从不消失、动作跨段续接、切点吸附在音乐事件上。本仓库把每一次跑通的过程都记录下来：真实尝试 → 踩过的坑 → 突破口 → 最终可用的提示词。

> 🎬 所有案例均由这些提示词实际生成，成片演示统一收录在 [X 文章页 @LoveUolanda](https://x.com/LoveUolanda/articles)。

## 每篇案例的结构

```
case-studies/YYYY-MM-short-name/
├── README.md      <- 背景、问题、突破口、可复用的经验
└── prompt.md      <- 完整最终提示词，可直接粘贴进 H3
```

## 快速上手（三件套用法）

1. **复制 `prompt.md` 全文**粘贴到 H3（每段提示词都是自包含的，不依赖上下文）；
2. **上传锚定图**：图 1 锁外貌+服装（提示词里对图 1 零外貌描写），图 2 按需锁脸/背/多视角；
3. **附 `audio1`**（舞蹈/卡点类）：切点、抖腿、换装全部吸附在音频 onset 网格上。

核心纪律速览：**每段自包含 · 图 1 零外貌 · 全局规则拼进每一段（禁止规则段压底） · 卡点=onset · 分段间局部特写+动作续接 · 转场写成"动作钩子+切点原因+下段续动"**。

---

## 🧭 案例导航

### 2026-08 · 基础篇：运镜、结构与多主体

| 预览 | 案例 | 简介 |
|:---:|---|---|
| <img src="docs/images/004-furina-mv.jpg" width="160"> | [004 · Furina Windsurfing Fashion MV](./case-studies/2026-08-furina-windsurfing-fashion-mv/) | 分层参考架构 + 文本驱动高潮：角色主视觉/三视图装备/分段运镜指南多图分工。🎬 [成片](./case-studies/2026-08-furina-windsurfing-fashion-mv/result-video.mp4) · [运镜指南图](./case-studies/2026-08-furina-windsurfing-fashion-mv/picture-3-segment1-cinematography-guide.png) |
| <img src="docs/images/006-sticker-comedy.jpg" width="160"> | [006 · Sticker Character Kitchen Comedy](./case-studies/2026-08-sticker-character-kitchen-comedy/) | 贴纸角色混入真实厨房的混搭媒介喜剧。[角色贴纸图](./case-studies/2026-08-sticker-character-kitchen-comedy/picture-1-sticker-character.png) |
| <img src="docs/images/007-cinematic-reveal.jpg" width="160"> | [007 · Cinematic Character Reveal (Two-Part)](./case-studies/2026-08-cinematic-character-reveal-two-part/) | 两段式电影感角色揭示，BGM 跨段连续不断。🎬 [动作参考](./case-studies/2026-08-cinematic-character-reveal-two-part/reference-motion-sample.mp4) · [姿态库](./case-studies/2026-08-cinematic-character-reveal-two-part/picture-1-pose-library.png) |
| <img src="docs/images/008-finger-dance.jpg" width="160"> | [008 · First-Person Finger-Controlled Dance](./case-studies/2026-08-first-person-finger-controlled-dance/) | 单图输入实现第一人称"手指操控"舞蹈。🎬 [参考舞步](./case-studies/2026-08-first-person-finger-controlled-dance/reference-dance-demo.mp4) |
| — | [001 · Three-Person Occlusion-Linked Orbital Long Take](./case-studies/2026-08-three-person-orbital-long-take/) | 三人遮挡联动的环绕长镜头：谁被挡住、谁先出列，全部写进物理逻辑。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| — | [002 · Asymmetric Speed-Ratio Duo Choreography](./case-studies/2026-08-dual-subject-speed-contrast/) | 双人不对称速度比编舞：一快一慢同框共舞的节奏控制。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| — | [003 · Micro-Cam Anchor-Flow Flight](./case-studies/2026-08-single-subject-three-pose/) | 单人三姿态微运镜：锚点流动式贴身飞行机位。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| — | [005 · Water Obstacle Variety Show](./case-studies/2026-08-water-obstacle-variety-show/) | 综艺式水上障碍闯关：节拍锚定的即兴表演。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |

### 2026-09 · 进阶篇：卡点、换装与连续舞蹈

| 预览 | 案例 | 简介 |
|:---:|---|---|
| <img src="docs/images/009-prank-cosswap.jpg" width="160"> | [009 · Three-Person Prank, Freeze Gag + Cos Swap](./case-studies/2026-09-three-person-prank-freeze-gag-cos-swap/) | 反推实战：三人恶作剧定格笑点 + 仅换皮肤的 Cos 换装。🎬 [成片](./case-studies/2026-09-three-person-prank-freeze-gag-cos-swap/result-video.mp4) |
| <img src="docs/images/010-snap-lock.jpg" width="160"> | [010 · Snap-Lock Editorial Reveal](./case-studies/2026-09-snap-lock-editorial-reveal/) | 音频吸附式 SNAP-LOCK 时尚揭示：两态相机 + 全程零外貌文本。🎬 [参考视频](./case-studies/2026-09-snap-lock-editorial-reveal/reference-video.mp4) |
| — | [011 · Song-Style Classical Dance (Six Segments)](./case-studies/2026-09-song-style-classical-dance-six-segment/) | 六段歌曲式身韵水袖舞：手递手英雄姿势阶梯 + 音乐不重启。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| — | [012 · Editorial Lamp-Rhythm Fashion A/B](./case-studies/2026-09-editorial-lamp-rhythm-fashion-ab/) | 灯光节奏时尚片 A/B：暗奢甩裙 vs 甜美折脚跳，音乐驱动灯光切换。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| — | [013 · Action-Chain Sock Fan Comedy](./case-studies/2026-09-action-chain-sock-fan-comedy/) | 25 状态物理状态机：脱袜-闻袜-扔镜头-弹回-光脚扇子舞的喜剧动作链。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| — | [014 · Purple-Veil Pavilion Dance (Seven Segments)](./case-studies/2026-09-purple-veil-dance-seven-segment/) | 七段紫纱亭舞：驱动轮换编舞 + 细节切转场链 + 紫底暖键打光 + 永久面纱锁。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |

### 2026-10 · 大成篇：多段长舞与转场取证

| 预览 | 案例 | 简介 |
|:---:|---|---|
| <img src="docs/images/016-waterfront-solo.jpg" width="160"> | [016 · Waterfront Solo Dance (Two Segments)](./case-studies/2026-10-waterfront-solo-dance-two-segment/) | 水岸白裙独舞：低阈值切镜检测(≤0.08)逐帧取证单镜头真伪 + 小节吸附切分 + 链记法动作续接。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| <img src="docs/images/017-sock-showcase.jpg" width="160"> | [017 · Sock Showcase, Right-Entry Three-Shot](./case-studies/2026-10-sock-showcase-right-entry-three-shot/) | 三镜袜子展示：每个服装状态=独立镜头，画右一大步跨进入画、首帧已穿新装，跳切痕迹可见是特征。逐帧转场取证实录。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| <img src="docs/images/018-leg-lift-contact-cut.jpg" width="160"> | [018 · Leg-Lift Contact-Cut Stocking, Six Looks](./case-studies/2026-10-leg-lift-contact-cut-stocking-six-look/) | 抬腿触地即切袜·六形态：永久支撑腿 + 单一活动腿，"脚触地"这一物理事件=剪辑触发器（CONTACT=CUT）。AnimateDiff 渐变升级为利落硬切。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| — | [015 · Xiashan Veiled Solo (Twelve Segments)](./case-studies/2026-10-xiashan-veiled-solo-twelve-segment/) | 十二段面纱独舞：双图分权（图1服装/图2脸+背+纱）+ 链记法编舞 + 切点原因转场 + 醉酒式运镜（只有相机醉，人物永不醉）。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |
| <img src="docs/images/019-identity-only-half-body.jpg" width="160"> | [019 · Identity-Only Half-Body Dance (Six Segments)](./case-studies/2026-10-identity-only-half-body-dance-six-segment/) | Identity-only 双图分权：图1只锁脸、图2只锁全身外观+环境，"图1半身像感"降级为纯镜头语言，开场零姿势继承（六段都从舞谱第一拍起跳）。111 BPM 六段连续可爱舞蹈，Motion Cut 全部切在未完成动作中间，Hero Action 专属镜头。🎬 成片见 [X 文章页](https://x.com/LoveUolanda/articles) |

---

## 反推工作流（本仓库案例的生产方式）

每个 2026-09 之后的案例都经过同一套双 skill 流水线：

1. **probe**：ffmpeg 提取时长/帧率/音频波形，onset 检测输出卡点网格；
2. **五遍逻辑通读 + 低阈值切镜检测**（scene 阈值 0.27 探不到的转场，≤0.08 现形）；
3. **全帧率逐帧核对**：确认每个切点真伪、每个服装状态边界；
4. **复述确认** → 产出 H3 提示词 → 回测 → 收入日记。

配套工具：[`video-to-h3-prompt`](https://github.com/LoveRain1997/video-to-h3-prompt)（可复用的 H3 反推 skill）· 上游规范：[`h3-prompt-writing`](https://github.com/MiniMax-AI/MiniMax-H3/tree/main/skills/h3-prompt-writing)

## License

MIT — see [LICENSE](./LICENSE).
