# 舞蹈动链 H3 库(可重复学习的动作链标准件) · Rev.1.4

> **版本记录**
> Rev.1.4|2026-10-30|新增 K 章「2026-10-30 批量反推动链扩展库」:15 支新片+2 张姿势参考图、74 条动链(K1-K74)经 video-to-h3-prompt 流水线反推并入(双人支撑拉伸/saber 技术下腰/3DCG 舞台变装/情绪撩发写真/吸血鬼写真/腿脚微动作/双人对镜甜舞/K-pop 群舞/卡点换装/AIGC 摆拍等);每片附背景人物档案+节拍判定+镜头形态分流;其余章节与使用规则不变
> Rev.1.3|2026-10-09|使用规则新增第 9 条「时间窗动作链完整性规范」(强制前置检查:五规则+动作设计五步逻辑+时间窗容量表+失败诊断四情况+逐窗验收十项);第 8 条十条自检不变
> Rev.1.2|2026-10-09|自检清单替换为用户定稿十条(运镜流程/物理机位/动作库优先/同步时间码/动作峰值/节奏连续/转场钩子/段自包含/视觉一致性/最终排错);第7条同步规则不变
> Rev.1.1|2026-10-09|使用规则新增第 7 条「舞蹈动作×摄影机运镜实时 1:1 同步」六原则+三条统一口诀,并新增第 8 条「生成前自检清单」(12 项,含同步六查+双系统+段结构);运镜流程(E 章)、拍摄角度设计(I 章)、重要经验(同步规则)列为每次生成前必复习项
> Rev.1.0|2026-10-07|新增 I 章物理摄影机视角案例库(25 类视角物理定义规范,用户提供的写法标准全文并入)+J 章写真式姿势-运镜章(J0 母语言十律+J1 母模板+J2-J10 九支实测范本,视角描述全部物理化改造);E5 末加"完整规范见 I 章"引用,E7 末加"视角词进提示词按 I 章改写"纪律;H 章范本 1 处 "slight low angle" 物理化;版本机制自本版建立,此前历史见 git log
> 来源:四支参考舞反推(《双倍可爱》甜系宅舞、《宅舞vs抖舞》左右分屏、《与你提酒》逍遥古风、《皇上》宫廷古风)。
> 每条动链 = 一个 2-8 拍的完整编舞单元,带**入态/出态**,可像积木一样首尾相接拼成整支舞。
> 英文描述均可直接粘贴进 H3 提示词;拍位为**相对拍**(链内第几拍),可放到任何 BPM 网格上。
> H 章 = 13 支单人成品范本(2026-10 并入):整段提示词可直接粘贴套用,H0 为从范本提炼的成品规律。
> K 章 = 2026-10-30 批量反推动链扩展(15 支新片+2 图,74 条):每片带背景人物档案+节拍判定+镜头形态分流,风格覆盖双人支撑/技术动作/写真微动作/宅舞/K-pop/AIGC 摆拍。

## 0. 使用规则

1. **三层结构写进每段提示词**:持续层(全段恒定:宅舞=内八膝弹跳;抖舞=胯八字;古风=提沉呼吸)+ 动链层(本段选用的链,逐拍)+ 微表情层(反拍的头/眼/手指)。
2. **对接**:上一链的出态 = 下一链的入态。拼接时在 H3 里写一句出态描述(如 `landing with weight on her right leg, right hand at chest height`)。
3. **密度**(实测基准):宅舞每 8 拍 2-3 条链 + 2 拍定格;快板古风每 8 拍 4-6 动;慢板古风每 8 拍 1-2 动,用呼吸/眼神/裙摆余动填充。
4. **旋转预算**:整支舞 ≤2 次;**静止必须明写**("holds one beat of stillness" 落在具体 downbeat),否则模型匀速化。
5. **镜头**:切点落在乐句收点或造型高点,切在动作中必须 match-on-action;可爱手势半径收在肩宽内,扩展类才超肩宽;头部是"最小的鼓",动作频率高于手臂。
6. **动作链十要素标准(两个反推 skill 统一,源自 all-around-dance-choreographer/action-library)**:每条链必须写全`动作状态 → 受力来源 → 进入路径 → 逐拍动力变化 → 技术峰值 → 惯性延续 → 回收顺序 → 身体/服装物理 → 镜头几何 → 音乐触发`——H3 必须先知道"人是怎么动起来的"(进入路径/支点/轴线/重心/角动量/恢复路径),禁止退化成"动作名+形容词"(如只写"做一个 720°旋转")。旋转补轴线与角动量,地板动作补进入/回收路径,跳跃补起跳蹬地与落地吸收,裙摆/袖/长发补延迟物理。
7. **舞蹈动作 × 摄影机运镜实时 1:1 同步(最高优先级经验,每次生成前必复习)**:运镜不是舞蹈完成后的装饰,而是与舞者在同一真实时间里共同运动的摄影机。六原则:
   - **同时启动**:人物开始动作,摄影机同一时刻开始响应;
   - **同步运动**:人物移动、伸手、转体、跳跃时,摄影机同步跟拍或改变机位;
   - **峰值同步**:手指伸展、旋转到位、脚步落地等动作强调点,与镜头构图强调点同时发生;
   - **同步恢复**:人物收势、回中或反向运动时,摄影机同步减速、回移或改变方向;
   - **连续衔接**:上一动作的恢复直接进入下一动作,不插入无意义的停顿或延迟运镜;
   - **绝对时间码**:每段明确写出人物动作与摄影机运动共享的起止时间。
   统一口诀:**一套时间码、两条同步运动轨迹、同一组动作峰值**。落地写法:每个 onset 的时间戳同时是身体峰值时间戳和相机响应时间戳;相机块写 MOVEMENT TRIGGER 时必须引用与本段动作链相同的时间码。
8. **生成前自检清单(用户定稿十条,每次输出提示词前逐项过,任何一项不过即修改后再交付)**:
   - [ ] 1. 运镜流程:已复习运镜设计流程,镜头运动服务于舞蹈和叙事。
   - [ ] 2. 物理机位:已明确摄影机类型、位置、高度、距离、朝向、倾角及运动路径。
   - [ ] 3. 动作库:优先使用已有动作库中的可靠动作,舞蹈不是静态 pose 集合。
   - [ ] 4. 动作与运镜同步:人物动作和摄影机运动共用同一套精确绝对时间码,1:1 同步。
   - [ ] 5. 动作峰值:伸展、发力、跳跃、旋转、落地等关键节点与镜头构图同步到位。
   - [ ] 6. 节奏与连续性:动作真正踩拍,重心转换自然,相邻动作无缝衔接,不靠慢走换位。
   - [ ] 7. 转场钩子:每段结尾具有明确的动作、视线或身体方向钩子,能够接续下一段。
   - [ ] 8. 每段自包含:每个独立 Segment 都写入必要的公共规则、画面约束和完整音频/BGM描述。
   - [ ] 9. 视觉一致性:锁定 Picture 1 的人物身份、服装、环境和视觉世界,避免背景漂移与身份混合。
   - [ ] 10. 最终排错:检查重复人物、额外角色、碎片化画面、无意义运镜、动作重复和不必要静止。
9. **时间窗动作链完整性规范(TIME-WINDOW ACTION-CHAIN INTEGRITY,强制前置检查,生成前必执行)**:
   - **核心原则**:先确定时间窗能完成什么动作,再安排动作细节、音乐重拍和同步运镜;禁止先堆高级动作再把它们硬塞进过短时间窗。抱臂反复摇晃、原地抖动=窗口过载的失败信号,不能靠加"高级/强力/流畅/Hero"形容词修复。
   - **五规则**:①一个时间窗必须有完整的动作结果(起始状态/动力来源/动作传递/主要重拍/动作完成/自然回收,不许只列动作名让 H3 猜连接) ②时间决定动作容量(不足时减少动作数量/简化连接/延长窗口,绝不硬塞) ③每个动作有明确完成时刻(不拖进下一窗,不用循环摇晃填时长) ④运镜不能挤占舞蹈时间(与人物共用时间轴:动作启动相机启动/重拍构图峰值/收势相机减速) ⑤高级 Hero 动作分配完整运动过程(如 720°=轴心建立/蓄力/连续旋转/定点/减速/回收,可跨相邻窗连成连续 Hero 链,不可压进不足窗口,不可只写"旋转720°")。
   - **动作设计五步逻辑**(设计与检查逻辑,非每动作占五窗):①建立支撑与预载(哪脚承重/重心去向/身体准备向哪转——预载是动作的一部分,不是空等) ②明确动力传递(支撑脚/重心→骨盆→胸腔→肩→肘→腕→指尖,不必过全关节但动力源必须可信) ③到达唯一主要重拍(一个最重要可见结果:肘部斜切完成/旋转到位/双臂打开/掌心翻转;摄影机同时达对应构图) ④完成回收与制动(吸收惯性/手臂回收/支撑脚稳定/相机同步减速——不能只完成前半段) ⑤给下一动作留明确入口(终态自然产生下链起始动力,不是突然重新站好)。
   - **时间窗容量表**(初始估算,真实速度/BPM/节拍位置/难度共同决定):
     | 时间窗 | 适合的设计 | 主要风险 |
     |---|---|---|
     | 0.3-0.6s | 一个明确短促重拍(肘部切分/胸腔冲击/腕部翻转) | 塞完整多步链导致动作丢失 |
     | 0.6-1.2s | 一条完整短链(重心交换→躯干转向→手臂释放) | 同时要求太多独立方向变化 |
     | 1.2-2.5s | 一条结构清晰复合舞句(动力传递+主动作+收势) | 罗列太多动作,模型只执行一部分 |
     | 更长 | 复杂舞句或分阶段 Hero 动作 | 无中间目标,原地重复或拖延 |
     反例:不能写"02.600-05.200:交叉手臂/侧弓步/两次肩击/180°旋转/手腕绕环/双臂打开/回收"——2.6s 完成不了,尤其还要求真实重心与运镜配合。可靠写法:挑一条有清晰完成点的主链,按音乐决定合并或独立窗口。
   - **失败诊断四情况**:A 抱臂来回摇晃多次=动作无明确完成点或窗口负荷过高→删重复腕/肩/抱臂描述,指定唯一一次交叉绕臂(从哪个方向开始/何时切开/落在哪个身体方向),下一动作与释放后状态衔接;B 写 720° 实际只转一点或一直打转=旋转预算/动作阶段/结束状态不明或窗口不足→写死支撑脚与旋转轴/一次连续双周旋转/完成时刻/定点方向/减速方式,窗口太短先调整时间分配或减少周围动作,不用重复旋转补时长;C 动作很多但没有舞句=列表无动力传递与因果→选定一条主舞句(侧弓步承重→骨盆反向→胸腔展开→肘部切线→手腕释放→回收),删掉不服务这条链的额外动作;D 人物动作完成但运镜拖后=摄影机被写成独立任务或重拍时刻不清→运镜与动作共用时间窗,用同一动作的启动/峰值/回收控制摄影机,不另加动作结束后的推近或环绕。
   - **逐窗验收十项**(交付前每个时间窗过):时间窗容量(动作数量复杂度适配秒数)/动作完整性(明确开始/主要结果/完成状态,不拖下窗)/动力学因果(支撑脚→重心→骨盆→躯干→肩肘腕传递顺序)/唯一动作结果(一个主重拍,不重复摇晃)/Hero 动作预算(旋转跳跃复合动作有独立足够时间,蓄力展开制动合理)/音乐时序(完成点对应实际重拍,未验证拍点不冒充已验证)/同步运镜(相机启动/构图峰值/恢复与身体共用时间窗,不额外占用舞蹈时间)/转场入口(结束状态为下一动作提供身体方向和动量)/反重复检查(无抱臂反复摇晃/原地抖动/反复摆同一手势)/生成后可判定(能据生成视频判断动作是否完成/卡点/重复,而非只凭观感)。未通过的窗口先重写,不直接输出为最终提示词。
   - **执行标准一句话**:在给定时间里,模型必须有足够清晰且可执行的指令,把动作从起始状态完整带到明确的完成状态。高级舞蹈不是动作名称越多越好,而是在合理时间内完整完成高质量动作链,并让摄影机恰好捕捉到动作的形成、重拍与释放。

---

## A. 宅舞动链(甜系 idol)

### A1 内八弹跳待机链(2拍循环|万能底)
- 入态:任意站姿 → 出态:开立内八、膝弹跳中
- 分解:每拍——双膝内扣下沉半拍、回弹半拍;重心在双脚球上;手臂随拍自然下沉
- H3:`standing feet apart with knees bent inward pigeon-toe, a continuous small knee bounce on every beat, weight on the balls of both feet, arms relaxed at her sides`
- 来源:《双倍可爱》12.5s/17s/29s/43s 反复出现的"默认待机状态"

### A2 猫爪颤肩链(4拍|萌)
- 入态:A1 出态 → 出态:双手回到脸侧,弹跳保持
- 分解:拍1 双手屈肘抬至肩侧、五指张开成猫爪拳心朝前;拍2 快速耸肩一次(半拍抖动);拍3 换双肩再耸;拍4 膝内扣颤膝一下、下巴微收
- H3:`elbows out at shoulder height, fists beside her face with spread fingers in cat-paw, quick shoulder shrugs on the half-beats while her knees tremble inward`
- 来源:《双倍可爱》16.5-17.5s

### A3 双拳交替冲链(4拍|元气,半拍accent)
- 入态:双拳收于胸前 → 出态:双拳收回胸口
- 分解:拍1 左拳前冲(半拍)→拍1.5 右拳前冲→拍2 左→拍2.5 右;拍3 双拳收胸、膝内扣弹跳两下;拍4 重复一遍半拍双冲
- H3:`pumping small alternating fists forward at chest level, one punch per half-beat, then gathering both fists back at her chest with two bouncy knee knocks`
- 来源:《双倍可爱》42-43.5s

### A4 拼心歪头链(2拍|镜头pose)
- 入态:双臂自然 → 出态:心形手在胸口,头向一侧歪定住
- 分解:拍1 双手拇指食指在胸口拼出心形;拍2 头向拼心方向歪、眼看来头,定住
- H3:`forming a heart shape with both thumbs and index fingers at chest level, tilting her head toward the heart, holding the pose for one beat`
- 来源:《双倍可爱》26.5s

### A5 敬礼歪头链(2拍|萌)
- 入态:任一手位 → 出态:一手在额头侧,头歪
- 分解:拍1 一手收至额头旁做敬礼状;拍2 头向同侧歪、眨眼感,定住
- H3:`snapping one hand to her forehead in a little salute, head tilting to the same side with a wink-timed hold`
- 来源:《双倍可爱》27.5s

### A6 V字踮脚收束链(4拍|乐句尾)
- 入态:任意 → 出态:双脚并拢落地,双臂落下
- 分解:拍1-2 双臂从体侧画弧举成斜上 V、同时踮起脚尖;拍3 并脚小跳双脚微离地;拍4 落地双臂落下收势
- H3:`raising both arms into a V overhead while rising on tiptoes, then a small jump landing feet together as her arms float down`
- 来源:《双倍可爱》15-16s

### A7 侧平指顶胯链(2拍|扩展类)
- 入态:开立 → 出态:重心回到中位
- 分解:拍1 一手水平侧指至最远、同侧顶胯、另一手叉腰;拍2 收回中位弹跳
- H3:`extending one arm sideways to its full reach with a finger point while the same-side hip pops out, then snapping back to center`
- 来源:《双倍可爱》14s

### A8 提裙展示链(2拍|半拍accent,含安全裤展示变体)
- 入态:双臂在体侧 → 出态:裙摆回落、双手离裙
- 分解:拍1 双手捏住裙摆向两侧微撑、膝盖内弯半蹲(半拍下沉);拍2 松手让裙摆回落、起立弹跳
- **安全裤展示变体**(2拍,小跳版):拍1 屈膝小跳、顶点双手抓裙摆两侧向外下翻,裙成钟形、安全裤外露一拍;拍2 落地屈膝缓冲、裙摆自然回落、双手离裙、下巴微抬看来头
- H3(标准):`gathering the skirt hem with both hands and dipping on the half-beat with knees knocking inward, then flicking her wrists outward as she rises`
- H3(展示变体):`a small vertical hop at the apex of which both hands catch the skirt hem and flick it outward and downward, the skirt lifting in a clean bell shape with the safety shorts flashing for one beat, landing softly as the skirt settles`
- 来源:《宅舞vs抖舞》11.5s;展示变体为《爱你》SEG05 定制

### A9 原地快速转体链(2拍|裙摆飞)
- 入态:面向镜头 → 出态:面向镜头,裙摆刚落、头发刚飞完
- 分解:拍1 单脚为轴起转(留头);拍2 转完精准收正面、裙摆甩开头发飞起、双臂打开 Landing
- H3:`a fast full spin in place on one foot, skirt flaring outward and hair flying, landing facing the camera exactly on the beat with arms opening`
- 来源:《双倍可爱》22s

### A10 并脚小跳后踢链(2拍|轻盈)
- 入态:弹跳中 → 出态:回到 A1 待机
- 分解:拍1 双脚微离地小跳、小腿向后勾、双臂外开;拍2 落地回弹跳
- H3:`a small jump with both feet leaving the floor, heels kicking back, arms opening sideways, landing softly back into the bounce`
- 来源:《双倍可爱》35s

### A11 叉腰戳镜头链(2-4拍|第四面墙)
- 入态:任意 → 出态:一手叉腰一手收回
- 分解:拍1 一手叉腰;拍2 食指向镜头戳一下;拍3 再戳一下(头随拍歪);拍4 收手回弹跳
- H3:`one hand on her hip while the index finger of the other hand pokes toward the camera twice, her head tilting with wink timing`
- 来源:《双倍可爱》36.5s solo

### A12 背手点脚定格链(2拍|可爱定格)
- 入态:任意 → 出态:回到弹跳
- 分解:拍1 双手背到身后、一脚向前交叉点脚尖;拍2 头向点脚侧歪、两拍可爱定格
- H3:`clasping her hands behind her back with one toe crossed forward in a point, head tilting to the side in a two-beat cute hold`
- 来源:《宅舞vs抖舞》左屏 99-102s

### A13 展袖开臂链(2拍|开场常用)
- 入态:双臂体前交叉 → 出态:双臂侧平举、提踵落回
- 分解:拍1 双臂在体前低位交叉;拍2 向两侧划弧"展袖"打开、同时提踵
- H3:`crossing her arms low in front, then sweeping them open to both sides like unfolding sleeves as she rises on her toes`
- 来源:《宅舞vs抖舞》左屏 10-12s

### A14 头顶比心 8 拍招牌链(8拍|全曲记忆点)
- 入态:任意 → 出态:合掌于胸
- 分解:拍1-2 双臂从体侧抬起;拍3-4 双臂在头顶合拢比出心形、定住;拍5-6 保持、胯随拍轻摆;拍7-8 双手合拢落至胸前、膝内扣小跳两下
- H3:`raising both arms overhead to form a heart, holding the shape while her hips sway gently on the beats, then bringing her palms together at her chest for two small hops with knees knocking inward`
- 来源:《宅舞vs抖舞》左屏 139s/144s(8 拍一次的重复招牌)

### A15 X 交叉水平展臂链(2拍)
- 入态:任意 → 出态:双臂侧平
- 分解:拍1 双臂胸前交叉成 X;拍2 水平展开到两侧
- H3:`crossing her arms into an X at chest level, then spreading them wide and horizontal`
- 来源:《宅舞vs抖舞》左屏 57.5s

### A16 叉腰定格链(8拍|pose→hold 型,全带出入态)
- 入态:双手收拳于腰侧,面向镜头 → 出态:双手背后+内八字站
- 分解:拍1 双手叉腰+双脚开跳与肩同宽,&下巴快点▲;拍2 重心左顶胯上身微左倾;拍3-4 定格(头部每拍小点);拍5 双手滑至腹前交叠;拍6 双手背到腰后;拍7-8 脚跟并拢内扣、头歪 15° 停满 2 拍
- H3:`hands snap to hips with a jump-out stance, chin-flick accent on the and, hip pop left, two-count freeze with head nods, slide hands behind back, pigeon-toe head-tilt hold`
- 来源:《宅舞vs抖舞》加密版 97.5-102s

### A17 猫爪框脸链(8拍)
- 入态:站姿双臂垂 → 出态:开立手垂
- 分解:拍1 双手举至头侧垂腕成猫爪+左膝内扣点地,&双腕抖动▲;拍2 猫爪保持换右膝内扣;拍3 右爪斜上推,&左手收下颌;拍4 双手收至脸颊框脸;拍5-6 定格框脸、头左右各歪;拍7 双臂打开成 V;拍8 垂落回正面
- H3:`cat-paw bent wrists beside head with knee-in pops, wrist-shimmer accent, one paw pushes diagonally up, frame the face, hold with alternating head tilts, open to V and drop`
- 来源:《宅舞vs抖舞》加密版 181-186s

### A18 拳托腮镜像链(8拍)
- 入态:站姿双臂垂 → 出态:双拳托腮并腿(可直入 A19)
- 分解:拍1 右拳收至下颌下肘外抬、左膝内转,&肘部上颠▲;拍2 重心移左脚右脚尖点地;拍3-4 定格头右歪;拍5 镜像换左手;拍6 保持;拍7-8 双拳同托下颌、双肘外开、并腿定格
- H3:`fist tucks under chin with elbow flared and knee turned in, elbow-bounce accent, two-count hold, mirror to the other side, double-fist chin pose freeze feet together`
- 来源:《宅舞vs抖舞》加密版 183.5-185.5s

### A19 下蹲猫爪起身雨刷链(8拍)
- 入态:站姿(或接 A18) → 出态:站直手于脸侧
- 分解:拍1 屈膝下蹲双手收至胸前成猫爪,&蹲底抖肩▲;拍2 蹲位保持双爪前挠 2 次;拍3 起身双臂向左上挥;拍4 向右上挥(雨刷摆);拍5 双臂头顶大绕环一周;拍6 绕环落回胸前;拍7-8 站直定格手在脸侧比型
- H3:`drop into a squat with chest-level paw hands, shoulder-shake accent, scratch twice at the bottom, rise with windshield-wiper arm sweeps, one big overhead circle, land in a face-side pose`
- 来源:《宅舞vs抖舞》加密版 187-189.5s

### A20 叉腰点地侧伸链(8拍)
- 入态:站姿 → 出态:开立叉腰(可直入 A16)
- 分解:拍1 左手叉腰、右腿直腿点出、右手贴右大腿,&点地回弹▲;拍2 收腿并步头回正;拍3 镜像左侧;拍4 收;拍5 双手叉腰开立左顶胯;拍6 右顶胯;拍7-8 定格开立叉腰、下巴 1 点
- H3:`hand on hip with side toe extend and rebound accent, mirror side, hip pops left-right, freeze wide with a chin nod`
- 来源:《宅舞vs抖舞》加密版 190-192s

### A21 背手交叉脚定格链(8拍|A12 的满拍版)
- 入态:任意站姿 → 出态:开立手垂
- 分解:拍1 双手滑到背后;拍2 右脚跟提起向左脚交叉半步;拍3-6 定格 4 拍(仅拍4、拍6 各一次头部小歪);拍7 右脚弹回开立、小跳弹▲;拍8 双手回体侧
- H3:`hands glide behind back, heel crosses in, four-count statue hold with only two head tilts, pop back to stance with a bounce accent`
- 来源:《宅舞vs抖舞》加密版 99-103s

### A22 头顶交叉戳脸链(8拍)
- 入态:开立 → 出态:框脸定格(可接 A17)
- 分解:拍1 双臂头顶交叉指尖上伸,&向上顿挫▲;拍2 向左侧屈体;拍3 向右侧屈体;拍4 回正;拍5 双手下降框脸;拍6 双手食指戳脸颊;拍7-8 定格戳脸 pose
- H3:`arms cross overhead with a stretch-and-punch accent, side bends left-right, hands descend to frame the face, double cheek poke, hold`
- 来源:《宅舞vs抖舞》加密版 72-76s

### A23 九十度鞠躬收尾链(8拍|段落终/片尾)
- 入态:末段定格后任意站姿 → 出态:收尾 pose
- 分解:拍1 双臂向体侧打开 45°;拍2 上身前倾 90° 鞠躬头低;拍3-4 保持躬身;拍5 起身回正;拍6 双手腹前交叠;拍7-8 站定收尾定格
- H3:`arms open to sides, deep ninety-degree bow, two-count hold, rise, hands fold in front, end pose`
- 来源:《宅舞vs抖舞》加密版 237.8-238.6s(双侧同步收尾)

---

## B. 抖舞动链(高能 flow)

### B1 胯部八字引擎(持续层|可垫在任意链下)
- H3:`a constant hip figure-8 engine: knees pulsing in and out while the hips swing side to side on every beat, never stopping`
- 来源:《宅舞vs抖舞》右屏全程

### B2 刺拳对侧踢链(4拍|每拍1动)
- 分解:拍1 左刺拳+右腿前踢;拍2 右刺拳+左腿前踢;拍3-4 重复,前脚掌轻
- H3:`throwing alternating straight-arm punches forward with opposite-leg front kicks, one per beat, light on the balls of her feet`
- 来源:《宅舞vs抖舞》227-229s

### B3 深蹲撑膝→波浪起身链(4拍|level change)
- 分解:拍1-2 跳落宽站深蹲、双手撑膝;拍3-4 起身身体波浪+单臂前滚
- H3:`dropping into a deep squat with hands braced on knees, then rising through a body wave with a forward arm roll`
- 来源:《宅舞vs抖舞》231-234s

### B4 甩腕手花+胯8字链(2拍|半拍accent)
- H3:`rapid flower-hand wrist flicks beside her shoulders layered over a hip figure-8`
- 来源:《宅舞vs抖舞》145-146s

### B5 单腿立转链(2拍)
- H3:`a spin on one leg with both arms in a high V, the other knee bent, landing in a wide stance`
- 来源:《宅舞vs抖舞》95-97s

### B6 开合跳落宽站链(2拍)
- H3:`a jumping-jack hop landing into a wide stance, arms swinging down then back up into a V on the next beat`
- 来源:《宅舞vs抖舞》226s

### B7 邀请式翻掌链(2拍|半拍accent)
- H3:`flipping both palms up in an inviting gesture while popping her hip to the same side`
- 来源:《宅舞vs抖舞》150-151s

### B8 错位身体波浪链(4拍)
- H3:`a body wave with one arm up and one arm low, staggered, traveling down through her torso`
- 来源:《宅舞vs抖舞》146-148s

### B9 抖肩膝内扣链(2拍|半拍accent)
- H3:`shimmies her shoulders left and right while her knees knock together, hands loose at hip level`
- 来源:《宅舞vs抖舞》236s

### B10 中位摆掌交替沉膝链(4拍)
- H3:`hands waving side to side at mid-torso while the knees alternate deep dips, a pendulum-like bounce`
- 来源:《宅舞vs抖舞》141-143s

### B11 屈膝弹动底座链(8拍|持续层,可与其它抖舞链并行叠加)
- 入态:开立略宽于肩膝微屈 → 出态:弹动不停(底座)
- 分解:拍1 膝弹下-上、胯左顶,&右胯回顶▲;拍2 镜像;拍3-4 重复+双肩交替上提;拍5-8 循环、双臂随 bounce 体侧自然甩
- H3:`relentless knee-bounce groove, hip pops alternating on every half-beat, shoulders lifting in opposition, loose swinging arms`
- 来源:《宅舞vs抖舞》加密版 181-191s 全程底层

### B12 绕腕波浪链(8拍)
- 入态:B11 进行中 → 出态:双手甩至体侧、律动继续
- 分解:拍1 右腕内绕一圈收至胸前,&指尖弹出▲;拍2 左腕内绕;拍3 双腕同时外绕;拍4 双手向两侧甩开五指张开;拍5 右手托腮瞬间;拍6 换左手;拍7 双手向上腕波浪;拍8 甩腕落下
- H3:`alternating inward wrist rolls to chest, flick accent, double outward rolls, fling hands open, quick cheek touches, overhead wrist wave and drop`
- 来源:《宅舞vs抖舞》加密版 182-186s

### B13 交替冲拳滚动链(8拍|半拍双速)
- 入态:开立弹动 → 出态:开立手垂弹动中
- 分解:拍1 右拳向前滚出左脚小踏,&拳到最远点抖▲;拍2 左拳滚出;拍3-4 双拳交替加速至每半拍 1 拳;拍5 双拳同时前推;拍6 收拳拉回腰间挺胯;拍7 双臂上开成 V;拍8 落下续 bounce
- H3:`rolling alternating punches with in-place steps, double-time punches on every half-beat, double push, pull back with hip thrust, open V`
- 来源:《宅舞vs抖舞》加密版 226.6-228.6s

### B14 宽站砸胯斜压链(8拍)
- 入态:双脚大步分开约 1.5 肩宽 → 出态:宽站手侧开
- 分解:拍1 重心砸向左、左臂向左下斜切压,&胯撞到位▲;拍2 重心拉回双臂抬平;拍3 镜像右;拍4 回中;拍5-6 重复幅度加倍、头跟随切的方向;拍7 双臂体前大交叉;拍8 向两侧猛甩开
- H3:`weight slams side to side with diagonal arm presses hitting the half-beat, doubled second pass, big arm cross then fling wide`
- 来源:《宅舞vs抖舞》加密版 228-230.5s

### B15 下蹲起身体波链(8拍)
- 入态:弹动中 → 出态:站立弹动
- 分解:拍1 体波从胸向下传上身前拱;拍2 下沉入深蹲双手拂过膝盖;拍3 蹲底 bounce 2 次;拍4 顶胯起身手沿腿滑上;拍5 站直瞬间挺胯前顶▲;拍6 胯画半圆收回;拍7 双臂上举随浪;拍8 甩落
- H3:`body roll down into a deep squat, double bounce at the bottom, pelvic-thrust rise with hands gliding up the legs, arm wave overhead and fling down`
- 来源:《宅舞vs抖舞》加密版 233-235.5s

### B16 旋转甩臂链(8拍|正反两圈)
- 入态:弹动中 → 出态:面向镜头开立
- 分解:拍1 右脚踏步启动左臂上抬引领;拍2 顺时针全身转 360° 双臂展开,&转身中段加速▲;拍3 转完面向镜头双臂甩开;拍4 bounce 缓冲 1 拍;拍5 逆时针再转 360°;拍6 甩臂;拍7 并步;拍8 定点弹动
- H3:`step to wind up, full spin with arms flung open, land facing camera, reverse spin, settle into the bounce`
- 来源:《宅舞vs抖舞》加密版 103.5-105.5s、189.5-190.5s

### B17 点肩扭胯小步链(8拍)
- 入态:开立 → 出态:手在胯侧弹动
- 分解:拍1 左脚向左小步、右手拍左肩、左胯顶,&胯二次顶▲;拍2 右脚并步手收;拍3 镜像;拍4 并步;拍5-6 step-touch 连续左右、双手交替点肩;拍7 双手从肩滑到胯侧;拍8 双胯画圈一周
- H3:`step-touch side to side tapping opposite shoulders, hips popping every half-beat, hands slide down to hips, one hip circle`
- 来源:《宅舞vs抖舞》加密版 98-100s

### B18 急停胯顶收势链(8拍|段尾)
- 入态:flow 收速(段尾) → 出态:段落定格→下段换装淡入(或直入 A23 鞠躬)
- 分解:拍1 右脚向侧一大步、右胯猛顶出▲;拍2 左手叉腰、右臂上举过头垂腕;拍3 定格胯保持顶出,&快速抖胯 2 次▲;拍4-5 保持;拍6 头歪向举手一侧;拍7-8 hold 至段落结束
- H3:`big side step with hip thrust, one arm up with bent wrist, hold with a double hip-jiggle accent, head tilt to finish`
- 来源:《宅舞vs抖舞》加密版 238-238.6s

---

## C. 古风动链(身韵)

### C1 提沉起势链(4-8拍|所有古风的呼吸引擎)
- 入态:静立/跪坐 → 出态:立直、气提、目视前
- 分解:拍1-2(沉)含胸低头、呼气;拍3-4(提)节节抬头挺腰、吸气;可循环
- H3:`her chest rounding and head dropping on the exhale, then lifting head and spine vertebra by vertebra on the inhale, breath-led undulation`
- 来源:《皇上》00:04-06;《提酒》提沉贯穿全片

### C2 云手横八字链(4拍|平圆)
- 入态:立/背身 → 出态:双臂一上一下
- 分解:拍1-2 左臂上撩右臂下落;拍3-4 交替,双臂在胸前连成横八字;重心随环左右移
- H3:`both arms tracing a continuous wide horizontal figure-eight at chest height, one arm lifting as the other sinks, her weight swaying with the loop`
- 来源:《提酒》18-20s

### C3 立圆托月链(4拍|立圆+下胸腰)
- 分解:拍1-2 单臂从体前沿立圆撩至头顶;拍3-4 上胸腰节节后弯、头后仰看手,"托月"定住
- H3:`one arm sweeping upward in a vertical circle overhead while her upper back arches in a slow chest-lift, head releasing back to gaze at the raised hand`
- 来源:《提酒》6-9s;《皇上》00:10-13 坐姿云手同族

### C4 遮面-停-露眼神链(4拍|欲遮还露三段式)
- 入态:手持扇/手背在脸侧 → 出态:眼神已露、手停在脸侧
- 分解:拍1-2 扇(手)掩面、定住 2 拍;拍3-4 缓缓拉开露出眼神、另一腿后点步立半脚尖
- H3:`covering her face with the folding fan, holding for two beats, then slowly sliding it aside to reveal her eyes while one leg points back on demi-pointe`
- 来源:《提酒》32-34s、46-49s(两次)

