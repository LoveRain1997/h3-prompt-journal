# 分段生成，动作反而更流畅 —— 篮球女孩 MV 工作流上手指南

> 以《[篮球女孩 · 元气可爱应援舞 MV](../case-studies/2026-11-basketball-girl-cheer-dance-mv-4-segment/)》为例：50 秒、150.5 BPM、四段独立生成后期拼接。🎬 [成片](../case-studies/2026-11-basketball-girl-cheer-dance-mv-4-segment/result-video.mp4)

很多人想让 H3「一次生成一支完整的舞」，结果动作越来越糊、人物越来越走样——长时间线恰恰是动作崩坏的根源。**正确做法是反过来：切短、独立、再拼回来。** 分段生成不但没有牺牲流畅性，反而是流畅的前提。

## 工作流五步

1. **切歌**：把整首歌交给 [audio-lyric-splitter](https://github.com/LoveRain1997/audio-lyric-splitter)——按歌词感知切段，每段 10–15 秒、绝不切断唱句、切点卡在气口；同时输出每段的 BPM / beat / bar / 乐句时间网格（cuts_manifest JSON）。
2. **写段**：每段写一份**自包含**提示词——音乐网格（首 downbeat、phrase accents）+ 完整动作链（准备重心→发起→扩展→强拍→回收→衔接）+ Hero 动作挂重音 + 物理运镜。所有参考图都用 `<Picture 1>` 全程全参考锁定人物。
3. **分段生成**：官网逐段喂「同一张图 + 该段音频切片」；或在 ComfyUI 用本地工作流（`MiniMaxH3ReferenceToVideo` + `MiniMaxH3AddGuide` 续接组：上段末帧喂下段做 guide，见案例里的 `comfyui-workflow.json`）。
4. **匹配开场**：后一段以**局部特写**重新开场（前景手掌/前臂/指尖），与前一段的结束构图做视觉匹配——不要求模型记住上一段的身体姿态。
5. **拼接**：按原曲顺序把四段拼回去，音频天然无缝（切段时零切词），画面接缝被特写匹配遮住。

## 为什么分段反而流畅

- **模型不需要记住上一段**：跨段记忆是身份漂移和动作崩坏的来源；每段独立、每段完整，生成质量稳定。
- **音乐时间轴锚住每段节奏**：动作峰值、镜头响应、剪辑点全部挂在同一条 onset/乐句网格上，段内 1:1 同步。
- **特写开场 = 剪辑匹配**：手掌、手腕、指尖这类局部构图天然适合硬切，接缝不可见。
- **本地续接加强**（可选）：ComfyUI 里把上段末帧作为下段的 guide 图，帧级过渡更紧，但动作主体仍然每段独立设计。

## 仓库地址

| 资源 | 地址 |
|---|---|
| 本案例（四段提示词全文 + ComfyUI 工作流 + 成片） | https://github.com/LoveRain1997/h3-prompt-journal/tree/main/case-studies/2026-11-basketball-girl-cheer-dance-mv-4-segment |
| 案例总库（30 篇反推与实测，每篇附可粘贴提示词） | https://github.com/LoveRain1997/h3-prompt-journal |
| 切歌工具（歌词感知分段 + cuts_manifest） | https://github.com/LoveRain1997/audio-lyric-splitter |
| 视频反推技能（把参考视频反推成 H3 提示词） | https://github.com/LoveRain1997/video-to-h3-prompt |

一句话总结：**音乐切短、每段自包含、特写匹配开场——分段生成，就能获得流畅的动作。**
