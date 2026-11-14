# 《月有亏时》｜南宫阙 · MiniMax H3 古风舞蹈 MV 完整提示词

> **版本：** Director Cut · Rev.3.0（原地古风舞蹈重构）  
> **画幅：** 竖屏 9:16，写实电影摄影  
> **输入：** 每段只使用同一张 `<Picture 1>` 与对应段的 `<Audio 1>`；不使用 Video 1  
> **音频：** `月有亏时.mp3`，总长 207.520s；BPM 133.93；beat 0.448s；bar 1.792s；phrase 3.584s；first downbeat 1.758s  
> **分段：** 17 段，9.371–14.222s；逐段沿用原始 JSON 时间轴与局部时长

---

## 一、执行总纲（最高优先级）

### 1. Picture 1 绝对锁定

`<Picture 1>` 是唯一且完整的视觉母参考，直接决定人物身份、脸、发型、身材比例、服装、饰物、材质、肤质、色彩、光线、背景、建筑、空间布局、天气氛围、构图关系与镜头透视。**提示词不再重新描写或补充这些视觉属性**；不得根据文字重新设计人物或环境。所有段落都在同一张图所定义的视觉世界内完成。只改变人物动作、摄影机观察位置与剪辑视点，不改变图1中的任何视觉设定。

不得添加、替换、删减或重新解释图1中的人物外貌、服装层次、发饰、首饰、建筑、植物、陈设、天气元素或光源。不得引入新人物、分身、回忆人物、武器、法器、扇、伞、书卷、玉简、飘带、水袖、乐器或任何手持道具。人物全片空手。

### 2. 原地舞蹈规则（硬约束）

- **全片不走动、不沿屋脊行进、不向镜头逼近或远离、不横穿场景、不做舞台走位。** 人物始终在图1所示的原始站立区域内完成舞蹈，脚下只允许原地虚实步、点步、并步、盖步、轴心转身、重心交换、屈膝沉身、提踵和短距离脚掌调整。
- “点步、盖步、并步、转身”只服务于原地舞句，不得被模型扩展成连续行走。每次脚步完成后，人物重心仍回到原始表演区域。
- 舞蹈必须贯穿全片。不能用长时间站立、看月、抬头、走路或空镜替代舞蹈。空镜只作短促剪辑呼吸，不能切断动作链；切回人物时承接上一镜动作，不重新起势。
- 每段至少安排 2 条有明确动作结构的古风舞蹈链；较长段落安排 3–4 条。不要把每拍拆成互不相关的小动作，也不要只写“优雅舞动”。

### 3. 动作库依据与选型

以用户指定的 `dance-motion-chain-h3.md` 当前版本为动作设计依据，重点调用古风身韵 C1 提沉起势、C2 云手横八字、C3 立圆托举、C5 拧倾出胯亮相、C7 留头转身、C12 静态平衡、C16 云手穿掌背转前，以及 Hero 库的 TURN / LINE / ACCENT 动力链。所有动作均改造成**无道具、原地定点版本**；不使用依赖扇、长绸、水袖、圆场碎步或行进路线的动作链。

动作不是名称罗列。每条链写清：起始支撑与预载 → 动力从脚底/重心传至骨盆、胸腔、肩肘腕 → 主要动作峰值 → 惯性控制 → 制动回收 → 下一链入口。动作难度服从时间窗容量，宁可减少数量，也不压缩成模型无法执行的动作堆叠。

### 4. Hero 配置

全片保留三个主要 Hero，分别落在 SEG07、SEG13、SEG16：
- SEG07：点步翻身 → 探海线（TURN + LINE）。
- SEG13：单次 360° 掖腿转 → 开臂制动（TURN + ACCENT）。
- SEG16：Attitude / Arabesque 高位延展 → Hero Lock → 受控回收（LINE）。

每个 Hero 必须有完整全身镜头，明确承重脚、预载、动力传递、技术峰值、定点、制动与释放。不得为了“高级”加入空翻、连续多圈旋转、无支撑悬浮或高危地面技巧。Hero 动作不能被特写剪碎。

### 5. 摄影机与分镜