### C5 拧倾出胯亮相链(2-4拍)
- 分解:拍1-2 拧腰 45°、出胯、一手斜上指或叉腰;拍3-4 定住亮相,头随拧方向
- H3:`twisting her torso 45 degrees with the hip pushing out on the accent, one arm extended diagonally, holding the posed line`
- 来源:《提酒》40s;《皇上》行进穿手转后

### C6 圆场碎步行进链(4拍|可位移)
- 分解:拍1-4 碎步快速小步行进(向镜头/侧向),双臂体侧小幅画圆或持道具定式;上身平稳
- H3:`traveling in tiny quick gliding steps, arms circling small and low at her sides, upper body calm and level`
- 来源:《提酒》11-14s、102-106s

### C7 平转甩发链(2-4拍)
- 分解:拍1 留头起转;拍2 甩头收;可接连续 2-3 个平转行进,裙摆横扫
- H3:`a single-foot traveling turn with head spotting, then a whip turn with the hair snapping around, the long skirt flaring into a horizontal disc`
- 来源:《提酒》44-46s、100-102s;《皇上》00:44

### C8 连环平转高潮链(8拍|全片唯一高潮,放 70% 进度处)
- 分解:拍1-2 起转;拍3-6 连续 3-4 个快平转走小弧线,双臂一开一合驱动;拍7-8 急停面向镜头、双臂胸前交叉猛然打开、亮相定住
- H3:`a chain of three to four fast pivot turns traveling in a small arc, arms alternately folding and opening to drive the spin, long hair flying horizontal, ending in a hard stop facing camera with arms snapping open from a chest cross`
- 来源:《皇上》00:58-01:04

### C9 坐姿后弯-提沉还原链(8拍|地面慢板)
- 分解:拍1-4 坐姿双手体后撑地、胸腰节节后弯成桥、头全仰发落地;拍5-8 吸气节节还原
- H3:`seated backbend: hands planted on the floor behind her hips, her spine arching vertebra by vertebra until the head drops all the way back, then gathering back up with an inhale`
- 来源:《提酒》81-87s

### C10 跪坐起身撩臂链(4拍)
- 分解:拍1-2 由跪坐双臂向两侧撩开画大弧(展袖);拍3-4 连身带臂立起成跪立、头后仰
- H3:`rising from sitting to a tall kneel while both arms sweep wide arcs from the floor to overhead like unfolding water sleeves, chin lifting`
- 来源:《皇上》00:18-21

### C11 地面段链(8拍|俯卧/仰卧/侧卧)
- 变体 a 俯卧举腿:`lying prone with both legs raised straight up and ankles crossed, arms in a T on the floor, slowly scissor-swaying the legs`(《皇上》开场)
- 变体 b 仰卧后撑举腿:`lying supine propped on both hands behind, one leg extending straight to vertical while the other scissors slowly`(《提酒》64-67s)
- 变体 c 俯卧眼镜蛇:`propping up on her forearms with one leg bending up behind, chest arching like a cobra toward the light`(《提酒》70-74s)
- 密度:每 8 拍 1-2 动,用呼吸/发丝/裙摆余动填充

### C12 静态平衡链(4拍|宫廷感"稳")
- 分解:拍1-2 立半脚尖、动力腿前吸腿、双臂过高举、仰头定住;拍3-4 缓落
- 变体(后吸腿展翅):背身双臂大张、后腿吸成 attitude、立半脚尖前倾定格
- H3:`rising onto demi-pointe with the free knee drawn up in front, arms crossing high overhead, chin lifted, holding the balance for two beats`
- 来源:《皇上》00:41-44、01:12-14

### C13 掩口托腮叙事链(2-4拍|给谁看)
- 分解:拍1-2 兰花指缓缓抬至掩口(或托腮)、眼含笑看来头;拍3-4 手落下、头回正
- H3:`her right hand with orchid-finger curvature floating up to cover the lips, eyes smiling toward the camera, then the hand floating down`
- 来源:《皇上》00:21、01:16

### C14 托腮定格收势链(2-4拍|终止式)
- 分解:拍1-2 向一侧轻倾、右手抬至腮边掩面、歪头浅笑;拍3-4 定格(淡出)
- H3:`a slight body lean, the right hand cupping her cheek, head tilted with a coy smile toward the camera, holding still as the shot holds`
- 来源:《皇上》结尾 01:16-17.5

### C15 弓步甩臂出画链(2-4拍|终止式·位移)
- 分解:拍1-2 低弓步沉、持道具手向外甩;拍3-4 裙摆横扫、沿斜线出画
- H3:`dropping into a low lunge with one final arm swoosh, the skirt sweeping wide, exiting the frame on a diagonal`
- 来源:《提酒》110-112.5s

### C16 云手穿掌·背转前链(10拍)
- 入态:背身双臂上扬 → 出态:面向镜头、手交叉胸前
- 分解:拍1-2 右手领云手经面前向左横磨;拍3-4 穿掌翻腕、左脚盖步;拍5-6 左轴转身上步背转前;拍7-8 双臂经脸前交叉下沉;拍9-10 开手落位
- H3:`Cloud-arm sweep across the face, thread-palm turnover, a back-to-front step turn, arms cross and sink at the chest.`
- 来源:《提酒》6-12s

### C17 撩袖背身涮腰扫扇链(10拍)
- 入态:持扇胸前站立 → 出态:正身持扇脸侧
- 分解:拍1-2 双手撩袖+右转身背对镜头;拍3-4 背身大涮腰(腰走右→下→左)、扇随腰贴地划弧;拍5-6 涮至左上位胸腰打开;拍7-8 螺旋拧转回身;拍9-10 收扇正身
- H3:`Sleeve-flick turn to back view, a full waist-circle sweeping the fan through a floor-level arc, spiral back to front.`
- 来源:《提酒》16-22s

### C18 后踢碎步上行走月链(8拍)
- 入态:开扇亮相(画面右) → 出态:背身展臂望月
- 分解:拍1-4 碎步+两次后踢小腿走向月亮正下方(背身纵深向上);拍5-6 双臂展翅张开;拍7-8 仰头望月定住
- H3:`Light skip-runs with back-flick kicks travel upstage to the moon, wing-spread arms, a moonward gaze hold.`
- 来源:《提酒》28-33s

### C19 下场大涮腰·翻身盖扇链(7拍)
- 入态:望月背身 → 出态:正身持扇站立
- 分解:拍1-2 右脚撤步下蹲、扇自右上向左下贴地扫;拍3-4 涮腰经前向上;拍5-6 拧仰翻身、扇盖过头顶;拍7-8 收扇起身
- H3:`Lunge into a right-to-left floor-sweep, the waist-circle continues up through front, a cover-fan arc overhead, gather and rise.`
- 来源:《提酒》33-37s

### C20 沉跪即起·举杯吸腿平衡链(9拍)
- 入态:持扇站立 → 出态:扇在脸侧
- 分解:拍1-2 双手举扇过顶("举杯"式)、快速沉跪即起;拍3 右腿前吸绷脚;拍4-6 平衡停留扇在头顶;拍7-9 落腿、扇落经脸侧
- H3:`A two-hand cup-raise overhead, front-attitude lift, hold the balance, lower the fan past the face.`
- 来源:《提酒》40-45.5s

### C21 遮面碎步逼近·残影链(8拍|破第四面墙)
- 入态:扇在脸侧 → 出态:近景左前方
- 分解:拍1-4 扇遮面、碎步向镜头方向横移;拍5-6 两次后勾脚点步;拍7-8 逼近至近景占比(转体帧叠半透明残影特效)
- H3:`Fan-covered-face sneaking walk toward the lens with two back-flick taps; a translucent echo-double trails the spin frames.`
- 来源:《提酒》45.5-50.5s;残影只挂转体帧

### C22 落扇亮相·回身甩发链(4拍)
- 入态:近景遮面 → 出态:背身中位
- 分解:拍1-2 落扇、正面微笑亮相;拍3-4 回身背对+大甩发、碎步退回中后区
- H3:`Drop the fan for a front-facing smile reveal, whip away with a hair flick, scamper back upstage.`
- 来源:《提酒》50.5-53s

### C23 侧弓步横拉臂→举杯链(7拍)
- 入态:背身退回中后区 → 出态:站立双手举扇
- 分解:拍1-2 右侧弓步、左臂贴地平拉;拍3-4 重心提起;拍5-7 双手举扇过顶成举杯式
- H3:`Side lunge with an arm skimming the floor, then rise pulling the fan overhead in a two-hand toast.`
- 来源:《提酒》53-57s

### C24 跪落拜月·跪转·贴地扫扇链(8拍)
- 入态:站立举扇 → 出态:跪坐后仰举扇
- 分解:拍1-2 沉气屈膝跪落、扇经面前落下;拍3-4 跪转一整圈(裙摆铺开+残影);拍5-6 扇贴地横扫;拍7-8 跪坐伸右腿、双手举扇上身向后仰(斟酒式)
- H3:`A breath kneel as the fan lowers past the face, one full kneeling spin with the skirt fanned wide, a ground-sweep, then a seated arch raising the fan like pouring a toast.`
- 来源:《提酒》57-62s

### C25 坐地遮面涮腰链(7拍)
- 入态:跪坐伸腿 → 出态:坐地扇在前
- 分解:拍1-2 上身左拧、扇遮面;拍3-4 坐姿涮腰、双臂横向摆;拍5-6 扇指斜上前伸;拍7-8 收拢
- H3:`Seated twist with the fan at the face, lateral arm swings riding a seated waist-circle, a diagonal reach, gather.`
- 来源:《提酒》62-66s

### C26 后撑翻躺·仰卧举腿链(5拍)
- 入态:坐地 → 出态:仰卧举腿
- 分解:拍1-2 双手后撑、双腿抬离地;拍3-4 向左翻身落躺;拍5 双腿上举划圈
- H3:`Support behind and lift the legs, roll over the hip to lying, circle the raised legs.`
- 来源:《提酒》66-69s

### C27 地面滚转链(19拍|俯卧↔仰卧交替)
- 入态:侧卧 → 出态:侧卧伸腿
- 分解:拍1-2 滚成俯卧;拍3-6 右腿后高举两次、肘撑抬头看镜头;拍7-10 回滚仰卧、单腿竖举;拍11-14 再滚回俯卧大抬腿;拍15-16 双腿并拢竖举;拍17-19 缓落侧卧
- H3:`A floor-roll cycle: prone with high back-leg lifts and elbow-prop gaze to camera, roll to supine single vertical leg, roll back prone, finish both legs vertical then lower to side-lying.`
- 来源:《提酒》69-80.5s

### C28 侧卧→跪→立起身链(12拍)
- 入态:侧卧 → 出态:站立举扇
- 分解:拍1-2 收腿推地坐起;拍3-4 跪撑起身成跪立;拍5-6 跪立展胸涮臂;拍7-8 单膝蹬地起立;拍9-12 俯身捡扇举过顶
- H3:`Gather from side-lying to kneel, a chest-opening sweep on the kneel, press up to standing, reclaim the fan and lift it overhead.`
- 来源:《提酒》80.5-88s

### C29 吸腿平转 2-3 圈链(7拍)
- 入态:站立举扇 → 出态:正对镜头站立
- 分解:拍1-2 吸腿立半脚尖;拍3-6 连续平转 2-3 圈(裙摆飞起);拍7 收步正对镜头定住
- H3:`Relevé with a lifted knee into two or three skirt-flying spot turns, close and stop on the front.`
- 来源:《提酒》88-92s

### C30 敬月举杯·碰杯离场链(16拍|终止式)
- 入态:正对镜头 → 出态:全场无人→空镜
- 分解:拍1-2 直线走向镜头举扇(敬观众);拍3-6 摇扇退步回身(残影);拍7-10 走至月亮下、右臂持扇举向月牙(敬月)、左手扶腰;拍11-12 转向镜头再举扇(碰杯);拍13-14 微欠身;拍15-16 从画面左下走出画
- H3:`Walk to the lens raising the fan like a toast, retreat with a fan waggle, raise the fan to the crescent moon, pivot to the viewer for a farewell clink, a small bow, then exit frame-left past the lens.`
- 来源:《提酒》92-111.5s(结尾 6.5s 空镜月亮收尾)

### C31 发幕遮脸坐起→甩发露脸链(3拍)
- 入态:俯卧单腿朝天 → 出态:侧坐拧身目视镜头
- 分解:拍1 双手压地、右腿外划落地、躯干垂直盘起;拍2 长发垂成整幅黑幕完全盖脸;拍3 头自左向右平绕甩发、发横扫露侧脸
- H3:`She presses both palms down and spirals up to sit, long hair falling as a black curtain covering her face, then whips her head right so the hair flings off in a wide horizontal arc revealing a profile glance to camera.`
- 来源:《皇上》00:04-06.5

### C32 侧卧高踢绷脚 120° 链(1拍)
- 入态:左侧卧展臂 → 出态:侧卧高踢定(全片地面最高点)
- 分解:拍1 右腿直膝上踢至约 120°、绷脚背、右掌按地、脸转向镜头
- H3:`Lying on her side she kicks one leg to 120 degrees with pointed toes, opposite palm pressing the floor, face turned to camera.`
- 来源:《皇上》00:08.5-09.5

### C33 坐姿平转甩发链(1拍)
- 入态:侧坐望指 → 出态:转回近正坐
- 分解:拍1 头带动上半身原地横甩一周(坐姿平转)、长发水平扫出满弧、裙裾翻飞
- H3:`From a side sit, head leads a full seated horizontal spin, long hair sweeping a full arc, skirt flipping with the turn.`
- 来源:《皇上》00:14-15.5

### C34 背身渐升双臂链(2拍|蓄势留白)
- 入态:背对站立走位中 → 出态:双臂至最高点(接终段转体)
- 分解:拍1-2 背对走位中双臂一拍一拍抬至头顶最高点
- H3:`From back view, both arms rise slowly overhead to the highest point, then drop into a final spin with the skirt's last flare.`
- 来源:《皇上》66-72s

### C35 五圈行进连环平转链(8.5拍|高潮,C8 强化版)
- 入态:叉腰拧胯走步 → 出态:背对站、发落定
- 分解:拍1 提膝走步拧胯叉腰;拍2-4 连续行进平转约 4-5 圈、头点甩定位、发横飞、裙平展、行进路线走浅弧(中左→中中→中右);拍5 末圈甩发接蹲转沉重心
- H3:`Four traveling chain pirouettes with head spotting, arms wrapped at the waist, skirt flaring on each rotation, ending back to camera.`
- 来源:《皇上》50-58.5s

---

### C36 落袖遮面亮相链(4拍|遮挡→揭示家族)
- 入态:袖/伞/纱遮面 → 出态:正面亮相+粒子铺陈
- 分解:拍1-2 遮面定住(伞/袖/纱皆可,含背影态);拍3 遮挡物落下或移开、正脸显露;拍4 粒子(花瓣/火花/金屑)随亮相炸开、定住
- H3:`a sleeve (or paper umbrella) veils the face and holds, then drops away to reveal the face as a burst of petals and sparks scatters, settling into the pose`
- 来源:《绝世舞姬》21.7-23.1(伞遮面→落伞+金屑)、26.6-30.5(背影纱帘→回眸)
- 家族:C22 落扇亮相的同族放大版;"遮挡→揭示"是混剪核心转场

### C37 裙摆开花平转链(4拍|大裙摆旋)
- 入态:开立蓄力 → 出态:裙摆收、面向镜头
- 分解:拍1 蓄力下沉;拍2-3 连续平转 2-3 圈、裙摆大幅张开如花(俯角微仰拍最出效果);拍4 收裙定住
- H3:`two to three fast spins with the oversized skirt flaring into a full flower shape, then gathering to a stop facing camera`
- 来源:《绝世舞姬》13.8-18.3(夜雾白裙/紫裙三连旋)

### C38 坐地吸腿高举链(2拍|地面高位腿)
- 入态:坐地/半仰 → 出态:腿落、回正
- 分解:拍1 坐地(或半仰撑地)一腿竖直高举至 120°+、绷脚;拍2 缓落或换边
- H3:`seated on the floor, one leg rising straight to a 120-degree vertical hold with pointed toes, the other leg extended along the floor`
- 来源:《绝世舞姬》5.0-6.9;C32 侧卧高踢的坐地族

### C39 下腰成桥链(4拍|深后弯)
- 入态:站立背对或侧对 → 出态:起身回正
- 分解:拍1-2 下腰成桥(双手或单手撑地、胸腰全开);拍3 单臂向远端延伸、指尖最远;拍4 收腹起身
- H3:`arching back into a deep bridge with one hand planted, the opposite arm reaching to its farthest point overhead, then curling back up`
- 来源:《绝世舞姬》30.5-31.8

### C40 下腰后抬腿链(2拍|站下腰变体)
- 入态:开立 → 出态:回正
- 分解:拍1 后下腰、一腿向后抬起;拍2 收回回正;户外大场景低机位仰拍最出效果
- H3:`arching back into a backbend with one leg lifting behind, then recovering to stand`
- 来源:《绝世舞姬》18.3-21.0

### C41 水平控腿下腰链(4拍|探海变体·高难)
- 入态:开立 → 出态:回正
- 分解:拍1-2 后下腰同时一腿向后抬起至水平(与地面平行控住);拍3-4 控 2 拍缓收
- H3:`arched back with one leg extended and held perfectly horizontal, a controlled attitude promenade hold, then recovering`
- 来源:《绝世舞姬》70.2-72.8;探海系 LINE Hero 的站姿变体

### C42 侧翻链(1-2拍|胆量动作)
- 入态:助势侧对 → 出态:落定亮相
- 分解:拍1 侧手翻/侧空翻过(裙装飘飞);拍2 落地接亮相;旋转帧可挂残影
- H3:`one acrobatic side aerial through the air, dress flaring, landing into a pose`
- 来源:《绝世舞姬》33.1-34.5(薄荷裙侧翻)

### C43 跪滑起身链(4拍|地面→立)
- 入态:站立 → 出态:立定手上举
- 分解:拍1-2 跪地滑步前冲(膝滑);拍3 起身手上举(可持伞旋转);拍4 定住
- H3:`sliding forward on both knees, then springing up with arms sweeping overhead into a held shape`
- 来源:《绝世舞姬》76.0-77.0、39.9-41.0(花瓣跪滑)

### C44 跪转螺旋链(4拍|跪姿旋)
- 入态:跪坐 → 出态:跪坐回正
- 分解:拍1-4 跪姿螺旋转(手弧在头顶或胸前引领、身体随之旋绕),目随手动
- H3:`a kneeling spiral turn, the hand's arc leading and the torso winding around it, eyes following the hand`
- 来源:《绝世舞姬》36.9-39.9

### C45 平转甩袖链(2拍|速度模糊)
- 入态:持袖/披帛 → 出态:袖落
- 分解:拍1-2 快速平转、长袖/披帛横向甩出成模糊圆;夜景+微仰拍最出效果
- H3:`fast spinning with the long shawl whipping out into a blurred circle around her, motion trails visible`
- 来源:《绝世舞姬》13.8-15.5(夜滨紫裙)

### C46 大跳展袖链(2拍|空中造型)
- 入态:助跑/蓄力 → 出态:落地屈膝缓冲
- 分解:拍1 大跳腾空、双袖向两侧完全展开(空中 T/斜线);拍2 落地缓冲接亮相
- H3:`a grand jump mid-air with both long sleeves fully spread to the sides, landing softly into a pose`
- 来源:《绝世舞姬》12.8-13.8(红亭大跳)、45.1-47.6(袖裹跳)

### C47 背身渐行链(转场走位|不回头)
- 入态:亮相毕 → 出态:出画或切入下一镜
- 分解:背身向远方渐行、fabric 随风、不回头;镜头静止在背后或缓慢跟随;用于段落收尾/转场
- H3:`walking away from the camera in a straight line, fabric trailing in the wind, never looking back`
- 来源:《绝世舞姬》34.5-36.2(红伞过桥背身)

### C48 开弓放箭链(4拍|武侠 Hero)
- 入态:侧身持弓 → 出态:放箭后随势收臂、目送箭出
- 分解:拍1 侧身举弓搭箭;拍2 开弓满弦、后手拉至颊侧、前臂伸直、沉肩;拍3 满弦定半拍(呼吸停顿);拍4 松后手放箭、弓臂回弹、眼神随箭送出
- H3:`side stance drawing a bow to full draw, anchor hand to the cheek, one held breath at full draw, then release — string snapping forward, bow arm recoiling softly, eyes following the arrow out`
- 来源:《绝世舞姬》47.6-48.2(竹林绿衣开弓)|注:箭的飞行是可选 VFX,只写"release+目送"即可成立

### C49 屋檐飞跃链(4拍|武侠 AIR,空中切镜)
- 入态:檐上蹲蓄 → 出态:落到下一檐、fabric 慢半拍落下
- 分解:拍1 蹲蓄摆臂;拍2 蹬檐跃出、空中四肢大展、fabric 全开;拍3 滞空 Apex;拍4 落下一檐、膝吸收;**切镜点=滞空顶点,下镜直接接落点**(空中切是转场不是动作失败)
- H3:`leaping between rooftops, arms and fabric fully spread at the apex of the jump, cut mid-air, landing on the next roof with knees absorbing`
- 来源:《绝世舞姬》49.7-50.5(金殿夜景飞跃)

## D. 多人宅舞动链(2-4人配合)

> 多人纪律(合并自三份报告):①人数是常量 token(每段重复 `exactly four dancers`,禁写 "a group");②先锁机位再写队形(首句 `locked tripod wide shot, full bodies visible`);③队形用几何槽位(`L/C/R four slots`、`2x2 grid`),不用相对关系;④一次转换一个语法(转身 XOR 聚拢 XOR 横移 XOR 让位),配否定约束 `no position change, turn in place`;⑤**动者与静者必须显式声明**(`front row crouches while back row holds`);⑥层次显式写(`one crouches while three stand`);⑦齐-分-齐交替(连续两段 full-sync 后强制 split/canon);⑧接触配合写死接触点与承重(`three partners catch and cradle`);⑨半拍 accent 用具体部位落地(`sharp hair whip on the off-beat`);⑩solo 预算花在结尾;⑪同向齐舞非镜像(远景读作一个生物);⑫Slot 锚定背景参照物。

### D1 立姿弹动合掌挥手(4拍|BLESSING)
- 分解:拍1 双膝弹动+双手体前合拢;拍2 单臂侧平举打开;拍3 收回胸前;拍4 头部左右轻点
- H3:`Four dancers bounce knees shoulder-to-shoulder, fold hands then wave one arm open.`|全员同步

### D2 屈肘拳交替上冲+斜指(8拍|BLESSING)
- 分解:拍1-2 双肘上提肩侧握拳、右拳上冲;拍3-4 左拳上冲;拍5 双臂前平举摊掌;拍6 左臂斜上指右手叉腰;拍7-8 收拳至胸+头部点两下
- H3:`Flexed fists at shoulders punching up alternately, flat-palm reach into a diagonal point with head-bob.`|全员同步

### D3 开合跳 V 字臂(8拍|BLESSING)
- 分解:拍1 跳开双脚双臂 V 上举;拍2 跳合臂落肩侧;拍3 跳开双臂侧平 T;拍4 收;拍5-8 重复、末拍加重下蹲弹
- H3:`Jumping-jack splits with arms blasting V-up to T-spread, closing each rep with a bouncy knee dip.`|全员同步、末拍重音

### D4 鸡翅膀肘交替(4拍|BLESSING)
- 分解:拍1 右肘上提外张左手叉腰;拍2 换左肘;拍3 双肘同时外张;拍4 双臂下甩+单腿提膝
- H3:`Chicken-wing elbows popping out one at a time, flaring together before dropping arms on a knee lift.`|全员同步

### D5 祝福三连(8拍|BLESSING 招牌)
- 分解:拍1 双臂侧平 T 指尖拉长;拍2 双臂上举手腕交叉成 X;拍3 合掌自面前下落至胸;拍4 胸前合掌微点头行礼;拍5-6 交叠步横移双臂水平扫;拍7-8 再开 T 向前两步
- H3:`Signature blessing combo — T-spread arms, cross wrists overhead into an X, draw prayer hands down to the chest with a small bow.`|全员同步、记忆点(副歌复现)

### D6 兔耳手顶胯(4拍|BLESSING)
- 分解:拍1 双手举至头侧比兔耳+右胯顶出;拍2 收手换左胯;拍3 双手绕头一圈;拍4 双臂下甩回体侧+小跳
- H3:`Bunny-ear hands by the head with side hip pops, circling arms overhead and snapping down.`|全员同步

### D7 逐人退场+滑步收尾(8拍|BLESSING 终止式)
- 分解:拍1 最右者转身向右跑出画;拍2 最左者蹲身向左滑出画;拍3-4 留守二人继续交替冲拳踏步;拍5 第三人跑出;拍6 末位向前滑步成弓步、直臂指镜头;拍7 起身高跑出画;拍8 空场
- H3:`Sequential breakout exit — dancers peel off running one by one, the last slides into a deep lunge pointing at camera then dashes off.`|轮替 solo、solo 预算花在结尾

### D8 菱形入场渐亮(8拍|うみたがり)
- 分解:拍1-2 暗场静止(一人深蹲低收三人立姿定格);拍3-4 灯起、左右两人手臂外翻甩出(半拍 accent);拍5-6 一人单臂上举斜切;拍7-8 蹲者起立全员踩点收胸
- H3:`Four dancers converge from a wide diamond into a tight huddle, one arm shoots straight up, then they scatter on the downbeat.`|波浪卡农

### D9 门形换位 gate swap(8拍|うみたがり)
- 分解:拍1-4 左对两人相向穿行交换位置、右对同时镜像;拍5-6 换位完成瞬间全部甩腕收拳(半拍 accent);拍7-8 向中心聚拢半步
- H3:`Two pairs cross paths like opening gates, clapping fists on the meet point, then reform as a new line.`|2+2 镜像

### D10 前折波纹立起 L→R 卡农(8拍|うみたがり)
- 入态:四人全部前折头朝下
- 分解:拍1 最左甩头立起;拍2 第二人;拍3 第三人;拍4 最右(半拍 accent);拍5-8 立起后依次双手胸前交叉下拍
- H3:`In a straight line, all four fold forward at the hip, then snap upright one by one left to right like a ripple, each with a sharp hair whip.`|L→R 卡农

### D11 多臂生物 creature(16拍|うみたがり)
- 分解:拍1-4 四人向中心收拢重叠(前一人可见、三人藏于身后,各人手臂从她身侧不同高度伸出呈扇面);拍5-12 手臂按"上→侧→下"次序逐一波浪挥动(半拍 accent)、整团缓步向镜头推进;拍13-16 整团旋转换面
- H3:`The group stacks into one column: front dancer visible, three hidden behind, arms fan out at different heights and wave in sequence like a many-armed creature.`|全团拟一人

### D12 茧式缠绕→解旋下腰+托扶终格(16拍|うみたがり)
- 分解:拍1-4 全员按序前折互相搭肩交叠成"茧"小幅旋转;拍5-8 缠绕收紧两人背对背折叠;拍9-12 反甩解旋、一人被拽出向后下腰、被同伴托背;拍13-16 逐个脱出散开。**终格变体**:三人托扶一人向后仰塌(三点承托)、灯缓暗至黑
- H3:`The clustered group folds over each other into a coiled knot, spins slightly, then unwinds as one dancer is swung out into a deep back-dip held by a partner.`|接触配合、写死承重

### D13 聚拢结→爆发(8拍|うみたがり)
- 分解:拍1-3 小碎步向中心聚成紧凑背对团;拍4 全团同步下蹲(半拍 accent);拍5 一人从团中直臂冲天而起;拍6-8 团散开
- H3:`Four dancers converge into a tight huddle, one arm shoots straight up, then they scatter on the downbeat.`|聚散

### D14 高抬腿行进军(8拍|うみたがり,三段复用)
- 分解:拍1-4 高抬腿原地踏+对侧直拳(每半拍一格);拍5-6 变侧向并步双臂横摆;拍7-8 其中一人原地全旋一周
- H3:`Four dancers march in place with high knees and alternating straight punches, every movement landing on a half-beat accent.`|全员同步

### D15 双层开场造型(8×2拍|向阳)
- 分解:3 人跪坐低排背身双手体后交握随拍耸肩点头;1 人站高台双臂 V 位大幅挥;第二个 8 拍幅度加大
- H3:`opening tableau: three girls kneel in a row facing away with hands clasped behind their backs, one girl stands on a raised step behind them with arms spread wide.`|3静1动+高低分层(高台=零成本 C 位)

### D16 收缩-绽放聚拢散开(8+8拍|向阳)
- 分解:前 8 拍双臂交替上挥+胸前击掌、碎步向中心聚成两层(前 2 半蹲后 2 错位站);后 8 拍前排双手头上交叉 X 造型、散开成菱形
- H3:`four dancers shuffle-step toward center into a tight two-layer cluster, front row crouches while back row stands offset, then bloom outward into a diamond.`|聚散+双层读法

### D17 箭头 C 位指脸(8×2拍|向阳)
- 分解:主 C 箭头顶点单手指向镜头/框脸;翼位同步侧点步半蹲;后 8 拍全员指天+收手拍胯
- H3:`arrow formation, lead girl at the apex pointing at camera, two wings do small side-toe-touch squats on the same beat.`|C 位大动作+翼位小动作的主次层

### D18 让位穿出独舞(8+8拍|向阳)
- 分解:前 8 拍碎步向中心聚拢;后 8 拍三人依次从副 C 身后/身侧穿出退向画外两侧、副 C 原地续做大动作独占画面(同时镜头推近);再下 8 拍成员从两侧回归穿插
- H3:`three dancers peel off through the center and exit to both frame edges, one featured dancer keeps dancing alone at center stage.`|3 让 1、动线交错不重叠

### D19 接力 solo roll call(8×3拍|向阳)
- 分解:每 2 拍轮换一人:当前主位者做大动作(原地 spin/踢腿/挥手),其余 3 人手背后定格;从左翼到右翼依次传递
- H3:`roll-call sequence: each dancer steps forward for a two-beat spin while the other three freeze with hands behind their backs.`|轮流做、其余静止

### D20 收尾链 spin-展臂-交叉-合掌(8×2拍|向阳)
- 分解:拍1-4 主 C 原地 spin 裙摆展开、其余 3 人双手体前交握定格;拍5-6 四人同时展臂大开;拍7 手腕头上交叉;拍8 合掌收于胸前+主 C 前突半步 freeze
- H3:`final chain: center girl does a solo spin with skirt flare while three girls hold still, then all four fling arms open, cross wrists overhead, and clap hands at chest into a freeze frame.`|1动3静→4人齐动→定格

### D21 群舞水袖波纹链(8拍|6-8人,长袖)
- 分解:全员横排持长水袖;拍1-2 前排蹲沉甩袖向下、后排同时向上抛袖;拍3-6 L→R 波纹逐对启动,袖浪如多米诺;拍7-8 全员袖卷收于胸前+沉膝
- H3:`six dancers in a line holding long water sleeves; sleeve waves ripple left-to-right in pairs — the front row slings sleeves down as the back row throws them up, ending with all sleeves coiled to the chest and knees sinking.`|D10 卡农的水袖版
- 来源:《绝世舞姬》64-66(夜水岸金楼多人水袖齐舞)

### D22 壁咚压墙互动链(5拍|2人剧情,第二人只出手)
- 分解:①发起者抓腕举过头顶压墙 ②上步贴近、身体压近 ③被压者头回眸过肩、侧脸看向镜头 ④发起者另一手抚发、指入发间 ⑤被压者顺势靠进墙、眼望镜头
- H3:`he catches her wrist and pins it against the wall above her head, steps in close; she turns her head back over the shoulder with a profile glance to the lens, his other hand slides into her hair, and she leans back into the wall accepting the hold, eyes on the camera.`
- 来源:壁咚 7.1s AI 实测(2026-10-04)|注:**第二人物只以手臂/手入画,永远不出脸**——省一个身份锚;镜头语法见 E9

---

## E. 运镜规划章(录舞镜头语法)

> **1:1 同步铁律(适用本章全部条目)**: 人物动作和摄影机运动共用同一套精确绝对时间码——同时启动、同步运动、峰值同步、同步恢复、连续衔接、绝对时间码;一套时间码、两条同步运动轨迹、同一组动作峰值。每个 onset 时间戳同时是身体峰值时间戳和相机响应时间戳。

### E1 十一条运镜纪律(出自 9 人团舞一镜到底实测,角度已按画中画实证修正)
1. 一镜到底时把"切"翻译成"景别跳变":中景↔极限大全景须 ≤2s 内完成,用运动模糊当转场(`whip-pan transition with motion blur`)。
2. 每个景别停留 ≥1.5s 再换挡。
3. 运镜起脚时机 = 动作收势/释放瞬间,绝不在动作顶点起脚(`start the camera move on the release beat, not the accent peak`)。
4. 大定点(hit)前 1.5-2s 提前跑位,**画框先于动作到位**(`frame arrives before the hit lands`)。
5. 地板动作=机位镜像:人蹲机蹲、人起机起(`pedestal down with the drop, rise with the recovery`)。
6. 向镜头推进的踢腿/位移动作:机器 Plant 定住,让动作走进镜头(`lock the camera, let the choreography hit the lens`)。
7. 换主角用一次到位的 Whip Pan,落点即新主角中心。
8. 队形展开时倒退 Pull Out,速度略快于展开速度,先到等舞者。
9. 队形横移用平行 Truck,步速=舞者步速,队形锁中轴。
10. **机位角度规律(画中画实证修正)**:全程低机位(膝-腰高度)、默认轻仰 5-15°;C 位特写仰角最大(15-25°);踢腿段仰拍最大;仅群像大全景回腰位近水平;**全片无俯拍**。("眼平默认"为误判——低角度仰拍才是这类录舞的核心质感。)落地手段见 E5:机位写成实物+位置(物理化),不写角度形容词,单机位不分屏。
11. 宽景收尾用 Static 缓停,运镜静止=全曲终止信号。

