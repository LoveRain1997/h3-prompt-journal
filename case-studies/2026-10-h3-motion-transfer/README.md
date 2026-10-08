# 020 · H3 Motion Transfer — Subject-First Reconstruction (动作迁移)

![cover](./cover.png)

- **Date:** 2026-10
- **展示成片:** [result-video.mp4](./result-video.mp4) — 9.4s · 928×1664 竖屏 · 一镜合成
- **输入:** `<Picture 1>` 人物+世界锚定图 · `<Video 1>` 目标动作视频 · `<Audio 1>` 时序音频
- **Prompt:** see [prompt.md](./prompt.md) — MULTIMODAL RECONSTRUCTION 全文，可直接粘贴
- **工作流:** H3动作迁移工作流.json（ComfyUI · MiniMax H3 Ref2VA 双通道）

## 案例对照

| | 目标视频（Video 1） | 迁移结果（本成片） |
|---|---|---|
| 人物 | 黑裙绣花抹胸裙·双髻·室内 | **青绿仙裙·湖边石上**（全部来自 Picture 1） |
| 环境 | 白墙室内 | 湖面山林（Picture 1 世界） |
| 动作 | 踢腿小舞：转体→点步→踢腿→比手势→收势 | **同构编舞**：转体露背→点步→踢腿→手势链→收势，机制逐拍对应 |
| 镜头 | 固定全身平视 | 固定全身平视（首帧几何迁移） |
| 时长 | 9.29s | 9.42s（Audio 1 重定时） |

## 方法论：三参考 Strictly Separated

动作迁移最容易翻车的是**参考角色泄漏**——目标视频的人脸渗进结果、目标环境跟着动作一起搬过来。这套提示词的解法是把三个输入拆成互斥的信息通道：

```
PICTURE 1            = PERSON + CLOTHING + IDENTITY + ENVIRONMENT + WORLD
VIDEO 1 FIRST FRAME  = CAMERA GEOMETRY + OPENING BODY ORIENTATION
VIDEO 1 REMAINDER    = MOVEMENT MECHANICS + TRANSITIONS + CAMERA BEHAVIOR
AUDIO 1              = TIMING + RHYTHM + ACCENTS + PHRASES
```

关键设计：

1. **SUBJECT-FIRST 初始化顺序（不可逆）**: 先建 Picture 1 的人 → 再建 Picture 1 的世界 → 才做镜头重定位 → 再接视频1开场体态 → 最后重建运动。从视频1出发再"换人"是错误路径。
2. **首帧只读镜头几何**: 视频1第一帧不是视觉模板——只提取景别/距离/高度/角度/构图/朝向，人物、背景、服装、光线全部丢弃。
3. **视频1 = 动捕参考**: 只提取 preparation → initiation → expansion → accent → recovery 的运动机制（重心转移/脚放置/骨盆/手臂路径/幅度速度），不逐帧复制画面。
4. **音频1 是时序权威**: 不保留视频1原始节奏、不整体变速——动作按音频1的 BPM/重拍/乐句重新定时。
5. **FINAL VALIDATION 清单**: 八项逐条自检（人物/背景/开场/视频1人已弃/视频1景已弃/运动是机制而非复制/时序已重定/镜头在图1世界内），任何一项否 → 重建。

## 硬约束

> ⚠️ **H3 动作迁移单次生成最长 8–9 秒。** 目标视频超长必须先剪到 8–9s，或按乐句拆段逐段迁移再拼。超限会导致动作漂移、身份崩坏、尾部截断。本案例 9.4s 已是上限值（工作流 Duration=9s / 124 帧 @24fps）。

## 工作流要点（ComfyUI）

- 模型: `minimax_h3_hybrid_fl2va_ref2va` + `ref2v_turbo_4step` LoRA + SageAttention patch
- 双通道可切: 标准 20 步 simple 调度 / turbo 6 步+手动 sigma（开关切换）
- 调度推荐: 高动态（打斗类）beta-8 + ExtendIntermediateSigmas(2, 0.75)；低动态（文戏类）beta-4 + (3, 0.75)
- 续接: 用 GetImageRangeFromBatch(-1, 22) 取尾帧 + ImageAddNoise(0.2–0.5) 缓解油腻，**成片剪辑时裁掉加了噪声的前 22 帧**
- 输出: 1344×768（工作流内）→ 成片 928×1664 竖屏，Duration=9s

## Takeaway

动作迁移不是"换脸"也不是"背景替换"，而是 **Picture 1 的人 + Picture 1 的世界 + Video 1 的动作语言与镜头语言 + Audio 1 的时序 → 一段全新的实拍表演**。三个参考各管一路、互不越权；首帧只当取景器，不当代模板；时长卡死 8–9 秒。