- **低机位仰拍为主**：多数舞蹈主镜头在人物腰线以下或接近屋面高度观察，保持全身比例自然、面部可读、支撑脚清楚。摄影机可以短距离侧移、低位弧移、轻摇上跟随手臂、随转身短弧跟拍，但不绕人物整圈。
- 用中全身/全身镜头交代动作完整性；在云手、穿掌、盘腕、指尖、眼神、支撑脚与衣袖惯性等关键节点直接切特写。特写必须服务动作信息，不用长推拉制造景别变化。
- 空镜仅从 `<Picture 1>` 已经存在的画面中截取局部、虚实和光影层次；不添加新的景物，不把歌词名词拍成物件。空镜长度短，且必须通过动作方向、视线或遮挡匹配切回舞者。
- 每段选择少数有动机的镜头变化，不用无意义环绕、反复推拉、重复脚到脸的运镜。摄影机与舞蹈共用时间轴：动作启动时摄影机启动，重拍峰值时构图到位，动作制动时摄影机同步减速。

### 6. 歌词与声音

歌词只提供情绪、主题与段落能量，不是分镜清单。不得因歌词出现某个名词就生成对应道具、人物、地点或字面动作。导演通过古风舞蹈、身体张力、节奏、眼神和剪辑表达抽象情绪。人物不唱歌、不念白、不做口型；不加对白、音效、环境声、字幕、歌词字卡或片名。每段只保留对应 `<Audio 1>` 原始切片，不重混、不重启、不拉伸。

---

## 二、原曲切片索引

| 段落 | 原曲时间 | 时长 | 音频文件 | 舞蹈任务 |
|---|---:|---:|---|---|
| SEG01 | 00:00.000–00:09.371 | 9.371s | `seg01_00m00p00s-00m09p37s.mp3` | 建立身韵与人物气场 |
| SEG02 | 00:09.371–00:21.892 | 12.521s | `seg02_00m09p37s-00m21p89s.mp3` | 自由冲动与舞句展开 |
| SEG03 | 00:21.892–00:34.413 | 12.521s | `seg03_00m21p89s-00m34p41s.mp3` | 身体挣脱与转身控制 |
| SEG04 | 00:34.413–00:45.734 | 11.321s | `seg04_00m34p41s-00m45p73s.mp3` | 内省与细腻身韵 |
| SEG05 | 00:45.734–00:57.756 | 12.022s | `seg05_00m45p73s-00m57p75s.mp3` | 疲惫中的身体控制 |
| SEG06 | 00:57.756–01:09.777 | 12.021s | `seg06_00m57p75s-01m09p77s.mp3` | 压力聚集与对抗性舞句 |
| SEG07 | 01:09.777–01:21.798 | 12.021s | `seg07_01m09p77s-01m21p79s.mp3` | Hero 1：点步翻身接探海线 |
| SEG08 | 01:21.798–01:34.999 | 13.201s | `seg08_01m21p79s-01m34p99s.mp3` | 舞句连贯与身韵舒展 |
| SEG09 | 01:34.999–01:45.760 | 10.761s | `seg09_01m34p99s-01m45p76s.mp3` | 质询与停顿中的细节 |
| SEG10 | 01:45.760–01:56.941 | 11.181s | `seg10_01m45p76s-01m56p94s.mp3` | 温柔回忆感与重新收束 |
| SEG11 | 01:56.941–02:11.163 | 14.222s | `seg11_01m56p94s-02m11p16s.mp3` | 两难冲突与身体对抗 |
| SEG12 | 02:11.163–02:25.044 | 13.881s | `seg12_02m11p16s-02m25p04s.mp3` | 由封闭转向舒展 |
| SEG13 | 02:25.044–02:38.485 | 13.441s | `seg13_02m25p04s-02m38p48s.mp3` | Hero 2：掖腿转单圈与开臂制动 |
| SEG14 | 02:38.485–02:51.927 | 13.442s | `seg14_02m38p48s-02m51p92s.mp3` | 迎风感由舞蹈张力呈现，不行走 |
| SEG15 | 02:51.927–03:03.647 | 11.720s | `seg15_02m51p92s-03m03p64s.mp3` | 高潮余势与节奏变化 |
| SEG16 | 03:03.647–03:15.368 | 11.721s | `seg16_03m03p64s-03m15p36s.mp3` | Hero 3：高位延展与稳定释放 |
| SEG17 | 03:15.368–03:27.520 | 12.152s | `seg17_03m15p36s-03m27p52s.mp3` | 尾奏：舞蹈回收与人物状态完成 |