### E2 动作→运镜映射表(10 对)

| 舞蹈动作 | 运镜指令 |
|---|---|
| 单人定点 solo | Static → 缓 Push In |
| 成员接龙换人 | Whip Pan(落点=新人中心) |
| 散开成横排 | 倒退小碎步 Pull Out |
| 全员下蹲/起身 | 贴地 Pedestal Down/Up 同步镜像 |
| 前排 feature | Push In 至前排中景(膝上) |
| 全员 V 臂大定点 | 提前 1.5-2s 跑位的极限大全景 |
| 踢腿向镜头 | 腰位 Plant 静止 |
| 队形横移 | 平行 Truck 同速跟随 |
| 全员自转 | 半步后撤+横移避让 |
| 终点定格 | Static 缓停收尾 |

### E3 切点与转场规律(双人宅舞 17 镜实测)
- 切点普遍吸附重拍 onset:乐句收点/动作收点/换人点,从不切在动作半途;
- **副歌可 8 小节一刀不切**——靠队形对称+动作幅度撑画面;
- solo 轮替=快切呼吸口(1-2s),并给 solo 者换纯色底(人物色标化:观众不看脸也知道镜头主角);
- **软转场(叠化)只给亲密段**——头靠头等接触动作配叠化+更近景,规则本身就是情绪信号;
- 白闪三连可用于段落转场;终段长镜头+定格延至曲终,不再切。

### E4 单镜头长舞不无聊(5 条,古风 77-118s 实测)
1. 写"高度层剧本":地面段→起身链→站立段,用高度变化代替切镜(一次起身=一次隐性切镜);
2. 每 8-12s 单变量重置一次:横移一格或翻转朝向,绝不同时写位移+转身;
3. 甩发/转体当软切点,写在段落边界(`hair whip as a visual reset`);
4. 静-爆两极:开头结尾各留 3-4s 绝对静止,全片只给一次连续多圈转体,其余单发;
5. 动感外包给服装物理(发、裙、纱)与地面反光,提示词禁写镜头运动词;走位调度表用九宫格(上/中/下 × 左/中/右)+高度层(地面/跪/立)描述。

### E5 特殊机位写法:机位物理化(单机位,绝不分屏)

病根:`camera at floor level tilted up 10-15°` 这类"镜头形容词"会被 H3 平均成"稍微低一点"。有效写法(实证)是**把机位写成场景里的物理事实——机位 = 一件有位置的东西**,单机位即可,不做双视角/分屏:

1. **机位=实物+位置**:不说"低机位仰拍",写"一台手机平放在她脚边的地板上,镜头离地约 5-15cm,朝正上方仰拍她"(`a smartphone lying flat on the floor at her feet, lens about 5-15cm above the ground, pointing sharply upward at her`)。俯拍同理挂到高处实物(天花板支架/二楼栏杆/柜顶)。机位一旦是"东西",就无法被平均掉。
2. **写出该位置的画面几何**:地面机位=地面贴近镜头、她高耸在镜头上方、站直时身后出现天花板、抬膝/踢腿向镜头逼近(`she towers over the lens, the floor close to the lens, the ceiling visible behind her, strong upward geometry and foreshortening`);俯拍机位=地面占满画面、身体强烈前缩、她抬头看进镜头。
3. **四连否定排除退化**(必带):`NOT an eye-level camera tilted upward / NOT a waist-height low shot / NOT a tripod-mounted cinema camera / NOT a crop or a digital zoom`——点名禁止模型的偷懒退化。
4. **透视用物理因果**:写死 `all enlargement in the frame comes from real spatial perspective, not digital zoom`;她靠近/越过镜头→自然放大变形;机位本身全程固定不动。
5. **仰角由物理关系自带,不写度数**:"lens on the floor pointing sharply up at her" 自带极端仰角;"tilted up 10-15 degrees" 这种度数写法会被吃掉。
6. **角度模板速查**:
   - 仰拍:phone flat on the floor at her feet, lens 5-15cm above ground, pointing sharply upward at her
   - 侧面仰拍:phone on the floor beside her, lens near the ground, pointing up along her profile
   - 俯拍:camera mounted high (ceiling rig / upper-floor railing / top of a cabinet), looking steeply down at her
   - 贴地平拍:phone on the floor, lens 5-15cm above ground, pointing horizontally
   - 其它特殊机位(门缝/镜面/过肩):同一公式——实物+在哪+朝哪+该位置看到什么几何+四连否定
7. **适用边界**:眼平/胸高中景等普通机位直接写 shot 类型即可;只有"角度本身是效果"时才物理化。E1 rule 10 的"低机位仰拍"是观察结论,落地手段是本节的机位物理化,不是分屏。
8. **完整规范**:25 类视角的逐类物理定义块(通用隐藏锁/眼平/轻微低/腰位/膝位/贴地极端仰/虫眼/高机位/强俯/正上方90°/斜俯/侧面/前三分之二/正后/后三分之二/贴身广角/贴地侧向/背后跟随/手持人类视角/荷兰角/上倾斜/下倾斜/透视响应/防简化锁/8要素组合结构)见 **I 章**——视角写法一律以 I 章为准,本节是其中"机位=实物"的实证摘要。

---

### E6 混剪快切转场章(《绝世舞姬》82.9s/44镜实测)
1. **硬切全部卡在音乐节拍上**;换装/换场切镜时舞蹈能量跨切延续——切场景不切律动,观众读作"同一个人在跳"。
2. **遮挡→揭示家族**(本片核心转场):袖/伞/纱遮面→移开亮相(C36)、背影→回眸、纱帘/窗格框式 reveal、水面倒影→实体(S 倒影手)。"先藏后露"本身是节拍。
3. **白闪/白雾转场**进新场景(入伞海、入玻璃球);**粒子铺陈**(花瓣/火花/金屑/雪)在切点前后撒,粒子连续=场景连续。
4. **快闪连切**:高潮点前 3-4 个 0.07-0.25s 定格闪切(75.4-76.0s 实测 4 连闪),落拍收在正拍——密度即高潮。
5. **运动模糊 whip** 转场用于情绪转折(群舞→独舞);模糊帧糊掉换装过程。
6. **俯拍只用于"倒影/漂浮"概念镜头**(水面倒影手、花池漂浮收尾),舞技镜头全部平视或仰拍——与 E1 rule 10 互证。
7. **特写细节插片**:手部/头饰/饰品特写 0.5-1s 插在两段舞之间当节拍休止符。
8. **风格突变转场**:实拍↔AI 镜头直接对切(风格差本身就是节拍);AI 大殿俯瞰环绕可整段插入。
9. **影子分身**:白墙+侧光,人与墙影同舞(C31 同族);静态机位,影子是"第二舞者"。
10. **orbit 环绕只在旋转镜头用**(火环旋 23.1-26.6):环绕角速度=旋转角速度,裙摆火带连续。
11. 转场走位用 **C47 背身渐行**(不回头)收段落,下一镜从新场景新姿势直接进——段落间不解释、不衔接,靠音乐粘合。
12. 首镜**黑场淡入+框式构图 reveal**(纱帘/窗格),末镜**俯拍漂浮慢旋**收尾——首尾都是"非舞"镜头,把舞包在中间。
13. **旋转相位匹配剪辑**(56-64s 四连实证):在旋转中切镜,下一场景**同向同速继续转**——连续 4+ 场景(庭院红裙→海滨粉裙→雪地大旋→白裙),旋转是跨场景缝合线;切点=旋转周期中相位对齐处(同一肩方位),服装/场景任换,**转速、方向、发旋方向不变**。比"能量跨切延续"(规则1)更具体可执行。

### E6 附:视角词纪律(2026-10-07)
E1-E7 规律里出现的"低角度仰拍/荷兰角/中低角度浮动"等视角词是**分析语言**;写进提示词时一律按 **I 章**物理定义式改写(机位物理位置+高度+距离+光轴方向+空间关系+物理结果,必要时用 8 要素结构),不写角度形容词——"low angle" 会被模型平均掉,"a real camera positioned at knee height with the lens pointing upward" 不会。

### E7 弧形运镜与变焦语法(双人舞 16.8s 实测,2026-10-03 并入)
1. **弧形横移开场**:低角度仰拍,从人物右前方平滑左向弧形横移至正面——开场 1s 内完成"侧→正"。
2. **snap zoom / zoom punch**:两次快速急推/急拉、径向动态模糊,**卡在音乐重拍上**。
3. **roll + 荷兰角**:转身/失衡瞬间机身带 roll、荷兰角约 25° 短暂保持,随后**快速甩回水平**——roll 是瞬时的,不是常态。
4. **慢速 orbit**:由右绕回正面再到左前方,时近时远;转速与时距不均匀才是"人拍的"。
5. **前景/后景换人**:跟拍者微后撤让另一人占前景构图;solo 项目=让袖/发/伞占前景扫过镜头。
6. **重拍降机位+微前推**:高抬腿等重拍动作,机位略降并轻微前推。
7. **正面中低角度浮动跟拍**:随扭胯行进步小幅前后/左右浮动——不是死锁定机。

### E8 醉酒式镜头(第一视角失衡运镜)
核心定义:**人物稳定优雅,摄影机失衡**;运动链 = observe → react late → overshoot → correct → reacquire(观察→迟反应→过冲→修正→重新捕捉)。
1. **滞后追随**:人先转,镜头晚半拍才转;人先移,镜头追过头再修正。
2. **过冲-修正**:靠近过头→小退让;横移过头→修回;这是醉酒感的主要来源,不是手抖。
3. **轻 roll**:水平线偶倾缓复,荷兰角 ≤25° 且瞬时;**禁止 constant rolling**。
4. **垂直 bob**:醉酒者步态的轻微上下起伏,非剧烈晃动。
5. **旋转时最明显**:人物旋转稳定优雅,镜头迟疑→跟转→微过→带一点 roll→重新找到人物。
6. **永远有追随目标**:脸→身体→转身方向→舞蹈路径→手臂衣袖→重新入画。
7. **禁止清单**:random shaking / violent handheld / extreme motion blur / chaotic spinning / camera falling / severe dutch / constant rolling / out-of-control / 主体频繁出画。
8. **只有摄影机醉,人物永不醉**——人物平衡、优雅、节奏准确、不眩晕。
9. **母规则(H3 可整段粘贴)**:
```text
The camera represents the first-person viewpoint of a mildly intoxicated observer.

The subject remains completely stable, graceful, and professionally controlled.

The camera moves with imperfect body balance rather than random handheld shake:
slight lateral drift,
uneven forward momentum,
delayed reactions,
brief over-approach,
delayed rotational follow,
subtle roll,
small corrective retreats,
and imperfect re-centering.

The camera reacts to the subject's movement rather than generating independent random motion.

The movement pattern is:
observe → react late → overshoot → correct → reacquire.

During turns, the subject rotates first and the camera follows slightly late.
During lateral movement, the subject moves first and the camera chases afterward.
During strong accents, the camera may briefly surge forward or drift sideways.

The camera remains readable and physically plausible at all times.

Only the camera behaves intoxicated.
The performer never behaves intoxicated.
```
10. **适用**:情绪漂移/等待/微醺/夜路段落;Hero 与高精度段保持稳定相机——**稳定与失醇的对比**才让醉意被读出来。

### E9 互动剧情镜头语法(壁咚 7.1s 单镜头实测,2026-10-04 并入)
1. **单机位手持微晃**,胸上中近景起幅,双人始终同画——互动视频不用切镜,张力靠推近;
2. **缓慢向脸部推近**:腰部中景→胸上特写,推近速度与情节张力同步升级;
3. **接触重拍机身轻震**:压墙/抓手等接触瞬间 1-2 帧轻震,静止段回到稳定——震动是接触的触感外化;
4. **第二人物只出手不出脸**:互动对象仅以手臂/手部入画,无第二张脸——单主角互动视频的身份锚省略法(配 D22 链,H3 少锁一个人);
5. **视线交代对话**:被压者回眸看镜头侧(第四面墙),发起者视线看被压者——双人关系靠视线方向而非正反打。

模式:**每个服装状态 = 一个独立镜头**。每镜头两段式:**右入迈步入画(入画第一帧已穿新装)→ 落定中心摆 pose 后保持住,人物在画面中被硬切走**——不走出、不清屏、没有空帧。实测:4 镜 5.9s——镜1 0.000-2.267(状态1,右入→手抱胸前 pose 定住被切)→ 镜2 2.267-4.233(状态2,右入迈步→比 V 定住被切)→ 镜3 4.233-5.900(状态3,大跨步入画→终 pose 到片尾;4.233-4.4 有 0.17s 微镜头快闪变体)。

1. **右入=新装**:每个镜头开场 = 从画右迈步入画,入画第一帧已穿新装;上一镜头的人物是**保持 pose 在画面里被切走的**——没有走出、没有清屏、没有空帧停留。
2. **剪辑痕迹可见是特征不是缺陷**:切点两侧 = 中心 pose 定住 ↔ 右侧迈步入画,位置跳变明确告诉观众"换了";同景同机位下 scene detect 阈值 0.27 探不到,≤0.08 才现形。
3. **微镜头快闪变体**:状态3 前有 0.167s 的微镜头(4.233-4.4),可作快闪强调。
4. **文字标签联动(可选用)**:顶部常驻横幅写全片主题(「带你认识三种袜子」),左侧编号标签与镜头一一对应(1.脆皮水 / 2.菱格黑丝 / 3.蕾丝花边),切镜瞬间换标签;H3 应用可按需移除文字,靠袜饰差异本身区分状态,audio 直接铺底卡点。
5. **恒定项锁死**:主服装(红色漆皮挂脖束身短裙)、场景、机位(固定正面全身、无运镜)全程不变——**只有"变化项"(腿部/袜子)在镜头间切换**,观众视线被引导到唯一变量上。
6. **服装状态目录写法**:每状态一条,含编号标签原文+变化项精确描述(材质/花纹/高度),不变项写一次。示例:状态1「脆皮水」=无袜、腿部涂油呈水光;状态2「菱格黑丝」=黑色菱格纹连裤袜;状态3「蕾丝花边」=红色蕾丝翻边过膝袜。
7. **H3 应用**:每状态一段独立提示词——`she enters frame-right mid-stride wearing <state>, settles at center, holds the pose as the shot cuts`;状态间硬切由剪辑完成,不在提示词内写 morph/in-shot swap,**也不写 walk-out/empty frame**。
8. **适用**:服装/袜子/配饰流水线展示、变装卡点、同款多色对比;不适合叙事性舞蹈(状态间无情节)。
### E10 姿态锁定原位换装(三姿态模板·卡点跳切,《三种袜子》系列 3 段实测,2026-10-05 并入)

模式:**姿势全程锁死的"原位换装"**——与 E9(右入跨进=新镜头)同族不同支:E9 靠走位重置,E10 靠**姿势完全不动、唯一变量(下装/袜饰)在跳切间切换**。三段实测(18.4s):V1 站姿侧身锁定(4.69s,5 状态)、V2 深蹲抱膝锁定+抖腿(5.70s)、V3 提裙站姿锁定(8.03s,3 状态+文字标签)。片型 = 编辑式快照 snap-lock(锁定 pose ↔ 跳切换装,两态互斥)。

1. **三姿态模板(受力来源与进入路径)**:
   - **站姿侧身锁定**(V1):双脚站立支撑、重心沉在支撑腿,侧身 45°、双手交叠腰侧;进入路径 = 图1 直接给出,无需动作进入;头部微动是唯一活体信号(证明是活人不是照片);
   - **深蹲抱膝锁定**(V2):入态 = 屈膝深蹲、双膝并拢上提抱向胸口(受力 = 前脚掌+臀位平衡的双点支撑),蹲位全程锁死;上半身(手指唇部等小动作)自由,腿部锁定;
   - **提裙站姿锁定**(V3):双手提裙摆向两侧外翻(受力 = 双脚站立+双臂反向张力),裙摆位置全程不变;唯一变量 = 裙下沿露出的袜饰。
2. **抖腿链(V2 精华,逐拍分解)**:抖腿 = 蹲姿中**膝部/小腿的快速颤动 0.3-0.4s**,骑在两个强拍**之间**的弱拍间隙(onset 实测:2.55S 抬手起 → 2.6-2.9s 腿部重运动模糊颤动 → 3.11H 回稳)——**上半身与手部构图全程不乱**(手指仍停在唇边),运动模糊只属于腿部;抖完渐清晰回锁。写法:`her knees vibrate rapidly for 0.3s with heavy motion blur on the legs only, the upper-body frame and hand pose completely unchanged, then sharpen back into the locked crouch`。
3. **卡点纪律**:切点全部吸附 onset 网格(V1 实测 1.87/2.85/3.75 吸附 1.87S/2.65-3.03/3.03S;V3 变装落 4.32S)——先 onset_probe 拿强拍表,再排换装顺序,**切点=onset**;抖腿类颤动则刻意骑弱拍间隙。
4. **唯一变量纪律**:姿势、上装、场景、机位、构图全程锁死,**只有下装/袜饰在跳切间切换**——换装前后姿势逐帧同构(arms identical, head identical, only legs differ)。
5. **文字标签联动(可选)**:左侧标签与状态一一对应(V3:「小白袜 or 脆皮水」→「小白袜」→「脆皮水」);可整体移除。
6. **H3 应用**:一镜一段独立生成(同 E9 一镜一状态);写法 = `fixed frontal camera, the pose locked exactly as <Picture 1>, only the legwear swaps to <state> at the beat — the pose, arms, head and framing are frame-identical across the cut (jump cut)`。
7. **适用**:袜饰/下装/鞋类流水线展示、穿搭对比、同款多色;与 E9 组合 = 走入式(换大件)与原位式(换小件)两条流水线。

## F. 同曲异构双版本纪律(宅舞 vs 抖舞,5 条)

1. **同一拍网格,两套密度**:先写死音乐网格,宅舞版每小节 1-2 个"pose verb"+显式 `freeze N counts`;抖舞版每小节写满 `on every half-beat` 级事件、禁 `freeze/hold`(收势链除外);两版拍位逐拍对齐。
2. **驱动源声明前置**:宅舞版开头 `upper-body driven, movements live above collarbone, feet stay planted`;抖舞版 `lower-body driven, knee bounce is the engine, arms follow the hips`。不写这句,两版会融成中庸中间密度。
3. **形状词 vs 路径词分库**:宅舞只用形状词(frame, poke, fist, paw, tilt——可静止);抖舞只用路径词(roll, slam, fling, thrust, circle——带轨迹)。跨库用词是双版本失败主因。
4. **入态/出态显式缝合**:链边界两版必须落在同一拍,只允许内部密度不同。
5. **反差段落显式配对**:`left side: three statues plus a bow (2 actions per 8 counts); right side: maximum flow (10+ actions per 8 counts); both share the identical final bow on the last beat`——极化段必须双版本写进同一个 prompt。

---

## G. Hero Action 库(跨舞种技术峰值 · 观赏性插件)

> 定义:HERO 不是"摆个漂亮姿势",而是**舞蹈动力链的终点和下一条动力链的起点**:
> `Preparation → Initiation → Technical/Signature Peak → Apex(音乐重拍) → Hero Action → Hero Lock → Release → Transition`
> "这里加一个 Hero" → 先判定五大族 → 找专业动作名 → 按八步链写。

### G0. H3 实现度分级(A/B/C/S,生成可行性而非舞蹈难度)
- **A** 高辨识+可控,直接用(Signature Gesture/Point&Lock/Pirouette/Contemporary Fall/Fall-Recovery/Waacking Line/Pop Hit)
- **B** 技术复杂,缩短技术动作、强化前后链(Grand Jeté/Fouetté/探海翻身/双飞燕简化/Attitude 平衡)
- **C** 高危空翻/高速地面技巧 → 用"技术视觉模拟"或简化版(Windmill/Flare/旋子简化)
- **S** 极强冲击但真实性要求极高 → 仅特殊高潮(Airflare/1990)

### G1. 五大技术族(动作链模板)
- **AIR**:`Preparation → Takeoff → Air Shape → Apex → Landing → Absorption → Hero`(Grand Jeté/紫金冠/双飞燕简化/Sissonne)
- **TURN**:`Axis Prep → Weight Transfer → Initiation → Rotation → Exit → Open Shape → Hero`(Pirouette/Fouetté/平转/掖腿转/Piqué)
- **FLIP**:`Entry → Momentum → Inversion → Technical Peak → Exit → Recovery → Freeze`(对 H3 最危险,禁写成一句"完成空翻";C/S 级)
- **LINE**:`Weight Placement → Extension → Counterbalance → Maximum Line → Head/Eyes → Hero Lock`(探海/Arabesque/Attitude/倒踢/High Release——**古风 MV 核心**)
- **ACCENT/SIGNATURE**:`Groove → Build → Accent → Sudden Shape → Lock → Release`(Hit/Dime Stop/Point/Pose——**宅舞/K-pop/_idol 核心**)

### G2. 各舞种可用 Hero 精选(需要时扩展)
- 中国古典舞:紫金冠跳(B)、探海翻身(LINE+TURN)、串翻身(B)、点步翻身(A)、掖腿转(A)
- 芭蕾:Pirouette(A)、Grand Pirouette Attitude(B)、Grand Jeté(A/B)、Sissonne(A)
- Contemporary:Fall & Recovery(A)、Spiral(A)、Off-axis Tilt(A/B)、Floor Roll(A)
- Jazz/Disco:Calypso Leap(B)、Barrel Turn(B)、Multiple Pirouettes(B)、Attitude Pirouette(B)
- Popping/Locking:Hit&Dime Stop(A)、Waving(A)、Lock-Point-Lock(A)、Scoo Bot(A)
- Waacking/Vogue:Double Waack→Line→Pose(A)、Dip(A/B)、Hand Performance(A)
- K-pop/宅舞:Point Choreography(签名手势)本身就是 Hero——**辨识度>难度**
- 宫廷/汉服特供:探海(LINE)、Attitude 后吸腿(LINE)、Fall&Recovery(地面段)

- 绝世舞姬补充(VFX/概念 Hero,源视频 2026-10 反推):**火环旋转**(裙摆化光带环绕,+orbit 同速环绕)/ **凤凰翼展开**(背后金翼随双臂展开,back view)/ **影子分身**(白墙双影同舞)/ **水面倒影手**(俯拍指尖破倒影)/ **水下旋转**( fabric 漂浮慢旋)/ **俯拍漂浮收尾**(花池慢旋定帧)。全部属 S 级实现难度:H3 用"裙摆光带/翅膀合成/影子"等描述词可达形似,水下与倒影建议整段概念化处理。
### G3. Hero Lock 写法(秒级窗口,三种型)
- 技术型:`07.40-08.10 Technical Peak(平转末圈稳轴) / 08.10-08.42 Hero Action(最大斜向延展+袖打开) / 08.42-08.72 Hero Lock(重拍锁定0.3s,眼神定轴,袖端微惯性) / 08.72-09.20 Release(进入下链)`
- Popping 型:`05.20-05.72 wave / 05.94-06.08 full-body hit / 06.08-06.30 Dime Stop Lock / 06.30-06.90 release into groove`
- Breaking 型:`06.00-08.20 power sequence / 08.20-08.70 exit / 08.70-09.05 Freeze / 09.05-09.50 release`

### G4. HERO 分镜模板(12.5s 段直接套用)
- HERO-01 古典舞大技巧:步法→沉→重心→跳/转→Apex→落地→线条→Lock→释放
- HERO-02 古风袖舞:步法→重心→身韵→袖启动→扩张→头眼→Hero→袖惯性→转场
- HERO-03 Contemporary:Contraction→Spiral→Fall→Floor→Recovery→Suspension→Hero
- HERO-04 Ballet:Prep→Plié→Takeoff/Turn→Extension→Apex→Controlled Finish→Hero
- HERO-06 Popping:Groove→Isolation→Wave→Tutting→Hit→Dime Stop
- HERO-08 宅舞/K-pop:Travel→Isolation→Point Choreography→Accent→Signature Shape→Hero Lock

### G5. Hero 价值公式与选型纪律
`Hero 价值 = 技术含量 × 辨识度 × 音乐峰值 × 镜头可读性 × 生成稳定性`
- Signature Gesture / Point&Lock / Waacking Line / Pop Hit:生成最稳(★★★★★),优先常用
- Grand Jeté / 探海系:视觉顶级,需前后链加固
- Windmill/Flare/Airflare(C/S):真实性风险最高,偶像团舞默认禁用
- 每支舞 Hero 数量:2-4 处,分布 30%/50%/70%/90% 进度;**绝不为"更多"而加**
- 汉服项目选型:LINE(探海/Attitude/High Release)+ TURN(Pirouette/平转)+ ACCENT(Point&Lock/Dime Stop)为主;AIR 用小跳级;FLIP/C/S 禁用

---

## H. 成品范本库:13 支 I2VA 反推提示词全集(2026-10 并入)

> 来源:`H3_I2VA_反推` 13 支单人视频反推;首帧图目录 `D:\Users\Administrator\Downloads\H3_I2VA_反推\`,每支上传对应 `XX_..._首帧.jpg` 作 <Picture 1>,粘贴提示词即可生成。
> 全部正文零外貌/服装/环境描写(<Picture 1> is the sole visual authority);时长与原片一致(11 号超 H3 上限,截取前 15s);声音两字段为按体裁重建,需要原声时在装配阶段铺回原音轨。

### H0. 13 支范本提炼的成品规律(与 A-G 章的对接)

1. **开头三件套锚**(13 支一致,照抄结构):`For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.` → `[Shot 1] <体裁+镜头+时长> ... matching the style and the exact opening pose of <Picture 1>` → `From the opening pose (<首帧姿态一句话复述>), ...`。首帧姿态复述=入态声明,即 0.规则#2 出入态对接的成品形态。
2. **身份委托句**(必备一句):`identity, outfit, room and framing are carried entirely by <Picture 1>` 或 `every visual detail ... comes solely from <Picture 1>`——正文其余部分只写动作与镜头,永不写外貌/服装/环境。
3. **三层结构的成品写法**:持续层 `Continuous layer throughout: knees stay soft with a light bounce on the beat ...`(09/10/11);accent 层用绝对秒逐条列出(`0.0-2.0s — sustained layer ... accent: at 0.8s ...`)(01);微表情层可单列 `Micro-expression layer: ...`(01/02)。
4. **声音两字段三模式**:
   - **重建**(默认):overall_soundscape 写环境音+衣料/脚步声;non_diegetic_music 写体裁+BPM+情绪+能量段落(01/02/06/09/10/11/12/13)。
   - **原声保留交接**:`overall_soundscape: N/A - the source carries a loudness-verified non-silent audio track whose content was not audibly audited; lay back the original track per the assembly note.` + `non_diegetic_music: N/A (any music is part of the original track; do not regenerate).`(03/04/05)——文字复刻不了波形,原声在装配时铺回。
   - **全 diegetic 演奏**(乐器/唱):`non_diegetic_music: N/A - all music is diegetic: the live guqin performance ...`(07)。
5. **BPM 与拍点落位**:BPM 写进 non_diegetic_music(~75-85 / ~100 / ~125-130);卡点段在正文用绝对秒列拍点(03:`bottoms land at 0.0, 0.6, 1.2, ...` + `metronomic squat-bounce cycle every 0.6 seconds`)——循环引擎当持续层、accent 写成"第几个 cycle 的变体"(03 double-pump at 3.9),即 B 章引擎链的成品用法。
6. **结尾纪律**(13 支全部写死终态):`settles into a held pose` / `motion easing to a stop right at the cut` / `pose holds frozen at the cut`;原片硬切的写 `cut off hard, with no fade-out`(08/09/10)——对齐 0.规则#4"静止必须明写"。
7. **镜头语法样本库**:locked-off static(01/05/10)、handheld subtle sway(02/03)、slow steady push-in 全程(12)、pull-back 开场→slow push-in(04)、固定全身→7.0s 起缓推半身(13)、4 镜头切点 5.9/12.9/19.9s(07);切点全部落乐句/动作收点(对齐 E3)。本组均为常规机位;需要极端仰拍/俯拍/特殊机位时按 E5 机位物理化写法(实物+位置+画面几何+四连否定,单机位不分屏)。
8. **AI 生成画面同构**(08/12):风格句放开头(`AI-generated xianxia fantasy shot` / `soft donghua art style`);字幕/文字锁:`the caption block stays perfectly static for the entire duration — no re-rendering, no flicker, no shift, no new text`。
9. **晚入场第二舞者**(03):`At 3.5s a second dancer walks into the right frame edge and takes a matching stance, mirroring ...`——单机位段的多人轻量写法,与 D 章"先队形骨架再挂动作"的槽位法互补。
10. **<Picture 1> 是"进行中"状态时先接住再展开**:lean-in(04 `She straightens up from the lean-in of <Picture 1> as the camera pulls back`)、行进中(05 `mid-stride walking away ... back to the lens`)——正文第一句必须消化首帧的中间态,不能假装从定格开始。

### 01_光仔_风吹乱了花(15.1s)
首帧:`01_光仔_20260923__首帧.jpg` | 单镜头固定机位,胸口高中近景,抒情花瓣舞

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] A serene, lyrical short clip in one continuous locked-off medium half-body shot at chest height, matching the style and the exact opening pose of <Picture 1>; total runtime 15.1 seconds. From the opening pose (head bowed, hands folded in front of the lower chest), the movement develops as follows: 0.0-2.0s — sustained layer: the upper body breathes with slow shoulder rises and a gentle left-right sway, about one full cycle every two seconds; accent: at 0.8s the chin lifts and the gaze rises from the ground to the lens, at 1.6s the folded hands loosen and the right palm rotates upward. 2.0-5.0s — accent: at 2.2s the right arm lifts sideways and traces a wide arc from the chest through the drifting petals toward the upper right, fingers spreading one by one; at 3.5s the left hand mirrors a smaller arc low across the belly; micro-expression: the head tilts left as the eyes track the petals sweeping left to right. 5.0-8.0s — accent: at 5.4s the right hand rises to hover beside the right ear in a delicate pinched-finger shape, the wrist turning slowly inward then outward; at 6.8s the head tilts right about ten degrees and the gaze locks straight into the lens while the left fingertips rest at the chest. 8.0-11.0s — sustained layer: the shoulder sway continues on every musical beat; accent: at 8.3s both arms open softly to the sides, at 9.4s they re-cross in front of the chest, at 10.5s the crossed wrists release into upward-facing open palms. 11.0-15.1s — accent: at 11.2s a gust sweeps the petals sideways across the frame as the arms descend slowly; micro-expression: the eyelids lower softly and the head bows about fifteen degrees by 13.0s; from 13.0s to 15.1s the hands settle back folded in front of the lower chest, the body stills, and the clip ends on the quiet closing pose as the last petals drift down.

overall_soundscape: A soft continuous breeze with petals rustling past, faint fabric movement, and open-air ambience.

non_diegetic_music: A gentle Chinese-style pop ballad with soft percussion and a wistful, lyrical mood pacing the slow arm phrases.
```

---

### 02_派小星_神之八秒渐变版(8.4s)
首帧:`02_派小星_20260825_首帧.jpg` | 单镜头手持中景+全程色调渐变(2.0s 起暖黄→4.0s 起复古胶片)

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] A playful eight-second dance challenge clip in one continuous handheld medium shot with a subtle sway, matching the style and the exact opening pose of <Picture 1>; total runtime 8.4 seconds. From the opening pose (right hand rising overhead toward the upper right, palm open), the choreography develops as follows. Sustained layer: on every half-second beat the shoulders bounce, the hips pop alternately left and right, and the knees stay soft and springy. Accents: 0.5s — the right arm peaks at forty-five degrees overhead right while the left hand lifts to the waist side, gaze angled up; 1.0s — the right arm sweeps a wide arc from overhead toward the left as the left hand falls and the head dips; 1.5s — both arms cross in front of the chest and spring open, right high and left low. Beginning at 2.0s the color grade transitions gradually into a warm nostalgic tone, deepening into a high-contrast retro film look by 4.0s and holding to the end. 2.0s — arms form a W shape at chest height; 2.5s — the right hand flicks beside the right side of the head; 3.0s — both arms extend along a diagonal toward the upper left; 3.5s — the right hand shades the brow in a gazing-into-the-distance gesture; 4.0s — arms fold back to the chest; 4.5s — the right arm opens to the right side, palm up; 5.0s — both hands rise overhead forming a triangle; 5.5s — the right hand draws a small circle at chest level; 6.0s — both arms spread fully horizontal; 6.5s — both hands cup the chin; 7.0s — the right arm shoots forward with the index finger pointing straight into the lens; 7.5s — both hands clasp together above the head and hold. Micro-expression layer: the head swings in small left-right tilts that follow each leading hand, the eyes chase the moving hand, and at 7.0s the gaze locks dead-on to the camera with a bright finish held through 8.4s.

overall_soundscape: Quiet indoor room tone with light footsteps and faint fabric swishes from the arm movements.