---

## 三、17 段 H3 完整提示词

### SEG01｜00:00.000–00:09.371｜建立身韵与人物气场

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 9.371 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.200] 低机位全身建立。人物双脚原地稳稳承重，先做 C1「提沉起势」：呼气含胸、头微垂；吸气由腰背逐节提起，肩沉肘坠。摄影机贴近地面沿人物正前方短滑，向上抬至低仰全身，动作全貌清晰。

[Shot 2 | 2.200–4.100] 切低仰中全身。接 C2「云手横八字」前半：左臂上撩、右臂下沉，胸前划出宽而连续的横向圆弧；重心只在两脚之间左右虚实交换，不迈步、不改变站位。摄影机横移小半身宽，跟随高低手形成层次。

[Shot 3 | 4.100–6.781] 切手部特写，双腕先后翻转，兰花指由松到合再舒展，手指轨迹连续而有控制；镜头沿手臂向上摇到眼睛，面部只保留自然细微表情。

[Shot 4 | 6.781–9.371] 回低机位全身，完成 C2 横八字另一半，双臂交替绕回胸前，再以 C5「拧倾出胯亮相」收尾：腰胯先拧、胸肩随后，手臂一高一低拉出斜线，重拍定住半拍后柔和释放，身体仍留有下一段入口。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG02｜00:09.371–00:21.892｜自由冲动与舞句展开

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 12.521 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.700] 低仰全身。以原地虚步点步起势：一脚脚尖轻点侧前方后收回，承重腿保持稳定；腰胯微拧，双手从胸前交叠穿掌，手腕翻转后向两侧分开。

[Shot 2 | 2.700–5.300] 连续接 C16「云手穿掌」：右手领云手经面前横磨，左手穿掌翻腕；双臂在胸前交叉下沉，再向外打开。脚下只做原地盖步和重心交换，绝不向屋脊方向行走。摄影机低位侧前方短弧移，不绕人物整圈。

[Shot 3 | 5.300–7.000] 空镜短切：只取 Picture1 已有画面元素的局部与光影变化，镜头轻微横移，作为舞句呼吸，不新增物件或景物。

[Shot 4 | 7.000–10.300] 低仰全身回到人物。做 C3「立圆托举」的无道具身韵版本：单臂沿身体前方画立圆至头顶，胸腰顺势提起但不过度后折；另一臂从腰侧穿出形成反向弧线。原地小幅轴心换向，双脚始终留在固定表演区域。

[Shot 5 | 10.300–12.521] 切低仰脸部近景，头随领先手的方向最后转到位，眼神从收敛转为明亮；镜头不推拉，利用动作完成点直接切近景。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG03｜00:21.892–00:34.413｜身体挣脱与转身控制

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 12.521 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.600] 低仰全身。双脚一前一后建立虚实步，膝部微屈，躯干先含后提；双臂由身侧向内收，手腕在胸前交错翻转，形成受限感。保持原地，不向前走。

[Shot 2 | 2.600–5.600] 接 C16 的穿掌背转前变体：一手从面前云手横磨，另一手穿掌；以支撑脚为轴做四分之一转身，背部短暂朝向镜头，双臂经过脸前交叉下沉，再转回三分之四正面。摄影机低位横移跟随，不抢动作。

[Shot 3 | 5.600–8.800] 全身镜头清楚呈现 C7「留头平转」的单次转身：先定头、躯干和骨盆依次启动，完成一次受控轴心转向；自由脚点地辅助，不做连续多圈。双臂由收至开控制惯性，转完脚掌稳稳落地。

[Shot 4 | 8.800–10.800] 切脚步特写，支撑脚压地、脚跟微转、脚尖点地回收，清楚表现重心落稳；镜头随后顺势切至手腕翻花。

[Shot 5 | 10.800–12.521] 低仰中全身，双臂从胸前交叉猛然展开成斜向长线，胸腔打开、头部最后定向，形成明确重拍亮相，随即自然回收。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG04｜00:34.413–00:45.734｜内省与细腻身韵

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 11.321 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.500] 低仰中全身。C1 提沉放慢但保持音乐脉搏：含胸沉肩、气息下沉，随后脊柱逐节提起；双手从腰侧沿身体中线缓缓托起。双脚不移动。

[Shot 2 | 2.500–4.700] 脸部侧前近景，眼神从下方抬起，头部微侧后回正；镜头固定，以表情和呼吸完成反应镜头，不重新描述或改变人物外貌。

[Shot 3 | 4.700–7.300] 手部特写，C2 云手的缩小版：双腕交替翻转，掌心一上一下绕胸前小圆，手指柔和延伸；镜头沿手腕运动做短横移，保持原有衣袖形态。

[Shot 4 | 7.300–9.300] 低仰全身。原地做「旁提—回正」身韵：一侧腰肋向上提，躯干形成柔和侧弧，同侧手臂上举、另一手下按；再由腰胯带回中轴，接一个小幅拧身。

[Shot 5 | 9.300–11.321] 空镜仅作短暂呼吸，随后切回低仰半身：她将双手收至胸前，手腕交叠后缓慢分开，动作未完全结束便进入下一段。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG05｜00:45.734–00:57.756｜疲惫中的身体控制

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 12.022 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.500] 低仰全身。原地虚步：承重腿微屈，另一脚脚尖轻点前侧、收回，再点向侧方；上身保持平稳，双手低位绕腕，表现疲惫但仍有控制。

[Shot 2 | 2.500–4.700] 切面部近景，呼吸稍重，眼睑短暂下落再抬起；头部不垂坠，不演哭泣。镜头稳定，不推近。

[Shot 3 | 4.700–7.000] 切手与袖口特写，手指从轻握逐节松开，腕部向外翻转，肘部带动前臂画一条柔弧；镜头焦点从近处手指转到后方脸部。

[Shot 4 | 7.000–10.000] 低仰全身，做「沉—拧—穿—收」连续短链：屈膝下沉，腰胯拧向一侧，前手穿掌越过胸前，后手反向绕至腰侧；重心在两脚间转换但双脚不离开固定位置。

[Shot 5 | 10.000–12.022] 切脚部近景，脚掌压实、脚尖点地回收；切回低仰中全身，双臂垂落后借肩胛带动再次抬起，保持动作流动。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG06｜00:57.756–01:09.777｜压力聚集与对抗性舞句

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 12.021 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.500] 低仰全身。建立宽站姿，膝部下沉，骨盆向右拧、胸腔反向扭转，双肘收于肋侧；摄影机从低侧前方缓慢横移，突出身体扭力。

[Shot 2 | 2.500–5.000] 接 C2 云手横八字，但加重拍：一臂上撩、一臂下切，第二拍交换高低；手腕翻转带出掌形，胸腔随臂线旋开。脚下仅做原地重心切换。

[Shot 3 | 5.000–7.300] 手臂与肩部近景，连续两次「穿掌—反腕—收肘」短促动作，第二次在重拍突然停住；镜头跟手横移，在停点同步刹住。

[Shot 4 | 7.300–10.000] 低仰全身，做「点步翻身」简化链：一脚向侧点地建立支撑，骨盆带动躯干转向，双臂一前一后打开；头部最后转回镜头方向。不是翻滚或空翻，不改变所在位置。

[Shot 5 | 10.000–12.021] 空镜短切后回到低仰半身，双手在胸前交叠，向外推出并打开，肩线由紧变松，给下一段留出打开的手臂轨迹。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG07｜01:09.777–01:21.798｜Hero 1：点步翻身接探海线

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 12.021 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.000] 低仰全身连续镜头。Hero 准备：双脚建立稳定虚实步，承重脚掌压地，膝部屈伸预载；骨盆先拧向转动方向，双臂收至身体中线，视线定住一个前方点。