non_diegetic_music: An upbeat K-pop-style dance track with bright synths and a steady driving beat, cheeky and playful.
```

---

### 03_温夫人_相扑猫(8.0s)
首帧:`03_温夫人_20260920_首帧.jpg` | 单镜头平拍中景,猫咪扑玩具体育动作全链

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Vertical 9:16 smartphone video, one continuous handheld shot with only a slow lateral sway of a few percent of the frame width (no push, no cuts), the subject holding the same framing as <Picture 1>. Opening from the exact state of <Picture 1>: a deep sumo-stance squat, knees wide and bent, both arms reaching down between the knees with limp cat-paw wrists. She repeats a metronomic squat-bounce cycle every 0.6 seconds: each cycle rebounds up (hair, cardigan hem and skirt bouncing) with the hands curling into loose paw fists near the chest at the crest, then drops back into the deep squat with the arms swinging forward-down and the limp wrists dangling between the knees. Cycle bottoms land at 0.0, 0.6, 1.2, 1.8, 2.4, 3.0, with crest paw-curls at 0.9, 1.5, 2.1; at 3.3 a quick half-rise with the arms crossing inward, then a second deep drop at 3.9 (double-pump accent, hands together in front of the thighs); further bottoms at 4.5 and 5.1 with crest arm-flares at 4.2 and 4.8; at 5.4 a shallow dip with the head turning toward the camera. 5.4-6.0 she pushes up out of the squat to a full stand, arms sweeping down and back, ponytail flying; 6.0-6.3 standing tall in left-facing profile with one small knee pump; 6.3-6.6 weight onto the right leg, left knee bending with heel lifted in a step-touch, arms floating out at waist level; 6.6-6.9 the near-side hand rises to the chest, palm opening; 6.9-7.2 the arm raises elbow-bent and pushes an open palm outward with fingers spread in a paw-press; 7.2-7.5 the press holds with the chin lifted; 7.5-8.0 the arm draws back down and she settles into a low ready bounce in right-facing profile to the end. At 3.5s a second dancer walks into the right frame edge and takes a matching stance, mirroring the 6.9-7.5 paw-press at the right edge.

overall_soundscape: N/A - the source carries a loudness-verified non-silent audio track whose content was not audibly audited; lay back the original track per the assembly note.

non_diegetic_music: N/A (any music is part of the original track; do not regenerate).
```

---

### 04_张心心小仙女_哒哒哒卡点(10.5s)
首帧:`04_张心心小仙女_20260_首帧.jpg` | 单镜头固定全身景,15 个拍点卡点舞

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Vertical 9:16 smartphone video, one continuous handheld shot: a fast pull-back during 0.0-0.5s opens the framing from the close-up in <Picture 1> out to a full-body shot, then a slow steady push-in tightens the framing through the rest of the take (subject and background enlarging together, a slight upward re-frame near the end), no cuts. She straightens up from the lean-in of <Picture 1> as the camera pulls back, arms swinging once and settling into a shoulder-width stance by 0.5; 0.5-1.2 two small knee bounces with one shoulder shimmy at 0.8 and a head nod; 1.2-1.5 the right hand lifts to the chest and the wrist rolls begin; 1.5-2.9 double-fist wrist rolls in front of the chest with alternating thumb flicks on the beat (1.8, 2.1, 2.4), hips swaying side to side with each roll; 2.9-3.2 the rolls snap into a double thumbs-up at chest height (3.2 accent) with the head tilting; 3.2-3.9 two small thumbs-up pumps (3.4, 3.7); 3.9-4.4 the arms swing down and wide, then the right arm sweeps up across the body; 4.4-4.8 the right hand flicks across face level with fingers spread while the left palm opens outward at shoulder height, mouth opening wide on the hit; 4.8-5.2 the hands drop with one deep knee-bounce dip at 5.0; 5.2-6.3 alternating chest-level fist pumps switching every 0.3s (accents 5.4, 5.7, 6.0), hips counter-swaying; 6.3-6.6 the fists stack center-chest for one beat; 6.6-7.4 single-fist collar pops, the right fist popping up to the collar at 6.8 with the left hand dropping to the hip, alternating twice more (7.1, 7.3); 7.4-7.9 both hands curl over the collarbones in a collar grab, the body popping tall at 7.6; 7.9-8.5 both index fingers point up beside the face with bounce accents at 8.0 and 8.3, grin widening; 8.5-9.1 the fingers curl and re-aim inward to point at her own collar (9.0); 9.1-9.7 the hands flip open with palms facing the camera beside the face, two small push pulses (9.3, 9.6); 9.7-10.4 the hands pull back into a double claw-grab at the collarbones with elbows lifted out, holding the pose with a smile to the end.

overall_soundscape: N/A - the source carries a loudness-verified non-silent audio track whose content was not audibly audited; lay back the original track per the assembly note.

non_diegetic_music: N/A (the beat-locked choreography rides the original track named in the source title; do not regenerate music).
```

---

### 05_怡寶_裙子被剪(8.2s)
首帧:`05_怡寶来啦_2026090_首帧.jpg` | 单镜头固定微仰中全景,剧情反应链(发现→检视→比量)

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Vertical 9:16 smartphone video, one single continuous locked-off static shot, eye level, no pan, no push, no cuts for the full take, the framing identical to <Picture 1> throughout. Opening from the exact state of <Picture 1>: mid-stride walking away from the camera toward the doorway ahead, back to the lens, the opening in the back of the skirt exactly as visible in <Picture 1>. 0.0-0.4 she finishes the current stride with arms counter-swinging, the back opening flashing wider as the trailing leg pushes off; 0.4-0.8 the left pump lands heel-to-toe, the red sole flashing as the right heel lifts; 0.8-1.2 steps shorten on approach, long hair swaying against her back; 1.2-1.6 the right arm reaches forward-right for the door handle; 1.6-1.8 the hand grips the handle, body decelerating, weight sinking onto the right leg; 1.8-2.0 the head turns back over the left shoulder, a profile glance at the camera with a small smile; 2.0-2.3 she pivots leftward to face front, hair whipping outward, hand releasing the handle; 2.3-2.6 lands facing the camera, arms flung slightly out then dropping, feet shuffling into a parallel stance; 2.6-2.9 stands full-front, chin dipping in a quick downward eye-flick toward the skirt; 2.9-3.3 weight shifts onto the left leg, right hip easing back, torso beginning to rotate right; 3.3-3.7 rotates into right-side profile, head tilting down to check along the skirt's side seam, left arm swinging behind; 3.7-4.1 the right arm bends up with the index finger extending; 4.1-4.5 holds the side profile with the index finger raised beside the cheek while the left leg crosses in front with heel lifted; 4.5-4.8 one small finger waggle with a deepening smirk; 4.8-5.2 the hand rises to temple height with fingers loosely spread, shoulders coiling; 5.2-5.6 a fast whip spin on the ball of the right foot, hair flaring, hem swishing; 5.6-5.9 lands facing the camera, arms sweeping out to hip level and rebounding; 5.9-6.3 the right arm rises bent with a loose fist at shoulder height, left heel lifting in a small step-in-place; 6.3-6.9 the arm sweeps down across the body as the hips shift left and weight transfers to the left leg; 6.9-7.5 the right arm wraps behind the back, right leg crosses behind with heel raised, hip cocking toward frame-left; 7.5-8.2 holds the final leaning pose with one tiny settle bounce, smile held to the end.

overall_soundscape: N/A - the source carries a loudness-verified non-silent audio track whose content was not audibly audited; carry the original track through intact per the assembly note instead of regenerating sound.

non_diegetic_music: N/A (any music is part of the original track; do not regenerate).
```

---

### 06_一点点点._小师妹慢摇舞(9.5s)
首帧:`06_一点点点._202609_首帧.jpg` | 单镜头固定微仰膝上中全景,慢摇舞(持续层:顶胯+膝弹+重心迁移)

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Vertical short-form dance clip, one static locked-off knee-up medium shot — the recording viewpoint comes from a real physical camera positioned slightly below her chest line on a stable support, lens angled gently upward toward her face and torso, no filming equipment visible; starting exactly from the neutral standing pose of <Picture 1> (facing camera, arms loosely bent at sides). A continuous groove layer runs through the whole 9.5 seconds: hips pop side to side on every beat, knees bounce in alternating soft bends, and weight rolls between the legs with each hip shift. Over that layer: at 0.00-0.50s the right hip pops once and the right wrist flicks up in front of the chest. At 0.50-1.50s the right hand sweeps an arc to the upper right, fingers leading, head turning right with the eyes tracking the hand; at 1.50s the left hip pops, the right wrist presses down, chin lifts and eyes return dead-on to camera with a small smile. At 2.00-3.00s the left arm lifts to a side hold while the right arm draws down, head tilting left with eyes dropping low-left; then both hands cross at the chest and spring open as the head re-centers, smiling at the lens. At 3.00-4.00s a big right hip pop twists the torso left, the right hand brushes past the waist toward the back while the left arm reaches overhead with the wrist turning in, head tipping back-left and eyes floating up; she then settles the hold for one beat while the hip carves a small clockwise circle and the raised left wrist flicks twice, gaze sliding back to camera. At 4.00-5.00s the left hip pops as the left hand slides down from overhead until its fingertips rest against her cheek, head tilting right; a quick left-to-right hip swing rides under it, the right hand gliding up her side to the underarm, chin dropping with eyes cutting low; at 5.00s a deep knee dip makes both arms open in two wide simultaneous arcs, eyes sweeping across the lens. At 5.50-6.50s the right hip pops as the arms gather into a chest cross with the smile widening; then the right foot steps out to the right side, right arm pushing flat to the right and left arm swinging back, torso leaning right with the head and eyes following the hand; weight settles onto the right leg, left toe taps down, the left arm recovers to the front and the head snaps back to camera. At 6.50-8.00s the hips draw one full clockwise circle as the right elbow rolls small circles at chest height, the head circling gently with the eyes chasing the hand; the circle ends parked on the right hip, the left hand rises to her cheek, the head tilts left and the eyes slant upward in a coquettish sideways glance. At 8.00-9.50s a deep knee bounce sends the hips front and back while the right hand sweeps overhead with the wrist flaring out, head falling back and eyes up; she rises quickly, right arm staying high and left arm stretching to the side, head leveling to camera with a bright smile; the finish lands on a held pose - weight on the right leg, left toe pointed, the right hand floating slowly down to the chest, chin tucked slightly, gaze locked straight into the lens as the smile freezes. Total duration 9.5 seconds.

overall_soundscape: Low indoor room tone with the soft thud of the side step and knee bounces on the floor, and light swishing of fabric on every arm sweep.

non_diegetic_music: Upbeat Chinese DJ slow-swing remix of a classic romantic ballad, around 100 BPM with a steady four-on-the-floor kick and a catchy melodic hook, playful and flirtatious in mood.
```

---

### 07_念念清_谁在抚琴配相思成疾(28.1s)
首帧:`07_念念清_20260914_首帧.jpg` | 4 镜头(切点 5.9/12.9/19.9s):背抚琴→正面渐强→胸上吟唱特写→高潮收势

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Vertical short-form performance clip, static locked-off back three-quarter medium shot; starting exactly from the pose of <Picture 1> (seated facing away, both hands resting on the strings of the guqin). At 0.00-1.50s the hands begin alternate gentle plucks over the strings. At 1.50-3.00s the right hand glides toward the far end of the strings in sweeping picks while the left hand presses and slides along the near end, the torso swaying subtly with each phrase. At 3.00-5.00s the alternating plucks quicken and widen, shoulders rocking with the rhythm. At 5.00-5.90s both hands open outward and pause at the edges of the strings, ending the phrase. [Shot 2] At 00:05.900, the camera cuts to a static frontal medium shot of the same seated playing position. At 5.90-7.50s playing resumes, right fingers picking outward as the left hand slides a rising glissando, gaze lowered onto the strings. At 7.50-9.00s the right hand breaks into a rapid rolling tremolo across the strings with left-hand vibrato, the head nodding gently and the torso leaning slightly forward. At 9.00-11.00s the texture thickens, the body rocking in back-to-forward waves that set her hair swaying. At 11.00-12.90s a crescendo lifts the shoulders, the head tilting right and upward, and the section ends with the hands splitting apart - left pressing the high positions, right pulling the low strings - as the torso twists right. [Shot 3] At 00:12.900, the camera cuts to a static chest-up close-up. At 12.90-14.00s the hands lift from the strings to chest height in a singing posture, head bowing slightly as the lips shape the opening lyrics. At 14.00-15.50s the head rises with the eyes lifting while one right-hand pluck enters the low edge of frame. At 15.50-17.00s the head turns to the right, gaze reaching right-front, brows lifting on a sustained note. At 17.00-18.50s the head returns toward camera, the sung emotion visibly intensifying. At 18.50-19.90s the head tips back with the eyes up and the mouth opening on the strongest note, then settles: head back to front, gaze dropping to the strings as the vocal line softens. [Shot 4] At 00:19.900, the camera cuts back to the static frontal medium shot. At 19.90-21.50s the hands return to full playing, the left hand sliding wide while the right hand rolls sweeping strokes, torso leaning into the rhythm. At 21.50-23.00s alternating strokes quicken further and the head nods on the beat. At 23.00-25.00s the performance peaks: the widest arm strokes yet, the torso swinging forward and back in large waves, hair swinging with each surge. At 25.00-26.50s a diminuendo draws the hands back toward the center of the strings, the body sitting upright and the head lowering. At 26.50-27.50s the strokes slow and the left hand holds the closing note with vibrato. At 27.50-28.10s both hands come to rest flat on the soundboard, seated perfectly still, head slightly bowed in a held finishing pose. Total duration 28.1 seconds.

overall_soundscape: Quiet indoor room tone; the woody resonance of plucked silk strings with long decays, faint rustle of sleeves grazing the strings, and soft audible breaths between vocal phrases.

non_diegetic_music: N/A - all music is diegetic: the live guqin performance and a soft, plaintive female vocal singing a slow, freely-phrased melancholic Chinese ballad that builds to one peak and recedes.
```

---

### 08_ai景行小博士_minimax本地部署对比(12.8s)
首帧:`08_ai景行小博士_2026_首帧.jpg` | 单镜头,实为 AI 仙侠画面(金龙+云海)+底部两行静态对比字幕;缓慢推近

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] A single continuous 12.8-second vertical AI-generated xianxia fantasy shot that continues exactly from the state of <Picture 1>; the two-line caption block at the bottom stays perfectly static for the entire duration — no re-rendering, no flicker, no shift, no new text. 0.0-3.0 s: the dragon keeps its diving line from the opening pose, then carves into an S-curve and threads through a gap in the cloud sea; cloud layers drift slowly left and part around the body; small golden light particles begin peeling off into short trailing streaks. 3.0-9.0 s: the dragon climbs upward through the clouds, head rising toward center frame; the cloud sea churns harder, gaps opening and closing; the particle wake thickens into a denser golden streak; the small foreground figure standing on the clouds holds its ground, looking up at the dragon while its robes flutter stronger in the wind. 9.0-12.8 s: the climb continues with the head reaching upper-center frame, mane and whiskers streaming backward; cloud surge and golden particles peak as the framing gently tightens (the dragon slowly growing larger in frame); the ascent is still in progress when the video cuts off hard, with no fade-out.

overall_soundscape: A deep low-end rumble and airy high-altitude wind wash running under the whole clip, swelling gently as the climb peaks in the final seconds.

non_diegetic_music: Epic orchestral-electronic hybrid score around 90-100 BPM — atmospheric strings with low percussion building 0-4 s, main groove 4-9 s, energy peak 9-12.8 s, cut off without fade-out.
```

---

### 09_14cc_林黛玉倒拔垂杨柳(11.9s)
首帧:`09_14cc_2026092_首帧.jpg` | 单镜头固定全身景,神之八秒挑战变体(深蹲蓄力+高举 V)

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] One locked-off full-body vertical shot, 11.9 seconds, continuing exactly from the standing pose of <Picture 1>; identity, outfit, room and framing are carried entirely by <Picture 1>. Continuous layer through the whole take: knees stay soft and bounce lightly on every beat of the ~125-130 BPM track, chest and shoulders dip on each beat, weight sways subtly side to side, and a light natural smile never fully leaves the face. 0.0-1.0 s: from the neutral standing start, the right arm lifts to chest height. 1.0-3.0 s: the right hand rises overhead then falls to shoulder height; both hands cross over the chest, then both arms open out to the sides. 3.0-4.0 s: hands gather in front of the chest and push upward, palms flipping outward, ending with both arms high in a V. 4.0-6.0 s: holding the high V, the torso tips right with a slight chin lift, then tips left, then the arms lower to side-horizontal. 6.0-7.0 s: arms sink back to the sides as the torso re-centers into a tall poised beat-hold. 7.0-8.0 s: both arms swing back with the torso leaning forward to load up, then a deep squat with both hands reaching forward and down. 8.0-9.5 s: rising out of the squat, both hands sweep up overhead, torso tipping right at the top, then re-centering. 9.5-11.9 s: the right arm drops while the left stays up for one asymmetrical beat; hands come to the chest and press down into a finishing gesture with soft knees, then arms settle to the sides as she stands facing the camera, motion easing to a stop right at the cut.

overall_soundscape: The soundtrack is fully dominated by the music; no distinct room noise or environmental sounds stand out.

non_diegetic_music: Fast electronic dance track around 125-130 BPM with vocals; sparse intro groove 0-4 s, then a fuller high-energy section 4-11.9 s, cut off mid-phrase with no fade.
```

---

### 10_家酱_中秋快乐慢摇(11.0s)
首帧:`10_家酱_20260925__首帧.jpg` | 单镜头固定全身景,~80BPM 慢摇(持续层:胯八字+交替肩滚)

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] One static full-body vertical shot, 11.0 seconds, starting exactly from the hands-on-hips stance of <Picture 1>; all identity, outfit and room detail come from <Picture 1> alone. Continuous layer for the full take: a slow-sway groove at ~75-85 BPM — hips trace a smooth side-to-side figure-eight, knees flex with each weight shift, shoulders roll alternately, and the torso sways gently over the moving hips; an easy relaxed smile holds throughout. 0.0-1.0 s: hips push right, return to center as the shoulders pick up the groove, then push left. 1.0-3.0 s: hands leave the hips and hang loose; hip pops continue right-left on the beat as the right arm bends and lifts. 3.0-5.0 s: the right arm reaches out to the side, then sweeps up past the shoulder to overhead while the hips pop right and the head tips right; the arm arcs back down as everything re-centers. 5.0-6.5 s: the left arm lifts sideways and holds while the shoulders alternate; then both arms open into a wide side spread with the hips pushing right and the weight settling onto the right leg. 6.5-8.0 s: the torso leans right with a slight upward glance, then the arms float down and gather to the sides as the hips push left. 8.0-10.0 s: hands return to the hips; hip pops and shoulder rolls keep cycling right-left, with the head turning to glance right during one left-lean. 10.0-11.0 s: the right arm extends out to the side pointing as the hips re-center, one final hip push right, and the pose holds frozen at the cut.

overall_soundscape: The music dominates the track; only a quiet home room tone sits underneath, with no distinct environmental events.

non_diegetic_music: Laid-back slow-sway track around 75-85 BPM with soft, relaxed vocals and light sparse hi-hats; groove builds in from about 2 s and is cut at the end without fade-out.
```

---

### 11_萌爱moi_站在光里(原 17.3s → 截取 0-15s)
首帧:`11_萌爱moi_202608_首帧.jpg` | 单镜头固定近全身景,6 重拍 K-pop 风舞蹈(原片 15-17.3s 收尾余韵已舍弃)

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Vertical real-life dance clip in one single continuous take, camera locked on a fixed tripod with near-full-body framing unchanged for the whole 15 seconds; every visual detail of the dancer, her outfit and the room comes solely from <Picture 1>. From the opening pose of fingertips resting on the shoulders with elbows out, she dances a continuous upbeat K-pop-style cover for 15.0 seconds. Continuous layer throughout: knees stay soft with a light bounce on the beat, shoulders and hips sway gently side to side, the high ponytail trails every head movement with a slight delay, and a bright playful smile is maintained. 0.0-1.7s: she holds the shoulder-touch while slowly turning her head from left to right, gaze sweeping across the lens. 1.7-2.5s (accent 1): both arms burst open at once, the left arm shooting straight overhead and the right arm swinging down and out at 45 degrees, torso leaning left, head tipping back, mouth opening in a big grin. 2.5-3.5s: the left arm stays high while the right arm draws one full vertical circle at her side. 3.5-4.5s (accent 2): the right index finger points straight at the camera as the left foot steps forward, chin lifting with a cheeky brow raise. 4.5-5.5s: still pointing, she pivots about 90 degrees left on her left foot, ponytail swinging wide. 5.5-6.5s (accent 3): the right arm sweeps over her head as she rotates back to face the lens, both arms meeting overhead in a ring while the right knee rises thigh-high, balancing on the left leg. 6.5-7.5s: the raised leg lowers, the arms melt down to chest height with palms turned up in an offering shape, and she sinks into a small half-squat. 7.5-8.5s (accent 4): she springs up out of the squat, both arms flinging overhead into a wide V with a tiny hop off the floor, then lands. 8.5-9.5s: after landing the arms drift down and the right hand brushes past her cheek and hair, head tilting with a soft smile. 9.5-10.5s (accent 5): the right index finger jabs a point at the camera combined with a quick wink, torso tipping right. 10.5-12.5s: she keeps the point with the left hand now on her hip, swaying in small side-to-side shifts and nodding her head twice on the beat. 12.5-13.5s (accent 6): the right arm pulls back and both arms sweep outward in large arcs to a full side-extended T line. 13.5-15.0s: holding the open-arm line she rotates about 45 degrees into a three-quarter stance, one arm reaching forward and the other back as if greeting the light, ponytail drifting, ending the fifteenth second in half-profile with a settled smile.

overall_soundscape: Quiet indoor room tone under the music, with soft thuds and scuffs of platform boots stepping and pivoting on the wooden floor and a faint rustle of fabric on each arm swing.

non_diegetic_music: An upbeat K-pop-style dance track at a steady mid-tempo, bright and playful, with every accent landing exactly on the musical hits.
```

---

### 12_栗子Ai绘画_凡人修仙传元瑶(7.4s)
首帧:`12_栗子Ai绘画_20260_首帧.jpg` | 单镜头 AI 动画,极慢推镜(全身→胸像),灵气球→炸散→凝珠+末尾字幕

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Chinese xianxia-themed AI-painted animation with a soft donghua art style, delicate brushwork and cinematic glow, one single continuous 7.4-second shot in which the camera pushes in very slowly and smoothly from a full-body framing to a bust shot; all visuals of the character, costume and scenery come exclusively from <Picture 1>. Drifting petals float through the frame for the entire duration. 0.0-0.8s: from the standing pose with hands folded inside the sleeves, she lifts her chin and raises her gaze toward the distant moon halo while hair strands and hem begin to stir in a light breeze. 0.8-2.0s: the right arm rises slowly out of the wide sleeve, the sleeve sliding down to bare the wrist, fingertip reaching toward the moonlight. 2.0-3.0s: a small pale-cyan orb of spiritual light condenses just above the fingertip, its glow lighting her face from below. 3.0-4.2s: as the camera closes in, a faint smile surfaces and the orb swells brighter, drawing a few petals into a slow orbit around it. 4.2-5.2s: the orb bursts softly into a swarm of firefly-like motes scattering around her; her eyes close and her head tips back slightly in serene absorption as the wind lifts hair and skirts more strongly. 5.2-6.2s: the push-in reaches chest level; she opens her eyes, raises the left hand, cups a handful of drifting motes in both hands and gazes down into her palms. 6.2-7.4s: the motes fuse into one gently glowing pearl; she looks up toward the camera with a soft smile and holds the cradling pose, while in the final second a small line of white Chinese caption fades in along the bottom of the frame.

overall_soundscape: High, airy night ambience of soft wind over clouds, with a delicate crystalline shimmer as the orb condenses and a fine sparkle-chime sweep as it bursts into drifting light dust.

non_diegetic_music: A gentle ethereal Chinese-style instrumental, slow airy pads over plucked guzheng and faint strings, dreamy and wistful.
```

---

### 13_熙熙驾到啦_cos银月(10.9s)
首帧:`13_熙熙驾到啦_202609_首帧.jpg` | 单镜头,7.0s 前固定全身景→之后缓推至半身;害羞展示链(平举→抱臂→侧身捻发→比心→指镜头 wink)

```
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Vertical real-life cosplay video in one single continuous take: the camera holds a fixed full-body framing until 7.0s, then pushes in slowly and smoothly to a half-body close-up by the end; the cosplayer's entire look and the room are taken only from <Picture 1>. From a standing-at-ease pose with arms hanging at the sides, the cosplayer performs a shy show-off sequence. 0.0-1.0s: small weight shifts side to side while the head tilts toward one shoulder, a faintly nervous closed-lip smile aimed at the lens. 1.0-2.5s: both arms float up to a shoulder-height side stretch with palms down as the head turns toward the upper left, gaze drifting into the distance and the smile softening. 2.5-3.8s: holding the stretch, the wrists flap twice like small wings and the smile widens enough to show teeth. 3.8-4.8s: the arms fold back in with hands crossing over the chest, chin dropping so the gaze falls to the floor in a shy, lightly blushing expression. 4.8-6.0s: keeping the arms crossed, the body rotates about 90 degrees to the left into a side stance while the head turns back over the shoulder toward the camera, the long side locks swinging to the front. 6.0-7.0s: in side stance the right hand rises to slowly twirl one long front lock of hair, left arm hanging, eyes glancing down diagonally with a light smile. 7.0-8.0s: as the camera begins pushing in, the cosplayer turns back to face front and shapes a complete heart with both hands at chest height, head slightly cocked and eyes expectant. 8.0-9.0s: holding the heart, the body sways left and right with the hair swaying along, the smile deepening into crescent eyes. 9.0-10.2s: the heart releases; the right arm extends with the index finger pointing straight at the lens together with a quick wink, then the arm eases back slightly while the smile holds. 10.2-10.9s: the finger keeps pointing at the camera with a bright open-eyed smile while a small line of white Chinese caption fades in at the bottom center, settling into the half-body framing at the end.

overall_soundscape: A calm bedroom room tone with faint fabric rustle on each arm movement and the soft pad of shoes during the small weight shifts.

non_diegetic_music: A light, cute J-pop-style tune over a bouncy kawaii electronic beat, playful and sweet.
```

---

## I. 物理摄影机视角案例库(视角写法规范 · 2026-10-07 并入)

> 来源:用户提供写法标准全文。**核心原则(见 I.25):不要"命名效果"(`Extreme low angle`),要"定义产生效果的现实条件"(物理位置/高度/距离/光轴/空间关系/物理结果)。** 所有进提示词的视角描述以本章为准;E5 是本章"机位=实物"的实证摘要,E6 附是落地纪律。

### I.0 通用摄影机隐藏锁

适用于所有角度。建议放在 `camera_system` 前部，作为统一底层约束。

```text
PHYSICAL CAMERA BASELINE:

The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment.

The camera itself remains completely outside the visible frame.

Only the recorded image is visible.

No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition.

The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective.

Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image.

The perspective must remain physically consistent with the camera's actual location.

Any apparent perspective exaggeration must result naturally from camera-to-subject distance and lens characteristics.

The camera does not physically appear in its own recorded image.
```

---

### I.1 正常平视 / Eye-Level

不要只写：

```text
eye-level shot
```

推荐：

```text
CAMERA — NATURAL EYE-LEVEL VIEW:

The recording viewpoint comes from a real physical camera positioned approximately at <Subject 1>'s natural eye level.

The lens faces directly toward <Subject 1> from a natural frontal or subtle three-quarter position.

The camera remains at a stable human-height position.

The optical axis is approximately horizontal.

<Subject 1>'s face, shoulders, torso, and surrounding environment remain spatially proportional to a natural human viewpoint.

The image should feel as though a person is standing naturally in front of <Subject 1> and recording from their own eye level.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.

The perspective must come from the actual eye-level camera position rather than from a digitally simulated normal view.
```

---

### I.2 轻微低机位 / Slight Low Angle

重点不是"低角度"，而是：

**摄影机低于胸口或腰部 + 稍微向上。**

```text
CAMERA — SLIGHTLY ELEVATED LOW VIEW:

The recording viewpoint comes from a real physical camera positioned noticeably below <Subject 1>'s eye level, approximately around lower torso height.

The camera is physically closer to the floor than the subject's face.

The lens points moderately upward toward <Subject 1>'s upper body.

The optical axis is angled upward rather than horizontal.

<Subject 1> therefore appears naturally slightly taller and more imposing than from an eye-level viewpoint.

The upward perspective is subtle and physically believable.

The camera-to-subject spatial relationship must remain consistent throughout the shot.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not imitate the effect by simply tilting a normal eye-level image upward.
```

---

### I.3 腰部低机位 / Waist-Level Low Angle

适合人物舞蹈、时装、全身。

```text
CAMERA — WAIST-LEVEL LOW POSITION:

The recording viewpoint comes from a real physical camera positioned approximately around <Subject 1>'s waist level.

The camera is physically below the subject's shoulders and face.

The lens points upward toward the torso and head.

The floor is therefore visible as a lower spatial plane beneath the performer.

The subject's upper body rises above the camera's optical axis.

The perspective is clearly lower than eye level but remains physically plausible rather than extreme.

The apparent increase in the subject's height comes from the actual low camera position.

The camera remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not create the effect by cropping a normal shot or digitally stretching the subject vertically.
```

---

### I.4 膝盖高度 / Knee-Level Low Angle

比腰部更明显。

```text
CAMERA — KNEE-LEVEL LOW POSITION:

The recording viewpoint comes from a real physical camera positioned approximately at <Subject 1>'s knee height.

The lens is substantially below the subject's torso.

The lens points upward toward the upper body and face.

The foreground floor is physically close to the camera and occupies a meaningful portion of the lower spatial field.

<Subject 1>'s legs rise from the foreground while the torso and head extend upward through the frame.

The lower parts of the body are naturally closer to the camera than the face.

The perspective creates clear but physically accurate vertical exaggeration.

The camera remains completely outside the visible image.

No filming equipment or support structure is visible.

The effect must come from the real camera height and distance, not from digital perspective manipulation.
```

---

### I.5 贴地极端仰视 / Floor-Level Extreme Low Angle

这是最值得复用的一类。

```text
CAMERA — FLOOR-LEVEL EXTREME LOW VIEW:

The recording viewpoint comes from a real physical camera positioned directly at floor level.

The lens is approximately 5–15 cm above the ground.

The camera is physically located beneath <Subject 1>'s body.

The lens points sharply upward toward <Subject 1>.

The floor is physically extremely close to the lens and creates strong foreground perspective.

<Subject 1> rises above the camera's viewpoint.

Her legs, torso, arms, face, and nearby objects follow physically consistent perspective relationships according to their distance from the lens.

Nearby body parts become visually larger because they are physically closer to the camera.

The face and upper body may become strongly foreshortened from below.

The perspective should feel like a real camera physically resting almost at ground level and looking upward.

The camera itself remains completely outside the visible frame.

No visible filming equipment, support structure, or mounting object appears.

Do not create this viewpoint by tilting down a normal camera from human height.

Do not crop a normal shot.

Do not use digital zoom or artificial perspective warping.
```

---

### I.6 极端虫眼 / Worm's-Eye View

它和一般低角度不同：

**主体明显高于镜头，空间高度感成为核心。**

```text
CAMERA — WORM'S-EYE SPATIAL VIEW:

The recording viewpoint comes from a real physical camera positioned extremely close to the ground beneath <Subject 1>.

The camera is only a few centimeters above the floor.

The lens points strongly upward.

The performer physically towers above the viewpoint.

The floor and lower foreground are extremely close to the lens, while the head and upper body are much farther away.

This creates strong natural foreshortening and vertical spatial exaggeration.

The surrounding ceiling and upper environment may naturally enter the background because of the steep upward optical axis.

The perspective must result from the camera's real ground-level position.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.7 高机位俯视 / High-Angle View

注意：不能直接变成正上方。

```text
CAMERA — ELEVATED HIGH POSITION:

The recording viewpoint comes from a real physical camera positioned clearly above <Subject 1>'s head and shoulder level.

The camera is physically elevated above the performer.

The lens points diagonally downward toward <Subject 1>.

The optical axis is angled downward rather than vertical.

The upper surfaces of the head, shoulders, clothing, and nearby environment become more visible because the camera is physically above the subject.

The subject remains spatially connected to the surrounding floor.

The perspective must come from the actual elevated camera position.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not simulate this by simply rotating a normal-perspective image downward.
```

---

### I.8 强俯视 / Extreme High Angle

比普通高机位明显很多，但仍然不是 90°。

```text
CAMERA — EXTREME ELEVATED VIEW:

The recording viewpoint comes from a real physical camera positioned significantly above <Subject 1>.

The camera is physically several times higher than the subject's head.

The lens points steeply downward toward <Subject 1>.

The optical axis forms a strong downward diagonal.

The floor becomes a major visible spatial plane.

The top surfaces of <Subject 1>'s head, shoulders, arms, and surrounding objects become strongly visible.

<Subject 1>'s vertical height is visually compressed because the camera observes her from far above.

The perspective must remain physically consistent with the elevated camera position and subject distance.

The camera remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not create the effect by cropping, flattening, or digitally warping an ordinary shot.
```

---

### I.9 正上方 90° 俯拍 / True Top-Down

这是最容易被 H3 做成"高机位斜拍"的一种，所以一定强调：

**vertical optical axis + directly above。**