[Shot 2 | 2.000–4.600] Hero 启动：点步脚轻触地面后回收，支撑脚带动骨盆和胸腔完成一次明确的点步翻身；肩、肘、腕依次打开，头部最后回正。摄影机低位跟随短弧移动，不做自身整圈环绕。

[Shot 3 | 4.600–7.600] Hero 技术峰值：转身动力直接延续为探海线，支撑腿稳固屈伸，动力腿向后上方延展，躯干向前形成反向平衡，前臂向斜前伸、另一臂向后拉开。完整全身必须可见，脚下支撑和身体轴线清楚。

[Shot 4 | 7.600–9.000] Hero Lock：在音乐重拍锁定探海最高可控线条，停留短促而清晰；摄影机同步减速并稳定，不切特写遮掩平衡。

[Shot 5 | 9.000–12.021] Release：动力腿有控制地下落，骨盆回正，双臂沿圆弧收回胸前，再做一次小幅云手穿掌，身体仍在原地，动作自然接入 SEG08。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG08｜01:21.798–01:34.999｜舞句连贯与身韵舒展

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 13.201 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.800] 低仰全身，承接上一段手臂回收，完成 C16 云手穿掌后转身：手从面前横磨、穿掌翻腕，双臂胸前交叉下沉，再向两侧打开；脚下原地盖步，不位移。

[Shot 2 | 2.800–5.500] 切低仰侧前全身，做 C3 立圆托举的双侧变体：右臂从下向上画立圆，胸腰提起；左臂从高位沉至侧下方，形成高低错落。动作完成后腰部回正，双脚留在原位。

[Shot 3 | 5.500–7.000] 手部特写，双腕连续盘腕，掌心由内翻外，指尖依次展开；摄影机贴着手部轨迹横移，手指动作结束时焦点落到眼睛。

[Shot 4 | 7.000–10.500] 低仰全身，连续完成「旁提—拧身—双臂云手—侧身探掌」四段舞句，动作由腰胯发起，手臂延迟跟随；两脚只做点步、并步和原地轴心换向，不向前后走位。

[Shot 5 | 10.500–13.201] 低仰中全身，双臂上举形成圆弧，随后分开成一高一低的斜线，胸口打开，头随上手方向最后转到位；以动作余势进入下一段。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG09｜01:34.999–01:45.760｜质询与停顿中的细节

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 10.761 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.300] 低仰中全身。C1 提沉起势短句，含胸、沉肩、手臂沿中线收拢；吸气时脊柱提起，双手停在胸前，保持重心居中。

[Shot 2 | 2.300–4.300] 切脸部近景，眼神先向一侧移动，再回到正前方；眉眼轻微收紧后松开，不张口、不对歌词做口型。

[Shot 3 | 4.300–6.500] 切手部特写，左手托住右腕下方，右手兰花指由合到开，腕部完成一圈小盘腕；动作在重拍落定。

[Shot 4 | 6.500–8.600] 低仰全身，做原地「虚步点地—拧腰—回身半转」：点步脚尖触地后收回，腰胯带动上身旋转，双臂沿身体两侧画弧，结束时面向三分之四方向。

[Shot 5 | 8.600–10.761] 空镜一拍后直接切低仰半身，她将手臂缓缓收回身体中线，肩部释放，眼神稳定；不做走动或新姿势停摆。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG10｜01:45.760–01:56.941｜温柔回忆感与重新收束

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 11.181 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.500] 低仰中全身。以柔和 C2 云手起句，双臂胸前横向交替画圆，重心轻轻左右虚实交换；身体位置固定。

[Shot 2 | 2.500–4.500] 切手部近景，手背经过脸侧但不遮住双眼，掌心向外翻开，指尖柔和延伸；镜头从手指切到眼神，不改变人物外观。

[Shot 3 | 4.500–7.000] 低仰全身，接 C5 拧倾出胯亮相的柔化版本：腰胯先拧、胸肩跟随，单臂斜上延展、另一臂回收到胸前，膝部微屈形成古典舞弧线；原地完成。