```text
CAMERA — TRUE TOP-DOWN VIEW:

The recording viewpoint comes from a real physical camera located directly above <Subject 1>.

The camera is physically aligned with the vertical axis above the performer.

The lens points straight downward toward the floor.

The optical axis is perpendicular to the floor.

<Subject 1> is physically located directly beneath the camera.

The composition is observed from an approximately 90-degree overhead viewpoint.

The floor becomes the dominant spatial plane.

The subject's body is arranged according to true overhead geometry rather than a diagonal elevated perspective.

The top surfaces of the head, shoulders, arms, hands, clothing, and surrounding objects are visible according to their real positions.

There is no forward or backward eye-level perspective.

The camera remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not interpret this as a normal high-angle shot.

Do not tilt a normal camera upward or downward to imitate the result.

The viewpoint must originate from the camera physically being directly above the subject.
```

---

### I.10 斜上方俯拍 / Diagonal Overhead

适合既看人物顶部，又保持脸部。

```text
CAMERA — DIAGONAL OVERHEAD POSITION:

The recording viewpoint comes from a real physical camera positioned above and slightly in front of <Subject 1>.

The camera is physically elevated above the head.

The lens points diagonally downward toward the upper body.

The optical axis is steeply downward but not vertical.

The camera remains clearly higher than the performer while retaining some frontal facial visibility.

The tops of the head and shoulders are naturally exposed by the elevated perspective.

The body extends downward and away from the camera according to real spatial depth.

The effect must result from the camera's actual elevated front-facing position.

The camera remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.11 侧面平视 / True Side Profile

这里不需要强调"camera angle"，而是强调**与主体横向共面**。

```text
CAMERA — TRUE SIDE POSITION:

The recording viewpoint comes from a real physical camera positioned directly to the side of <Subject 1>.

The camera and <Subject 1> remain on the same horizontal height.

The lens points laterally across the subject's body.

The camera observes <Subject 1> in a true side profile.

The body remains aligned along a clear lateral axis within the frame.

Depth is revealed through the subject's actual distance from nearby objects rather than through an artificially rotated composition.

The camera remains physically stationary relative to the environment unless movement is explicitly specified.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.12 三分之二侧前方 / Front Three-Quarter

适合人物写真、舞蹈和表演。

```text
CAMERA — FRONT THREE-QUARTER POSITION:

The recording viewpoint comes from a real physical camera positioned diagonally in front of <Subject 1>, approximately 30–45 degrees from her frontal axis.

The lens faces toward the front-side plane of the body rather than directly perpendicular to the body.

One side of the face and body is naturally more prominent than the other.

The camera remains at approximately eye or upper-torso height.

The perspective comes from the camera's real diagonal position relative to the performer.

The body orientation, facial direction, and environmental depth must remain physically consistent with this camera placement.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.13 正后方 / Rear View

```text
CAMERA — DIRECT REAR POSITION:

The recording viewpoint comes from a real physical camera positioned directly behind <Subject 1>.

The lens points toward her back along the same central body axis.

The camera remains physically behind the performer rather than merely rotating the subject toward the rear.

Her hairstyle, shoulders, back, clothing structure, arms, and surrounding environment are observed from their real rear-side positions.

Depth is determined by the actual distance between the performer and the camera.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.14 后方三分之四 / Rear Three-Quarter

```text
CAMERA — REAR THREE-QUARTER POSITION:

The recording viewpoint comes from a real physical camera positioned diagonally behind <Subject 1>, approximately 30–45 degrees from her rear axis.

The lens observes both the back plane and one side of the body.

The subject remains physically oriented toward the opposite direction.

The visible face, if present, must remain naturally consistent with the subject's actual head rotation.

The camera position creates the perspective rather than rotating or mirroring the recorded image.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.15 贴身近距离广角 / Extreme Close Wide Perspective

这种不是"角度"，但和 H3 的透视稳定关系非常密切。

```text
CAMERA — EXTREMELY CLOSE PHYSICAL DISTANCE:

The recording viewpoint comes from a real physical camera positioned very close to <Subject 1>'s upper body.

The lens is physically only a short distance from the face and shoulders.

The camera remains close to the subject rather than using digital zoom.

Nearby facial and body features naturally appear larger because of their physical proximity to the lens.

Features farther from the camera recede naturally in perspective.

Small head movements create visible perspective changes because the camera-to-subject distance is very short.

The image should feel physically close and intimate while preserving realistic anatomy.

The camera remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not imitate this distance using digital zoom or artificial facial enlargement.
```

---

### I.16 地面侧向 / Ground-Level Side View

这个和低角度不同：

**不一定明显向上，而是摄影机真正贴地横向观察。**

```text
CAMERA — GROUND-LEVEL SIDE VIEW:

The recording viewpoint comes from a real physical camera positioned only a few centimeters above the floor.

The camera is physically beside <Subject 1> rather than in front of her.

The lens points laterally across the scene with only a very slight upward orientation.

The floor is extremely close to the lens and forms a strong foreground plane.

The subject's legs, lower body, and surrounding floor geometry dominate the near field while the torso rises naturally above them.

The perspective must come from the camera's actual ground-level lateral position.

The camera remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not turn this into an ordinary waist-level side shot.
```

---

### I.17 背后贴近跟随 / Close Rear Tracking View

需要动态跟拍时使用。

```text
CAMERA — CLOSE REAR FOLLOWING POSITION:

The recording viewpoint comes from a real physical camera positioned closely behind <Subject 1>.

The camera follows her actual movement through the same physical environment.

The camera remains at approximately upper-torso height.

The distance between the camera and the performer stays physically close and consistent unless movement naturally changes that distance.

The camera follows the performer rather than orbiting around her.

Her movement through space remains continuous.

The background shifts according to real camera translation and subject movement.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not generate an external observer camera inside the scene.
```

---

### I.18 手持人类视角 / Handheld Human View

这里不要写"handheld camera"完事，要建立"人的物理高度 + 手部轻微运动"。

```text
CAMERA — HUMAN HANDHELD VIEW:

The recording viewpoint comes from a real physical camera held by an unseen person.

The camera is approximately at natural human chest-to-eye height.

Small natural handheld positional fluctuations occur as the operator physically holds the camera.

The movement is caused by subtle human hand and body motion rather than mechanical stabilization.

The camera remains close enough to feel personally operated.

The viewpoint maintains one continuous physical relationship with <Subject 1>.

The recording device itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.

Do not create floating-camera movement.

Do not create crane-like movement.

Do not create orbital camera motion unless explicitly specified.
```

---

### I.19 荷兰角 / Dutch Angle

Dutch angle 的本质不是"俯视"或者"仰视"，而是：

**摄影机自身绕镜头光轴发生 roll。**

```text
CAMERA — PHYSICAL DUTCH ANGLE:

The recording viewpoint comes from a real physical camera positioned at a natural human viewing height.

The camera remains physically stable in position but is deliberately rotated around its optical axis.

The horizon line is therefore visibly tilted.

The environment, floor, walls, and body geometry remain physically consistent with this single camera roll.

The entire frame tilts together as one continuous optical view.

The subject itself is not rotated independently from the environment.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.

The tilted composition must result from physical camera rotation rather than digitally rotating the finished image.
```

---

### I.20 向上倾斜 / Upward Tilt

这个和"仰视"也要分开。

**相机位置可以正常，但镜头光轴向上。**

```text
CAMERA — PHYSICAL UPWARD TILT:

The recording viewpoint comes from a real physical camera positioned at a stable human-height position.

The camera remains physically stationary.

The lens is physically tilted upward toward <Subject 1>'s face and upper body.

The lower part of the environment remains connected to the camera's real position.

The upward optical axis produces a natural change in the amount of ceiling and upper background visible in the frame.

The subject does not move merely to create the angle.

The viewpoint must be generated by the actual orientation of the camera lens.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.21 向下倾斜 / Downward Tilt

```text
CAMERA — PHYSICAL DOWNWARD TILT:

The recording viewpoint comes from a real physical camera positioned at a stable human-height or slightly elevated position.

The camera remains physically stationary.

The lens is physically tilted downward toward <Subject 1>.

The optical axis points downward while the camera remains in the same physical location.

The floor and nearby foreground become more prominent according to the real downward viewing direction.

The subject remains spatially grounded within the environment.

The viewpoint must come from actual lens orientation rather than digitally rotating the final frame.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.
```

---

### I.22 "人物靠近镜头"透视增强模块

当舞蹈动作需要和极端视角联动时，追加这一段。

```text
SPATIAL PERSPECTIVE RESPONSE:

<Subject 1>'s movement must physically change her distance from the camera.

When she moves toward the camera, the nearest body parts and props naturally become larger because of reduced camera-to-subject distance.

When she moves away, the same elements naturally become smaller and deeper in the frame.

The perspective change must happen through real spatial movement.

Do not enlarge the subject digitally.

Do not use digital zoom to imitate the perspective change.

Do not independently scale body parts.

The visual exaggeration must come from ordinary optical perspective produced by physical distance.
```

---

### I.23 极端视角通用"防简化锁"

对于特别容易被 H3 做错的角度，直接追加：

```text
PERSPECTIVE AUTHENTICITY LOCK:

The requested perspective is defined by the physical location and orientation of the recording camera, not by a visual effect.

The camera must occupy the specified physical height and distance relative to the subject.

The optical axis must point in the specified direction.

All perspective distortion must follow ordinary physical optics.

Do not approximate the requested viewpoint with cropping.

Do not approximate it with digital zoom.

Do not approximate it by rotating the finished image.

Do not artificially stretch or compress the subject.

Do not change the subject's anatomy to imitate the perspective.

The environment must remain geometrically consistent with the camera's actual position.

The camera remains unseen and outside the visible frame.
```

### I.24 最推荐的 H3 组合结构

以后不要把几十个角度描述全部塞进去。

每个 Shot 建议按照这个顺序：

```text
[Shot N]

[1. CAMERA PHYSICAL PLACEMENT]
The recording viewpoint comes from a real physical camera positioned ...

[2. HEIGHT]
The lens is approximately ... above/below ...

[3. DISTANCE]
The camera is physically ... from <Subject 1>.

[4. OPTICAL AXIS]
The lens points ...

[5. SPATIAL RELATION]
<Subject 1> is physically ...

[6. PHYSICAL RESULT]
Therefore, the image naturally shows ...

[7. MOVEMENT RESPONSE]
When <Subject 1> moves ..., her distance from the camera ...

[8. CAMERA LOCK]
The camera remains ...
The camera itself remains completely outside the visible frame.
No visible filming equipment or support structure appears.
```

---

### I.25 一个最重要的 H3 写法原则

不要：

```text
Extreme low angle.
```

而是：

```text
The recording viewpoint comes from a real physical camera positioned directly at floor level.

The lens is only 5–15 cm above the ground.

The camera is physically beneath <Subject 1>.

The lens points sharply upward toward her upper body.

The floor is extremely close to the lens.

Her upper body rises above the viewpoint and becomes naturally foreshortened.

The perspective becomes stronger when she physically leans toward the camera.

The camera itself remains completely outside the visible frame.

No visible filming equipment or support structure appears.

The effect must come from the camera's actual physical position, distance, and optical orientation.
```

前者是在**命名效果**。

后者是在**定义产生效果的现实条件**。

H3 更应该吃后者。

---

## J. 写真式姿势-运镜章(母模板+9支范本 · 2026-10-07 并入)

> 来源:9 支写真式视频密集抽帧反推(0.5s 密帧+0.08/0.03 双阈值切镜检测+切点 pts_time 定位,抽帧拼图逐帧核看)。
> 片型分流:V1 一镜到底(A型) / V2·V3·V6·V9 快剪 montage(C型,切点全部落在姿势间隙) / V4 一镜+甩镜旋转转场 / V5 五姿势硬切流 / V7·V8 锁定自拍手势链(A型锁定)。
> 视角写法**全部按 I 章物理定义式**(命名式 "low angle/eye-level/high angle" 一律不用);人物/服装/道具由图1锚定、正文零外貌;每支自包含可直接粘贴;声音未核听,overall_soundscape 为画面推断,non_diegetic_music: N/A 不脑补配乐。

### J0 写真母语言十律(运镜-姿势关系,反推实证)

1. **细节上摇开场**:镜头从身体局部(胸衣/脚/腿)低机位缓慢上摇到脸——局部引出人物,摇到脸之前人物几乎不动。
2. **大姿势锁死+微活性**:每个 pose 的躯干/腿完全锁定,只有手指(勾裙边/比心收放)、头角度(侧→正→歪)、眼神(离镜→回镜)、眨眼在动。"看着静止其实一直活着"是呼吸感来源。
3. **机位高度=姿势语义**:躺姿→物理高位斜俯;趴床托腮→眼平略高;坐/跪坐→眼平;腿部展示→贴地仰;背身回眸→低位平视。**换姿势=换机位物理位置**,从一个机位拍完全片是禁区。
4. **推近收束**:结尾镜头缓慢推到面部大特写,浅笑直视镜头。
5. **贴地低机位是签名镜头**:贴地/贴水(5-15cm)只服务"慵懒贴地/腿线展示"语义;90° 侧置倾斜构图(物理 dutch roll)只服务"贴水俯卧"单一姿势。
6. **固定自拍机位+手势序列**:镜头纹丝不动,人物做手势链(指天→指镜头→指地→双手交叠),手势之间表情变化(wink/抿嘴)。
7. **眼神接触节拍**:每个 pose 的"高光帧"=眼看镜头瞬间;视线先离开(看手/闭眼)再回镜头,构成无声节拍。
8. **手永远在做事**:比心、框脸、托腮、抱膝、拢发、撩发、玩领带、举面具、勾裙边——没有一只手闲垂。
9. **切点纪律**:硬切只落在"上一姿势已摆稳、下一姿势已就位"的间隙;动作不跨切连续;快闪连切(0.1-0.5s)只用于结尾收束。
10. **环境虚化留白**:全部浅景深,背景(人群/海平线/课桌排/楼梯)只供纵深与色彩,人物占画面 70%+。

### J1 母模板(姿势表填空式,视角按 I 章物理式)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic posed-portrait video, [DURATION]s, exactly one performer: the woman shown in <Picture 1>. Her face, hairstyle, outfit and any props come ONLY from <Picture 1>; this text contains zero appearance description and never redesigns her.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment. The camera itself remains completely outside the visible frame. Only the recorded image is visible. No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition. The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective. Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image. All apparent perspective exaggeration must result naturally from camera-to-subject distance and lens characteristics.

POSE-AND-CAMERA LAW — applies to every shot:
1. One settled pose per shot. The torso, arms and legs of the pose stay LOCKED; only fingers, head angle, eye-line and blinks stay alive inside the hold. She looks still but is never frozen.
2. The camera's PHYSICAL POSITION matches the pose semantics — written as real placement, never as an angle name: lying pose → the camera physically above her, lens angled diagonally downward; chin propped → camera at her eye level or slightly above; sitting or kneeling → camera at her eye height, optical axis horizontal; leg display → camera resting on the floor 5-15cm above the ground, lens pointing up along her legs; back-turned glance → camera low and level beside her. Change the pose, move the camera's physical position.
3. Her hands are never idle: holding, framing her face, gathering, playing with fabric, hair, or the prop in tiny continuous motions.
4. The highlight frame of every pose is the moment her eyes return to the lens; before that she looks away, looks down, or closes her eyes, then gives the lens a soft direct gaze.
5. Camera motion is small and motivated only: a slow tilt-up from a body detail to introduce her, a slow push-in for emphasis, a tiny handheld sway always present. No orbit, no wide coverage.
6. A hard cut lands only in the gap between two settled poses; no action crosses a cut; each cut opens on the new pose already in place.
7. The film ends with a slow push-in until the lens is only a short physical distance from her face — a big facial close-up, a soft held smile into the lens.

SHOT TABLE (one row per pose):
[00:00.000-00:0X.XXX | SHOT n | camera physical position/height/distance + optical axis | framing | locked pose: torso/arms/legs | hand micro-action | gaze beat | camera move]

overall_soundscape: [ENVIRONMENT AMBIENT INFERRED FROM THE SCENE]
non_diegetic_music: N/A
```

### J2 V1·红毯银钻礼服·一镜到底上摇摆拍(9.9s)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic posed-portrait video, 9.9s, ONE continuous take, no cuts. Exactly one performer: the woman shown in <Picture 1>; her face, updo hairstyle, jewelry and the embellished gown come only from <Picture 1>, zero appearance text. World: an evening gala red-carpet corner — deep red velvet backdrop with blurred white signage and out-of-focus suited crowd; warm event lighting, shallow depth of field, she fills most of the frame.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment. The camera itself remains completely outside the visible frame. Only the recorded image is visible. No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition. The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective. Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image.

POSE-AND-CAMERA LAW:
1. The pose stays LOCKED; only fingers, head angle, eye-line and blinks stay alive inside the hold; she looks still but never frozen.
2. Her hands are never idle: resting, framing her face, heart-gesturing in tiny continuous motions.
3. The highlight frame is the moment her eyes return to the lens; she first looks aside or down, then gives a soft direct gaze.
4. Camera motion is small and motivated: one slow physical tilt-up to introduce her, then a stable hold with a tiny handheld sway; no orbit, no wide coverage.

TIMELINE:
[00:00.000-00:01.500] The recording viewpoint comes from a real physical camera positioned directly in front of her at lower-chest height, physically close to the gown so the embroidered bodice fills the frame. The camera remains in one place while the lens is tilted physically upward toward her face; the upward optical axis carries the view from the bodice past the collarbones and necklace to her jaw and left-facing profile. Her hands rest lightly on the waistline, fingertips barely moving on the fabric.
[00:01.500-00:03.000] The camera levels into a NATURAL EYE-LEVEL position: physically at her eye height, a natural frontal position with a subtle three-quarter angle, optical axis approximately horizontal, stable human-height position; her face, shoulders and torso stay spatially proportional to a natural human viewpoint. She turns her head from profile toward the lens; a soft smile lands as the eyes meet the lens; bust-up framing.
[00:03.000-00:06.500] POSE LOCK: both hands rise beside her cheeks and form a heart / face-framing gesture; elbows stay in; only the fingers open and close in micro-motions while the head tilts gently with the gesture; gaze holds the lens with two brief blink-breaks. The camera holds the same eye-level physical position with a tiny handheld sway.
[00:06.500-00:07.500] The gesture folds: one hand brushes near her lips and chin, wrist rotating slowly, then both hands lower.
[00:07.500-00:09.900] CLOSING POSE: both arms cross loosely low at the waist, shoulders relaxed; her head turns to frame-right with a calm smile off-lens; the camera keeps the same eye-level physical position, bust-up, tiny sway, to the end.

overall_soundscape: quiet gala-hall room tone with a distant blurred crowd murmur, inferred from the scene.
non_diegetic_music: N/A
```

### J3 V2·黑翼面具桌面写真·快剪六姿势(6.9s)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic posed-portrait montage, 6.9s, six hard-cut shots, ONE pose per shot. Exactly one performer: the woman shown in <Picture 1> — face, long dark hair, black mini dress, black wings and the crystal mask come only from <Picture 1>, zero appearance text; use the mask and wings exactly as shown. World: a dim modern dining room at dusk, long table and grey windows behind; cool low-key window light, shallow depth of field.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment. The camera itself remains completely outside the visible frame. Only the recorded image is visible. No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition. The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective. Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image.

POSE-AND-CAMERA LAW:
1. One settled pose per shot; torso and legs LOCKED; only fingers, head angle, eye-line and blinks stay alive.
2. The camera physically rests ON THE TABLETOP for every shot: positioned at the same height as her seated torso, a short distance in front of her, optical axis horizontal (SHOT 1 starts slightly below the table edge with the lens angled gently up along her body). Changing shots changes her pose, not the camera's physical home on the table.
3. Hands are never idle: the mask is raised, lowered, held, or cradled; hair is flicked; fabric is touched.
4. Every pose's highlight frame is her eyes returning to the lens; before that she looks away or down.
5. A hard cut lands only in the gap between two settled poses; no action crosses a cut. One whip-style hair-flick transition is allowed at the written moment; motion blur covers it.

SHOT TABLE:
[00:00.000-00:00.930 | SHOT 1 | the camera rests on the tabletop slightly below its edge, lens angled gently upward | extreme close-up traveling up | she sits ON the table, stocking-clad legs stretched across the tabletop toward the lens, so her legs are physically closest to the lens and naturally largest | mask raised beside her head in one hand | gaze over the mask to lens | slow tilt-up from the legs to her full seated pose]
[00:00.930-00:02.200 | SHOT 2 | camera on the tabletop, level with her seated torso, optical axis horizontal | full body seated | same seated pose, wings spread behind | mask held up at head side, fingers adjusting it | direct gaze | tiny sway]
[00:02.200-00:02.400 | TRANSITION | one fast hair-flick whip with motion blur | — | — | — | whip pan]
[00:02.400-00:03.370 | SHOT 3 | camera on the tabletop, optical axis horizontal | medium front | seated facing lens, both wings fully spread | mask lowered to rest between her knees, both hands on it | direct gaze | tiny sway]
[00:03.370-00:05.000 | SHOT 4 | camera on the tabletop | side profile medium | side-seated, knees drawn up, one arm hugging them | free hand touches her head, hair flicked once | eyes to lens past the knee | tiny sway]
[00:05.000-00:06.000 | SHOT 5 | camera on the tabletop | three-quarter medium | seated turned three-quarter, both legs folded sideways and crossed | one hand at her neck/collar | over-shoulder gaze to lens | tiny sway]
[00:06.000-00:06.900 | SHOT 6 | camera on the tabletop, physically a little higher than her kneeling line, lens angled gently down | medium | kneeling upright on the tabletop | the mask cradled in both hands before her knees | direct gaze, soft smile | tiny sway]

overall_soundscape: quiet dusk room tone with a faint air-conditioner hum, inferred from the scene.
non_diegetic_music: N/A
```

### J4 V3·教室JK写真·快剪五姿势(6.9s)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic posed-portrait montage, 6.9s, five hard-cut shots, ONE pose per shot. Exactly one performer: the student girl shown in <Picture 1>; face, hair and the sailor-style school uniform come only from <Picture 1>, zero appearance text. World: an empty retro classroom — wooden desks in rows, large windows with brown curtains, green trees outside; soft window daylight with a slightly desaturated nostalgic grade, shallow depth of field.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment. The camera itself remains completely outside the visible frame. Only the recorded image is visible. No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition. The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective. Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image.

POSE-AND-CAMERA LAW:
1. One settled pose per shot; torso and legs LOCKED; only fingers, head angle, eye-line and blinks stay alive.
2. The camera's physical position changes with the pose and is always written as real placement: SHOT 1 sits low in the room; SHOTS 2/4/5 sit at her eye height; SHOT 3 sits low and level beside her.
3. Hands are never idle: adjusting the collar or tie, covering the face, brushing hair, resting on the skirt.
4. Every pose's highlight frame is her eyes returning to the lens; before that she looks aside, hides her face, or looks down.
5. A hard cut lands only in the gap between two settled poses; no action crosses a cut.

SHOT TABLE:
[00:00.000-00:02.400 | SHOT 1 | the camera is positioned low in the classroom, around bench height, physically below her face and clearly below her raised seat, lens angled moderately upward, her extended leg physically closest to the lens and therefore naturally larger | low full body | she sits ON a classroom desk facing the window, one leg extended straight down toward the floor, the other bent on the desk | both hands at her collar, adjusting the tie in tiny motions | gaze down at her hands, then one glance to lens | locked low camera, tiny sway]
[00:02.400-00:04.130 | SHOT 2 | camera at her eye height, a natural frontal position, optical axis horizontal | medium front | standing, body bent slightly forward toward the lens | both hands covering her mouth and nose in a shy gesture, fingers pressing lightly | eyes looking at lens above her hands | tiny sway]
[00:04.130-00:05.030 | SHOT 3 | camera low in the room, around seat height, physically beside her and level, lens horizontal | medium | back turned to camera, weight on one hip | one hand gathering her hair for a whip | over-shoulder glance straight into the lens | locked, tiny sway]
[00:05.030-00:05.900 | SHOT 4 | camera at her eye height, optical axis horizontal | medium | seated sideways on a chair by a desk, legs together | one hand propping her chin, the other dropping to the skirt hem | gaze to lens with a head tilt | tiny sway]
[00:05.900-00:06.850 | SHOT 5 | camera at her eye height | half body | standing front, weight soft | both hands covering the lower face, peeking over the fingertips | peeking gaze to lens | tiny sway]

overall_soundscape: quiet empty-classroom room tone with faint outdoor leaves, inferred from the scene.
non_diegetic_music: N/A
```

### J5 V4·泳池白裙·贴地上摇+贴水倾斜构图(8.1s)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic posed-portrait video, 8.1s. Exactly one performer: the woman shown in <Picture 1>; face, long light-brown hair and the white off-shoulder dress come only from <Picture 1>, zero appearance text. World: a rooftop infinity pool under hard noon sun — turquoise mosaic water, city towers and hills beyond, palm shadows; bright high-contrast daylight, sparkling water reflections, shallow depth of field.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment. The camera itself remains completely outside the visible frame. Only the recorded image is visible. No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition. The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective. Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image.

POSE-AND-CAMERA LAW:
1. The pose stays LOCKED; only fingers, head angle, eye-line and blinks stay alive.
2. The camera's physical position defines everything: SHOT 1 rests directly on the pool deck; SHOT 2 rests at water-surface level laid on its side. Both are real placements, not angle names.
3. Hands are never idle: fingertips play with the dress hem and her own hair in tiny motions.
4. The highlight frame is her eyes returning to the lens and holding.
5. One whip-rotation transition covers the change of physical camera position; no other camera travel.

TIMELINE:
[00:00.000-00:01.630] SHOT 1 — the recording viewpoint comes from a real physical camera positioned directly on the pool deck, lens approximately 5-15cm above the ground, physically beneath her standing body, pointing sharply upward along her figure. The deck stone is extremely close to the lens and creates strong foreground perspective; her stepping foot is physically nearest to the lens and naturally largest; her body rises above the viewpoint with natural upward foreshortening. The view travels: her foot stepping into a slide sandal, up the calf and knee, to the white dress hem, to her relaxed hand with fingertips trailing.
[00:01.630-00:02.170] TRANSITION — one fast whip rotation with motion blur physically carries the camera down to water-surface level; the blur covers the move; no cut-like jump.
[00:02.170-00:08.130] SHOT 2 — MAIN POSE LOCK: the camera now rests at water-surface level at the pool edge, physically laid on its side so the whole frame is rotated around the optical axis — a physical dutch roll of the camera itself; the horizon and the water line tilt together with the camera while her body is not rotated independently. She lies prone on the pool edge, cheek resting on her folded arm, long hair spilling toward the water, legs bent and crossed, raised behind her; her free hand idly hooks and releases the dress hem; her eyes hold the lens with slow blinks, head tilting a few degrees twice; sun sparkles ripple on the water behind her to the end. The camera holds the same physical position and the same roll throughout.

overall_soundscape: soft water lapping against the pool edge with a light breeze, inferred from the scene.
non_diegetic_music: N/A
```

### J6 V5·海景金冠精灵·五姿势pose流+推近收尾(16.1s)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic posed-portrait video, 16.1s, four hard cuts, five shots, ONE pose per shot. Exactly one performer: the blonde elf-eared woman shown in <Picture 1>; face, golden hair, ornate crown, blue forehead jewel and the white-and-blue gauze gown come only from <Picture 1>, zero appearance text. World: a bright seaside terrace with an endless turquoise bay, small islands and white curtains; golden-hour daylight, dreamy shallow depth of field, the sea fills the background.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment. The camera itself remains completely outside the visible frame. Only the recorded image is visible. No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition. The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective. Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image.

POSE-AND-CAMERA LAW:
1. One settled pose per shot; torso and legs LOCKED; only fingers, head angle, eye-line and blinks stay alive.
2. The camera's physical position changes with the pose: above the bedding for the lying shot, at her eye height for the sitting shots, slightly pulled back for the full-body stretch, and finally moving physically closer to her face for the closing close-up — all written as real placements.
3. Hands are never idle: touching the collarbone, the neck, gathering hair, folding on the knees.
4. Every pose's highlight frame is her eyes returning to the lens.
5. A hard cut lands only in the gap between two settled poses; no action crosses a cut.

SHOT TABLE:
[00:00.000-00:03.070 | SHOT 1 | the camera is physically above her, held about one body-length up, lens pointed diagonally downward at her body on the bedding — the top surfaces of her hair, crown and shoulders are naturally visible, the bedding becomes the dominant plane, and her lying figure is naturally foreshortened because the camera is above | medium | she lies prone on white bedding, cheek resting on her folded arm, crown tilted, hair spread | free hand rests on her collarbone, fingertips drifting | eyes closed, then fluttering open toward the lens | locked high physical position, tiny sway]
[00:03.070-00:06.150 | SHOT 2 | camera at her seated eye height, a natural frontal position, optical axis horizontal | half body | she sits up facing the lens, shoulders relaxed | one hand touches her neck then slides down and away | lids low, then a direct soft gaze | slow physical push-in, the camera moving closer, never a digital zoom]
[00:06.150-00:09.100 | SHOT 3 | camera at her eye height, physically stepped back to include her whole figure | full body | from seated she leans back onto the bedding, legs bent and raised, crossed at the ankles, both arms stretched overhead | fingertips swaying, blue gauze floating off her arms | gaze up past her arms, then to lens | gentle physical pull-back then locked]
[00:09.100-00:12.300 | SHOT 4 | camera low and level beside her, around seat height, optical axis horizontal | medium | side-seated, then turning to show her bare back with the gauze draped | one hand gathering her hair over the shoulder | over-shoulder glance straight into the lens, twice | locked, tiny sway]
[00:12.300-00:16.070 | SHOT 5 | camera at her eye height, moving physically closer until the lens is only a short distance from her face | half body to big facial close-up | kneeling upright facing the lens, hands folded on her knees | fingers laced, thumbs circling slowly | soft smile straight into the lens | continuous slow physical push-in ending on a full-frame facial close-up]

overall_soundscape: soft sea breeze with faint distant waves, inferred from the scene.
non_diegetic_music: N/A
```

### J7 V6·白发cos卧室·九姿势快剪流水线(16.6s)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic posed-portrait montage, 16.6s, eight hard cuts, nine shots, ONE pose per shot. Exactly one performer: the cosplayer shown in <Picture 1>; face, pale hair and the white battle-dress with red bows and white gloves come only from <Picture 1>, zero appearance text. World: a warm sunlit bedroom — white bedding, headboard, green plant, wall art, warm floor sunlight patches; soft natural window light, shallow depth of field.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera occupying a physically plausible position in the shared environment. The camera itself remains completely outside the visible frame. Only the recorded image is visible. No recording equipment, support structure, mounting hardware, or filming apparatus is visible anywhere in the composition. The viewpoint must be produced by the camera's actual physical position, height, orientation, distance, and optical perspective. Do not simulate the viewpoint by cropping, rotating, warping, or digitally transforming a normal-perspective image.

POSE-AND-CAMERA LAW:
1. One settled pose per shot; torso and legs LOCKED; only fingers, head angle, eye-line and blinks stay alive.
2. The camera's physical position matches each pose and is always a real placement: eye height in front of the bed for kneeling and sitting shots; physically above the bed for the lying shots — lens angled steeply but not vertically downward, bedding becoming the dominant plane and her lying body naturally foreshortened; on the floor at the bed side, lens 10-20cm above the floor pointing up along her legs, for the sock close-up.
3. Hands are never idle: spreading the dress, signing, cradling the chin, clasping.
4. Every pose's highlight frame is her eyes returning to the lens; at least one wink lands in the film.
5. A hard cut lands only in the gap between two settled poses; no action crosses a cut.

SHOT TABLE:
[00:00.000-00:01.920 | SHOT 1 | camera at her kneeling eye height, a frontal position, optical axis horizontal | medium | kneeling upright on the bed facing the lens | both arms spread sideways, showing the dress silhouette, palms open | direct gaze | tiny sway]
[00:01.920-00:04.130 | SHOT 2 | camera at her eye height, physically closer | close medium | kneeling, body leaning toward the lens | both hands at her chest making double peace / heart signs, fingers wiggling | direct gaze | tiny sway]
[00:04.130-00:06.170 | SHOT 3 | camera physically above the bed, about one and a half body-lengths up, lens angled steeply downward but never vertical; bedding dominant, her lying figure foreshortened | medium | side-lying on the pillow, eyes closed, asleep | one arm draped over her eyes | eyes closed | locked elevated position]
[00:06.170-00:07.800 | SHOT 4 | camera at her eye level, physically slightly above her propped elbows, lens angled gently down | medium | prone on the bed, elbows propped | both palms cradling her chin, legs crossed and swaying behind | direct gaze, bright smile | tiny sway]
[00:07.800-00:10.370 | SHOT 5 | camera on the floor at the bed side, lens 10-20cm above the floor, pointing up along her legs; the wooden floor planks occupy the near field and her crossed legs rise above the viewpoint | close-up traveling | seated on the bed edge, white-socked legs crossed toward the floor | toes flexing slowly, sock-ring detail visible | gaze out of frame above | slow physical lateral drift along the legs]
[00:10.370-00:12.230 | SHOT 6 | camera physically above the bed, lens angled steeply downward, never vertical | full body | lying on her back on the bed, hair fanned out | both arms thrown overhead, palms open | gaze up into the lens | locked elevated position]
[00:12.230-00:13.970 | SHOT 7 | camera at her seated eye height, optical axis horizontal | full body | sitting on the bed edge, legs crossed at the knee, heels dangling | hands resting on her lap | direct gaze | tiny sway]
[00:13.970-00:16.560 | SHOT 8 | camera at her eye height, moving physically closer | close medium | kneeling upright close to the lens | hands clasped together before her knees | head tilts, one slow wink, then a soft smile into the lens | slow physical push-in]

overall_soundscape: quiet sunlit-bedroom room tone, inferred from the scene.
non_diegetic_music: N/A
```

### J8 V7·灰开衫室内·固定自拍手势链(15.5s,单镜头)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic selfie-style portrait video, 15.5s, ONE locked take. Exactly one performer: the woman shown in <Picture 1>; face, long wavy hair with a small white flower clip and the grey knit cardigan outfit come only from <Picture 1>, zero appearance text. World: an indoor corner with a vertical metallic-striped wall and a pale chair; soft even interior light, shallow depth of field, she fills most of the frame.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera held by an unseen person at arm length — positioned at her natural eye level, physically only a short distance from her face and shoulders, optical axis horizontal. Small natural handheld positional fluctuations occur as the operator physically holds the camera; they come from subtle human hand and body motion, not mechanical stabilization. Because the camera-to-subject distance is very short, her small head movements create visible natural perspective changes. The camera remains close to the subject rather than using digital zoom; nearby features are larger because they are physically closer to the lens. The camera itself remains completely outside the visible frame. No visible filming equipment or support structure appears.

CAMERA LAW: the camera's physical position NEVER changes for the whole film — one continuous arm-length selfie relationship, bust-up framing, eye-level, with only breathing-level micro sway. All life comes from her gesture chain, head angle and expressions.

POSE-AND-GESTURE LAW:
1. Torso stays front-facing and settled; only the arms, hands, head angle and face are alive.
2. Gestures land as readable beats, one at a time, each held for 1-2 seconds with finger micro-motion inside.
3. Eye contact with the lens is continuous; expressions change on the gesture beats: smile → wink → pursed lips → soft grin.
4. The hands are never idle: waving, pointing, fist-playing, heart-signing, touching her chest.

GESTURE TIMELINE:
[00:00.000-00:01.000] right hand waves hello at frame edge, soft smile.
[00:01.000-00:02.500] fingertip points at her own cheek, head tilts.
[00:02.500-00:05.000] gesture play: one fist then the other pops forward at chest height, elbows loose; a wink on the second pop.
[00:05.000-00:06.500] both fists gather at the chest in a tiny bouncing rhythm, lips pursed.
[00:06.500-00:08.500] one hand sweeps up past her head in an arc-wave, chin lifts.
[00:08.500-00:09.500] fingertip points at her cheek again, head tilts opposite.
[00:09.500-00:11.000] arms fold loosely across the chest, one brow lifts.
[00:11.000-00:13.500] small double-fist dance at chest height, bouncing with the shoulders; one wink.
[00:13.500-00:15.490] one hand settles flat on her chest, shoulders drop, a slow soft smile holds into the lens to the end.

overall_soundscape: quiet indoor room tone, inferred from the scene.
non_diegetic_music: N/A
```

### J9 V8·粉纱裙楼梯·固定中景手势三连(2.7s,单镜头)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic selfie-style portrait video, 2.7s, ONE locked take. Exactly one performer: the woman shown in <Picture 1>; face, long braided hair and the pastel tulle dress come only from <Picture 1>, zero appearance text. World: a warm stone stair hall with a symmetrical staircase and black railing behind her; soft warm lamp light, shallow depth of field.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera held by an unseen person at arm length — positioned at her eye level, physically a short distance in front of her, optical axis horizontal, small natural handheld fluctuations from real hand-and-body motion. The camera itself remains completely outside the visible frame. No visible filming equipment or support structure appears.

CAMERA LAW: the camera's physical position NEVER changes — fixed front-facing medium shot, eye-level, tiny breathing sway only.

GESTURE TIMELINE:
[00:00.000-00:00.500] right index finger points straight up, bright smile, eyes to lens.
[00:00.500-00:01.000] the same finger swings to point at the lens itself.
[00:01.000-00:01.500] the finger sweeps downward, pointing at the floor.
[00:01.500-00:02.650] both hands fold together in front of her waist, body settling into a slight head-tilt, a warm held smile into the lens to the end.

overall_soundscape: quiet stair-hall room tone, inferred from the scene.
non_diegetic_music: N/A
```

### J10 V9·蓝开衫居家·大特写表情流+尾段闪切(10.1s)

```text
integrated_multimodal_description:
Vertical 9:16 photorealistic close-up portrait video, 10.1s. Exactly one performer: the woman shown in <Picture 1>; face, long dark hair, cross earrings and the light-blue knit cardigan over a polka-dot bow collar come only from <Picture 1>, zero appearance text. World: a cozy dim room with a softly blurred PC setup glowing blue behind her; intimate low light, very shallow depth of field, her face and knee fill the frame.

PHYSICAL CAMERA BASELINE:
The visual viewpoint comes from a real physical camera held by an unseen person at arm length — positioned slightly above her eye level, physically very close to her face, lens angled gently downward toward her; small natural handheld fluctuations from real hand-and-body motion. Because the camera-to-subject distance is very short, her small head movements create visible natural perspective changes. No digital zoom is used at any time. The camera itself remains completely outside the visible frame. No visible filming equipment or support structure appears.

POSE-AND-CAMERA LAW:
1. The camera's physical position holds one intimate selfie relationship for the whole film, micro sway only; hard cuts only at the written points.
2. The base pose stays LOCKED: seated hugging one knee up, the knee pressed against the bottom of the frame.
3. All life is facial: eyelids, blinks, gaze direction, lip motion, plus tiny hand gestures near her hair and chin.
4. The highlight frame is always her eyes returning to the lens.

TIMELINE:
[00:00.000-00:07.625] SHOT 1 — big close-up on the locked knee-hug pose: lids hang low, gaze drifts down; one finger combs slowly through her hair; eyes lift to the lens; a slow blink; lips part softly; head tilts a few degrees; gaze returns to the lens again.
[00:07.625-00:09.080] SHOT 2 — her chin rests on the raised knee / folded arm, head tilting sideways, a sleepy smile, eyes narrowing at the lens.
[00:09.080-00:10.110] THREE FLASH CUTS, each a settled close-up pose in the same framing: (a) arm folded over the knee, gaze soft; (b) fingertip propping her chin, head upright; (c) head lying sideways against the knee, eyes closed, hair spilling — the film ends on this held closed-eye pose.

overall_soundscape: quiet room tone with a faint electronic hum from the blurred setup, inferred from the scene.
non_diegetic_music: N/A
```

---

## K. 2026-10-30 批量反推动链扩展库(15 支新片+2 图 · 74 条并入)

> 来源:15 支参考视频+2 张姿势参考图,经 video-to-h3-prompt 流水线反推(contact sheet 总览→转折区间密帧→因果重建;单通道证据标"推测";v08/v09 时间码以无 -ss 全解码帧索引锚定)。
> 拍位为**相对拍**;每片先给「背景人物档案」(场景/人物/节拍/镜头形态)再列动链;英文 H3 描述可直接粘贴。短标题↔原片名对照见章末页脚。
> 风格覆盖:双人支撑杂技 / 写真跪姿+技术下腰 / 3DCG 舞台变装 / 情绪撩发写真 / 自拍萌系 / 吸血鬼写真 / 氛围写真腿脚 / 双人对镜甜舞 / 学院宅舞 / K-pop 群舞 / 卡点换装 / AIGC 萌系摆拍 / 真人饭拍 / AIGC 旗袍夜景 / 写真姿势图×2。

**片<v01>《绫华的锻炼时间》(双人支撑拉伸·10.4s·竖屏)**
- 背景人物:室内玄关——深色木门、白色高脚椅、衣柜玻璃门映出衣物、暖白室内光,镜头贴地侧拍。人物两名:基座穿藏青色蓬裙(跪伏,头埋低不可见);飞者白色古风广袖长裙+银白及腰长发+腰侧粉色流苏(俯卧于基座背上)。画外行动者:无。
- 节拍:有音轨(mean -9.9dB);拉伸动作无卡点,自由散板(推测)。
- 镜头形态:A 一镜到底(全程同机位贴地侧拍,无切点)。

### K1 双人跪撑驮负静持链(4拍|双人支撑/拉伸)
- 入态:飞者已全身俯卧横陈基座背上 → 出态:姿态还原、静持
- 分解:拍1 基座跪伏成"人桥"——双膝着地、上体前折、髋部顶高成稳定台面;飞者胸腹贴其背、双腿并拢向后伸直绷脚、双脚悬空离地;拍2 飞者右臂向斜前方完全伸展、指尖探向椅沿(对侧腿微抬配平力矩——推测);拍3 飞者抬头:下颌离背、颈前侧拉长,银白长发由竖直垂帘摆成斜幕、发梢惯性回摆半拍;拍4 头落回、发帘回垂,重心回中,基座全程纹丝不动(静态,明写)
- H3:`partner acro-stretch: one performer kneeling folded into a stable human table while the other lies prone across her back with legs extended and toes pointed, reaching one arm far forward for balance, lifting her head once so the long silver hair swings from a vertical curtain into a diagonal fall before settling back, static floor-level side view`
- 来源:《绫华的锻炼时间》0.5-10s

### K2 俯卧天鹅垂帘链(2拍|微动作插件)
- 入态:俯卧姿态、面部朝下 → 出态:头落回、发帘回垂
- 分解:拍1 下颌缓慢离背抬起、颈前侧拉长,垂发整体向后摆成斜幕(发梢滞后半拍);拍2 头缓慢落回、发帘竖直回垂、发梢轻晃衰减
- H3:`lying prone with her face down, slowly lifting the chin so the long hair swings back into a diagonal curtain with the ends lagging half a beat, then lowering the head and letting the hair fall straight again`
- 来源:《绫华的锻炼时间》5.5-8.5s

**片<v02>《saber白礼服》(写真跪姿·9.6s·竖屏)**
- 背景人物:暗调室内两景——景1(0-3.5s)白垫木地板、中性偏冷光;景2(4-9.6s)深色走廊镜面地板、强蓝色逆光轮廓光+镜面倒影。人物:Saber cos(阿尔托莉雅):金色齐刘海短发+低马尾、脑后大蓝缎蝴蝶结、白色抹胸礼服短裙、白色长手套(腕部系红色细绳)、白色过膝袜、红色高跟鞋。画外行动者:无。
- 节拍:有音轨(mean -9.1dB);写真自由散板(推测)。
- 镜头形态:B 编辑快照(判据:光线与场景在 3.5-4s 间硬切,共 2-3 个切段)。

### K3 跪伏垂首启颜链(4拍|写真/虔诚)
- 入态:深跪伏地、上体前折、发帘盖脸 → 出态:跪直、指尖收于锁骨、目视镜头
- 分解:拍1 深跪伏、额头近地、双手收于胸前领口、发帘全遮脸;拍2 卷腹式节节直起、头最后抬、发帘从脸滑落肩侧;拍3 右手指尖抵下颌/锁骨、下颌微收;拍4 目视镜头定住(静态,明写)
- H3:`kneeling deeply folded forward with her hair curtaining her face, curling up vertebra by vertebra until the head rises last, hair sliding off her face, one fingertip coming to her collarbone as her eyes lift to the lens and hold`
- 来源:《saber白礼服》0-3.5s

### K4 腕系红绳过顶交叉链(4拍|写真/束缚感)
- 入态:跪坐、双臂垂 → 出态:双臂过顶手腕交叉、红绳绷直、仰视镜头
- 分解:拍1 双臂沿体前上举;拍2 双腕在头顶上方交叉、腕间红绳绷紧(手套褶皱随腕部受力聚拢);拍3 手臂完全伸直、上体微后仰、肋骨上提;拍4 目光自腕下仰视镜头定住
- H3:`raising both arms overhead and crossing the wrists so the thin red string between them pulls taut, back arching slightly as she looks up at the lens from under her crossed arms, blue rim light tracing the white gloves`
- 来源:《saber白礼服》4-5.5s

### K5 侧坐举拳宣誓链(4拍|写真/英气)
- 入态:背身 → 出态:侧坐面向镜头、举拳于脸侧、腰背反弓定住
- 分解:拍1 转身落座、双腿侧收叠于体侧(红高跟交叠入镜);拍2 上体转向镜头、右臂屈肘举拳至脸侧(宣誓位);拍3 腰背反弓、胸口上提、下颌微收;拍4 目视镜头、拳不落(静态,明写),蓝轮廓光勾边、镜面地板映红鞋
- H3:`sitting sideways on the mirror floor with red heels crossed, turning to camera and raising one gloved fist beside her face in a pledged pose, spine arching with the chest lifted under hard blue rim light, holding still`
- 来源:《saber白礼服》6-9.6s

**片<v03>《saber下腰挑战》(技术动作/原作复刻·8.2s·4K竖屏)**
- 背景人物:室内走廊两景——景1(0-2s)米色瓷砖地面、暖光;景2(2.5-8.2s)白墙深色踢脚线走廊、顶光+左侧粉紫补光。人物:同 v02 Saber cos。画外行动者:无。右上角画中画为原作对照图(后期层,非现场元素)。
- 节拍:有音轨(mean -12.8dB);挑战类实拍自由节拍(推测)。
- 镜头形态:C 快剪(2 个场景切段)。

### K6 蹲伏触地蓄势链(2拍|Hero Action/原作复刻)
- 入态:深蹲伏地 → 出态:单掌撑地蓄势定住
- 分解:拍1 双膝深蹲下沉、双掌触地、上体前倾、发帘垂落盖脸(复刻原作蹲姿);拍2 一手离地前伸触地滑动半步、重心压低定住(静态,明写)
- H3:`dropping into a deep crouch with both palms on the floor and the head bowed so the hair hangs forward, sliding one hand half a step ahead and freezing in the low predatory crouch`
- 来源:《saber下腰挑战》0-2.2s

### K7 贴墙下腰满弓链(8拍|Hero Action/技术峰值)
- 入态:站立背对墙 → 出态:满弓后弯、双手扶墙低位、目视镜头定住(回收路径未入镜,推测为扶墙卷腹回直)
- 分解:拍1-2 背对墙站立、双臂上举后仰、双掌先后贴墙(进入路径:髋前顶+胸腰节节后弯);拍3-5 双掌交替沿墙面向下走、重心随之节节下沉,腰背弧度逐拍加深、长发全数后垂;拍6-7 技术峰值:满弓——胸腰完全打开、头全仰、面部朝上转向镜头、张嘴发力,双腿垂直承重、足跟压实;拍8 定住亮相(静态,明写)
- H3:`standing backbend against the wall: palms pressing on the wall overhead then walking them down rung by rung as the spine arches deeper, long hair falling all the way back, until the chest faces up in a full arch with the head released back and eyes finding the camera, heels loaded, holding the pose`
- 来源:《saber下腰挑战》2.5-8.2s

**片<v04>《奥黛塔变装》(3DCG/MMD风·变装歌舞·153.4s·横屏)**
- 背景人物:全黑影棚舞台,一束顶部聚光锥+地面椭圆光斑,抛光地面带倒影,远景少量星点粒子;背景在纯黑与深灰渐变间切换。无道具、无画外行动者。横置已核查:光锥垂直、人物立轴垂直,非相机 Roll。人物:年轻女性(16-20 岁感),薰衣草银紫发——短发 BOB 与盘发髻(编发冠+大呆毛)两种发型交替,黑羽/黑钩发饰,红紫瞳。服装六套轮换:蓝白羽毛芭蕾裙(星纹抹胸+白羽肩饰+蓝缎垂尾+银白系带高跟靴+黑蕾丝手套)/酒红开衫+水手领内搭+黑打底裤或白百褶裙/粉天鹅印花 T(下摆侧打结)+黑运动短裤/灰格法兰绒衬衫+黑内搭+格裙+红色细高跟/白色水手服+藏青领巾+藏青百褶裙+白筒袜+"MARINE"白水手帽/粉一字肩毛衣。
- 节拍:完整 BGM(mean -10.5dB/max 0dB);动作卡点清晰,约 100-120BPM 流行曲(推测)。
- 镜头形态:C 多镜头快剪(特写/中景/大远景间跳切,多套服装交叉剪辑;每个动作窗口内先切镜再动作)。

### K8 蓝裙开场臂浪·三段抬臂+掩口偷笑链(5拍|优雅/舞台)
- 入态:侧脸近景低头垂目、双臂垂于体侧 → 出态:右手掌掩口、左手护颌,闭眼含笑定格
- 分解:拍1 (00:20-20.7) 近景:右腕屈肘抬至脸旁、手腕放松指尖下垂,切大远景;拍2 (21.3-22.7) 双小臂胸前交叉再向两侧弹开成 X 展臂、肩线上提、重心移左脚;拍3 (23.3-24.3) 双臂过顶手腕交叉、踮脚立半足尖,裙摆蓝缎垂尾滞后半拍回摆;拍4 (24.3-25.3) 双手落至脑后抱头、肘外张、髋向左顶;拍5 (25.3-27) 切胸上近景:右手掌心掩口、左手屈肘收在颌下护位,眨两次眼、眼尾下弯,holds one beat of stillness;镜头每次在动作起点前 0.3s 切入
- H3:`opening in a single overhead spotlight on black stage, crossing forearms then flinging both arms wide into an X, rising onto tiptoe with wrists crossed overhead as the blue sash tails lag behind the spin, hands settling behind her head with elbows flared, then a cut to chest-up closeup where one palm covers her mouth in a held giggle with two slow blinks`
- 来源:《奥黛塔变装》00:20-27s

### K9 背面指天迪斯科+扭胯走远链(6拍|复古/背影杀)
- 入态:背对镜头站光斑中央、双臂垂 → 出态:双手背到腰后整理衣摆、远离镜头半身位
- 分解:拍1 (34-35) 右臂斜上 45° 指天、左手叉腰、双脚小交叉站位,定 1 拍;拍2-3 (35-36) 保持指天、胯向左顶两次、脚跟小幅度离地弹跳;拍4-6 (36-38) 背对镜头向光锥深处走,步幅小、胯随每步左右送、开衫下摆与裙摆左右甩动延迟半步;拍7-8 (38-40) 双手背到腰后拢衣摆、肩胛收拢、站定;全程只给背影,靠胯线与肩线讲故事
- H3:`seen from behind in a tight spotlight, one arm pointing diagonally to the rafters while the hip pops twice on the beat, then walking away with small steps and rolling hip sway, jacket hem and pleated skirt swinging a half-step late, finishing with both hands gathering the jacket at her lower back`
- 来源:《奥黛塔变装》00:34-40s

### K10 鞠躬→心形手→低位爵士手→V字吐舌链(6拍|元气/收尾组合)
- 入态:侧身走位中 → 出态:脸侧 V+挤眼吐舌定格,cut 大远景
- 分解:拍1 (41-42) 侧身急停、上体前屈约 45° 鞠躬、双臂自然垂向地面、短发整片前甩盖脸;拍2 (42-42.7) 卷腹式直起、手顺势带到颌前、发丝回落肩后;拍3 (43-43.5) 双手于胸口拼心形(指尖对指尖+拇指对拇指)、头右歪;拍4 (43.5-44.5) 双臂体侧低位打开、掌心朝前五指大张、手腕快速抖两下(jazz hands);拍5 (44.5-45.5) 右拳收至胸前小幅度上冲两下(加油拳);拍6 (45.5-47) 切近景:右手举至脸侧成 V、挤左眼 wink、吐舌尖,holds one beat of stillness 后硬切大远景
- H3:`snapping from a walking stop into a deep waist bow with hair flopping forward, curling back up into a finger-heart at her chest, flinging both arms low with spread palms doing quick jazz-hand wrist shakes, two small chest-level victory punches, then a closeup finishing freeze with a V-sign beside her face, winking with tongue out, held one full beat before the wide shot`
- 来源:《奥黛塔变装》00:41-47s

### K11 遮面 peek-a-boo→惊吓爪→掌风 wave 链(4拍|萌/近景)
- 入态:胸上近景正面,双掌掩口鼻 → 出态:右手停在脸侧翻掌 wave、左手回胯、T 恤滑落露右肩
- 分解:拍1 (01:00-01:01) 双掌心捂住口鼻、指缝闭合、眼睛闭;拍2 (61-61.5) 十指缓缓张开成栅栏、双眼从指缝里瞟镜头(眼神先动、手后动);拍3 (61.5-62.5) 双手向两侧弹开至脸旁、五指大张成"惊吓爪"、瞪眼+嘴笑开、肩膀耸起;拍4 (62.5-63.5) 右手停在脸侧翻掌向外 wave 两次、左手落回胯边、胯随拍左右顶、宽 T 恤布料在露肩处迟半拍滑落
- H3:`chest-up to camera, hiding her mouth behind both palms then spreading the fingers into a fence to peek through with her eyes first, flinging hands apart into spread-claw scare pose beside her face with a shoulder shrug, waving one open palm while the loose tee slides off her shoulder a half-beat late, hip swaying on the beat`
- 来源:《奥黛塔变装》01:00-01:03.5s

### K12 聚光灯原地平转+背身收臂定格链(4拍|旋转/大远景)
- 入态:大远景正对镜头 → 出态:背对镜头、右臂直臂上举、头从左肩回眸
- 分解:拍1-2 (01:04-65.5) 以左脚为轴原地平转约两周:双臂先水平张开借角动量、再收拢贴身加速(角动量收缩明显),裙摆与蓝缎带被离心力甩成水平环、地面倒影同步旋转;拍3 (66-66.8) 转毕背对镜头急停、右臂直臂高举、发梢与呆毛惯性回甩过肩;拍4 (67-68) 手臂缓落、头从左肩上回眸镜头,cut 正面近景接发丝落定;旋转轴线始终垂直、无倾倒
- H3:`wide shot in a cone of light, spinning two full flat turns on her left foot with arms opening to gather momentum then pulling in to accelerate, skirt and sash flaring into a horizontal ring, stopping hard with her back to camera and one arm shot straight up, hair whip-lashing over the shoulder, head peeking back from the left shoulder as the arm lowers`
- 来源:《奥黛塔变装》01:04-01:08s

### K13 红高跟螺旋下沉→抱膝蹲→跪姿后弯链(5拍|技术/地面)
- 入态:站立(红色细高跟) → 出态:跪姿胸腰后弯成弓、右手插发扶头
- 分解:拍1 (01:45.9-46.5) 足部近景:右足跟碾转半步、左足前交叉点地、双膝开始屈、重心沉向右跟(高跟落地先跟后掌);拍2 (46.7-47.5) 大远景:边顺时针小旋转边下蹲——螺旋式下沉、格裙与衬衫下摆绕腿水平甩;拍3 (47.7-48.5) 蹲底:双膝并拢、双臂环抱小腿、下颌内收、足跟承重,holds one beat of stillness;拍4 (49-50) 放开手臂、右膝落地成跪、左膝立起足踩地、上身开始后展;拍5 (50-51.5) 技术峰值:跪姿下腰——右手扶头后插入发中、胸腰向后打开成弓、头后仰、左脚背压地吃住平衡;回收路径被剪辑隐藏(推测为左手扶左膝卷腹回直,53s 后已见立姿背影)
- H3:`in red stilettos, crossing one foot in front and spiraling down into a deep squat while turning clockwise, skirt hem swirling around her shins, hugging her knees for one held beat, then releasing onto one knee into a kneeling backbend with chest arched open, one hand braced in her hair behind the head, instep pressed to the floor for balance`
- 来源:《奥黛塔变装》01:45.5-01:51.5s

### K14 过顶交叉转身→背身 T 展→定妆头滚链(4拍|收尾/定格)
- 入态:正面水手服站姿 → 出态:右臂折搭头顶、左手叉腰、眼瞟侧、笑意定格约 3 拍
- 分解:拍1 (02:24-25) 双臂过顶手腕交叉、原地转半圈(正面转至背面);拍2 (25.5-27) 背面双臂水平展开成 T、掌心向后,随即右臂屈肘搭上头顶、胯向右送(sassy back pose);拍3 (27.5-29) 转回正面、双臂落下、右手带至脸侧;拍4 (29.5-33) 定妆:右臂折过头顶、手腕搭在头顶指尖垂向右侧、左手叉腰、下颌内收,眼球先看镜头再瞟向右、嘴角挑起,holds three beats of stillness;镜头腰部以上中近景、微仰、人物居画面左 1/3
- H3:`crossing wrists overhead while turning half around, opening into a back-view T-pose with palms out, hooking one forearm over her head with hip cocked, rotating back to front and freezing in the over-head-arm wrist-drape pose with the other hand on her hip, chin tucked, eyes drifting from lens to side with a smirk, holding three beats in a slight low-angle medium shot`
- 来源:《奥黛塔变装》02:24-02:33s

**片<v05>《夏天结束了》(真人cos·海滨情绪·16.1s·竖屏)**
- 背景人物:三个户外海滨点位——日落海面(低角度橙光、逆光金边)/沙滩彩色小屋(午后暖阳)/白墙绿树(正午顶光)。画外行动者:海风(发丝的主要发力者)+持机者(镜头呼吸感晃动)。人物:真人 coser(20 上下),银白渐雾蓝 BOB 假发+深蓝印花三角头巾(脑后蝴蝶结),重腮红、水光唇;藏青领白水手服→白色宽松 T(右肩滑落)→浅蓝短裤。
- 节拍:有 BGM(mean -11.4dB);表演自由散板,动作不严格卡点(推测)。
- 镜头形态:B 编辑快照(3-4 个场景块,块内 2-5s 长镜头,块间硬切)。

### K15 指背拂额·初醒式撩发链(3拍|温柔/风合作)
- 入态:闭眼迎风、发丝横糊双眼 → 出态:发别耳后、睁眼看镜头、嘴角小笑
- 分解:拍1 阵风把发丝压过眼睑、眉微蹙、眼闭忍;拍2 右手食指与中指指背从眉心向太阳穴扫、把发丝推离眼周;拍3 顺势将一绺发别到耳后、指尖擦过耳廓、眼睁开;发丝物理:被推开的发约 0.3s 后又有少量回弹遮额(风持续做功);眼神落点:睁眼直视镜头;镜头面部大特写占画面上 2/3、顶光偏橙、头巾边入画
- H3:`eyes closed as wind presses hair strands across her eyelids, brushing them away with the backs of two fingers from brow to temple, tucking one lock behind her ear with a fingertip grazing the ear, then opening her eyes straight into the lens in a tight face closeup, strands fluttering back across her forehead a beat later`
- 来源:《夏天结束了》00:00-2.5s

### K16 海风横甩·剪影怅望链(2拍|怅惘/逆光)
- 入态:侧脸望海、长发全拢于背后 → 出态:发贴颊落定、视线仍钉在海平线
- 分解:拍1 阵风从背后掀起长发、发梢先翻过肩头、头巾尾带同向抽动;拍2 技术峰值:整片头发横甩过脸、运动模糊横贯画面——她不闭眼、不抬手、不侧头,视线钉在海平线;拍3 发从脸前滑落贴颊、眼神未动;核心反差:头随动角度<5°,全部做功交给头发;回弹方向:顺风向前→贴颊静止;镜头侧脸大特写、日落逆光金边、海面虚化底
- H3:`in profile against a sunset sea, a gust lifting her long hair and whipping the whole mass horizontally across her face with motion blur while she does not flinch, eyes locked on the horizon, head turning less than five degrees, strands sliding off her cheek as the wind releases, backlit rim-light on every flyaway`
- 来源:《夏天结束了》00:07.2-8.5s

### K17 慢拢发离颈·忧郁提拉链(4拍|慢镜/怅惘)
- 入态:侧脸、手抬向额角 → 出态:低头松手、发落回原位
- 分解:拍1 右手入画、指尖从额角插入发间向后梳;拍2 慢速把颈侧全部头发拢向脑后、肘节节抬高(进入路径:额角→耳后→颈后三段);拍3 手在颈后握住发束向上提离后颈、露出后颈与下颌线、下颌微抬、眼睑半合,holds one beat of stillness;拍4 低头、松指、发束垂落回肩;整链速度约为正常一半(推测拍摄升格);镜头侧脸特写、日落逆光、海面底
- H3:`slow-motion profile as fingertips slide into her hair at the temple and gather every strand toward the nape in three segments, elbow rising, lifting the gathered hair off her neck to expose the nape and jawline with heavy-lidded eyes, holding one beat before dropping her chin and letting the hair fall back`
- 来源:《夏天结束了》00:08.6-12.2s

### K18 顽皮摇头弹发+抓发藏脸链(4拍|开心→含羞)
- 入态:正面大特写、抿嘴笑 → 出态:头倾右肩、脸颊贴手背、闭眼含羞
- 分解:拍1 头先向左倾、抿嘴憋笑、眼神左右瞟;拍2 头快速左右小摆两次(幅度小频率高)、两侧发梢水平抽打面颊、刘海弹跳、张嘴笑出声(技术峰值=甩发与笑声同拍);拍3 摆动衰减、发回落、笑收成抿嘴;拍4 右手五指插进右侧发里抓住一绺、头向右肩倾、眼闭、脸颊贴向手背(回收=用头发藏半张脸);镜头正面大特写、头顶绿树叶入画、正午顶光
- H3:`front closeup tilting her head then shaking it quickly side to side so the bob ends slap her cheeks and bangs bounce while she bursts out laughing, the swing decaying into a pressed-lip smile, then fingers diving into the hair on one side to grab a fistful and hiding half her face against the back of her hand, eyes closed, shy`
- 来源:《夏天结束了》00:13.9-16.1s

**片<v06>《橘福福》(真人cos·自拍快剪·27.6s·竖屏)**
- 背景人物:三个晴天户外点——城市广场(蓝天+高楼)/金色稻田/白色雏菊花田;硬光直射,自拍者的影子清晰投在人物自己脸上(11s 起);18.6s 附近插入两帧黑底"备选"字卡(剪辑余料)。无画外行动者(自拍臂长机位)。人物:真人 coser(20 上下),金色长假发+白色挑染束、棕白双色毛绒虎/熊耳、绿色美瞳;白色金饰吊带裙(藏青缎带蝴蝶结+金珀挂坠)、白花耳环、裸肩;手持道具:雏菊、草叶/稻穗。
- 节拍:有 BGM(mean -11.2dB,轻快流行推测);手势卡点松散(推测)。
- 镜头形态:B 编辑快照(0.5-2s 碎片硬切,全部自拍近景特写,10s 处一次摇离面部再摇回)。

### K19 猫爪拳贴颊·wink 发言链(3拍|萌/自拍)
- 入态:自拍大特写、手在画外 → 出态:拳贴右颊+头歪+笑定格
- 分解:拍1 右手松拳提到右颊旁、腕内扣拳眼朝脸、肘下沉;拍2 挤左眼 wink、嘴张开发言/唱、拳随语速小幅捶颊两下(发力来源=前臂小幅屈伸);拍3 头向右歪贴向拳、左眼睁开、嘴角翘起,拳不落,holds one beat of stillness;耳饰与发束随头歪延迟摆;镜头前置自拍、微俯、面部占画面 3/4
- H3:`front-camera closeup raising a loose fist beside her cheek with the wrist curled inward, winkling one eye while the fist knocks lightly against her cheek twice on her words, then tilting her head to lean into the fist with one eye open and a smirk, holding the pose as ear fluff and hair sway late`
- 来源:《橘福福》00:11-14s

### K20 草叶叼唇·deadpan 到破功链(3拍|反差萌/道具)
- 入态:面无表情直视镜头、草叶横叼唇间 → 出态:头摇草晃、眼弯笑破
- 分解:拍1 一根草叶横叼在唇间、叶尖朝右、面无表情 deadpan 直视、下颌完全静止;拍2 右手两指捏住草茎、把草从唇间抽出一半再推回(腕指做功、唇不追);拍3 头小幅度左右摇、草叶跟着晃、嘴角绷不住上弯、眼弯成缝(回收=笑破但草不落);细节:自拍者影子投在自己脸上;镜头面部特写、正午顶光
- H3:`closeup holding a grass blade sideways between her lips with a deadpan stare, pinching the stem to slide it halfway out and back, then shaking her head slightly so the blade wobbles until she breaks into crescent eyes and a grin without dropping the grass, her own shadow falling across her face in harsh noon sun`
- 来源:《橘福福》00:14.5-19s

### K21 摇镜拾雏菊·花瓣贴脸链(3拍|道具/镜头几何)
- 入态:面部特写居中 → 出态:雏菊贴右颧骨、头向花倾、wink
- 分解:拍1 手持镜头从脸快速右摇、白雏菊花海占满画面约 0.5s(转场由摇镜完成);拍2 摇回时她已把一朵白雏菊举到右脸旁、花瓣贴颧骨(进入路径:摇镜遮蔽内完成举花,动作被剪辑藏起);拍3 头向花倾、挤眼 wink、嘴角小笑;镜头几何:自拍臂长、摇镜前后构图一致(人物右侧留花位);吊带蝴蝶结随肩转微晃
- H3:`selfie camera whipping off her face to sweep across a field of white daisies and snapping back as she raises a single daisy against her cheekbone, tilting her head into the flower with a wink, the gesture completed hidden inside the pan so the pose appears fully formed`
- 来源:《橘福福》00:10-11s

### K22 "哇"声张爪迎镜·指 wiggle 链(3拍|元气/打招呼)
- 入态:自拍特写、平静看镜头 → 出态:眼笑成月牙露齿、手落回画外
- 分解:拍1 头微后仰、嘴大张成"哇"、右手五指大张举到脸侧(肩驱动整臂上抬);拍2 五指朝镜头 wiggle 两下(像小爪抓空气)、嘴从 O 形收成笑(技术峰值=张嘴与张爪同帧爆发);拍3 眼笑成月牙、露齿、手落出画、头回正;白花耳环与熊耳随仰头后倾;镜头自拍特写、城市广场蓝天硬光
- H3:`front-camera closeup snapping her head back with mouth wide in a happy gasp as one hand flies up beside her face with all five fingers spread, wiggling the fingers at the lens like little grabs, mouth folding from an O into a grin with crescent eyes before the hand drops out of frame`
- 来源:《橘福福》00:21-22.5s

**图<img02>《狐耳白发六宫格》(AIGC 写真·2x3 拼图姿势参考)**
- 背景人物:和风酒廊/居酒屋木格酒架前,木地板+深色圆垫,暖光;人物:白发狐耳角色(白狐耳+巨大蓬白狐尾),白色短上衣+金色镶边胸襟、金色高领环、纱质肩袖、金臂环腕环、腰侧红绶带长垂、赤足金脚链;道具:绿釉小酒瓶。A/B/C 三格共享同一坐姿基座(盘腿交叉坐)、D/E/F 三格共享侧坐-抱膝基座,判定为"同基座微变体",适合做"大姿势锁死+微活性"模板(J 章纪律)。
- 节拍:静态图片,无节拍;时序为重构(推测)。

### K23 狐耳写真链·盘坐 V 字手三连(4拍|AIGC/写真·大姿势锁死)
- 入态:盘腿交叉坐于深色圆垫 → 出态:一膝立起、狐爪手举至耳侧、眼神斜上
- 分解(大姿势锁死,只有手指/头角/眼神/眨眼在动,手永远在做事):拍1 基座锁定——盘腿脚踝交叠、赤足金脚链、白狐尾在身后铺开、双手各比 V(一上护颊一下护膝)、眼闭头微右歪;拍2 微活性:头转正、下颌收 1cm、双眼睁开直视镜头、V 字手不动;拍3 微活性:下 V 手收回叠放大腿、上 V 手五指松开成狐爪上提至耳侧;拍4 一膝立起、上身微前倾、眼神从直视滑向斜上方、眨一次慢眼;红绶带与广袖全程垂坠方向不变
- H3:`sitting cross-ankled on a floor cushion in a sake-bar alcove with the white fox tail fanned behind, double V-signs beside her face and knee, opening her eyes to camera, melting the lower hand into her lap while the upper blooms into a relaxed fox-paw at her ear, one knee rising as her gaze drifts upward, silk sleeves and red sashes dead still`
- 来源:《狐耳白发六宫格》上排 A→B→C(单图三变体,时序为重构·推测)

### K24 狐耳写真链·绿酒瓶三连(3拍|AIGC/写真·道具链)
- 入态:侧坐木地板、一膝立、手抵唇边沉思、绿釉酒瓶立在脚边 → 出态:抱膝坐、双手合抱酒瓶抵胫前、下颌搁膝抬眼
- 分解(大姿势锁死):拍1 侧坐基座:尾绕至身侧、右手两指抵唇边、绿瓶在脚边入画;拍2 转正面向镜头、右手拾瓶(腕内旋 90° 执瓶颈)向前递出半臂、左手扶膝、直视镜头——递瓶的手臂全程有"请"的弧线;拍3 收瓶抱膝:双腿屈起、双手合抱瓶身抵在胫前、下颌搁上膝头、眼从瓶口上方抬起来看镜头;手指永远在做事:抵唇指→执瓶指→抱瓶指逐拍更换任务
- H3:`in a wood-floored sake room, seated with one knee up and fingertips at her lips beside a green ceramic flask, lifting it with a wrist turn to offer it forward half an arm's length while looking dead into camera, then hugging the flask with both hands against her shins, chin resting on her knees, eyes lifting over the bottle mouth`
- 来源:《狐耳白发六宫格》下排 D→E→F(单图三变体,时序为重构·推测)