[Shot 4 | 7.000–9.200] 短暂空镜，只用参考图中既有空间局部做焦点转换；镜头不引入任何新物件或场景。

[Shot 5 | 9.200–11.181] 回低仰中全身，双手从胸前穿掌向外分开，随后收回至腰侧；眼神由柔软转为清醒，手臂末端保留余势。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG11｜01:56.941–02:11.163｜两难冲突与身体对抗

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 14.222 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.800] 低仰全身。建立稳定弓步但不移动脚位，前腿承重、后腿伸展；骨盆与胸腔反向拧转，双臂一前一后拉开对抗线。

[Shot 2 | 2.800–5.500] 接「大涮腰」的安全站姿变体：双膝保持弹性，腰部从一侧向前下方画弧再回到另一侧，胸腔和双臂依次跟随，头部最后通过；不做极限后仰。

[Shot 3 | 5.500–8.500] 低机位全身持续拍摄「穿掌—背转前—开臂」链：一手经面前横磨，另一手穿掌翻腕；以原地轴心转身短暂背对镜头，双臂交叉下沉，再回到正面打开。

[Shot 4 | 8.500–10.500] 切脚步近景，支撑脚压实，后脚脚尖点地并回收，膝盖吸收惯性；镜头同步短促横移并停住。

[Shot 5 | 10.500–14.222] 低仰全身，完成一组有力量的「沉身—双臂下切—提身—斜向展臂」舞句，重拍在双臂最大展开时命中；保持原地，末尾手臂回收形成下一段入口。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG12｜02:11.163–02:25.044｜由封闭转向舒展

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 13.881 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.700] 低仰全身，接前段手臂回收，双手在胸前交叠，腕部翻转后向两侧穿出；肩胛先动、肘部随后、指尖最后完成。

[Shot 2 | 2.700–5.400] 做 C2 云手横八字完整一轮：一臂上撩一臂下沉，随后交换，胸前形成连续横向双圆；腰胯轻微左右移重，脚底不离开原地。

[Shot 3 | 5.400–7.500] 切手部与侧脸近景，手掌沿面侧经过，眼神从手背后方显露；镜头小幅横移，焦点从手指转到眼睛。

[Shot 4 | 7.500–10.700] 低仰全身，接 C16 的盖步转身简化版：一脚原地盖步建立轴心，骨盆先转、胸肩随后，双臂经脸前交叉下沉，再向外打开；转身不超过半圈，完成后仍回到原位置。

[Shot 5 | 10.700–13.881] 低仰全身稍近，完成「旁提—探掌—收腕—展臂」连续舞句，双臂从胸前绕出高低线条，身体中轴逐渐挺拔，动作持续到切段。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG13｜02:25.044–02:38.485｜Hero 2：掖腿转单圈与开臂制动

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 13.441 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–1.500] 低仰全身，建立掖腿转准备。双脚收至稳定轴心，承重脚掌压实，膝部柔和预载；自由腿脚尖沿支撑腿内侧收至掖腿位置，双臂在胸前合拢，头部定点。

[Shot 2 | 1.500–4.300] Hero 启动与旋转：支撑脚掌推地并沿轴心完成一次完整 360° 掖腿转；骨盆先转，胸腔和肩线依次跟上，双臂保持紧凑控制转速，头部清晰留头找点。摄影机低位短弧跟随，不自行绕满一圈。

[Shot 3 | 4.300–6.600] Hero 峰值与制动：双臂在转到正面时有控制地打开，膝部吸收惯性，自由脚落地并稳定；镜头保持完整全身，不切碎技术动作。

[Shot 4 | 6.600–8.500] Hero Lock：开臂成斜向长线，胸腰提起，眼神定向；保持短促重拍，衣袖只保留自然惯性。

[Shot 5 | 8.500–11.300] 释放进入 C2 云手和 C16 穿掌组合：双臂横向交替画圆，随后一手穿掌翻腕、另一手收至胸侧；双脚原地小幅换重，不走位。

[Shot 6 | 11.300–13.441] 切手腕近景，再回低仰半身；手腕完成最后一次外翻，肩线松开，身体保留顺势转向的下一段入口。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG14｜02:38.485–02:51.927｜迎风感由舞蹈张力呈现，不行走

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 13.442 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.500] 低仰全身，固定表演点。以原地「虚步点步—并步—提沉」建立节奏，双臂从身侧向上撩起，肘部柔弯，手腕最后翻开。

[Shot 2 | 2.500–5.500] 接 C3 立圆托举与 C2 云手：一臂沿立圆升至头顶，胸腰提起；另一臂低位横向穿过，双臂随后交换高低，形成连续的空间圆弧。镜头低位侧前短弧移，人物不移动。

[Shot 3 | 5.500–7.000] 空镜短切，镜头只从 Picture1 既有空间元素中选取局部虚实与光影，不新增环境内容；以运动方向匹配下一镜手臂轨迹。

[Shot 4 | 7.000–10.500] 低仰全身，做「原地沉身弓步—大涮腰—双臂顺风旗线」：两脚固定成稳定弓步，腰部由侧向前下画弧再提起，一臂斜上、一臂斜后形成长线；身体不向前冲、不跨场移动。

[Shot 5 | 10.500–13.442] 继续双臂云手绕顶，手腕先行、肘部跟随，最后双臂从头顶两侧分开成高低错落的展开姿态；摄影机随高位手臂向上摇，最后落回低仰全身。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG15｜02:51.927–03:03.647｜高潮余势与节奏变化

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 11.720 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.500] 低仰全身，接上一段高低臂线，双臂沿圆弧收至胸前，手腕交叠后再次穿出；脚下原地并步、点步，不向任何方向行走。

[Shot 2 | 2.500–5.300] C2 云手横八字加速一轮，随后接 C5 拧倾亮相：腰胯先拧，胸肩跟上，双臂一高一低展开，重拍短锁；摄影机横移并在重拍同步停住。

[Shot 3 | 5.300–7.300] 切面部近景，头随动作方向轻转，目光重新落定；镜头固定，不推拉。

[Shot 4 | 7.300–9.700] 低仰全身，做「原地平转半圈—双臂开合—回身穿掌」：轴心清楚，转动一次完成，双臂先收后开制动，避免多圈旋转。

[Shot 5 | 9.700–11.720] 脚步与手部交叉特写：支撑脚压地，另一脚尖点地回收；切回全身，双手从胸前缓缓分开，动作不停。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG16｜03:03.647–03:15.368｜Hero 3：高位延展与稳定释放

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 11.721 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–1.500] 低仰全身，Hero 预备。双脚原地建立支撑，重心明确移至主力腿，膝部柔和屈曲；双臂向两侧打开形成反向平衡，胸腔提起。

[Shot 2 | 1.500–3.600] Hero 启动：动力腿从地面沿身体后侧抬起，骨盆保持稳定，支撑腿向上伸展；躯干从髋部向前延长，双臂分别向前与后方拉开。动作不是踢腿摆拍，必须由支撑脚、骨盆和躯干共同控制。

[Shot 3 | 3.600–5.400] Hero 技术峰值：进入可控的 Attitude / Arabesque 高位延展线，后腿抬至稳定高度，膝部保持自然弯曲或延伸的清晰舞姿，胸口打开，头部顺前臂方向延伸。完整全身持续可见，摄影机低位小弧移但不遮挡支撑脚。

[Shot 4 | 5.400–6.500] Hero Lock 与制动：重拍锁定，支撑腿稳住，手指延伸；随后动力腿有控制地下落，骨盆回正，双臂柔和回收。

[Shot 5 | 6.500–8.600] 接原地 C1 提沉与 C3 立圆托举：双臂从低位沿立圆升起，脊柱逐节提起，随后向两侧打开，表现释放后的身体舒展。

[Shot 6 | 8.600–11.721] 低仰全身回到稳定站姿，双手沿胸前穿掌后自然落于身体两侧；不走动、不新增动作道具。摄影机从屋面高度轻抬至低仰中全身，结束时保持人物仍有细微呼吸与衣袖余动。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

### SEG17｜03:15.368–03:27.520｜尾奏：舞蹈回收与人物状态完成