**图<img01>《蓝水手服走廊截图》(单帧姿势参考)**
- 背景人物:室内清水混凝土走廊,灰色大板墙+方柱、绿色安全出口指示灯、反光水泥地坪、冷白顶光。人物:18-22 岁感少女,黑长直+空气刘海+白色花形发饰与蓝色发带;浅蓝紫短款学院西装外套(藏青袖口)、白衬衫、藏青领带、蓝格纹百褶短裙(白色蕾丝衬裙层)、白色过膝袜(膝侧黑丝带蝴蝶结)、黑色厚底乐福鞋。

### K25 走廊应援交叉跳步定格链(3拍|元气/单帧反推)
- 入态(推测):立正、双臂垂 → 出态(=帧内定格):双拳收胸、左足尖前点小腿交叉、右手拎挂饰至脸侧、张嘴喊
- 分解:拍1(推测) 双拳收到胸口、肘内夹成应援预备、膝微屈蓄力(弹簧下沉半拍);拍2(推测) 左足尖前点地、双小腿前后交叉、重心压在右足、格裙摆向右扬;拍3(=帧证据) 右手拎钥匙扣挂饰甩至脸侧高度、腕外翻让挂饰垂落、嘴张开喊(应援口令或跟唱)、下巴微抬;蓝外套下摆与领带随交叉步左摆;来源为单帧截图,拍 1-2 为动作反推
- H3:`in a bare concrete corridor, pulling both fists to her chest with elbows tucked, crossing one shin behind the other onto pointed toes while swinging a keychain charm up beside her face, mouth open mid-chant, pleated plaid skirt swinging with the cross-step, full body in a slight low angle`
- 来源:《蓝水手服走廊截图》(单帧截图+推测)

**片<v07>《好女孩——薇薇安(测试)》(吸血鬼写真快剪·60.6s·竖屏)**
- 背景人物:约 10 处场景轮换——灰色布艺沙发+木地板(暗调窗光)/白色床品卧室(自然窗光)/暗调木墙/烛光桌(暖光)/蓝调时刻窗前。人物:吸血鬼贵族风少女 cos("薇薇安"):银白偏紫长卷发(结尾段变蓝紫)、红瞳、精灵尖耳+额侧白色小弯角、黑紫缎面女仆风连衣裙(白泡泡袖+黑紫马甲裙+褶边领+黑缎蝴蝶结中央嵌蓝宝石胸针)、黑色细项圈;黑丝/黑色过膝袜+黑色厚底高跟鞋(银色踝扣+紫色缎带);手持道具:白瓷拿铁杯、红玫瑰。画外行动者:无。
- 节拍:有 BGM(mean -14.3dB);写真自由散板(推测)。
- 镜头形态:B 编辑快照(判据:10+ 次场景硬切,段内自拍式固定机位微晃)。

### K26 沙发高跟腿链(两景)(4拍|慵懒/腿线)
- 入态:立于沙发旁 → 出态:双踝交叠搭在沙发扶手上静止
- 分解:拍1 立姿入画、黑丝+厚底高跟鞋(银踝扣+紫缎带)在窗光下高光;拍2-3 抬腿翻身把双腿搭上沙发扶手、双踝交叠、足尖悬空——小腿以踝为轴慢摆约±15°(惯性来自小腿自重,鞋面缎带随摆轻颤);拍4 坐姿变体:双膝并拢交叠、指尖沿黑丝膝头轻抚一遍(28-30s/45.6-47s 两景复用)
- H3:`in black platform heels with violet ribbon ankle straps she lifts her stockinged legs onto the sofa armrest, ankles crossed with the calves swaying slowly from the ankle, then sits with knees together as fingertips glide once over the sheer knee, dim window light`
- 来源:《薇薇安》00:00-4.5s;00:28-30s;00:45.6-47s

### K27 白床交叠蹭脚链(2拍|慵懒)
- 入态:仰卧床上、双腿屈膝 → 出态:双脚交叠静止
- 分解:拍1 屈膝并拢向侧倾倒、双腿交叠横陈床面(黑丝脚背绷直);拍2 上位脚脚背贴下位脚小腿来回轻蹭两次、脚趾同步蜷缩伸展,静止收住
- H3:`lying on white sheets with knees drawn and legs folded sideways, the top foot rubbing slowly along the other calf with toes curling and flexing, natural window light`
- 来源:《薇薇安》00:05-9s

### K28 枕上转醒链(4拍|柔焦叙事)
- 入态:侧卧枕上、双眼闭合 → 出态:侧身抱枕、目视镜头浅笑
- 分解:拍1 侧卧、银紫长发铺满白枕、双眼闭合;拍2 眼睑缓缓睁开、目光先落在镜头前虚处再聚焦;拍3 头自枕上微抬转向镜头、下颌收半分;拍4 上身卷向枕头环抱、面颊贴枕、浅笑定住(静态,明写)
- H3:`waking on a white pillow with long lavender hair spread wide, eyelids opening slowly as the gaze drifts then focuses, lifting the head to find the lens before curling around the pillow with a cheek pressed down and a soft smile, holding still`
- 来源:《薇薇安》00:15-24s

### K29 领结宝石微调链(4拍|细节微动作)
- 入态:面部特写正视 → 出态:指尖仍搭在蝴蝶结上、目视镜头微笑
- 分解:拍1 指尖从画外入画、轻捏黑缎蝴蝶结翼部左右各正一次;拍2 指腹推正中央蓝宝石胸针半毫米、宝石反光闪一下;拍3 指尖顺缎带下滑半寸停住;拍4 目光从手上抬回镜头、眨眼一次浅笑
- H3:`close-up as her fingertips straighten the black satin bow at her collar and nudge the sapphire brooch a hair, sliding down the ribbon half an inch before the eyes lift back to the lens with a slow blink and a smile`
- 来源:《薇薇安》00:21-26s;00:46-52s

### K30 烛光捧杯链(4拍|暖调)
- 入态:坐于烛光桌前、白瓷杯在胸前 → 出态:杯仍捧在胸前、目视镜头
- 分解:拍1 双手捧白瓷拿铁杯于胸前、烛光在脸上跳动(杯中液面微晃);拍2 目光从杯上抬起直视镜头、头微歪;拍3 杯沿抬至唇下轻碰半秒(浅啜或欲啜);拍4 杯回胸前、下颌微收定住
- H3:`holding a white latte cup with both hands at her chest in candlelight, lifting her gaze from the cup to the lens with a head tilt, touching the rim to her lower lip for a half second, then settling it back down`
- 来源:《薇薇安》00:36-40s(时间码为推测)

### K31 玫瑰贴唇链(4拍|浪漫/道具)
- 入态:持玫瑰于画面下方 → 出态:玫瑰贴颊、目视镜头浅笑定住
- 分解:拍1 红玫瑰举至唇鼻前、完全挡住下半张脸、双眼缓闭;拍2 花沿脸颊缓缓下滑贴住颧骨、眼睑睁开;拍3 唇角自花瓣后弯起浅笑、头向花倾;拍4 定住(静态,明写)
- H3:`pressing a red rose fully over her mouth and nose with eyes closing, sliding the bloom slowly down her cheek as the eyes open and a smile curves from behind the petals, head tilting into the flower and holding`
- 来源:《薇薇安》00:40-43.5s

### K32 "十年后"时间跳跃链(2拍|剪辑结构/梗)
- 入态:窗前面部特写(银紫发) → 出态:同机位同姿态、发色转蓝紫、浅笑定格
- 分解:拍1 硬切黑底白字卡"十年后"约 2s(后期层);拍2 切回同一窗前机位——姿态与构图与切前一致,仅发色由银紫转蓝紫,对镜头缓慢眨眼一次、浅笑定住(梗:吸血鬼不老,只有发色随时间漂移)
- H3:`hard cut to a black title card reading "TEN YEARS LATER", then back to the same window framing and pose with the hair shifted from silver-lavender to blue-violet, one slow blink into the lens and a held gentle smile`
- 来源:《薇薇安》00:55-60.6s

**片<v08>《维琳娜》(鸣潮维里奈 cos·氛围写真·75.0s·竖屏)**
- 背景人物:单人女性 coser,角色判读为《鸣潮》维里奈(判据:银白长发+头顶呆毛+精灵尖耳+白金藏蓝制服+紫瞳)。两套造型:A(室内特写)白色立领短外套、金色圆筒扣、金色多层荷叶领结、藏蓝露肩裙配白色绒球珍珠肩带、白色过膝袜、灰白色玛丽珍鞋、白色手套、金色长耳坠;B(户外街拍)白色露肩水手上衣+藏蓝水手领(肩带白色绒球)、藏蓝高腰裙、白色荷叶袖套、白色侧马尾扎大号白色印花蝴蝶结、白色厚底珍珠踝带玛丽珍。道具:白瓷咖啡杯(拿铁/黑咖啡)、米色曲奇、户外木质圆桌+菜单本、米色布艺沙发+木茶几白瓷茶具、白床品。场景共约 10 处:暗调木墙窗边→沙发茶几区→户外街角咖啡馆(蓝天树影)→白纱帘沙发窗边→暗背景室内→自然光卧室白床→灰调室内→逆光绿植户外。画外行动者:仅画外持机者(POV 腿部镜头),无第二入画者。
- 节拍:有 BGM(mean -15.5dB,抒情慢板类推测);动作无固定周期卡点,摆脚/眨眼均为自由速度→自由散板。
- 镜头形态:C 快剪(判据:≥10 次场景硬切,单镜 1.5-11.5s,多为手持自拍式微晃;9.0-9.9s、35.4-38.1s、56.2-59.3s 为三处静态微动长镜,已在链内明写)。

### K33 分帘拨呆毛链(3拍|软萌)
- 入态:正面大特写静止,刘海垂帘遮右眼 → 出态:手撤出画,呆毛竖立,歪头微笑看镜
- 分解:拍1 右手自画外右上入画,指背贴颊把遮眼刘海向右拨成斜分帘(发力=腕指小肌群,头不动、视线跟手动);拍2 手沿发帘滑至头顶,两指轻捏呆毛根部上提半厘米松开,呆毛弹性回摆、周边发丝延迟颤动;拍3 手撤出画,头右倾约 5°,嘴角上提、眨眼一次收势
- H3:`extreme close-up selfie, her hand slides into frame brushing the bangs away from one eye, then two fingers pinch the single ahoge strand on her crown and flick it upright, she tilts her head with a soft smile and one slow blink`
- 来源:《维琳娜》00:00-3.2s

### K34 沙发慵懒腿链(两段)(6拍|慵懒)
- 入态:仰躺沙发、双腿伸向低机位镜头 → 出态:双踝交叠静止、脚尖轻点
- 分解:段1 低机位交踝摆脚(3.5-8.9s):拍1 双腿沿沙发面伸直,右踝搭上左踝,脚尖放松;拍2-3 上位脚以踝为轴左右慢摆约±15°(周期约 2s,大腿不动,白袜随摆起细褶);拍4 摆动衰减停住,膝微屈一弹;拍5 下位脚抽出换到上位,交叠方向反转;拍6 新上位脚继续慢摆,藏蓝裙摆随躯干呼吸微起伏。段2 俯视提膝交叠(10.0-14.9s):拍1 机位翻至脸侧俯视,靠镜头腿屈膝上提至画面中央;拍2 该腿外旋下落、横搭对侧膝上成二郎腿;拍3 上位脚踝带动小腿前后点动两次;拍4 交叠双腿整体小幅弹跳(沙发反弹性);拍5-6 保持交叠,脚尖随乐轻点,镜头手持呼吸感微晃
- H3:`reclining on the sofa shot from a low angle, she crosses her ankles and the top foot sways lazily side to side, then the camera looks down as she lifts one knee, drapes that leg over the other and taps her toes gently while the crossed legs bounce softly`
- 来源:《维琳娜》00:03.5-8.9s;00:10-14.9s

### K35 饼干轻咬眨眼链(4拍|甜)
- 入态:面部特写,戴白手套的手持曲奇入画 → 出态:饼干停在锁骨前,对镜微笑
- 分解:拍1 手把曲奇送至唇前,张口轻咬掉一角(只动下颌,视线全程不离镜头);拍2 咀嚼两下,饼干停在唇边,头微左歪;拍3 手把饼干下移到锁骨前,缓慢眨眼一次(闭眼约 0.4s,睫毛颤动);拍4 饼干再次抬回唇边补咬一小口,嘴角带笑上扬
- H3:`close-up as her gloved hand brings a cookie to her lips, she takes a small bite without breaking eye contact, chews twice, lowers the cookie to her collarbone with one slow blink, then lifts it back for another tiny bite`
- 来源:《维琳娜》00:15-21.9s

### K36 风拢发托腮链(4拍|氛围)
- 入态:街边桌旁侧坐,侧马尾被阵风吹起 → 出态:手滑至颈侧衣领,头转向镜头浅笑
- 分解:拍1 阵风把侧马尾整体横吹过肩(发丝位移约 30cm,飘动明显滞后于头部);拍2 抬右手拢住飞发别到耳后(指尖贴鬓角滑行);拍3 顺势掌根托住下颌脸颊、肘撑桌面,头随手势压低约 10°;拍4 手沿下颌线下滑到颈侧领口,头回转向镜头,抿唇浅笑
- H3:`wind lifts her long side ponytail across her shoulder, she tucks the flying strands behind her ear, cups her cheek on her palm with elbow on the table, then slides the hand down to her collar and turns to the camera with a small smile`
- 来源:《维琳娜》00:22-26s

### K37 拂面遮眼挥手链(两景)(4拍|魅)
- 入态:正视镜头特写 → 出态:手撤出画,眨眼微笑
- 分解:段A 天幕拂面(26.4-30.9s,蓝天仰角、藏青袖):拍1 手从画右上入画,掌心朝脸横扫过双眼前,发丝被带起;拍2 手背贴额前滑向右侧太阳穴;拍3 双眼随手之遮挡闭合,头微仰;拍4 手离开,眼缓睁成月牙、笑意加深。段B 遮额横挥(47.0-50.8s,灰调室内、白外套):拍1 五指张开的手掌自右上入画盖住额头与右眼;拍2 掌心贴脸向左横移过半张脸(指缝间露眼);拍3 原路挥回右下,带动刘海飘起;拍4 手撤出画,眨眼对镜微笑
- H3:`her open palm enters the frame and slowly sweeps across her face covering her eyes with hair strands dragged along, then the hand waves back out of frame as she blinks into the lens with a deepening smile`
- 来源:《维琳娜》00:26.4-30.9s;00:47-50.8s

### K38 慵懒腿脚三景链(6拍|慵懒)
- 入态:坐姿小腿悬垂 → 出态:仰躺伸腿向镜、双脚尖交替点动
- 分解:段A 悬垂晃鞋(31.2-35.1s,白纱帘沙发沿):拍1 双小腿自然垂下悬空;拍2 一脚绷脚下压(厚底鞋跟离地)、另一脚勾起;拍3 双脚交替前后打水状小摆(幅度约 20cm,珍珠踝带反光闪动);拍4 双膝并拢内扣、脚尖相碰停住。段B 跪卧绷脚互剪(38.4-42.3s,白床):拍1 趴跪床面、小腿竖起;拍2 双小腿交剪一次上下互换;拍3 绷直脚尖、双脚同步左右轻摆;拍4 脚跟互磕一下。段C 交踝摇晃+点脚(52.0-59.3s,白床):拍1 仰躺、双腿伸向镜头双踝交叠;拍2 上位脚左右晃三次;拍3 双腿屈膝收向胸口再蹬直(脚尖绷直指向天空);拍4 双脚尖交替点动至近静止(56.2-59.3s 基本静态,仅脚尖微动)
- H3:`lazy footwork montage: sitting with calves dangling she seesaws her platform mary-janes, kneeling prone she crosses her raised shins and rocks her pointed toes, then lying back she extends her legs toward the camera with crossed ankles, wiggling her feet and flexing her toes`
- 来源:《维琳娜》00:31.2-35.1s;00:38.4-42.3s;00:52-59.3s

### K39 咖啡舔唇-wink 收尾链(4拍|微魅)
- 入态:暗背景特写、白瓷杯举至唇边 → 出态:逆光下发帘遮面,对镜单眼 wink 定格到片尾
- 分解:拍1 手捧白瓷杯啜饮一口(杯沿贴下唇约 1s,杯内黑咖啡液面晃动);拍2 杯下移至胸前,舌尖快速舔过上唇左右各一次,眼半阖;拍3 (切逆光)夕照亮发丝垂帘遮住双眼,抬手把发帘向侧拨开一缝;拍4 对镜单眼闭合 wink 约 1.5s、嘴角上扬,姿势保持至 75.0s 片尾
- H3:`she sips black coffee from a white cup close to the lens, lowers it and licks her lips with the tongue tip, then backlit by sunset her hair curtains over her eyes, she parts the strands and holds a one-eye wink at the camera until the shot ends`
- 来源:《维琳娜》01:00.1-07s;01:07.7-15s

**片<v09>《两个御姐合拍》(双人对镜甜舞·14.9s·竖屏)**
- 背景人物:酒店/公寓室内,米色木饰墙板与房门、门上金色长条牌、黑色电子锁挂绳,暖黄室内灯,全程单一固定机位。两名年轻女生并排穿同款浅蓝绞花针织开衫(麻花纹、木色扣、毛球拉头):左=黑色双马尾、素灰百褶裙、稍矮;右=黑长直披发、灰黑格纹百褶裙、稍高。均光腿,画面裁至小腿、鞋未见。无画外行动者。
- 节拍:有 BGM(mean -13.4dB);屈膝弹跳周期全程恒定约 0.4-0.5s、手势切换均落在弹跳谷值→固定节拍,约 120-130BPM(推测)。
- 镜头形态:A 一镜到底固定机位(判据:15s 内门框与门牌位置像素级不动,无变焦无平移无剪辑)。
- 双人总则:站位并排、间距约 0.5 个肩宽(40-50cm)、正对镜头、全程无肢体接触、无对视(都看镜头);配合方式="同向齐舞为底+三处错位加花"(1.6-2.4s 分工手势、10.0-10.8s 推掌/撩发、13.0s 镜像 OK 环眼);起手 0.0s 右生手掌已立在脸侧(右先半拍、左以大摆臂跟进);对靠与转身均由左生先启动、右生半拍内对齐。

### K40 开场双掌弹跳+错位指天拳托链(4拍|甜·双人)
- 入态:二人自然站立、左臂垂 → 出态:左指天/右拳托下巴,同步屈膝定格
- 分解:拍1 [0.0-0.4] 右生手掌立于右颊旁小挥,左生右臂自体侧大弧线上甩至脸旁(裙摆随重心偏移);拍2 [0.4-1.0] 双人同步双掌立颊侧、肘外撑,屈膝下沉半拍再弹起;拍3 [1.0-1.6] 双掌向外腕部开合两次,髋随弹跳左右各顶一次;拍4 [1.6-2.4] 分工错位:左生收掌换食指指天上摆两次,右生握拳收在下巴下轻颤,膝弹保持同频
- H3:`two girls side by side facing the camera, the right one waves a palm beside her face a half-beat early while the left swings her arm up in a big arc, they bounce on bent knees with palms at their cheeks, then the left points her index finger skyward twice as the right holds a fist under her chin`
- 来源:《两个御姐合拍》00:00-2.4s

### K41 对靠转身回眸链(3拍|甜·双人)
- 入态:双掌颊侧 → 出态:转回正面、拳托下巴轻弹站直
- 分解:拍1 [2.4-3.2] 双人相向内倾、头几乎贴鬓,双拳收下巴,同步屈膝(内侧肩几近相碰,唯一的"接近"互动);拍2 [3.2-4.2] 左先右随同步向外转身约 90° 背对镜头,双马尾与长发甩出弧线,越肩回眸看镜头;拍3 [4.2-5.0] 转回正面,拳托下巴轻弹两下、身体拉直
- H3:`the duo leans their heads toward each other with fists at their chins, then spins outward in sync turning their backs with an over-the-shoulder glance as twin-tails and long hair whip around, before returning to face front bouncing lightly with fists under their chins`
- 来源:《两个御姐合拍》00:02.4-5s

### K42 指天摇摆+胸前比心链(3拍|甜·双人)
- 入态:拳托下巴直立 → 出态:胸前比心收、屈膝小弹
- 分解:拍1 [5.0-5.8] 双人食指指天,腕部向外画小圈摇摆、身体拉高;拍2 [6.0-6.8] 收指换拇指食指捏合胸前比心,两人心位一高一低错开,屈膝小弹;拍3 [7.0-8.8] 再指天摇摆两轮,手臂下落预备大摆臂
- H3:`both girls point their index fingers skyward waggling in small outward circles, pinch matching finger hearts at chest level offset one higher one lower on a bouncy dip, then repeat the sky-point twice before dropping their arms to prepare a big swing`
- 来源:《两个御姐合拍》00:05-8.8s

### K43 摆臂推掌-脸侧摆掌-镜像 OK 环眼链(6拍|甜·双人)
- 入态:双臂张开放松 → 出态:双人 OK 圈扣眼、歪头弹跳定格至片尾
- 分解:拍1 [8.8-9.8] 双臂从上向下大摆劈过体前(掌心朝下),同步屈膝下沉;拍2 [10.0-10.8] 错位加花:左生掌心朝前推出两次(欢迎式),右生单手拎起披发发尾向外一甩;拍3 [11.0-11.8] 双臂向后下摆再回摆,右生长发回落肩头;拍4 [12.0-12.8] 双掌立脸侧左右快摆(停止式),头反向小摆;拍5 [13.0-13.8] 镜像 OK 手势:左生 OK 圈扣右眼、右生扣左眼(圈口朝镜头);拍6 [13.8-14.9] 保持 OK 圈,头随节拍左右轻摆+膝弹,定格收尾
- H3:`both girls swing their arms down through the front in sync with a knee dip, the left pushes her palm forward twice as the right flips her long hair over her shoulder, they wave open palms beside their faces with heads tilting, and finish mirrored making OK circles around their inner eyes, wobbling their heads on the beat into the ending freeze`
- 来源:《两个御姐合拍》00:08.8-14.9s

**片<v10>《请pick西施吧～》(现代学院风单人宅舞·32.7s·4K竖屏)**
- 背景人物:地下通道/展馆廊道——抛光灰石大板块墙面与方柱、绿色安全出口指示灯、反光水泥地坪、冷白顶光,纵深可见金属伸缩缝线条;无他人入画(标题"西施"与画面无关,帧证据为准,全程为现代制服街舞)。人物:18-22 岁感少女;黑长直+空气刘海+白色花形发饰与蓝色发带;浅蓝紫(periwinkle)短款学院西装外套(藏青袖口)、白衬衫、藏青领带、藏青腰封,蓝格纹百褶短裙(下摆缀白蕾丝衬裙层、内着黑色安全裤);白色过膝袜(膝侧黑丝带蝴蝶结)、黑色厚底乐福鞋;无手持道具。
- 节拍:有 BGM(mean -11.1dB/max 0.0dB,明显响度限制);动作约每 0.5-1.0s 一换(50fps 密帧判读),推测约 120-128BPM 固定节拍(推测)。
- 镜头形态:A 一镜到底(判据:全程同机位竖拍、立柱与出口灯相对位置连续无跳切,景别变化全靠人物走位)。

### K44 合手弹腕开场链(4拍|萌)
- 入态:静立低头,双手交叠合于胸前 → 出态:双手收回胸前,屈膝微弹
- 分解:拍1 双手交叠合胸、低头蓄势,随重拍抬头提沉一次呼吸;拍2 双手在胸前一握一松轻晃,头左右各歪一次,受力全来自腕部小幅屈伸;拍3 右手抬至耳侧、指尖向外弹开一次(半拍 accent);拍4 手腕回勾收回胸前,膝部小弹吸收
- H3:`standing still then lifting her folded hands at her chest with a small nod on the downbeat, one wrist flick popping her fingertips open beside her ear on the half-beat, knees softly bouncing, static frontal locked-off vertical camera`
- 来源:《请pick西施吧～》00:00-2.2s

### K45 对角举臂后踢小跳链(4拍|元气)
- 入态:双手胸前持位 → 出态:双掌立于脸侧,屈膝弹动
- 分解:拍1 左手挥至头顶斜上方、右拳收胸;拍2-3 换右臂直臂斜上举,同时左小腿后勾、脚跟踢向臀部,身体向左侧倾——发力来自髋前侧提拉+对侧臂反向配重;拍3-4 换边再做一次,重心经小跳上提;拍4 落地屈膝,双手上抬至脸侧掌心朝前,借落地惯性弹两下收住
- H3:`alternating straight arms punching diagonally overhead while the opposite heel kicks back toward her hip in small skips, body tilting into the line of the arm, pleated tartan skirt bouncing with each landing, ending with both palms framed beside her face and knees absorbing into a bounce`
- 来源:《请pick西施吧～》00:02.4-4.6s

### K46 顶胯侧身框脸展示链(6拍|萌)
- 入态:掌立脸侧弹动 → 出态:双掌摊开于体侧、耸肩
- 分解:拍1 双腕交叉于胸前成 X,随拍向下拨开;拍2 右臂伸直指向右方、掌心向上做"请"式展示,左手叉腰,双腿开立;拍3-4 双臂展开、胯向右顶出,顺势侧身转 3/4 背对镜头——格纹裙摆随转身离心甩起、白蕾丝衬裙边外翻;拍5 转回正面,双手抬至脸颊两侧比"取景框"手势,屈膝下蹲一拍;拍6 双手向两侧摊开掌心向上、耸肩定格(受力顺序:胯驱动→臂跟随→肩回收)
- H3:`crossing her wrists into an X then sweeping them open into a palm-up presenting gesture, popping the hip and rotating three-quarters away so the plaid skirt flares off its lace petticoat, spinning back to frame her face with both hands in a viewfinder shape before opening the palms wide with a shrug`
- 来源:《请pick西施吧～》00:05.5-9.5s

### K47 背身平转甩发链(6拍|全片唯一大转·放 1/3 进度处)
- 入态:双手抬至领口、右臂屈肘上冲蓄力 → 出态:面向镜头、拳收胸前、屈膝微弹
- 分解:拍1 双手提至领口,右臂屈肘向上冲拳(起转预备);拍2 以左脚前掌为轴蹬地起转,双臂张开扩角动量,重心轴心垂直;拍3-4 平转 360°——技术峰值:转至背对镜头时长发完全水平甩出、格纹裙摆展平露出白色蕾丝衬裙与黑安全裤(黑发与裙摆双延迟层);拍5 转回面向镜头,发梢扫过面部借惯性继续飘,左拳上举急停亮相;拍6 拳收回胸前,屈膝下弹一次吸收角动量残量
- H3:`spot pivot turn on the left foot with arms opening wide for angular momentum, waist-length black hair whipping fully horizontal through the back of the spin while the layered skirt lifts off its lace hem, stopping hard facing camera with one fist punched up, hair settling across her face before she recovers into a knee bounce`
- 来源:《请pick西施吧～》00:10.4-12.6s

### K48 行进冲拳托腮接侧踢展臂链(8拍|元气)
- 入态:拳收胸前弹动 → 出态:并步站立、单手举于头侧
- 分解:拍1-4 原地提膝踏步,对侧拳随每步向上冲(4 次),发力来自支撑腿蹬地+髋上提,裙摆随提膝摆动;拍5-6 双拳收至下颌下方做"托腮"状、头歪向一侧(萌点 accent);拍7 双臂由体侧向外划开成 T,接双臂上举成 V 开腕、屈膝下弹两次;拍8 右腿向右直腿踢出点地、双臂做左低右高反向平衡,收腿并步、单手回落至头侧
- H3:`marching in place with opposite fists punching up on each knee lift, tucking both fists under her chin with a head tilt, sweeping the arms out to a T and up into an open-wrist V with two deep knee bounces, then kicking one leg straight out to the side with counter-tilted arms before stepping together`
- 来源:《请pick西施吧～》00:14.4-20.4s

### K49 收尾双横杠比心谢幕链(6拍|萌·放结尾)
- 入态:开立屈膝、双臂前平举 → 出态:双脚交叉站定、低头谢幕定格
- 分解:拍1 双臂前平举向下甩、开立步屈膝下沉;拍2-3 右小臂横于额前、左小臂横于胸前叠成"双横杠",同时右脚交叉落于左脚侧;拍4 双手沿中线上提至头顶合拢比心、随即开腕向外打开;拍5 双手落至肩侧握拳上举两次(半拍 accent);拍6 双臂自然下垂微张、低头谢幕,全部动量静止收零
- H3:`stacking one forearm across her brow and the other across her chest into a double-bar pose with feet crossed, lifting both hands overhead to close into a heart then popping it open, two small fist pumps by the shoulders, finishing with a soft bow and crossed feet, static full-body vertical framing`
- 来源:《请pick西施吧～》00:29.8-33s

**片<v11>《I Got Your Back》(K-pop 日综初舞台群舞·154.3s·横屏)**
- 背景人物:日本电视演播厅(CDTV Live! Live! 标识+HARUKA AUDITION/セーラー服姿で初パフォーマンス 字幕),多套 LED 舞美轮换:粉色 CDTV 墙、绿菱格、蓝白条纹、橙黄卡通收音机音符墙、红蓝棋盘格、品红格、白钻石灯阵、"I Got Your Back"横幅;镜面地板反射人影;画外有主持人旁白与节目字幕(推测)。人物:5 名女团成员,统一白色水手短袖(藏青海员领)+超大缎面蝴蝶结(薄荷绿/红/粉/浅蓝区分成员),黑藏青百褶裙(midi 与短裙混排),白过膝袜+乐福鞋或黑色长靴;两名成员戴细金丝眼镜;发型黑长直/齐刘海波波头/低马尾;全程手持银色/粉色麦克风。
- 节拍:有 BGM(现场音轨 mean -25.2dB/max -9.0dB,含观众混响);K-pop 中快板,推测约 124-128BPM(推测),编舞含大量半拍 accent 与膝弹律动层。
- 镜头形态:C 多镜头快剪(判据:同一乐句内宽/中/特写/摇臂高频切换,33-44s 内可见 5 个以上机位;成员走位与队形变换配合剪辑)。