```text
subject_definitions:
<Subject 1> is exactly the person in <Picture 1>. <Picture 1> is the sole authority for every visual attribute of the person and the entire scene. Preserve it unchanged; do not restyle, redesign, add, remove or reinterpret any visual element. The subject performs alone, empty-handed, in the same fixed position.

integrated_multimodal_description:
A photorealistic cinematic Chinese classical-dance MV segment, vertical 9:16, exact duration 12.152 seconds. Use <Picture 1> as the locked visual reference and <Audio 1> as the exact soundtrack. The lyrics are abstract emotional context only, never literal shot instructions. The performer does not sing or lip-sync. She remains within one fixed performance footprint for the entire segment: no walking, no traveling, no approaching or retreating, no crossing the rooftop or changing location. Use connected classical Chinese dance movement, clear weight mechanics and low-angle photography.

[Shot 1 | 0.000–2.500] 空镜短句，画面只取 Picture1 已有的环境元素与光影层次；镜头缓慢横移，不添加新的景物或道具。

[Shot 2 | 2.500–5.500] 低仰全身。人物双脚保持原位，做一组柔和 C1 提沉：含胸沉肩后逐节提起；双手从腰侧缓缓上托，呼吸平稳。

[Shot 3 | 5.500–8.000] 切手部近景，双腕做最后一组小幅盘腕与翻掌，指尖逐一舒展；镜头顺手臂摇到侧脸，眼神稳定自然。

[Shot 4 | 8.000–10.200] 低仰全身，双臂完成一次缩小版云手横八字，随后交叠收回胸前，再自然分落两侧；脚下不迈步、不改变站位。

[Shot 5 | 10.200–12.152] 回到与开场相呼应的低仰全身构图。她以稳定中轴、放松肩线和自然呼吸完成最后收势；只保留微小衣袖余动，画面保持到音频结束，不加片名或淡黑。

The same Picture 1 visual world remains unchanged. No additional props, handheld objects, weapons, fans, ribbons, water sleeves, scrolls, jade objects, extra people, costume changes, appearance redesign, new scenery, magical additions, text, subtitles, dialogue, lip-sync or sound effects. Do not replace choreography with walking or static posing.

overall_soundscape:
N/A — preserve <Audio 1> exactly. Add no dialogue, ambience, footsteps, cloth foley or sound effects.

non_diegetic_music:
N/A — <Audio 1> is the only soundtrack. Preserve this exact local slice, including original vocal, arrangement, beat placement and timing. Do not regenerate, remix, retime, stretch, restart or carry audio from another segment.
```

---

## 四、全片连续性与生成自检

1. **图1锁定**：是否只使用 Picture1 的人物与环境，没有重画外貌、服装、灯光、建筑或背景？
2. **无走动**：是否全片固定在同一表演点？所有脚步是否仅为原地点步、盖步、并步、重心交换或轴心转身？
3. **舞蹈密度**：每段是否有多条可读的古风动作链，而不是站立、走路或空镜填时长？
4. **动作库调用**：是否实际使用提沉、云手、穿掌、立圆、拧倾、点步翻身、掖腿转、探海与高位延展等动作结构？
5. **Hero 完整性**：SEG07、SEG13、SEG16 是否都有预载、动力传递、峰值、锁定、制动和回收的完整全身呈现？
6. **镜头服务动作**：仰拍为主，特写有信息价值；没有用脸部推拉、无目的环绕或特写剪碎技术动作。
7. **不逐字拍歌词**：没有因歌词名词新增道具、人物、动作或场景。
8. **段间接力**：每段结尾保留下一段可接续的手臂方向、重心状态或轴心方向；切段不要求重新站好或重新起势。
9. **音频准确**：17 段均沿用原始 JSON 时间窗与对应 Audio1 局部切片，不重新起拍、不跨段重启。

**最终导演原则：** 这是南宫阙在 Picture1 中完成的一支原地古风舞蹈 MV。图1决定“她是谁、在哪里、长什么样”；动作库决定“她如何舞”；音乐决定“何时发力”；导演决定“镜头如何让舞蹈变得有层次”。不走路，不添物，不重画图1，不把歌词拍成插画。