### K50 进场高踢接抱臂横移链(6拍|清凉)
- 入态:分组走位进场 → 出态:双指点自己脸颊、半蹲弹
- 分解:拍1 中央成员右腿前踢过腰——发力来自支撑腿提踵+髋屈肌急收,短裙翻起露出裙内层,双臂自然张开配平;拍2 落地前掌缓冲屈膝接小跳;拍3-4 三人一组双臂交叉抱于胸前成 X,双脚交替侧点横移,头随步位方向转(律动层:膝部保持半拍弹);拍5-6 金丝眼镜成员松开抱臂,双食指指向自己脸颊做"羞"点,配合眨眼,半蹲吸震收住
- H3:`one center member snapping a high front kick past her waist with the pleated skirt flipping, landing into a bounce, the trio crossing their arms over their chests and side-stepping with the heads turning on each step, closing on a bespectacled member poking both index fingers at her cheeks in a half-squat, wide TV variety lens with mirrored floor reflections`
- 来源:《I Got Your Back》00:05.5-9.2s

### K51 屋顶手比划链(4拍|萌)
- 入态:直立持麦对唱位 → 出态:摊掌耸肩
- 分解:拍1 双臂在头顶搭成三角"屋顶",肘外张、手腕相触;拍2 屋顶手沿身体中线整体下压至脸前翻腕(连续弧线,肩胛带动);拍3 右手食指回点自己脸颊、头歪;拍4 双手向外摊开耸肩一次(半拍 accent),重心回正
- H3:`forming a triangle rooftop overhead with both arms, sliding the whole shape down the centerline to her face and flipping the wrists, pointing one finger at her own cheek with a head tilt, then opening the hands wide with a shrug on the half-beat, medium close-up TV framing`
- 来源:《I Got Your Back》00:34.3-36.7s(同族动作 00:08.4-9.2s 复现)

### K52 收音机跳步展臂链(8拍|复古活力)
- 入态:宽站姿高重心 → 出态:半蹲双臂下压
- 分解:拍1-2 宽站屈膝半蹲,双臂由上向下大力甩压——发力来自躯干前屈+肩带下压,裙摆下摆翻飞;拍3-4 双臂屈肘上举成 V、拳心朝前,重心左右各弹跳换一次;拍5-6 双臂收回胸前屈肘,胯部左右顶摆两拍(律动层:膝弹持续);拍7-8 侧步两点横移、双臂配合下压推掌,队形整体横移,镜面地板倒影同步
- H3:`wide-stance deep knee dips swinging both arms from overhead down past the thighs, popping the arms up into a flexed V with side-to-side weight bounces, hips ticking left and right with hands coiled at the chest, finishing on travelling side-steps pushing the palms down as the line shuffles across the reflective stage`
- 来源:《I Got Your Back》00:40.5-44s

### K53 背身甩发转身冲拳链(4拍|转体 accent)
- 入态:长发成员正面对镜头 → 出态:拳落于体侧、屈膝弹
- 分解:拍1 长发成员向右后快速转身背对镜头——头先走、长发横向甩出(延迟层明显),短发成员同时向镜头顶胯;拍2 蹬地转回面向镜头,发梢扫过脸颊借惯性继续飘;拍3 绿蝴蝶结波波头成员右臂向上冲拳;拍4 同臂向下劈落收至体侧,屈膝下弹,"hey"口型对半拍
- H3:`the long-haired member whipping a fast full turn away from camera with her hair fanning horizontal then spinning back so the ends sweep her face, the bob-haired member beside her punching one fist up and chopping it down on the half-beat with a shouted accent, quick TV cut between wide and medium`
- 来源:《I Got Your Back》01:05.3-01:07.4s

### K54 深蹲横摆大扫臂链(8拍|律动·第二段主歌记忆点)
- 入态:开立直立 → 出态:直立双臂打开回弹
- 分解:拍1-2 双膝深屈、上体右倾,右臂上伸左臂下伸成对角线拉长(侧腰发力);拍3-4 换左侧做镜像对角拉长,两拍一次大幅钟摆;拍5-6 上体前屈近 90°,双臂贴地向下向内大扫——技术峰值:躯干折叠+发丝全部前垂,重心压至脚跟;拍7-8 直起,双臂经胸前交叉上提再打开,直立回弹收住
- H3:`deep side leans stretching one arm up and the other down into a long diagonal like a pendulum, folding fully forward at the waist sweeping both arms low toward the floor with hair falling forward, then rising through a chest-level arm cross into an open recovery with a knee bounce, red and blue LED checkerboard wall behind a staggered formation`
- 来源:《I Got Your Back》01:14-01:18.5s

### K55 交替甩臂下压步链(8拍|副歌主链·两段副歌复用)
- 入态:横移中、双臂低位 → 出态:双臂 V 举、继续横移
- 分解:拍1-2 右臂屈肘上举后向下甩拍向大腿,同时右膝由弯弹直(半拍 accent);拍3-4 左臂镜像甩下、左膝弹直,重心左右横移(律动层:胯随重心微坐);拍5-6 双臂同时下压+屈膝下沉一次(重拍 double accent);拍7-8 双臂上举成 V 开腕,脚下两点横移,百褶裙随步幅翻飞,队形保持斜线
- H3:`alternating arms snapping from a bent raised position down to slap the thigh while the same-side knee pops straight, weight rocking side to side, a double-arm push-down with a deep knee drop on the accent, then both arms up in an open-wrist V travelling with two-step side touches, pleated skirts flaring, magenta LED grid wide shot`
- 来源:《I Got Your Back》01:32.5-01:36.5s;01:40.7-01:43s(第二遍副歌复用)

### K56 肩拍推掌原地转回眸链(8拍|末段高潮)
- 入态:两排站位 → 出态:单手叉腰、后仰回眸定格
- 分解:拍1-2 双手交替拍对侧肩后向前下方推掌(像拍灰-送出);拍3-4 右手指点左腕作"看表"状、随即向外一甩;拍5-6 侧点步双臂下压,前后排交错换位;拍7-8 原地平转一圈——黑裙完全展开、轴心稳定,落定瞬间单手叉腰、上体后仰 15° 回眸镜头,镜面地板倒影延长旋转残像
- H3:`patting the opposite shoulders then pushing both palms forward and down, pointing at the wrist like checking a watch and flicking it away, cross-stepping with arms pressing down through a formation switch, one member doing a clean full pivot with the black pleated skirt flaring out and landing into a hand-on-hip lean-back glance over her shoulder at the camera`
- 来源:《I Got Your Back》02:00-02:06.5s

**片<v12>《依赖姐姐》(多场景换装手势舞+氛围卡点·72.0s·竖屏)**
- 背景人物:8 组场景硬切轮换——(1)暖光卧室窗帘前(银灰缎吊带+藏青纱裙→白缎抹胸→白衬衫粉结粉裙→粉蕾丝连体裙,棕红盘发+白花发饰+珍珠耳坠);(2)绿藤墙(奶油纱吊带裙+珍珠 choker,手持小相机,黑发);(3)庭院池塘(白蝴蝶结+白蕾丝边吊带裙,双手捧白纸包花束);(4)竹林(学院制服白衬衫粉领结粉格裙);(5)池塘白一字肩荷叶裙;(6)小路背影(白上衣+墨绿格裙+黑色单肩包);(7)夕阳草坪(薄荷荷叶吊带+牛仔短裤,前景树叶遮挡);(8)海崖矮墙(白色针织开衫+灰连帽+白荷叶长裙,阴天海景,风大)。全程单人,无画外行动者。人物:同一女生,前段棕红盘发戴花、后段黑长直/半扎;鞋袜基本不入画(中近景构图);手持道具:小相机、花束、黑包。
- 节拍:有音轨(mean -10.0dB/max 0.0dB),手势换点与转场点不成等差(转场实测约 10.3/25.6/37.2/50.0/55.5/57.7/59.5/61.7s)→判定按歌词/重音卡点而非固定 BPM(推测)。
- 镜头形态:B 编辑快照(判据:8 组以上场景硬切,组内为单机位手持自拍式固定机位,无运镜)。

### K57 猫爪翻腕摆掌链(8拍|软萌)
- 入态:侧身转正、双手低位 → 出态:双爪收至胸前
- 分解:拍1-2 双手提至胸前、五指蜷成猫爪向内各绕腕一圈(腕关节主导);拍3 双腕相靠、掌心向下同时下压翻腕一次;拍4-5 双掌心朝外于胸高处左右摆动(摆手拒绝感),头随手反方向歪;拍6 右掌外摆、左拳收腰对比;拍7-8 双爪上提至肩侧屈肘、指尖向下连卷两次(猫爪颤,半拍 accent),收至胸前站定
- H3:`curling both hands into cat paws circling the wrists at chest height, flopping the palms downward together, then waving both palms outward at shoulder level with the head tilting opposite, finishing with two downward paw curls by the shoulders on the half-beats, intimate handheld selfie framing with warm lamp light`
- 来源:《依赖姐姐》00:00.8-7.5s;00:20-25.5s(白缎裙段同族双掌摆复用)

### K58 比心托掌转指链(8拍|甜美)
- 入态:双手收于胸前 → 出态:双手交叠收于锁骨前
- 分解:拍1-2 双手拇指食指于胸前相捏成小心心、轻抖两下;拍3-4 右臂前伸翻掌心向上做"托举奉上",头随之微倾、视线落掌心;拍5 左手平掌自内向外抹过(擦掌收势);拍6-7 右手食指向外侧连点两下后绕腕收回;拍8 双手交叠按于锁骨前、耸肩一次,肩线全程放松下沉
- H3:`pinching a tiny heart with both thumbs and index fingers at her chest with a little shake, extending one arm to offer an upturned palm with the gaze dropping to it, wiping the flat hand across and pointing twice to the outside with a wrist roll, closing both hands stacked at the collarbone with a shrug`
- 来源:《依赖姐姐》00:13.3-20s

### K59 指脸颊握拳托腮链(8拍|邻家甜)
- 入态:叉腰站位 → 出态:双拳并拢抵下颌
- 分解:拍1-2 右食指点自己太阳穴画小圈、头歪(思考感);拍3-4 双食指同时点两侧酒窝位两次(半拍节奏);拍5-6 双拳提至肩前、前臂内旋拳心向上翻出;拍7-8 双拳并拢抵住下颌、头左右轻摆两次;粉蕾丝段同族收尾:双手比 V 置头两侧、手腕弹动两下
- H3:`circling one fingertip at her temple with a tilted head, double-tapping both dimples with index fingers, rolling both fists up from the shoulders palms-up, then tucking the fists together under her chin swaying the head side to side, ending in double peace-Vs at her head with flicking wrists, warm bedroom bokeh background`
- 来源:《依赖姐姐》00:26.7-33.3s;00:45-46.5s(V 手段)

### K60 卡点换装扫臂链(2拍x8组|剪辑结构·全片骨架)
- 入态:当前场景定姿尾拍 → 出态:新场景首帧"姿势已就位"
- 分解:拍1(切前半拍)单臂或双臂向斜下方大力扫出/原地半转,身体侧倾蓄力并压暗构图重心;拍2(重拍帧)服装与场景硬切——新造型在切后第一帧已完成姿态(手插发间/持花/叉腰/回眸),无过渡动作;切后 1-2 拍只动头与眼(歪头/回眸/垂眸),让裙摆与发丝物理自然沉降完成"呼吸感";结构点位:10.3s 银缎→白缎(扫臂+转身模糊帧)、25.6s→衬衫粉结、37.2s→粉蕾丝、50.0s→持花白裙、55.5-57.9s 连三切(制服→白裙→背包背影)、59.5-61.9s 连两切(薄荷吊带→海崖白衫)
- H3:`each outfit change lands on the beat drop: a hard diagonal arm sweep or half turn blurs the frame, the cut reveals the new outfit already holding its pose with hands in hair or bouquet in hand, then one or two beats of only head tilts and glances while the skirt and hair physics settle, vertical selfie-camera framing with jump cuts`
- 来源:《依赖姐姐》00:10.3-10.9;00:25.6-26.3;00:37.2-37.8;00:50-50.6;00:55.5-57.9;00:59.5-61.9s

### K61 海崖回眸甩发链(8拍|氛围感·放结尾)
- 入态:侧身倚矮墙、背对海面 → 出态:3/4 背身回望定格
- 分解:拍1-2 侧身倚白色矮墙、上身后仰约 15°,长发垂落过肩,缓缓回眸看向镜头(海风为持续外力,发丝全程微飘);拍3 手背于发间拢发一次,头随抬手倾斜;拍4-5 快速向右甩头转脸——长发横扫过面部(64.7s 帧呈运动模糊,技术峰值:头部角速度+发丝延迟形成扇面),随即回正再次回眸;拍6-7 转为 3/4 背对镜头,一手举至肩侧比"OK",从肩上方回望;拍8 头轻靠向肩、身体重量交给矮墙,定格收尾
- H3:`leaning back against a white seaside parapet with the wind lifting her long black hair, turning into a slow over-the-shoulder glance, snapping her head quickly so the hair whips in a blurred fan across her face before settling back to camera, then posing three-quarters away showing an OK sign above her shoulder with one last look back, overcast coastal light, static vertical framing`
- 来源:《依赖姐姐》01:01.7-12s

**片<v13>《我是银月呀❤》(AIGC 萌系摆拍·18.1s·竖屏)**
- 背景人物:日式居酒屋内景——木格酒架满陈清酒瓶(可见"濁り"等标签)、木质矮桌与蒲团、墙面电视(前段播黑白影像、7s 后播足球赛绿茵画面)、暖黄灯光、矮桌上散置食物与红色饮料杯;0-0.6s 为无人空镜定场。人物:年轻成年女性(20 岁上下感),银白超直长发垂腰、额侧碎发、颅侧编发盘绕;白色狐耳(缀银色钉饰);身后巨大蓬松白狐尾;白色短上衣+金色镶边胸襟、金色高领环嵌红宝石、纱质肩袖带金饰、金色臂环与腕环、腰间金封红绸带长垂及地、赤足、双踝金脚链带垂坠与趾环;1-3s 胸前叠加 Q 版狐娘贴纸动画;带"ZonerR念头通达/bilibili""AIGC-ZONER"水印,AI 生成/重绘质感。画外行动者:无。
- 节拍:有 BGM(mean -13dB/max 0dB,饱满);动作以"造型-保持"为主、无严格卡点,属自由节拍萌系摆拍(BPM 无法锁定,推测)。
- 镜头形态:C 多镜头快剪——共 5 段,硬切点 0.6s(甩镜模糊转场)/7.0s/12.2s/14.5s;各镜头内机位固定;全片无相机 Roll,酒架线均水平。

### K62 盘腿双 V 喵语链(4拍|萌)
- 入态:盘腿坐于蒲团、右手起于脸侧 → 出态:双手保持双 V 手势、张嘴"喵"表情定格
- 分解:拍1 右手举至脸侧五指张开、左手搭膝、目视镜头(0.8s);拍2 右手变 V 字上举、左手于脚踝前向下指 V、张嘴发声口型、狐耳随头势立起(1.4-1.8);拍3 右手换 OK 指、左手 V 字下指、双肩微耸——双手异型手势+喵口型为技术峰值(2.0-2.6);拍4 头向右歪、长发顺势垂滑、V 字保持、Q 版贴纸在胸前同步跳动(2.8-3.2);发力来源均为腕指小肌群,肩颈放松;白裙下摆铺地展开成扇形随坐姿静止;机位眼高固定,人物占画面中下 2/3
- H3:`sitting cross-legged on a floor cushion, waving alternating V-sign and OK gestures with both hands beside her face while mouthing a cute meow, fox ears perked, long silver hair sliding over still shoulders, eye-level static shot`
- 来源:《我是银月呀❤》00:00.6-3.2s

### K63 伸腿双猫爪链(3拍|萌)
- 入态:盘腿坐、双手收于脚踝 → 出态:双膝弯朝镜头伸出、双爪定格脸侧
- 分解:拍1 双手自脚踝处沿身前划弧上举至脸侧、五指张开、嘴张大(起手路径:腕带臂、臂带肘,全程坐骨不动)(4.5-5.9);拍2 双腿向前蹬伸、膝弯朝向镜头、小腿交叠悬起——重心后坐由尾椎与蒲团共同承接(6.1-6.5);拍3 双手屈腕收指成猫爪、掌心朝镜头、噘嘴,头部微左倾——造型峰值为"双爪+伸腿怼镜"透视(6.5-7.0);赤足金脚链随腿伸出而轻晃;裙摆滑落大腿根部露金饰;袖口红绸垂落静止;机位低于脸、腿在前景放大形成透视压迫
- H3:`reclining back on a cushion and stretching both bent knees toward the camera, she raises curled cat-paw hands beside her pouting face, gold anklets swaying on lifted feet, low-angle shot with legs foreshortened in the foreground`
- 来源:《我是银月呀❤》00:04.5-7s

### K64 桌沿托腮递葫芦链(4拍|俏)
- 入态(切镜后):侧坐桌沿、双腿并拢斜垂 → 出态:绿葫芦举至镜头前
- 分解:拍1 硬切入画——侧坐木质桌沿、右拳托下巴、双腿斜伸脚尖轻点、目光直视镜头(7.0-7.6);拍2 静止亮相:巨大白狐尾平铺身后桌面、仅尾巴尖端与耳廓偶发微颤(静态,明写)(7.6-9.5);拍3 右手离下巴、左手捞起搁在膝上的绿玉葫芦、躯干前倾启动(9.5-11.0);拍4 手臂前伸将葫芦递向镜头、头微歪眨眼,机位同时下摇让出腿部——道具怼镜为峰值(11.0-12.2);尾巴因躯干前倾被轻微牵拉移位;红绸带从腰间滑落桌面;葫芦入画时轻微虚焦引导视线
- H3:`perching sideways on a wooden table edge with her fist tucked under her chin, huge fox tail spread flat behind her, she lifts a small green gourd off her knee and reaches it straight toward the lens with a tilted head, static shot pulling focus to the offering hand`
- 来源:《我是银月呀❤》00:07-12.2s

### K65 赤足悬摆链(4拍|细节)
- 入态:腿部特写入画、双脚悬垂 → 出态:双脚交叠静止
- 分解:拍1 双脚悬空一前一后交替摆动、摆幅小而匀(惯性来自小腿自重)(12.3-13.0);拍2 右脚抬起搭上左脚踝、完成交叉(13.0-13.6);拍3 脚尖绷直下压、金脚链垂坠与趾环同步摇晃——足部细节峰值(13.6-14.0);拍4 缓慢解除交叉恢复悬垂(14.0-14.4);全程无面部入画;裙摆垂纹与红绸构成背景;低机位近距特写,景深极浅
- H3:`extreme close-up on bare feet with ornate gold anklets dangling and crossing at the ankles, toes pointing and curling as the chains sway, shallow depth of field over flowing white silk, low static camera`
- 来源:《我是银月呀❤》00:12.2-14.4s

### K66 抱膝低头抱葫芦链(3拍|治愈)
- 入态(切镜后):地垫全景观、双膝并拢立起 → 出态:低头抱葫芦静止保持至片尾
- 分解:拍1 硬切入全景——屈膝坐抱、双膝并拢立起、双手合抱绿葫芦抵于膝前(14.5-15.2);拍2 头缓缓低下、视线落向葫芦、狐耳向后压平半拍(耳动滞后头动)(15.2-16.0);拍3 静止保持:仅呼吸起伏与尾尖轻颤(静态,明写,推测微动)(16.0-18.1);全身蜷缩姿态受力闭环:膝承双肘、肘托葫芦、头重量垂落颈椎放松;尾巴绕至体侧垫地;机位正面眼高全景,人物居中,左右酒架对称收拢视线
- H3:`sitting curled up on the floor with knees drawn together, hugging a small green gourd against her knees and bowing her head to look at it, fox ears folding back a half-beat late, fluffy tail curled at her side, static symmetrical full shot`
- 来源:《我是银月呀❤》00:14.5-18.1s

**片<v14>《活动饭拍》(真人活动现场·11.6s·竖屏)**
- 背景人物:室外见面会/活动场景,午后暖侧光——米黄色墙面覆满树影光斑、右上暗色窗框;人物立于高台/台阶上,台下簇拥摄影师后脑勺与长焦相机(白炮黑身),画面中央一只举手机稳定器的手正对她。人物:年轻成年女性(20 岁上下),深棕发低盘发+粉白花环头饰;白色垂坠深 V 无袖连衣裙(披肩领、裙料轻薄飘逸);红唇、右腕银手链;无手持道具。画外行动者:台下摄影师群(持续举机),稳定器持机者一只手常驻画面中下部。
- 节拍:无固定节拍——自由散板;音量大(mean -7.4dB)但为现场环境声与人群响动(推测),动作随互动随意发生。
- 镜头形态:A 一镜到底(手持饭拍机位,全程连续无硬切,7.7-8.5s 机位平滑后退由中景转全景,画面带手持呼吸感微晃);无相机 Roll。

### K67 举脸比心链(4拍|甜)
- 入态:双手垂于身前 → 出态:双手桃心框住面部保持
- 分解:拍1 双手自身前抬起、肘部外张上提(复现段 6.9s 处可见以右手拇指食指先捻合起手)(0-0.2/6.9-7.1);拍2 双手拇指与食指相抵拼成桃心、举至脸前正对镜头(0.2-0.6);拍3 桃心整体随头部左右轻摆向两侧摄影师展示——峰值点:桃心稳定成形且面带笑容(0.6-1.2);拍4 桃心降至下巴高度、手指微调形状(1.2-1.5);发力源为三角肌前束与拇指食指对捏;手链与袖口随抬臂轻晃;手持机位带微晃、轻微仰拍、台下后脑勺作前景框
- H3:`raising both hands from her waist to form a heart with thumbs and index fingers framing her smiling face, tilting the heart side to side for the crowd of photographers below, handheld low-angle fancam with camera heads in the foreground`
- 来源:《活动饭拍》00:00-1.5s(复现:00:02.8-4.4s、00:06.9-8.9s)

### K68 收心垂手羞立链(3拍|甜)
- 入态:桃心散开 → 出态:直立站定、手交叠身前、侧头羞笑(静止)
- 分解:拍1 桃心双手分开、沿身前弧线下落至腰腹前交叠(1.6-2.0);拍2 头低下羞笑、双肩微收内扣(2.0-2.4/4.8-5.4);拍3 头转向一侧看别处再回正、身体直立静止亮相(静态,明写)(2.4-2.7/5.4-6.7);重心全程压在双脚无位移,靠头颈与手部小动作完成"撒娇-害羞-站定"节奏;白裙垂坠面料随下落手臂轻微贴身;机位保持手持仰角不变
- H3:`lowering her hands from the heart gesture to rest folded in front of her waist, dropping her head with a shy smile before glancing away and standing still in the white draped dress, steady handheld shot through dappled tree shadows`
- 来源:《活动饭拍》00:01.6-2.7s(复现:00:04.6-6.7s)

### K69 持心缓降收势链(3拍|甜)
- 入态:桃心贴脸保持 → 出态:桃心停于胸前、低头浅笑收尾(静态)
- 分解:拍1 保持桃心形状不变、整体从脸前匀速下降(8.9-9.6);拍2 降至下巴与锁骨之间、目光从桃心上缘越出看镜头(9.6-10.4);拍3 桃心停在胸前、头微低浅笑定格至片尾(静态收束,明写)(10.4-11.5);拍间无松手无变形是技术要点;下降匀速来自肘部缓慢屈曲;腕间银手链随缓降轻晃;机位同期已退为全景,人群与相机阵在前景形成"被围观"框架
- H3:`holding a perfect finger heart shape while slowly lowering it from her face down to her chest, eyes peeking over the heart at the camera before resting with a soft smile, wide handheld fancam surrounded by photographers`
- 来源:《活动饭拍》00:08.9-11.5s

**片<v15>《旗袍夜景》(AIGC 旗袍夜舞·16.8s·竖屏)**
- 背景人物:夜晚庭院式餐厅/酒馆——暖黄串灯虚化光斑、绿植、木质梁架、桌椅剪影,暗调暖光。人物:年轻成年女性(20 岁上下),黑长发半扎、八字刘海垂肩;左眼角旁红色梅花瓣妆贴;长款垂坠耳环;黑丝绒短袖旗袍:立领黑色盘扣、红色梅花亮片绣自下摆攀至胸前、侧开衩及膝;无手持道具。皮肤与光斑过度平滑,疑 AIGC 生成/重绘(推测)。画外行动者:无。
- 节拍:有固定节拍 BGM(mean -9dB/max 0dB);动作约每 0.8-1.2s 换招、与重拍基本吻合,约 90-105BPM 中速舞曲(推测)。
- 镜头形态:C 仅 2 镜——主体 0-15.6s 一镜到底(胸上高度固定中景、微幅漂移),15.7s 硬切面部特写至结尾;无相机 Roll。

### K70 掌花掩口飞扑链(4拍|媚)
- 入态:正面微侧站立、双掌合于面部前 → 出态:手臂回落体侧、身体转回正面
- 分解:拍1 双掌于脸前相互摩挲滑开、笑眼弯弯(0-0.4);拍2 右掌掩口、左掌自下向前伸拍向镜头方向——掌风扫过产生大面积动态模糊,为峰值(0.6-1.2);拍3 左臂横扫越过镜头前、身体随之右转回旋、头右倾长发甩出弧线(1.4-2.0);拍4 手臂借惯性回落体侧、胯部回正、脚步微调站稳(2.2-2.8);发力源为腰胯旋转带动大臂;旗袍下摆在转体处贴腿后又荡开;耳环随头部回旋横摆半拍;机位胸上固定,掌掠过镜头时占满画幅
- H3:`covering her mouth with one palm while flicking the other hand out toward the lens in a flirty wave, sweeping the arm across the frame with heavy motion blur as her hips twist and long black hair whips in an arc, static medium shot in a lantern-lit garden bar`
- 来源:《旗袍夜景》00:00-2.8s

### K71 下扫交叉滚腕链(4拍|舞)
- 入态:正面站立、右手起于脸侧 → 出态:双掌在胸前完成波浪下滑
- 分解:拍1 右手食指上指于脸侧、随即整臂下扫过腹前、胯向右顶出(3.0-4.0);拍2 双臂于胸前交叉——右臂横抱、左手举至头侧比 V(4.2-4.4);拍3 以手腕为轴双臂交叉滚开、双掌外翻同时推出——开合爆发为峰值(4.6-5.0);拍4 双掌在胸前交替波浪、掌根引掌尖依次下压滑落(5.2-5.6);拍1 发力自腰侧腹斜肌,拍3 为前臂旋前+腕屈同步;旗袍胸襟盘扣区随开胸动作展平;垂坠耳环在滚腕时小幅摆动;机位固定中景,交叉-展开的横向幅度占满画面宽度
- H3:`sweeping one arm down across her body with a hip pop, crossing both forearms in front of her chest and rolling the wrists open to flash both palms outward, then rippling the palms downward in a wave, medium shot with hip-hop style upper-body isolation in a qipao`
- 来源:《旗袍夜景》00:03-5.6s

### K72 举肘翘胯健身操链(4拍|飒)
- 入态:双手于胸前交替滚腕 → 出态:双手交叉落回胸前
- 分解:拍1 双掌上下相叠滚腕一周、右臂顺势上扬(6.5-7.1);拍2 右臂屈肘举过头顶、手落于脑后、躯干左倒胯向左顶(7.3-7.9);拍3 双肘同时外展高举、松拳收于耳侧、胯部左右连顶两下——双肘开合+胯部对侧顶胯为全片峰值造型(8.1-8.7);拍4 双臂沿体前下落、手腕交叉收于胸口(8.9-9.5);发力链:胯为主动源经腰传至背阔肌带动臂位;旗袍侧开衩随顶胯一开一合;长发随躯干侧倒甩向受力反侧半拍;脚下微屈膝弹动配合重拍(画面未含足部,推测);固定中景,肘部高举突破上边框
- H3:`rolling the wrists then lifting both elbows high and wide with loose fists beside her ears, popping her hips side to side under a slit velvet qipao as her long hair lags behind each lean, static medium shot framing the elbows at the top edge`
- 来源:《旗袍夜景》00:06.5-9.5s

### K73 猫爪击掌回眸链(4拍|媚)
- 入态:右手抚于腹部 → 出态:双掌合十于胸前、身体侧倾定格
- 分解:拍1 右掌自腹部沿躯干正中上滑至脸旁、翻掌向外立起(12.0-12.6);拍2 双手收指成猫爪举于两颊旁、胯部右顶配合(12.8-13.4);拍3 双爪在胸前合拢完成一次干脆的击掌、头顺势后仰笑出声——击掌与仰头同步为峰值(13.6-14.2);拍4 双掌合十贴胸、身体向左右交替侧倾摇摆、长发与裙衩随之荡开、耳环画弧(14.4-15.6);拍1 发力为手掌贴身滑行的自我抚触式动线;拍3 击掌冲击力经双臂传至肩带瞬收;拍4 惯性摆动逐拍衰减;机位固定,合十摇摆时身体斜出画框对角线
- H3:`sliding a palm up her torso to her cheek, flashing cat-paw hands beside her face with a hip pop, clapping once in front of her chest as she tips her head back laughing, then swaying side to side with pressed palms, static medium shot, hair and drop earrings swinging`
- 来源:《旗袍夜景》00:12-15.6s

### K74 特写眨眼收束链(2拍|甜)
- 入态(切镜后):面部大特写入画 → 出态:露齿大笑定格至片尾
- 分解:拍1 硬切入面部特写——对镜头单眼眨眼(wink)、嘴角上扬、梅花瓣妆贴入画(15.8-16.0);拍2 露齿大笑定格、头微侧、发丝垂肩、背景光斑全虚(静态,明写)(16.0-16.8);视线直锁镜头构成第四面墙互动;机位升至眼高、浅景深只留双眼与笑意清晰
- H3:`cutting to an extreme close-up as she winks one eye at the camera and breaks into a wide toothy smile, red plum-petal makeup beside her eye, bokeh lantern lights melting behind her, static face-level close-up holding to the end`
- 来源:《旗袍夜景》00:15.7-16.8s

---

## 拼舞模板(把链串成一支舞)

1. **选弧线**:建立(A1/C1 待机)→ 发展(手部组合链)→ 扩展(A7/C5)→ 高光(A9/C35/B5,全片唯一高潮放 70% 进度)→ 呼吸(C1/A12)→ 收束(A23/C30/C14)。
2. **填 bar 表**:每 8 拍一行;宅舞=2-3 链+2 拍镜头 pose(乐句尾必对镜头:比心/指镜头/V字);古风慢板=1-2 链+呼吸/眼神/裙摆填充;快板=4-6 动。
3. **写出入态**:上一链出态在下一链开头复述一遍(`landing with weight on her right leg, right hand at chest height`)。
4. **加持续层与微表情层**:持续层每拍不断(宅舞=内八弹跳;抖舞=B1 引擎;古风=提沉呼吸);反拍给头部/手指微动作。
5. **多人项目**:从 D 章取链,先写队形骨架(几何槽位)再挂动作,层次与动静显式声明(见 D 章纪律 12 条)。
6. **运镜**:从 E 章按"动作→运镜"映射表配镜头,切点落乐句收点,match-on-action。
7. **检查**:旋转≤2、静止已明写、头部鼓在反拍、手势半径合规、切点在乐句收点、人数/机位 token 齐全。

---
*来源视频:《双倍可爱❤️甜蜜暴击》(47.4s)、宅舞vs抖舞分屏(238.6s)、《与你提酒》(118.4s)、《皇上》(77.5s)、录舞运镜权威(61.5s)、《うみたがり》4人(222.5s)、《BLESSING》4人(96.8s)、向阳 BDF2021 队形版(144.9s);由八份逐拍反推报告提炼,动链合计 70+ 条;另并入 13 支 I2VA 单人成品范本(H 章,2026-10);《绝世舞姬》混剪(82.9s/44镜,E6 转场章+C36-C47+G 补充,2026-10-02);双人弧形运镜 16.8s(E7)+醉酒式镜头母规则(E8,2026-10-03);《三种袜子》右入换装 5.9s(E9)+三姿态原位换装系列 18.4s(E10:站姿侧身/深蹲抱膝抖腿/提裙站姿,onset 卡点实测,2026-10-05);2026-10-30 并入 K 章 74 条(15 支新片+2 图,短标题↔原片名:《绫华的锻炼时间》10.4s、《saber白礼服》9.6s(原片含书名号前缀"成为士郎的剑")、《saber下腰挑战》8.2s(原片《saber下腰动作挑战》)、《奥黛塔变装》153.4s(原片《花3000为奥黛塔制作视频后，最终决定放弃她.......》)、《夏天结束了》16.1s(原片《夏天结束了——做了四次不同情绪的撩头发》)、《橘福福》27.6s(原片《如此绝美的 橘福福 之后再也没见到》)、《薇薇安》60.6s(原片《好女孩——薇薇安（测试）》)、《维琳娜》75.0s(原片《这维琳娜对....对吗？》,鸣潮维里奈 cos)、《两个御姐合拍》14.9s(原片《两个御姐~格格巫和月月的合拍合集~_P1_好想谈恋爱》)、《请pick西施吧～》32.7s、《I Got Your Back》154.3s(原片【ILLIT】金丝眼镜水手服)、《依赖姐姐》72.0s(原片《依赖姐姐一辈子也不是什么坏事吧》)、《我是银月呀❤》18.1s、《活动饭拍》11.6s(原文件 ANbHNypfOZ8EhWqP)、《旗袍夜景》16.8s(原文件 AWsiPVCcHGVFeJGL)、《狐耳白发六宫格》写真图、《蓝水手服走廊截图》单帧)。*
