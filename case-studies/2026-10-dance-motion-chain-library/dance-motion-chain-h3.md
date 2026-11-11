# 舞蹈动链 H3 库(可重复学习的动作链标准件) · Rev.1.10

> **版本记录**
> Rev.1.10|2026-11-11|K 章追加片 v53-v106 共 54 支、K197-K322 共 126 条(王羽杉御姐变装/OOTD 批 49 支+唐安琪薄荷绿系列 4 支,密集抽帧 3fps 全覆盖+变装转折 8fps;3fps 总览存在 ±6.7s 漂移,链时间码以密帧帧序锚定):**变装机制五型归纳入库**——①真跳切手位/肢体掩剪(踢腿糊帧切、提膝顶点切、撸衫蒙面)②AI 渐变形(袜体渐长、衬衫纱化、领带浮现、凭空补现)③甩镜/撞镜模糊缝合④出画换装空镜交接⑤跷腿/足尖/交叉腿锚点卡点连切;**AIGC 判定全帧证据化**(高置信 AI:春诗/生日粉纱/书架露背/蓝裙/嘉桐摇/莫多莫多四格/jumpstyle/紧身连衣裙/拿下你 AI 渐变实锤/猎人猎物 AI 合成;混合:韩立/从不批腿/腿精;其余纠偏为实拍+重滤镜);新语汇:并膝纪律件(拍照从不批腿)、贴地机位件、影子上摇转场、X 交叉臂(EXID)、jumpstyle 跳步、四格级联变装、Office 椅袜鞋轮替
> Rev.1.9|2026-11-11|K 章追加片 v36-v52 共 17 片、K157-K196 共 40 条(短视频密集抽帧批,2-3fps 全覆盖+6fps 密帧):国风写真(团扇/双人折扇/收扇指弄)、卧室手势舞(骊山)、AI 写真批(少女真心疑似 AI/春诗 AI 高置信/春日列车 JK 重美颜/Heli 婚纱实拍/东京夜舞实拍)、**器乐动作首录**(Rather Be 小提琴:持琴回旋/举琴架弦/全弓快弓摆体)、啦啦队批(李珠珢:坐姿回眸甩发/抚腿起身/躬身甩发环绕背靠背)、新疆舞语汇首录(绕腕托帽移颈/连环转身)、宫斗演绎件(抚泪哭诉/拾狐抱胸贴脸,银月角色第二支)、Lolita 漫展件、口播道具件(转身递板/快剪卡点翻图)、饭拍群舞(KDC 路演按服装代号记录)、小恶魔 cos 蝙蝠翼件;**交叉比对**:两份《骊山四顾》SHA-256 一致(8125f39a…)系重复下载,反推一次;AIGC 判定全部帧证据化(b04 疑似 AI 中高/b05 AI 高置信/b12 混合/b02·b09·b14 纠偏为实拍)
> Rev.1.8|2026-11-10|T2VA 模式音频修复(minimax-h3-video-reverse 方法论,修复 video-to-h3-prompt 批量的音频缺口):18 片全部跑 onset 实测(onset_probe,22.05kHz 单声道转 WAV);拍速二分判别+格拟合分层——高置信实测:彩虹的微笑 126.3(v25/v26 双源互证)/姜杉 120/Liz 130.4/颜沁 127.7/秋装 122.4/白虎团锣鼓 127.7;低置信或倍频不定:Hwiseo≈89.6(autocorr 89.1 互证)/黄诗予≈100/第一次爱的人 92 vs 76/青花瓷 107 vs 原曲~60/上元 126 vs 63/李真率 85.7 vs 171/EXID 81 vs 动作周期 118/珠光 114/咲良 109;对账:51 链锚点 36 踩 onset±0.35s(70.6%),未踩多为证据覆盖缺口(前奏/黑场/安静段无 S 级 onset:v07 前 24s、白虎团 81-97s 等)或边缘 0.36-0.46s,《坏女孩营业》K131/K133/K134 确认为不卡点互动营业件(内容属性);各片「节拍」行已从(推测)升级为实测数据并注明置信层级
> Rev.1.7|2026-11-10|K 章追加片 v18-v35 共 18 片、K89-K156 共 68 条:K-pop 直拍批(Hwiseo《To My First Love》/tripleS《ANDLESS》双机位对比/IVE Liz《Looks Can Kill》/李真率《LALALILALA》/咲良饭拍/黄诗予生日SP/王心凌《彩虹的微笑》深圳+长春双场/《第一次爱的人》宁波/姜杉《Genie》九机位/EXID《I Love You》)+饭拍营业件(递麦双接/掩面捧脸/双指比心微活性/牵手旋回)+古风戏腔手势舞(上元)+京剧样板戏武戏首录(1972《奇袭白虎团》:斗篷物理/群像翻扑/过顶举摔)+婚纱换装微活性件;v14 编译合集与 v15 全场直拍按用户指示剔除;编号校正:C/D 两 agent 撞号,D 组重编 K131-K148
> Rev.1.6|2026-11-09|①K 章追加片 v17 K85-K88:AnimateDiff 补帧 8s AI 宅舞反推(横摆送胯/抓马尾摆胯/过顶钻石/胯波浪收势,BPM132 onset 实测网格);②新增 L 章「成品 T2VA 范本与续写提示词收录」:L1/L2 = Miniskirt(AOA)7 人办公室翻跳 12 Jobs 全文两版(基础版+密帧深化版,道具窗修正为大厅两侧白色方块),L3 = 8s 性感宅舞卡点续写提示词(BPM132,链位 K70/K45/K72/K73/B1/K74,音频 8.06s 实测 onset)
> Rev.1.5|2026-11-08|K 章追加 K75-K84:《潛行吧！奈亞子！W》宅舞翻跳 97.8s 密集抽帧(4fps×8 窗)反推 10 条——交替高踢/转体前伸/横移交叉开/背身甩发回转/变身双马尾/双马尾甩转(全片签名×7)/宽蹲摆胯/大弓步展臂高潮/力竭躺倒收尾/猫爪马尾横甩；一镜到底固定机位,变身点 24s,躺倒彩蛋收尾
> Rev.1.4|2026-10-30|新增 K 章「2026-10-30 批量反推动链扩展库」:15 支新片+2 张姿势参考图、74 条动链(K1-K74)经 video-to-h3-prompt 流水线反推并入(双人支撑拉伸/saber 技术下腰/3DCG 舞台变装/情绪撩发写真/吸血鬼写真/腿脚微动作/双人对镜甜舞/K-pop 群舞/卡点换装/AIGC 摆拍等);每片附背景人物档案+节拍判定+镜头形态分流;其余章节与使用规则不变
> Rev.1.3|2026-10-09|使用规则新增第 9 条「时间窗动作链完整性规范」(强制前置检查:五规则+动作设计五步逻辑+时间窗容量表+失败诊断四情况+逐窗验收十项);第 8 条十条自检不变
> Rev.1.2|2026-10-09|自检清单替换为用户定稿十条(运镜流程/物理机位/动作库优先/同步时间码/动作峰值/节奏连续/转场钩子/段自包含/视觉一致性/最终排错);第7条同步规则不变
> Rev.1.1|2026-10-09|使用规则新增第 7 条「舞蹈动作×摄影机运镜实时 1:1 同步」六原则+三条统一口诀,并新增第 8 条「生成前自检清单」(12 项,含同步六查+双系统+段结构);运镜流程(E 章)、拍摄角度设计(I 章)、重要经验(同步规则)列为每次生成前必复习项
> Rev.1.0|2026-10-07|新增 I 章物理摄影机视角案例库(25 类视角物理定义规范,用户提供的写法标准全文并入)+J 章写真式姿势-运镜章(J0 母语言十律+J1 母模板+J2-J10 九支实测范本,视角描述全部物理化改造);E5 末加"完整规范见 I 章"引用,E7 末加"视角词进提示词按 I 章改写"纪律;H 章范本 1 处 "slight low angle" 物理化;版本机制自本版建立,此前历史见 git log
> 来源:四支参考舞反推(《双倍可爱》甜系宅舞、《宅舞vs抖舞》左右分屏、《与你提酒》逍遥古风、《皇上》宫廷古风)。
> 每条动链 = 一个 2-8 拍的完整编舞单元,带**入态/出态**,可像积木一样首尾相接拼成整支舞。
> 英文描述均可直接粘贴进 H3 提示词;拍位为**相对拍**(链内第几拍),可放到任何 BPM 网格上。
> H 章 = 13 支单人成品范本(2026-10 并入):整段提示词可直接粘贴套用,H0 为从范本提炼的成品规律。
> K 章 = 批量反推动链扩展(106 支片+2 图,322 条):每片带背景人物档案+节拍判定+镜头形态分流;L 章 = 成品 T2VA 范本与续写提示词收录(Miniskirt 12 Jobs 两版+8s 卡点续写)。

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

**片<v16>《潛行吧！奈亞子！W》(宅舞翻跳·97.8s·4:3)**
- 背景人物:居家卧室——大床(浅蓝床品+粉色玩偶)、碎花墙纸、立式饮水机、"招财进宝"红金挂画、左墙镜子。人物:女宅舞者,白色水手服短袖(红领巾)+黑色蓬蓬裙+黑色高跟短靴;黑长发,0-24s 披发无饰、24s 变身点后双马尾+白发饰(变身与段落切换对齐,借转体甩发遮蔽完成)。画外行动者:无。
- 节拍:满电平 BGM(mean -10.3dB);快板宅舞,约 170-180BPM(推测,未核听)。
- 镜头形态:A 一镜到底固定机位(全程无切镜);结尾力竭躺倒彩蛋(93-97.8s 鞠躬折叠→坐倒床沿→仰躺腿搭床沿)。

### K75 交替高踢开场链(4拍|宅舞)
- 入态:站立双臂胸前交叉 → 出态:屈膝弹动中
- 分解:拍1 右腿高踢过腰、双臂同时打开成 V、头随踢后仰;拍2 落地屈膝吸收、双臂落体侧;拍3 左腿高踢同构;拍4 落地接半转预备,重心压前掌
- H3:`kicking her right leg high while both arms open into a V, her head tipping back with the kick, absorbing into a knee bounce, then the same phrase mirrored left`
- 来源:《潛行吧！奈亞子！W》0-4s

### K76 转体前伸链(2拍|宅舞)
- 入态:踢后落地 → 出态:正面双臂上举
- 分解:拍1 左转 90° 侧对、双臂向前平伸(引导转体);拍2 蹬地转回正面、双臂顺势举过头顶定住
- H3:`turning sideways with both arms reaching forward, then pivoting back to face the camera as her arms sweep up overhead`
- 来源:《潛行吧！奈亞子！W》4-6s

### K77 横移交叉开链(4拍|可位移)
- 入态:正面弹动 → 出态:回中弹动
- 分解:拍1-2 向左横移两步、双臂先胸前交叉再向体侧平打开;拍3 右腿侧踢、右臂同步上指;拍4 收回并步,交叉重复预备反向
- H3:`side-stepping left as her arms cross at the chest then sweep open, one side-kick with the opposite arm pointing up, snapping back to a bounce`
- 来源:《潛行吧！奈亞子！W》6-9s(18-19s 同构复用)

### K78 背身甩发回转链(4拍|甩发)
- 入态:正面 → 出态:正面手在脸侧
- 分解:拍1 左转背对镜头、双臂向两侧展开;拍2 背对甩头、长发/马尾横飞(延迟层);拍3 蹬地转回正面;拍4 双手落至脸侧猫爪框脸定住
- H3:`turning her back with arms spread, whipping her head so the hair fans out, spinning back to camera and landing cat-paw hands beside her face`
- 来源:《潛行吧！奈亞子！W》9-11s、19-22s(两处复用)

### K79 变身双马尾链(2拍|变身梗)
- 入态:披发 → 出态:双马尾+白发饰(借转体甩发瞬间完成更换)
- 分解:拍1 转体背对、发丝横甩遮住换发动作(动作遮蔽);拍2 转回正面时已是双马尾、双臂向体侧大开亮相——动作不断、变身"凭空发生"
- H3:`spinning through a hair-whip turn and facing camera again with twin-tails that were not there a beat ago, arms flaring wide on the reveal`
- 来源:《潛行吧！奈亞子！W》24s(变身点)

### K80 双马尾甩转链(2拍|双马尾·签名)
- 入态:正面或侧对 → 出态:回正面弹动
- 分解:拍1 头部主导横向甩动、双马尾滞后半拍水平横扫(最高点过肩);拍2 以甩发的角动量带转体 90-180°、马尾继续画弧回摆
- H3:`snapping her head sideways so the twin-tails whip through a horizontal arc half a beat late, the follow-through spinning her body around`
- 来源:《潛行吧！奈亞子！W》26-28s、34-36s、38-40s、58-60s、68-70s、78-80s、82-84s(签名复用×7)

### K81 宽蹲摆胯链(4拍|level change)
- 入态:并步弹动 → 出态:起身并步
- 分解:拍1 宽站下沉半蹲、双膝外开;拍2-3 保持低位的左右摆胯、双手随体前小幅平摆;拍4 蹬地起身收回,裙摆回弹
- H3:`sinking into a wide stance and swaying her hips side to side low, hands swinging small in front, then pushing back up to a bounce`
- 来源:《潛行吧！奈亞子！W》50-56s

### K82 大弓步展臂高潮链(6拍|副歌·全片最大幅度)
- 入态:弹动 → 出态:回中弹跳
- 分解:拍1 右大弓步沉低、右臂斜上全开左臂斜下后展(对角线拉满);拍2 保持推远;拍3 换左弓步镜像对角;拍4-5 再换右(或回中);拍6 双臂上举收 V 弹跳
- H3:`lunging deep side to side with one arm shooting up on the diagonal and the other sweeping low, trading the line left and right at full extension, closing with both arms up in a V hop`
- 来源:《潛行吧！奈亞子！W》88-93s

### K83 力竭躺倒收尾链(8拍|彩蛋收尾)
- 入态:V 跳落地 → 出态:仰躺床上静止(settled)
- 分解:拍1-2 深深鞠躬、上半身完全折叠、双马尾垂直垂落向地面;拍3-4 保持折叠两拍("没电了"暗示);拍5 直不起来的半起身、向后坐倒床沿;拍6-7 向后躺平、双腿搭在床沿垂下;拍8 完全静止躺平收束(全片终)
- H3:`bowing so deep her twin-tails hang straight down, staying folded like the power ran out, then dropping backward to sit on the bed edge and flopping flat with her legs hanging off the foot of the bed, holding still`
- 来源:《潛行吧！奈亞子！W》93-97.8s

### K84 猫爪马尾横甩链(2拍|萌)
- 入态:弹动 → 出态:弹动
- 分解:拍1 双手举至脸侧五指张开成猫爪、掌心朝前,同时头部左右快甩带动双马尾横扫面颊两次;拍2 爪保持、头回正眨眼
- H3:`flashing cat-paw hands beside her face while snapping her head side to side so the twin-tails sweep her cheeks, settling with a blink`
- 来源:《潛行吧！奈亞子！W》20.5-22s、66-68s

**片<v17>《AnimateDiff-补帧》(AI 宅舞·8.0s·9:16·24fps)**
- 背景人物:夜间城市街头——霓虹招牌虚化、柏油路面、暗色树影。人物:AI 生成(AnimateDiff+补帧)金发双马尾少女、白花发饰、粉色长袖上衣、黑色短裤;动作流畅无硬停顿(AI 特征)。画外行动者:无。
- 节拍:自带音轨(即所附 mp3,8.06s);onset 实测 BPM≈132,强拍 0.91s 间距:1.03/1.95/2.86/3.77/4.68/5.60/6.50/7.42s,0.81s 弱拍起手;能量密度全程均匀。
- 镜头形态:A 一镜到底(锁定髋高机位)。

### K85 横摆送胯开手链(2拍|AI宅舞)
- 入态:双臂前平伸 → 出态:体侧落下
- 分解:拍1 双臂胸前横扫打开、胯向反侧顶出送力;拍2 双臂沿体前大弧线下摆、重心左右交换,全程无硬停顿(AI 流动感)
- H3:`sweeping both arms open across the chest while the hip pops to the opposite side, then letting the arms fall along a wide arc as the weight shifts`
- 来源:《AnimateDiff 补帧》0-2s

### K86 抓马尾摆胯链(4拍|双马尾·Signature)
- 入态:双手升至颈侧 → 出态:松手双臂外放
- 分解:拍1-2 双手向上抓握双马尾根、肘外举定型;拍3-4 保持抓举、胯部左右大幅摆动两个来回(马尾随胯反相摆);末拍松手借势外放
- H3:`gripping both twin-tails up at the roots with elbows raised, holding the pose while the hips swing side to side twice, then releasing the hair into an outward arm throw`
- 来源:《AnimateDiff 补帧》2.9-4.7s

### K87 过顶钻石链(2拍|Signature)
- 入态:双手胸前合拢 → 出态:双臂下落
- 分解:拍1 双手指尖相抵成钻石/心形、沿中线直臂上举过顶,上身后仰、单腿后点;拍2 峰值定住半拍后双臂经体侧下落
- H3:`pressing the fingertips together into a diamond and raising it straight overhead with the back arching and one toe pointed back, holding the peak then lowering the arms`
- 来源:《AnimateDiff 补帧》5.6-7.4s

### K88 胯波浪收势链(2拍|收尾)
- 入态:双臂下落 → 出态:抬腿交叉定格
- 分解:拍1 上体波浪下传至胯、左右摆两次衰减;拍2 单腿抬起膝上提交叉、同侧手扶膝、另一手侧展定格
- H3:`rolling a body wave down into two decaying hip sways, then lifting one knee across with one hand on it and the other arm extended, freezing on the pose`
- 来源:《AnimateDiff 补帧》7.4-8.0s

**片<v18> 《To My First Love》(H1-KEY 赵辉玹直拍·青春叙事·213.5s·竖屏)**
- 背景人物:DDP 户外庆典开放舞台,深色地胶+橙色地面光带,LED 背景屏(红白几何箭头/绿紫像素块),雾机烟雾,追光手电常入画。人物:灰白细条纹短袖衬衫(开场披搭态)→白色泡泡袖一字露肩短上衣+灰色束腰马甲+灰色双排扣短裤裙+黑丝袜+黑色浅口高跟鞋;酒红色长直发八字帘;银黑手持麦+腰挂发射器。队友同系列白衬衫灰裙/黑抹胸裙作队形背景。
- 直拍特征:中景全身为主,腰-胸线手持跟拍,呼吸感晃动+横向平移,追焦稳定。
- 节拍:onset 实测≈89.6 BPM(beat 0.67s;与 autocorr 89.1 互证;0-24s 无 S 级 onset 为前奏/环境段);downbeat 归属推断,verse 8 分音符律动不变。
- 镜头形态:A 一镜到底跟拍(0-6s 开场等待态)。

### K89 双臂画弧三连-开合链(8拍|开场爆发·放正片起手处)
- 入态:正面直立持麦,双臂垂 → 出态:双臂落回腰侧屈膝微弹
- 分解:拍1(副歌 downbeat)右臂立掌从左向右横扫,左手后撑腰,发力源于腰腹旋转;拍2 右臂顺势斜下划落,重心压右腿,双臂斜向张开定格;拍3 换左臂屈肘横于胸前,右臂高举过头伸直,头左倾(肘先出再展臂);拍4 右臂自头顶向左下"斩落",肩带发力、手臂过肩全伸展,重心砸向左腿;拍5 双臂在胸前交叉(右臂在上);拍6 双臂向两侧弹开,掌心向下,身体借地反微弹起;拍7 双臂反向大展开(左上右下对拉),右腿向右点地,裙摆随摆;拍8 双臂收回落至腰侧,屈膝下弹吸收残量;服装物理:酒红长发在拍4 落臂时延迟半拍甩向左;镜头几何:手持横移跟随,全身始终在框
- H3:`sweeping the right arm across the body then chopping it down from overhead, crossing arms in front of the chest and bursting them back open to the sides, ending with a wide diagonal arm spread and a knee-bounce recovery`
- 来源:《To My First Love》00:06.0-09.0s

### K90 叉腰背身转体甩发-绕头撩发链(6拍|全片唯一叉腰快转)
- 入态:正面双手收至腰侧叉腰,小停顿 → 出态:正面右手撩发至脑后,面向镜头微笑定住
- 分解:拍1 叉腰蓄势(静态一拍,明写静止);拍2 前掌蹬地快速 spin 右转 180°+,角动量由蹬地+头先转提供,灰短裤裙摆水平展开,长发全甩出切向;拍3 背面定桩一拍,长发垂背飘落后摆;拍4 左肩带回带半身转回正面(发梢拖尾延迟约 0.3s);拍5 技术峰值:不待发落,借残余角动量绕头甩发一圈,发梢盖脸再飞向右侧(发完全横飞水平);拍6 右手向上抓拢头发撩至脑后,持麦手垂回体侧;镜头几何:跟拍机随转体小幅右移再回位
- H3:`quick spin with hands on hips into a back-facing hair whip, then riding the leftover momentum into a full around-the-head hair flip that covers the face before sweeping it back with one hand`
- 来源:《To My First Love》00:09.0-13.0s(绕头甩发峰值 00:12.2-12.8s)

### K91 挥手三连-转体甩发-领带回正链(6拍|verse 亮相互动件)
- 入态:正面持麦近嘴唱歌位 → 出态:双手摸回胸前领口系带,回唱歌位
- 分解:拍1(verse 8 分音符)持麦右手贴嘴,左臂屈肘前臂水平,自右向左上划出(腕带肘);拍2 左臂高举过头顶五指张开,向镜头方向亮相挥手(掌心朝外);拍3 左掌落至肩侧后再抬起挥一次,共两轮,身体随挥臂小幅右倾;拍4 右转 180°,左手顺势下压带动转体,发力来源为头先转+臂下压,长发横向全甩(水平切向,峰值 61.0-61.3s);拍5 转回正面,发落右肩,双手上提摸回胸前领口系带(回收顺序:臂-肩-手);拍6 头回正,重心回双脚,微笑定住一拍
- H3:`two rounds of raised-hand waving with fingers spread wide, then spinning half a turn whipping the hair horizontally and settling both hands back on the chest ribbon of the top`
- 来源:《To My First Love》00:58.8-61.5s

### K92 开臂跳-交臂下劈-360°转体甩发链(8拍|副歌爆发·全片唯一大跳)
- 入态:正面双臂胸前合抱屈膝下蹲蓄力 → 出态:落地回正面双臂垂,走位散开
- 分解:拍1(副歌 downbeat)合抱下蹲加深;拍2 开臂小跳起,双臂向两侧弹开,落地屈膝缓冲(起跳双臂带升力);拍3 双臂自体侧上划至头顶交叉成 X;拍4 技术峰值前半:双臂从头顶向两侧下劈开至体侧,掌心下压,深屈膝下弹(全身波浪下行);拍5 压膝回弹起,双臂收至胸前再斜上张开五指;拍6 右臂向右侧立掌"挡开",五指张开,身体右倾弓步;拍7 技术峰值后半:右臂斜上 45° 上扬、身体后仰,随即下压带动转体 360°,长发在空中放射状全甩(128.7-129.0s 空中发全开);拍8 落地借惯性半圈回转,发横飞盖脸,站定正面收势;服装物理:裙摆拍7 转体时上扬兜风、拍8 落定;重复变体 00:180.0-182.0s(过头下压+单膝提起+前臂挡脸后甩发转背)
- H3:`jump opening with arms crossing overhead then chopping down into a deep knee press, followed by an overhead-arm 360-degree spin with the hair fanning out radially mid-air before landing facing camera`
- 来源:《To My First Love》00:124.0-130.0s(峰值 00:128.6-129.1s;变体 00:180.0-182.0s)

**片<v19> 《ANDLESS》(tripleS 金琉然直拍·冷感未来·194.1s·竖屏)**
- 背景人物:MCD 室内舞台,黑色亮面地胶,背景屏红黑斜纹/蓝色科技波纹/紫色弧形灯带/白色光柱矩阵,台口白色条形地灯。人物:白色挂脖立领短上衣(胸前蓝色斜纹织带)+白色低腰短裤(蓝色斜纹侧饰)+白色宽筒褶皱堆堆长靴+白色全指手套;超长黑直发垂至大腿+齐刘海;金色耳挂麦。队友同队服发色各异。
- 直拍特征:全身中景,稳定器级平滑,胸线高度,随队形推拉横移,景深大;161-164s 前景设备/挡板遮挡。
- 节拍:强点密度实测 0.36s,拍速读法不定(171 BPM 或 85.7+8 分音符——后者与"低重力"律动更符,推测);格拟合 85ms。
- 镜头形态:A 一镜到底跟拍。

**片<v20> 《ANDLESS》(tripleS 池諝娫直拍·冷感未来·183.8s·竖屏,与 v19 同曲)**
- 背景人物:同 v19 场景与队服;发型识别点:齐刘海+头顶半扎高马尾+黑长直垂背(马尾与披发双段摆动)。耳挂麦。
- 直拍特征:中近景偏紧,对象居中率高;开场 5-8s 与 126-128s 有摇臂横穿画面顶部(黑条遮挡);前排队友偶发半遮挡。
- 节拍:同曲,强点密度实测 0.35s,读法同 v19(推测);格拟合 80ms。
- 镜头形态:A 一镜到底跟拍。

### K93 开立滑步-双臂波浪展开下压链(6拍|低重力滑行件)
- 入态:队形散开后面向镜头开立 → 出态:双手胸前收拢站直抬头
- 分解:拍1(慢重拍)双腿开立,双臂自体侧向斜下展开(掌心向下),身体下沉,发力源于髋部横移;拍2 重心向右横滑一步,双臂保持展开成"滑翔位",身体与地面夹角变小;拍3 双臂沿体侧下压至胯侧(掌推到底),深膝弯,重心最低点;拍4 技术峰值:双臂向后甩出(划水式换向),身体上浮站起,宽筒靴褶皱随腿摆;拍5 双臂收至胸前交叉;拍6 双手胸前收拢,抬头回正;服装物理:超长黑直发滞后重心两拍、滑步时发梢向移动反方向飘;镜头几何:机位随横移平行跟,速度均匀无抖
- H3:`sliding side to side with arms spreading low like wings, pressing them down to the hips then flicking them backward behind the body before gathering hands back at the chest`
- 来源:《ANDLESS》00:61.8-64.5s

### K94 上指-交握-斜下大展开-推掌回收链(7拍|副歌群舞同步件)
- 入态:正面站立双臂垂 → 出态:双手收至胸前站定
- 分解:拍1 右手食指斜上 45° 指(腕定肘伸),左臂垂,头随指尖抬;拍2 双手在胸前交握;拍3 技术峰值:双臂向斜下大展开(双掌张开、身体下沉成弓步),全队同步成纵深阵列;拍4 斜下展开定桩一拍(明写静止约 0.7s);拍5 双臂向前下方推掌(推水式),腰前弯;拍6 双手低位收拢,身体回升(回收顺序:手-腰-头);拍7 双手收至胸前站定;服装物理:长发在拍3 下沉时整体前披;镜头几何:机位后拉一档容纳群舞纵深再回推
- H3:`pointing one finger up, clasping hands then spreading both arms wide and low into a lunge, pushing palms down and forward like paddling before gathering back up`
- 来源:《ANDLESS》00:92.5-96.5s(同形群舞段 00:85.0-87.0s)

### K95 手部记忆点双式:爪形 spelling+脸侧屈肘(4拍|记忆点手势·副歌位)
- 入态:走位就位,面向镜头 → 出态:单手放下回体侧,转出走位
- 分解:拍1 双臂屈肘抬至肩侧,腕放松、五指弯曲成爪形,随节拍上下小弹两次(spelling 段);拍2 双手向脸侧收拢、指尖朝内,头微歪,笑点对镜头;拍3 变体(记忆点 pose):单手屈肘抬至右脸侧、手指弯向脸颊,另一手垂麦位,双脚跟踮起一拍;拍4 静态定桩约一拍(明写静止)后放下回位;发力全在前臂与腕,肩不动;镜头几何:拍3 时机位已推至中近景
- H3:`bouncing claw-shaped finger spells at shoulder height, then tucking one hand up beside the cheek with a bent elbow on tiptoe before releasing`
- 来源:《ANDLESS》00:52.0-54.0s(爪形 spelling);00:159.5-161.0s(脸侧屈肘)

### K96 双人镜像屈臂拉杆-推窗展开-流水压腕链(8拍|双人配合件)
- 入态:与队友并肩同向站位 → 出态:双臂收至胸前站定
- 分解:拍1 双臂屈肘胸前、拳心向下,向下"拉杆"一次(肘向后收,肩胛发力);拍2 右臂向上挥出、左臂下拉(交替互为反相);拍3 换边左上右下,身体随挥臂侧倾;拍4 双臂前平举交叉,随即向两侧"推窗"打开(立掌),技术峰值:双掌推开的同步性(与队友镜像零延时);拍5 双臂上提至肩侧屈肘拳向上,身体再侧倾;拍6 双臂前平举、手腕向下压至指尖向下(流水式,腕关节主导);拍7 胸前双手做五指开合抓握(白手套细节),配合弓步交换;拍8 收臂站定;镜头几何:机位横向微移保持双人同框
- H3:`pulling both fists down at the chest, alternating arm throws upward, opening the forearms out like pushing open a window, then rolling the wrists down with fingers fluttering`
- 来源:《ANDLESS》00:44.0-52.0s

### K97 肩侧摇步-前推掌-交叉展翅-波浪压腕链(6拍|verse 连续组合件)
- 入态:三人组前后纵深站位就位 → 出态:侧身转体双臂展开收,接走位
- 分解:拍1-2 双臂屈肘肩侧、拳抬起,身体左右摇+侧向跨步两拍(重心髋部驱动,马尾与披发反向甩);拍3 双臂向前平推掌(推水式),弓步前倾,技术峰值:推掌-前倾-下探三层递进(101.8-103.0s 重心最低);拍4 双臂胸前交叉再向外展开成"展翅"(掌张开,身体回升);拍5 双臂前平举、手腕下压指尖向下(波浪,与队友同拍);拍6 侧身转体,双臂展开收势;镜头几何:机位小幅后退跟随前倾
- H3:`rocking side to side with fists up by the shoulders, pushing both palms forward and down in a layered wave, crossing the arms and bursting them open into a wing spread`
- 来源:《ANDLESS》00:98.0-106.0s

### K98 INTRO 走位出列-仰头-开立定桩链(4拍|静态亮相件·放开场)
- 入态:群舞纵深队形中低位 → 出态:大开立下蹲定桩,保持至队形展开
- 分解:拍1(入态)自群舞中大跨步出列(马尾横飞,步幅大),手臂自然摆;拍2 到定点正面站立,双臂垂体侧,明写静态一拍;拍3 头部后仰仰望(颈部主导,躯干不动,双臂仍垂);拍4 双腿大开立下蹲定桩,双臂垂于两膝之间,队友同步落位形成纵深;发力:跨步为蹬地惯性、下蹲为自重控制;惯性延续:马尾在拍4 仍在摆;回收:无(定桩保持);镜头几何:机位随出列横移半步后停住
- H3:`striding out from the formation with the ponytail flying, standing still, tilting the head back to look up, then dropping into a wide-stance squat with arms hanging between the knees`
- 来源:《ANDLESS》00:11.75-13.0s(出列走位 00:08.0-11.0s)

### K99 三人排上举-同步下蹲-起身链(5拍|群形同步件·放 dance break 前后)
- 入态:三人一排侧对镜头站立 → 出态:起身走位散开
- 分解:拍1 三人同步双臂上举过头(掌相对,踮起);拍2 双臂保持高举,身体向侧微倾一拍(静态倾斜,明写);拍3 技术峰值:三人同步屈膝下蹲,双臂从头侧向下折落,身体前倾俯身(重心全落);拍4 低位保持半拍后蹬地起身,发上扬;拍5 起立走位散开,双臂自然摆;音乐触发:下蹲咬重拍、起身咬反拍;镜头几何:摇臂横穿画面顶部一次(黑条扫过,非切换),机位不避让
- H3:`three dancers raising both arms overhead in a line, leaning, then dropping into a synchronized low crouch with a forward fold before bouncing back up and scattering`
- 来源:《ANDLESS》00:124.0-128.0s

**片<v21> 《Looks Can Kill》(IVE 金志垣直拍·复古未来 disco·214.0s·竖屏)**
- 背景人物:MCD 行星主题舞台,紫色大行星球体+土星环充气装置、环形轨道灯、星型挂饰、串灯雨帘,结尾段彩纸雨。人物:白色无袖荷叶领短上衣+白色短裤(白色细腰带扣)+红色漆皮及膝长靴+粉色渐变过肘长手套;黑发齐肩内扣+耳侧碎发;金色圈形耳环;耳挂麦。背景队友:蓝色抹胸+浅紫短裤、橙发高双马尾白衬衫、红色蓬蓬裙白靴等,色彩手套系统(粉/蓝/黄/白)为全场视觉锚。
- 直拍特征:全身景为主,平滑推拉跟随,高度固定;126-128s 摇臂臂架入画遮挡(如实记录);170s 后偶有前景应援物遮挡。
- 节拍:onset 实测≈130.4 BPM(beat 0.46s,格拟合 105ms);disco 反拍律动不变,原估 120-125 修正上移。
- 镜头形态:A 一镜到底跟拍(196s 后为转场卡)。

### K100 后仰反弓甩发-回弹盖脸-半圈转体甩发链(6拍|开场爆发·全片最重甩发)
- 入态:正面站立双手于胸前 → 出态:转回正面双臂肩侧屈肘收势小跳
- 分解:拍1 双手向外推开(立掌),身体开始后仰,发力源于髋顶+胸展;拍2 技术峰值:后仰反弓至极限(腰胸反弓、双臂斜上下张开),齐肩黑发整体甩向后方(6.2-6.5s 发与地面近平行);拍3 回弹起身,头发借弹性向前甩起盖住整脸(惯性完全交给发);拍4 抬头,发落肩,双手收至胸前(回收顺序:头-臂-手);拍5 右转半圈,借转身再甩发一次,发横飞切向;拍6 转回正面,双臂落至肩侧屈肘,收势小跳一拍;服装物理:红漆皮长靴反光随转身扫过镜头,粉长手套指尖在拍1 张开、拍4 收拢;镜头几何:手持跟拍在后仰时轻微上仰角补偿
- H3:`arching back into a deep back-bend with the hair whipping fully behind, rebounding so the hair flips over the face, then spinning half a turn with a second horizontal hair whip before settling`
- 来源:《Looks Can Kill》00:04.75-09.0s(反弓峰值 00:06.2-06.5s)

### K101 双臂上挥-头顶交叠-开花下落-蹲低回弹链(5拍|记忆点开花件)
- 入态:侧身站立双臂在胸前 → 出态:回弹站起双手收至肩侧
- 分解:拍1 双臂交替向上挥(右上左下),身体微仰,腕带肘;拍2 双臂至头顶交叉、手腕相叠(静态交叠一拍,明写);拍3 技术峰值:双臂自头顶向下"开花"打开至体侧(掌心向外,指尖先开),与队友同步;拍4 身体下蹲低,双臂落至胯侧,重心全落;拍5 回弹站起,双手收至肩侧;音乐触发:开花落咬 downbeat、蹲低咬下一小节头;服装物理:短裤在蹲低时裤口绷开、手套腕部褶皱堆叠;镜头几何:机位固定,蹲低时构图容纳全蹲不裁头
- H3:`crossing the wrists overhead and blooming both arms down and open like petals, dropping into a low squat and bouncing back up`
- 来源:《Looks Can Kill》00:38.75-41.5s

### K102 拨浪摆-转身摆臂踢步-后仰对拉链(6拍|单人 solo 竖条·放 verse 中段)
- 入态:正面站立居中 → 出态:转回正面双臂胸前交替上摆(与队友同步)
- 分解:拍1 双臂向右侧同向摆(像拨浪鼓),身体右倾两小拍(发力源于髋侧顶);拍2 收臂左转至侧背位,双臂屈肘肩侧;拍3 摆臂式小跳步:双臂前后交替摆、双腿交替后踢踢臀(步频 2 拍 4 步),身体前倾,技术峰值:摆臂与踢步的节拍咬合(54.0-55.5s);拍4 摆幅加大成一上一下,头后仰;拍5 身体反弓、双臂斜上下对拉到极限(发与裙同摆);拍6 回正,双臂胸前交替上摆;服装物理:粉色长手套在摆臂时袖口滑落半寸再回弹;镜头几何:机位横移半步给转身让位
- H3:`swaying both arms to one side like a rattle-drum, turning sideways into a skip step with fists pumping and heels kicking back, then arching back with arms stretched in opposite diagonals`
- 来源:《Looks Can Kill》00:52.0-56.0s

### K103 双人箭头指-换位指线不断链(6拍|双人 spelling 记忆点·放副歌)
- 入态:与红裙队友并肩同向 → 出态:收指双臂落回体侧站定
- 分解:拍1 双臂一高一低斜上指(食指伸直、余指握),身体后仰,头抬看指尖;拍2 双臂转前平指(指尖向前),身体前倾,技术峰值:双人指线平行零偏角;拍3 交叉步与队友换位(内侧穿行),手指保持前指不断(指线即"箭头"的调度语言);拍4 双臂指斜下方(点地),身体侧倾;拍5 指回斜上(抬头),完成一次上下循环;拍6 收指、双臂落回体侧站定;音乐触发:每次换向咬 2 拍一次的 disco 反拍;服装物理:换位穿行时发梢扫过队友肩;镜头几何:机位后退半步容纳双人换位
- H3:`pointing diagonally up with one arm high and one low, switching to a straight-forward arrow point, crossing past the partner while the finger line stays constant`
- 来源:《Looks Can Kill》00:58.0-62.0s

### K104 合掌-V 举手-开花落-转体甩发-踮脚上举链(6拍|ending 前收束件)
- 入态:屈膝低坐双臂体侧下压 → 出态:双臂合掌上举踮脚,转接结尾定点
- 分解:拍1 屈膝低坐、双臂下压收势后于胸前合掌,起身(回收起手);拍2 双臂 V 形高举过头五指张开,站直亮相一拍;拍3 双臂自 V 向下"开花"打开至体侧(掌外翻,身体左右摆一拍);拍4 技术峰值:半圈转体甩发(发盖脸,100.3-100.7s),借转身惯性;拍5 回正面小步走位,双手向下拂裙摆两次(整理动作入编排);拍6 双臂合掌上举过头+踮脚(下段起手式);镜头几何:机位在拍4 转体时轻微跟随回摇
- H3:`pressing palms together then throwing both arms into a V overhead, blooming them down open, spinning with a hair whip, and rising on tiptoes with palms pressed overhead again`
- 来源:《Looks Can Kill》00:98.0-101.0s(踮脚上举 00:103.3-106.0s)

**片<v22> 《LALALILALA三光岛》(原 APRIL 李真率直拍·清爽甜酷·197.1s·竖屏)**
- 背景人物:户外广场白天舞台,大面积玻璃幕墙建筑背景;舞台器材=印"SONIDO"鼓组+镲片、立式麦架、绿色 LED 谱架、黑色监听音箱;可见鼓手、2-3 名白衣系队友(白蕾丝上衣白长裤/奶白长裙/红棕长发)、82-85s 左后方深蓝夹克持相机男工作人员。
- 直拍特征:手持跟拍、全身景、旋转走位时急速摇镜+变焦补偿、轻微抖动、平视略仰。
- 节拍:onset 粗测中位强点间距 0.70s,读法不定(85.7 或 171),格拟合差 165ms(户外掌声污染);维持(推测)。
- 镜头形态:A 跟拍(全程)。

**片<v23> 《咲良饭拍》(LE SSERAFIM 宫脇咲良·互动吟唱·17.1s·竖屏)**
- 背景人物:室内演唱会主舞台,深蓝黑底+蓝紫色斜向光束、白色轮廓顶光;画面内无队友。人物:宫脇咲良,米白 oversize 连帽开衫+灰蓝牛仔抹胸迷你裙(粉色字样)+黑色安全短裤+大圈耳环+眼下爱心贴纸,左手中黑麦。
- 直拍特征:长焦手持饭拍、中近景(膝上为主)、呼吸感推拉、随头手小幅摇移。
- 节拍:onset 粗测≈109 BPM(16 强拍,低置信)。
- 镜头形态:A 跟拍(长焦)。

### K105 跪姿起链(4拍|level change)
- 入态:单膝跪地低位定格(一膝点地、另一腿屈膝上抬,双手握麦于胸前) → 出态:完全站直、双脚并拢、麦收至右手垂于体侧
- 分解:拍1 跪位双手持麦向头顶划弧、双肘外撑成菱形,头随臂右转再回正,卡前奏重拍(发力来自肩带);拍2 双臂从头顶向两侧劈落成风车式,发丝随甩、躯干微前压;拍3 臂落至膝旁做两次手指小波浪,上身随之下压再抬,跪姿膝盖缓冲;拍4 左脚蹬地起身、跪姿腿收落,右手顺势把百褶裙往前抚一下,落位双脚并拢(裙被大腿带起一折后垂回,开衫袖口滑至小臂),卡鼓点收
- H3:`kneeling low with one knee up, arcing the mic hands overhead then sweeping both arms down to the sides, waving small at the knee, then pushing up to stand while smoothing the pleated skirt down`
- 来源:《LALALILALA三光岛》0-4.8s

### K106 转身甩发V臂链(4拍|spin)
- 入态:直立待转、双臂自然垂 → 出态:双臂宽位展开定格、重心压左、眼看右
- 分解:拍1 右脚为轴全速 360° 顺时针转身,长发水平甩出、百褶裙离心飞张成伞状(技术峰值,风力完全来自角速度);拍2 出转时右手撑胯急停、左臂横摆回中,发梢绕颈惯性回摆半拍;拍3 双肘上折做肩侧"爪爪"位、手腕放松,身体随小弹两下;拍4 双臂伸直过头举成 V、掌心朝前,再向两侧打开压低,重心左移右腿点出,裙摆斜摆落定(1:33s 处同型甩发旋转复现);旋转时跟拍机急速右摇+轻推焦,出转后拉回中线
- H3:`whipping a full spin with the skirt flying out like a fan, catching it with one hand on the hip, bouncing with bent elbows by the shoulders, then raising both arms into a V and opening them wide`
- 来源:《LALALILALA三光岛》9-11.8s、93s

### K107 俯身横扫起身链(4拍|arm sweep)
- 入态:直立、麦举嘴边、右臂垂 → 出态:直立回正、右拳收在下巴侧、麦回到嘴前
- 分解:拍1 双膝小屈下沉半拍、左拳胸前一记小顿卡重拍,身体向右前顶(先降重心再给水平动力);拍2 上身深前倾约 45°、双臂从右向左低横扫过膝,核心发力是髋部折叠+腰背,长发全甩到面侧、裙摆前后荡;拍3 股四头肌爆发蹬地立直,右臂逆势从低位划上头顶,发梢从左后方甩回(惯性多摆半拍才稳);拍4 收臂、右拳顿下巴旁,肩膀小抖两下收尾、麦提回嘴边;镜头几何:前倾时跟拍机下摇、起身时上摇追头
- H3:`dipping with a small fist pump, hinging deep to sweep both arms low across the body to the left, then snapping upright with one arm tracing up overhead as the hair swings back into place`
- 来源:《LALALILALA三光岛》45-47.8s

### K108 抱臂摇摆链(4拍|groove)
- 入态:双臂交叉环抱胸口(自我拥抱位)、双膝并拢微屈 → 出态:双臂大开、宽位站定、重心回中
- 分解:拍1 双臂从两侧收拢交叉抱胸、下巴内收含胸(回收顺序:先肘后手);拍2-3 保持环抱、整条脊柱左右钟摆,膝盖一屈一伸弹动,发力全在髋底核心、上肢锁死只随整体荡,长发蒙面跟随、百褶裙左右扫动(技术峰值:无手臂借力的纯重心摆);拍4 双臂向两侧爆开划大弧、肩带胸展开,左右各荡半拍回中,裙摆翻起落定;镜头几何:跟拍机小幅左右平移抵消摆幅保持居中
- H3:`crossing her arms into a self-hug and rocking the whole body side to side with bouncy knees, hair falling over the face, then bursting the arms open wide and settling back centered`
- 来源:《LALALILALA三光岛》53.5-56.8s

### K109 提膝挥拳掌浪链(4拍|attitude)
- 入态:直立、麦垂右手 → 出态:单臂过顶做掌浪、身体立直收正
- 分解:拍1 一腿屈膝上提至胯高、对侧手伸向侧前,百褶裙被大腿顶得掀起一折;拍2 提膝同时握拳上冲、躯干反向倾顶胯,以支撑脚小跳半圈稳定(技术峰值);拍3 落腿回位、双臂先后过顶交替做掌浪(手臂像水草左右摆,头随臂走,惯性逐拍衰减);拍4 掌浪收小、双手回落胸前两侧、膝盖弹两下收拍;162-163.8s 段复现同款过顶掌浪+头侧兔耳手(指尖翘动),多时间码合并;镜头几何:提膝瞬间跟拍机略上抬,掌浪段机位稳小摇
- H3:`lifting one knee high while punching the fist up and tipping the hips, then landing and weaving both arms overhead like a palm wave with the head following, finishing with small bounces`
- 来源:《LALALILALA三光岛》89.5-93.8s、162-163.8s

### K110 比V指枪甩发弓背链(4拍|playful)
- 入态:双手举至脸侧比 V、掌心朝外、双膝弹动 → 出态:直立、单臂举过头顶握拳、头回正定格
- 分解:拍1 双手脸侧比 V 弹两下,手腕翻转成指枪指向身体两侧、肘夹肋(腕内旋+肘回收);拍2 双臂如击剑交替向左前戳两下、肩膀送出,身体随戳前倾回弹,裙摆小幅前后翻;拍3 上身弓背低头、长发整片甩到面前(甩发点头),再猛抬头让发回卷——发梢在头已回正后仍前荡半圈(技术峰值=甩发与抬头的时差);拍4 起身同时右臂直举过顶、拳收肩上,头后仰一下再回正;镜头几何:弓背时跟拍机下摇接头部、起身时上摇
- H3:`flashing double peace signs by the face and flipping them into finger guns, fencing the arms forward twice, then headbanging the hair down over the face and snapping back up with one fist raised overhead`
- 来源:《LALALILALA三光岛》158-161.3s

### K111 掌浪安抚手势链(3拍|gesture)
- 入态:直立面向观众、双手交叠腹前、麦直握垂左手 → 出态:右臂伸直高举过头、身体后仰仰头张嘴
- 分解:拍1 右掌心朝下盖在左手背上,随节奏向前推一记"抚平"手势,噘嘴配合(安抚场内气氛,发力来自肩前束);拍2 右臂掌心朝下从左向右平扫大弧到体侧,躯干跟随右倾、长发从肩后滑落,宽松开衫在背后鼓起、袖口堆腕;拍3 扫到底后手腕轻抖两下做"撒碎"回收,随即缩肩挤眼做撒娇表情、指尖捏起点在下巴旁小弹(回收顺序:腕→肘→肩),最后手臂直举过顶、头后仰进入演唱段;镜头几何:长焦跟拍机随横扫右移半格再回中,举臂时轻微上摇
- H3:`sweeping the palm-down hand forward like smoothing the air, arcing it wide across the body with the torso leaning, then scrunching into a cheeky shoulder bounce and shooting the arm straight up while tilting the head back`
- 来源:《咲良饭拍》0-4.5s

### K112 甩发撩颈链(3拍|flirty)
- 入态:侧身对右、左臂斜举展开 → 出态:身体回正、手收回身侧、随拍左右小荡
- 分解:拍1 右臂举高掌心张开,头猛向左后甩、嘴大笑张开发声,长发整片向后翻卷(发力来自颈后+腹前收缩,技术峰值=发卷落回肩前慢半拍);拍2 手落回颈后按住发根、下巴内收眼神下瞟做害羞撩发位,抹胸裙随上身扭转微移、开衫领口滑向一侧;拍3 手从颈后顺势下滑、肘尖抬起、腕放松让手垂着晃两下,身体左右小荡、嘴唇收拢做"哦"口型跟唱,发梢惯性多摆两拍才静;镜头几何:甩头时跟拍机轻微上摇+左移接住头部
- H3:`tossing the head back with one arm raised as the hair rolls over, touching a hand behind the nape with a shy glance, then letting the wrist go loose and swaying with the beat`
- 来源:《咲良饭拍》7.5-10.3s

### K113 背身兔耳回眸链(3拍|cute)
- 入态:完全背对镜头、双手举肩侧指节上翘(兔耳手)、麦在左手 → 出态:面向镜头、右臂高举、仰头张嘴进长音
- 分解:拍1 背身状态双手在肩侧做兔耳指尖小抖、胯随节拍左右顶,长发完全盖背、开衫后背印花全露(机位保持中景等她回身);拍2 左转半圈回身、麦抬到嘴边,长发从背后甩起绕过脸颊、头顺势后仰让发落下(技术峰值=转身与甩发的时间重叠,开衫下摆画弧);拍3 面向镜头双手两侧摊开掌心朝上耸肩,随后右臂直举过顶、左手指在胸口点两下,仰头张嘴进长音;甩发段跟拍机轻微推焦
- H3:`facing away wiggling bunny-paw hands at the shoulders, spinning back around as the hair whips over the face and falls, then shrugging with both palms up and raising one arm high into the long note`
- 来源:《咲良饭拍》12-15.5s

**片<v24> 《我可以喜欢你吗》(黄诗予 YGG 生日SP·甜美元气·260.3s·竖屏)**
- 背景人物:室内小舞台,黑色 LED 墙铺像素星星/闪电+粉蓝歌词字("好想问问宇宙/我喜欢你靠/不敢告诉/就藏在心里");人物:黄诗予——白色短款印花 T+粉色多层蛋糕蓬蓬短裙+白色过膝袜+白色厚底短靴,粉色手柄麦克风,深棕长发两侧编细辫;队友白 T 配粉/粉白格裙变体(粉发成员、粉格裙成员)。
- 直拍特征:手持竖屏一镜到底跟拍,主体恒居画面中心,队形穿插时短促横摇(197-204s 曾短暂跟丢至粉发成员),快转时全身运动模糊。
- 节拍:onset 粗测≈100 BPM(强拍=2 拍读法,格拟合差 143ms,低置信);与动作周期 0.5s/拍(≈120)并存,拍速待定。
- 镜头形态:A 一镜到底跟拍。

### K114 垫步提膝侧移-抛臂-跪地下沉跪姿交替挥击链(9拍|全片唯一完整跪地段)
- 入态:立姿提膝垫步 → 出态:起身回立,长发甩落后摆
- 分解:拍1 右膝连提两次原地垫步,重心压在前掌,麦克风举嘴侧,裙摆随提膝小幅前掀;拍2 向右侧移半步,右臂平伸探出,发力来源为左足蹬地+髋侧顶;拍3-4 左向走位中接左转身 180°,发梢横向拖尾延迟约 0.3s,转身完成即刻右臂向上斜 45° 抛出(技术峰值,躯干后仰反弓);拍5 不回收,借抛臂反作用力垂直下沉,右膝跪地、左足前点,双臂顺势向下交叉合拢,裙摆在台面摊成扇形;拍6-7 跪姿双臂交替前抡:先单臂向地板斜下 punching,再横向低扫换边,发力全在肩带+躯干拧转,头随出拳方向点摆,长发每次摆动迟到半拍;拍8 跪姿借最后一次扫臂残余角动量甩头,长发盖过右脸再飞向右侧;拍9 前掌推地起身回立,手收至腰侧(回收顺序:臂→头→重心);镜头几何:跟拍机同步下压再上抬,跪地段主体保持中景
- H3:`stepping with high knee hops into a side reach, throwing one arm up on a turn before sinking into a deep kneel, alternating floor-level punches and sweeps from the kneel and whipping the hair around while staying down, then pushing back up to standing`
- 来源:《我可以喜欢你吗》00:30.0-37.5s

### K115 蹲身合掌问宇宙-起身走位-爪手脸框蹲链(8拍|两段蹲身表情包连缀)
- 入态:走位中立姿 → 出态:爪手蹲身定格带笑
- 分解:拍1 上半身前倾下沉,双手在腹前十指相扣,膝外展深蹲到底(屈髋+屈膝同步,静态 hold 一拍);拍2 蹲持,抬头看镜头微笑,裙摆叠压在大腿,麦克风垂在扣手下方(相对拍静止,明写 hold);拍3 前掌推地站起接右转走位,双臂松弛随步摆,长发延迟半拍;拍4 横穿舞台,双臂向两侧打开至平举、胸挺(步频不乱、臂走弧线);拍5 左转体带甩发,发梢横扫盖脸;拍6 不等发落,双肘高抬至耳侧、双腕内折、五指张开做"爪手",同时屈膝下沉半蹲;拍7 爪手在脸侧上下小抖两次,膝内扣弹跳维持节奏;拍8 双手贴至脸颊两侧框脸,肘尖内收,蹲位更深,笑定(技术峰值:蹲-手-表情三者同拍到位);服装物理:蛋糕裙层层错动,起蹲时最外层延迟回位;镜头几何:走位段机位横摇 2 次跟住,蹲身段回推近景
- H3:`rising from a kneel into a deep squat with fingers clasped at the waist, popping back up to cross the stage with arms flaring wide, then spinning with a hair whip and dropping into a paw-hands squat framing the cheeks with a bounce`
- 来源：《我可以喜欢你吗》00:38.0-44.75s

### K116 副歌过顶交替抡臂宽距弹跳链(6拍|全片副歌主件,三处复现)
- 入态:宽距屈膝站 → 出态:弹跳持位,臂落回肋侧
- 分解:拍1 双膝外展宽站半蹲,随拍弹跳,右臂从体侧直臂抡起过头顶(发力:蹬地弹跳+肩胛带甩,肘部不弯);拍2 右臂抡至对侧肩前下劈,躯干随臂折叠左侧屈,裙摆向反方向甩平;拍3 不停顿换左臂抡起过顶(连续发力,无回收拍),右臂经体侧自然回落;拍4 左臂下劈+右侧屈,膝弹跳维持 0.5s/拍,重心左右大幅横移,长发与裙摆反向滞后;拍5 双臂短暂同举过头成 Y,胸展开头微仰(技术峰值,只占半拍);拍6 双臂沿弧线收回肋侧,弹跳不停,接麦克风演唱位;服装物理:蛋糕裙随重心左右换边呈钟摆式摆动,辫梢迟一拍;镜头几何:机位随臂抡方向小幅俯仰,主体始终全身在框;音乐触发:副歌每小节强拍对应单臂过顶
- H3:`bouncing in a wide plie stance while sweeping alternating straight arms overhead in big arcs, torso folding side to side so the skirt swings like a pendulum, flashing a Y-shaped double-arm reach before pulling the hands back in`
- 来源:《我可以喜欢你吗》00:59.5-64.0s;00:132.0-140.0s;00:207.0-210.0s(三处同段复现)

### K117 收拳脸侧-蹬地转体甩发-回落跳步链(5拍|快速 spin 招牌件,三处复现)
- 入态:双拳收于脸侧 → 出态:正面跳步回位,发落定
- 分解:拍1 双拳收至两颊旁、肘外张,双膝内扣小弹跳蓄势(明写蓄势一拍);拍2 前掌蹬地 spin 右转 360°,角动量由蹬地+头先转提供,长发水平甩出切向盖过整个背,裙摆展开;拍3 转体后半圈手臂向上张开维持平衡,背面一瞬定桩;拍4 借残余角动量回正面,发梢继续飞出再落下(延迟约 0.3s),双拳仍收在脸侧(手位不丢);拍5 落地即接高抬膝小跳步两下回收,拳变掌自然下落;服装物理:转体中裙摆水平飞展、落地后回弹两次;镜头几何:手持机随转体小幅画圆,快转帧全画面运动模糊;音乐触发:转体卡小节尾强拍
- H3:`curling both fists by the cheeks, spinning a full 360 on the ball of one foot with the hair whipping horizontal and the skirt flaring, landing back to camera with fists still up and finishing into two bouncy knee hops`
- 来源:《我可以喜欢你吗》00:64.0-66.0s;00:210.5-212.0s;00:243.0-244.0s(结尾段为最长发甩,背面帧最完整)

### K118 藏心画横线-半心画弧哑剧手势链(7拍|歌词哑剧件,两段连缀)
- 入态:立姿演唱位 → 出态:半心画弧收手回演唱位
- 分解:拍1 双手合十收进胸口"藏"进心里,肩微含(按词"就藏在心里"触发);拍2 右手掌心向下在嘴前高度从左向右水平画一条长横线,头随指尖转向右("说不出口"封口哑剧,技术峰值:线画满一整拍且头手同速);拍3 指尖在末端向外一点弹出,胯同步左顶;拍4 收手至肩,肘外张;拍5 右手举过右肩上方,双腕在肩上交叉搭出半个心形,胯左顶定格半拍;拍6 半心沿对角线向左肩方向画弧下落,躯干侧屈追随,长发迟半拍;拍7 双臂打开甩出回收至体侧,左移半步接下句;镜头几何:固定中近景,画线段手部全程在画面上三分之一
- H3:`hiding clasped hands into the chest, drawing a long horizontal silence line across the mouth with the palm flat, then popping a finger point, crossing the wrists above one shoulder into a half-heart and tracing it down in a diagonal arc to the other side`
- 来源:《我可以喜欢你吗》00:143.0-146.5s;00:148.5-149.75s(画横线两处变体:143 处从左至右、148.75 处收肘变体)

**片<v25> 《彩虹的微笑·深圳》(王心凌商演直拍·啦啦队元气·45.5s·竖屏)**
- 背景人物:商演舞台,绿→紫→蓝 LED 大色块洗墙,无歌词屏;伴舞 4-6 人白上衣+浅蓝蓬裙、持白色啦啦花球。人物:王心凌——粉橘色齐肩 bob、牛仔泡泡袖短外套+牛仔荷叶边短裙,银色麦克风。
- 直拍特征:手持近景跟拍(胸像到膝上构图),随举臂上下俯仰,背景花球常虚化,无切镜。
- 节拍:onset 实测≈126.3 BPM(beat 0.475s,格拟合 52ms,高置信);锤拳泵 0.5s/次≈拍速吻合。
- 镜头形态:A 一镜到底跟拍。

**片<v26> 《彩虹的微笑·长春》(王心凌演唱会整首·粉亮皮甜酷·147.1s·竖屏)**
- 背景人物:大型演唱会舞台,浅色圆形/星形 LED 光斑背景,地面彩纸;伴舞 6-8 人黑色荷叶边短裙+白色啦啦花球(与主角强对比)。人物:王心凌——粉色亮皮 oversized 衬衫+同料包臀短裙+黑色细腰带+黑色短靴,白色麦克风,棕长发耳侧发夹;画面右上角 B 站投稿水印。
- 直拍特征:竖屏演唱会机位,景别比 v25 远(全身常在框),96-108s 镜头甩糊/被遮挡 6s+,队形段短暂变为群像构图。
- 节拍:onset 实测≈126.3 BPM(同曲双源互证,格拟合 100ms,高置信)。
- 镜头形态:A 一镜到底跟拍(含 96-108s 遮挡断点)。

### K119 开场胯摆-双臂上抛V-腕上交叉下扫链(6拍|同曲开场件)
- 入态:松弛立姿 → 出态:双臂落回体侧,接锤拳泵
- 分解:拍1 双肘微屈垂在肋侧,胯左右小幅摆动(静态律动 hold,发力:膝弹跳带动);拍2 双拳自腰间同时向上抛出成高 V,躯干拉长起踵(发力:蹬地+肩带快甩);拍3 双腕在头顶上方交叉(本曲"比 W/交叉腕"招牌变体,手背相贴一拍);拍4 双臂向两侧打开成弧线自上而下扫落,裙摆随身体右侧横移甩起;拍5 双臂扫至体侧低位后顺势向前小送,胯反向左顶;拍6 手沿身体收回肋侧,直接进入交替锤拳泵(惯性顺接);服装物理:牛仔荷叶边裙在双臂下扫时同步外翻回弹;镜头几何:近景机位随双臂上抛上仰,交叉腕时手部位于画面顶端边缘;音乐触发:开场"哇"音上双臂齐抛
- H3:`swaying the hips with loose elbows before throwing both fists up into a high V, crossing the wrists overhead, then sweeping both arms wide back down to the ribs to roll straight into alternating fist pumps`
- 来源:《彩虹的微笑·深圳》00:02.0-06.5s

### K120 交替锤拳泵-反向胯拧链(4拍|同曲主律动件,v25/v26 双源合并)
- 入态:立姿演唱位 → 出态:泵速渐收,手落回麦
- 分解:拍1 右拳收在右肋,向内下方向锤泵一次,同时胯向左拧(反向交叉发力,膝弹跳同步);拍2 左拳同幅锤泵,胯回拧向右,左右交替 0.5s/次,肘部始终贴肋不做大臂动作;拍3 泵击中加入头部分拍点动,肩带随之小幅滚压(技术峰值:泵-胯-头三点异相错位);拍4 泵速减半,麦克风抬到嘴,空出的手仍小泵两下再落;服装物理:牛仔/亮皮短裙下摆随胯拧左右荡,齐肩 bob 发尾每泵轻跳;镜头几何:v25 近景、v26 全身景各留证据,机位稳定少摇;音乐触发:主歌逐句末字重拍对应重泵
- H3:`hammering alternating fists down at the ribs while counter-twisting the hips on every pump, knees bouncing on the beat and the chin nodding off-phase, easing the pumps out as the mic comes up`
- 来源:《彩虹的微笑·深圳》00:09.5-16.75s;00:27.0-28.25s;00:36.0-37.25s;00:38.0-42.25s / 《彩虹的微笑·长春》00:45.5-48.25s;00:119.5-122.25s(同曲同段,长春版胯幅更大)

### K121 双拳托下巴-膝内扣弹跳链(3拍|同曲卖萌件,双源)
- 入态:锤拳泵半收 → 出态:回演唱位
- 分解:拍1 双拳从肋侧上提收在下巴下方,拳背相对,肘尖向下夹;拍2 双膝内扣弹跳两次,躯干左右小倾("害羞"语义,相对拍静止上半身、只有下肢弹);拍3 头侧倾贴向拳背一下,再双手打开下滑回体侧回收;服装物理:裙摆随内扣膝小幅收拢;镜头几何:近景为主,v26 全景中膝内扣清晰可见
- H3:`tucking both fists under the chin with knuckles together, knocking the knees inward in a shy little bounce and tilting the head onto the fists before releasing the hands`
- 来源:《彩虹的微笑·深圳》00:28.5-29.75s;00:15.0-16.0s / 《彩虹的微笑·长春》00:50.0-51.25s(同段呼应)

### K122 单臂高举弧线-侧平指互动链(5拍|同曲观众互动件)
- 入态:演唱位 → 出态:手臂收回,转身走位
- 分解:拍1 空手从体侧直臂向上抡起成大弧线过顶(发力:肩带+躯干后仰),麦克风不离嘴;拍2 臂在头顶沿弧线向对侧倒,躯干随之侧屈,裙摆向支撑腿侧贴;拍3 臂沿原弧落回,膝弹跳不停;拍4 空手转成侧平举指向观众席/伴舞方向,头转向指尖,定半拍(技术峰值:平举与头转同拍);拍5 指尖画小圈两下收回,向指的方向走位回收;镜头几何:v25 机位随举臂上仰后回平,v26 同段为全景侧移;音乐触发:句首起臂、句尾收指
- H3:`raising the free hand in one big overhead arc while singing, letting the torso lean into the descent, then leveling the arm into a side point toward the crowd with a couple of lazy fingertip circles`
- 来源:《彩虹的微笑·深圳》00:24.0-26.75s;00:33.0-34.25s;00:42.5-43.75s

**片<v27> 《第一次爱的人》(王心凌宁波 DAY1·抒情慢摇·231.6s·横屏)**
- 背景人物:体育馆暗场,红粉色荧光棒海洋铺满背景,台侧可见安保;无伴舞,单人环节。人物:王心凌——白色无袖收腰 A 字中裙(背中拉链,腰后蝴蝶结),深棕长发单侧细辫垂前,粉紫渐变麦克风。
- 直拍特征:横屏远距固定机位为主体,轻微横移/推拉,主体走远时镜头不追(40-56s 背身行进全程原地),构图稳定居中。
- 节拍:onset 粗测≈92.3(格拟合差 155ms,人声污染);慢歌叙述拍感 76 保留,低置信。
- 镜头形态:B 固定机位为主+缓慢横摇(非快剪)。

### K123 指上举臂行进泵链(4拍|v26 主歌变体)
- 入态:行进立姿 → 出态:臂落,接双肘泵
- 分解:拍1 右臂直臂向上冲到头顶,食指指天,左手持麦;拍2 指天腕部以腕为轴向下泵两次("raise the roof"变体),同时向前行进,每步提膝,裙摆随步幅翻折;拍3 举臂不落、改腕绕圈一次,面向镜头大笑(技术峰值:指天+行进+笑三线并行);拍4 臂沿弧线下落,双肘屈起交替泵两下回收;服装物理:亮皮衬衫袖口过腕,泵腕时袖口滞后半拍;镜头几何:v26 机位近景仰角,指天手在画框顶被裁一次
- H3:`marching forward with one arm punching straight up and index finger to the sky, pumping the raised wrist on every knee-lifted step, circling the wrist once with a grin before bringing the arm down`
- 来源:《彩虹的微笑·长春》00:39.5-42.25s

### K124 单臂高举绕腕挥手行进-甩头撩发链(7拍|v26 挥手互动主件)
- 入态:侧向站位 → 出态:甩发回正,laughing 接演唱
- 分解:拍1 空手直臂高举过顶,掌心向前,起步侧移;拍2-3 举臂腕部绕圆挥手两圈,躯干随挥手方向微摆,行进不停(发力全在腕+肩,肘伸直);拍4 挥手加入全臂前后摆幅,向远端观众区送,头仰起看指尖;拍5 手臂下落同时低头,长发整个翻过脸(技术峰值:落臂与甩头同拍);拍6 头从下向上甩回,发梢飞出画弧,脸从发帘后露出大笑;拍7 双手合到肩前小拍两下回收,回演唱位;服装物理:长发甩动完整覆盖面部约 0.4s,亮皮裙随侧移反光变化;镜头几何:机位横移跟行进,甩头帧面部被发遮挡属预期
- H3:`side-stepping with one arm held high overhead circling the wrist in a big wave toward the stands, then dropping the arm and snapping the head up to toss the hair off the face into a laugh`
- 来源:《彩虹的微笑·长春》00:65.5-72.0s

### K125 左臂平举缓转背身行进-斜上指角链(5拍|v26 转场件+镜头甩糊注记)
- 入态:面向镜头演唱 → 出态:背身斜上指,镜头转场
- 分解:拍1 左臂直臂向左侧平举伸出,指尖引路,身体开始向左缓转;拍2-3 保持平举匀速转身接背身行进,步幅小而稳,长发垂背,背中拉链与腰包入画(转体无蹬地加速,靠步频匀速,与 K117 快 spin 区别);拍4 背身行进中左臂向上斜 45° 抬起,指向画面上角(技术峰值:背身+斜上指同拍);拍5 指角 hold 一拍,另一手持麦垂在体侧;镜头几何:机位从正面急摇到背面方向,96-108s 区间镜头甩糊并被遮挡 6s+,此链尾帧全部运动模糊——作为转场触发器使用时建议配镜头快摇注记
- H3:`extending one arm level and slowly rotating into a back-facing walk upstage with small even steps, then lifting the same arm into a high diagonal point over the shoulder while still facing away`
- 来源:《彩虹的微笑·长春》00:96.0-100.5s(100.5s 后镜头被遮挡至约 108s)

### K126 白麦火炬高举-穿队形背行链(6拍|v26 群舞穿行件)
- 入态:群舞合围位 → 出态:背身行进没入队形
- 分解:拍1 白色麦克风整支举过头顶如火炬,左手扶腰侧,向前行进提膝;拍2 火炬臂在头顶小幅画弧,两侧黑裙伴舞持白花球同步上举,主角居中领走;拍3-4 行进右转,火炬臂落,双臂张开划水式摆动;拍5 穿入队形中线,转身成背身继续行进,伴舞在她两侧成高低造型(技术峰值:人从队形正中穿过的调度);拍6 背身走位渐远,裙摆随步摆,伴舞花球在画面两侧晃动;服装物理:亮皮裙在背光下发亮,黑裙伴舞花球白色形成前景/背景双层;镜头几何:机位后退拉远让出队形纵深,主角从全景中心渐变小;音乐触发:间奏重拍对应火炬上举
- H3:`marching through the center of the formation with the white mic raised overhead like a torch, sweeping it down to swim-stroke arms on the turn, then weaving into a back-facing walk as the dancers flank into poses`
- 来源:《彩虹的微笑·长春》00:113.5-117.0s

### K127 白裙背身缓行-裙摆随步链(5拍|v27 慢摇行进件)
- 入态:侧身站立 → 出态:背身驻足
- 分解:拍1 右转 90° 成背身,起步向台深处走,步幅小、膝微弹;拍2-4 匀速行进,A 字裙摆随左右迈步向两侧荡开又合拢(技术峰值:第 3 步裙摆展开幅度最大),单辫垂在背后随步轻甩,手持麦自然下垂随臂摆;拍5 驻足,脚跟并拢站定,肩线回平;镜头几何:固定机位不追,主体在画面中渐远渐小,构图从膝上景变全身远景
- H3:`turning away from camera and walking slowly upstage in a fit-and-flare dress, small bouncy steps letting the skirt swing open and closed with every stride before coming to a stand`
- 来源:《第一次爱的人》00:40.0-47.5s

### K128 转身举臂致意远端观众链(6拍|v27 致意主件,两处复现)
- 入态:背身/侧身驻足 → 出态:手臂落回,回演唱位
- 分解:拍1 背身或侧身站位,持麦手从低位抬到嘴,头先转向观众席方向;拍2 空手从体侧沿大弧线向头顶抡起(发力:肩带慢甩,躯干后仰配合);拍3 臂伸直至头顶偏斜方向,掌心向远端观众,定一拍;拍4-5 举臂以肩为轴前后摆动持续挥手 2-3 次,头随臂仰,发丝从肩滑落(技术峰值:挥手与仰头同拍);拍6 臂沿弧线落回体侧,身体转回正面,接演唱;服装物理:无袖裙露出整条手臂线,挥手时裙肩无位移;镜头几何:横屏固定机位,举臂手臂两度触到画框顶被裁,远端荧光棒海在挥手方向形成呼应
- H3:`turning from a back-facing stand to sweep one arm overhead in a slow arc, holding it toward the far stands and waving in sustained strokes with the head tipped back, then letting the arm fall back to singing`
- 来源:《第一次爱的人》00:79.0-83.5s;00:163.0-167.5s(第二处由背身驻足直接起臂,转身幅度更大)

### K129 指尖指观众-画圈停留链(4拍|v27 收尾互动件)
- 入态:浅鞠躬起身 → 出态:收手回体侧,视频收尾
- 分解:拍1 双手垂腹前微低头浅鞠(半拍静态);拍2 起身抬头带笑,持麦手抬至胸前小拳泵两下蓄意;拍3 右臂伸直指向镜头方向观众,食指明确,头微侧倾(技术峰值:指与倾同拍到位);拍4 指尖原地慢速画小圈 2-3 圈保持 3 秒以上,臂不松、笑持续,再收手;镜头几何:横屏固定机位正对指尖方向,荧光棒海为背景衬底
- H3:`rising out of a small bow into a couple of chest-level fist pumps, then pointing straight at the crowd with the index finger and tracing slow lazy circles while holding the pose with a smile`
- 来源:《第一次爱的人》00:226.0-231.6s(片尾持续到收镜)

### K130 颈侧整发-掌心拨发回正开唱链(4拍|生活态非编舞件)
- 入态:立姿停顿 → 出态:面向镜头演唱位
- 分解:拍1 持麦手不动,空手绕到颈后扶住后颈,头低偏(明写停顿,音乐进行中的自然休止);拍2 手指顺发根将长发整体拢过肩前;拍3 掌心从额侧向后拂,把散发全推到脑后,头随之抬起(技术峰值:拂发与抬头同拍);拍4 双手合握麦克风回嘴边,面向镜头开唱,肩线沉下;服装物理:长发从胸前整体位移到背后,裙摆无参与;镜头几何:固定机位胸像景,手部动作全程在画面中带
- H3:`resting one hand at the back of the neck, gathering the long hair over the shoulder and sweeping it back off the face with the palm while lifting the head, then bringing both hands to the mic to sing`
- 来源:《第一次爱的人》00:00.0-07.0s(生活态,非编舞,建议归"日常标准件"而非舞台链)

**片<v28> 《坏女孩营业》(颜沁 K-pop 偶像见面会饭拍·99.1s·竖屏)**
- 背景人物:淡紫/粉/蓝几何色块背景板+台口白色花丛+黑色返送音箱。人物:颜沁——棕色大波浪左侧低马尾+粉色圆珠发圈,婴儿粉圆领针织背心内搭白衬衫(领口灰色缎带蝴蝶结),灰白百褶短裙,白色堆堆袜+白色厚底运动鞋,黑色麦克风;队友:黑色阿迪外套+牛仔裤长发女、红色玫瑰蓬蓬裙女成员。真人饭拍,无 AIGC 特征。
- 直拍特征:长焦饭拍变焦(65-71s 由特写拉远为连续变焦非剪切,推测)。
- 节拍:onset 实测≈127.7 BPM(beat 0.47s,格拟合 91ms);原估 104 修正上移;手势一拍一变不变。
- 镜头形态:A 一镜到底。

### K131 递麦双接互动链(5拍|饭拍营业/K-pop 见面会)
- 入态:双手竖握麦垂于腰前站定 → 出态:麦回到自己唇边、眼神锁定镜头
- 分解:拍1 基座——双手上下叠握麦置于腰前,重心居中,下巴微收(持麦臂自重);拍2 邻位黑衣队友的手从画面左伸入覆住她双手,麦被带低 10cm,她顺势松上手、低头看交叠的手,嘴角先弯(对方臂越过她胸前,肩被轻碰向右让位);拍3 麦被提向队友唇边,她双手托住麦尾仰头看队友,马尾随仰头垂向右后(百褶裙纹路随转髋微旋);拍4 双臂回收把麦拉回自己唇前,头从仰转正再右倾 15°,马尾扫肩(马尾延迟半拍落下);拍5 麦贴唇、眼上翻入镜,左手落回裙前,肩线放平收势;镜头几何:全程镜头从中景推至近景,人物恒居中右
- H3:`standing in an idol line-up holding the mic with both hands at the waist, letting a teammate's hand glide over hers and lift the mic away, looking up with a shy smile while feeding the mic toward the teammate's mouth, then reclaiming it back to her own lips as the head rights and tilts, ponytail swaying half a beat behind each turn, eyes climbing back into the lens`
- 来源:《坏女孩营业》00:06-13.5s

### K132 掩面捧脸歪头链(4拍|饭拍营业·大姿势锁死)
- 入态:双臂交叉抱于腰前低头 → 出态:双手捧脸右歪头定住
- 分解:拍1(锁死前基座)双臂交叉压住裙腰,头低垂左偏 20°(核心静止,只有颈链预备);拍2 头猛甩向上后方,马尾整体抛过右肩成弧形(技术峰值:发梢最高点),左臂同时向侧松开半臂再收回(发浪过顶后回弹两次);拍3 双手从下颌两侧升起贴住脸颊成捧脸,肘内收夹肋,身体其余锁定;拍4 微活性:头以每拍 5° 速率向右歪三次,慢眨眼一次,眼球从下滑到正对镜头,捧脸手型不动,裙褶与鞋位全程零位移(回收顺序:先肩沉再头停)
- H3:`arms crossed over the skirt waist bowing the head, whipping the head up and back to send the side ponytail flying over the shoulder, raising both palms to cup the cheeks with elbows pinned to the ribs, tilting the head right in small five-degree steps, slow-blinking into the lens while everything below the neck stays locked`
- 来源:《坏女孩营业》00:20-28s

### K133 双指比心微活性链(4拍|饭拍营业·大姿势锁死)
- 入态:近景,双手于胸前交叉拼出一枚大指心 → 出态:双手各持半心、头转左 profile 再回正
- 分解:拍1 双手拇指食指在胸口拼成一枚完整心形,肘架平,手腕相抵(饭拍推至胸上特写,心形占画面中心);拍2 心形拆开成左右两枚半心,各手上提 3cm 分置锁骨两侧;拍3 微活性:头整体左转 45° 成侧脸,指心原位不动,眨眼一次;拍4 头转回正前方并微低 1cm,双半心向内再合拢 1cm 收势,肩胛下沉换一次重心(仅颈椎+腕关节运动,躯干锁定;背心领口随肩转出现褶光变化)
- H3:`locking a chest-level finger-heart with both thumbs and index fingers, splitting it into two little half-hearts at the collarbones, rotating only the head to a left profile and back while the hands stay frozen, chin dipping one centimeter on the return, eyes pinned to the camera the whole hold`
- 来源:《坏女孩营业》00:65-69.5s(69.5-71.5s 同姿势镜头拉远至全身)

### K134 牵手旋回裙摆链(4拍|饭拍营业·双人互动)
- 入态:双手叠握麦垂于裙前低头羞立 → 出态:回身面向镜头笑、双手张开的 wave 收势
- 分解:拍1 基座——双手叠握麦垂在裙前,头低右偏,马尾垂右,重心左脚;拍2 左臂向左平伸五指张开邀约,黑衣队友的手接入,她小步并右脚,身体拉成左倾 10°(被牵引而非自走);拍3 队友手臂从她头顶划过做引领,她低头钻转顺时针半圈,百褶裙摆张开成 45° 伞面,马尾在空中甩成横向弧线(技术峰值:转身中点裙摆最大展开;裙摆展开-回弹滞后身体半拍);拍4 转回正面对镜露齿笑,马尾延迟落下扫过右颊,牵着一的手举起晃两下,另一手张开五指在脸侧做小 wave 回收(发梢+裙摆双重回弹;镜头从中景跟摇半圈)
- H3:`clasping the mic low in front of the skirt with the head bowed, reaching the left arm out to catch a teammate's hand, ducking under the sweeping arm for a clockwise half turn as the pleated skirt blooms and the long ponytail whips horizontal, landing back facing the camera with a wide smile, ponytail settling a half beat late, finishing into a two-hand open-palm wave`
- 来源:《坏女孩营业》00:78-92s(90-92s wave 段拍位为推测)

**片<v29> 《秋冬换装》(穿搭换装跳剪·22.3s·竖屏)**
- 背景人物:室内一隅,白纱帘+浅木窗框+米色短绒地毯;模特黑色齐肩外翘卷发、红唇;三套造型:A 炭灰短袖高领+酒红蕾丝中长裙(裸足→酒红尖头细跟→酒红腋下包→黑色外套);B 橄榄绿长袖针织连衣裙+黑丝+黑色粗跟短靴+棕腰带+绿迷你包;C 奶油白 V 领裹身衬衫+藏青阔腿西裤+灰棕尖头靴+黑天鹅绒短外套+酒红手提包。实拍,无 AIGC 特征。
- 节拍:onset 实测≈122.4 BPM(格拟合 68ms);原估 98 修正上移;段切卡点不变。
- 镜头形态:C 快剪(每段内一镜,段间跳切换装)。

### K135 配件递进甩发回望链(5拍|穿搭换装·跳剪)(同构两段合并)
- 入态:段 A 裸足立定扶发 → 出态:段 C 拎包撩发走台步
- 分解:拍1(00:0.8-1.4s)裸足,右手插入发后拢住,左臂垂,右脚尖前点交叉锁位(基座锁定,只有腕颈活);拍2(1.6s 跳切)高跟鞋+酒红包瞬现:右腿提膝迈步,包坠手腕回荡,发从手中放开前荡(包带在腕上打转半圈);拍3(2.6-3.0s)行走中肩向右拧,回头过肩给镜头一个 3/4 笑,随即拧回全身背对(迈步发力自髋);拍4(3.2-3.6s)原地鞭甩发——头从背位向左后猛抡,整头发出横弧盖脸,包顺势荡出体外(技术峰值:发浪盖脸帧;发梢回弹两次);拍5(3.8-4.0s 复用段 C 17.5-19.5s)黑天鹅绒外套披上肩,双手从领口向上把发全部拢向脑后、下巴扬起,右手换拎包走台步,左手最后插入后发一捋(回收顺序:衣先稳、发后落)
- H3:`barefoot in a grey turtleneck and burgundy lace skirt holding the hair back, releasing it into a forward swing as heels and a burgundy bag pop in on the cut, walking into a three-quarter over-shoulder smile before whipping the whole head so the hair fans across the face, then settling a cropped velvet jacket on the shoulders, raking both hands up through the hair with the chin lifted, and striding off with the bag swinging from the right hand`
- 来源:《秋冬换装》00:0.8-4.0s+00:17.5-19.5s

### K136 连衣裙提靴系带链(4拍|穿搭换装·跳剪)
- 入态:橄榄绿裙手拎腰带立定 → 出态:系好带、拢发走步
- 分解:拍1 右手拎棕腰带垂在体侧,起步走来,腰带随步频前后荡(步行惯性;全身居中,地毯透视线引导);拍2 右膝高提至腰线,右手下探握住靴筒,头低垂盯靴,左臂后摆平衡(技术峰值:提膝最高点,裙摆贴大腿绷直);拍3 落腿瞬间头前甩,发浪盖脸遮住整脸再向后抡开(发回弹),同时左脚并步;拍4 双手在腰前捏住带尾穿扣系紧,眼随手动,系毕双手沿腰侧向外抚平、右手顺势把一缕发别到耳后,继续向镜头走(回收顺序:带→手→发;裙腰被腰带勒出细褶)
- H3:`striding forward in an olive knit dress swinging a brown belt from one hand, lifting the right knee high to grip the boot shaft while the head drops to watch, letting the hair whip over the face as the leg drops, threading the belt ends and buckling at the waist with eyes on the hands, smoothing the belt sides before tucking a strand behind the ear and walking on`
- 来源:《秋冬换装》00:9.5-12.5s

**片<v30> 《珠光婚纱》(婚纱写真一镜·14.2s·竖屏)**
- 背景人物:法式酒店套房——奶黄护墙板、白罗马柱、黑漆古董边桌+青花瓷瓶、奶油扶手椅、大理石拼花地面;模特深棕低髻、珍珠耳坠、钻饰 choker,象牙白蕾丝挂脖紧身胸衣+象牙缎面超大蓬蓬裙拖尾(露背 V 至腰)。商家宣传实拍;重度磨皮+局部甩镜动态模糊易被误读为 AI(判断依据:裙褶物理连续、手指与裙面接触正确、转场为手持甩镜,推测)。
- 节拍:onset 粗测≈114.3(13 强拍,格拟合 111ms,低置信);慢板叙述 68 保留。
- 镜头形态:A 一镜到底(手持环绕+甩镜转场+曝光跌落)。

### K137 正面提裙凝视链(4拍|婚纱写真·微活性)
- 入态:3/4 左身立定,头低左 profile → 出态:眼球入镜、下巴微扬定住
- 分解:拍1(大姿势锁死)双腿与蓬裙完全锁死,双手指尖分别压在裙腰两侧蕾丝上,头低垂左 30°(指尖与缎面摩擦力);拍2 微活性:右手五指逐指重新抓握蕾丝一次(只见指节起伏);拍3 微活性:下巴抬起 1cm,眼球先于头转、从下睫毛下缘滑入镜头(眼神先到、头后到);拍4 微活性:重心在双脚间移 1cm,裙体纹丝不动仅腰际缎面反光变宽,头角左偏回收 5°,2.0s 处甩镜糊场转下段(回收顺序:眼→颏→重心;机位绕人物向右缓移 15°)
- H3:`standing three-quarters left in a lace halter bridal gown with both fingertips pressing the satin skirt at the waist sides, head lowered in left profile, re-gripping the lace one finger at a time, sliding the gaze up to the lens before the chin lifts a breath, shifting weight one centimeter between feet while the huge skirt stays dead still`
- 来源:《珠光婚纱》00:00-04s(2.0-2.5s 为甩镜转场)

### K138 裸背回眸铺尾链(4拍|婚纱写真·微活性)(两段合并)
- 入态:全身背影,指尖悬于裙侧 → 出态:柱边全身背影、头转左回眸收尾
- 分解:拍1(00:5.6-8.0s)裸背全背影,双臂微离体侧、指尖虚触裙面,躯干随呼吸极慢起伏,镜头沿背向下缓移(大姿势锁死,仅肩胛与指尖活);拍2(9.6-10.3s)正面双手抓握裙缘后向右拧身成深 3/4 背,右手在右髋前抓拢一把缎面(核心旋转,裙随腰拧出螺旋褶);拍3(10.5-12.1s)头越过左肩回眸入镜,下巴下沉 1cm 压出颈线,抓裙手再收紧一次、肘外顶(技术峰值:回眸帧——背线+颈线+裙褶三线交会),眼球锁镜不随头回正;拍4(13.3-14.1s)曝光恢复后全身背影立于立柱旁,拖尾在地面铺成扇形,头再向左转 30° 做最后回眸,手垂回裙侧收势(拖尾随最后一移步展开-停驻;远机位全身,人物偏右)
- H3:`showing the bare back of the halter gown with fingertips hovering at the skirt sides, pivoting to a deep three-quarter back while the right hand gathers a fist of satin at the hip, turning the head over the left shoulder to pin the lens with the chin sunk and a re-grip of the gathered satin, finishing as a full-back silhouette by the column with the train fanned across the marble and the head turned left`
- 来源:《珠光婚纱》00:5.6-8.0s+00:9.6-14.1s

**片<v31> 《青花瓷翻唱》(翻唱自拍一镜·22.6s·竖屏)**
- 背景人物:暗调咖啡角——埃菲尔铁塔装饰画、烛形小灯、串灯花环、白色壁炉线脚;女生深棕碎刘海短发(发尾锁骨长),象牙白底青花蓝碎花短袖上衣,右肩黑色圆环包带+浅黄小包身入画下缘。真人自拍翻唱;字幕为后期歌词(天青色等烟雨/炊烟袅袅升起/就当我为遇见你伏笔)。简报"疑似古风/AI"修正:实为室内翻唱。
- 节拍:onset 粗测读法不定(107 或倍频),原曲量级 ~60 保留,低置信。
- 镜头形态:A 一镜到底(固定自拍机位,仅曝光渐暗)。

### K139 唱段微活性·天青色句(4拍|翻唱自拍·大姿势锁死)
- 入态:头微左低、口将张 → 出态:句尾眼回镜头、头回正
- 分解:拍1(大姿势锁死)胸像构图肩上锁定,肩线/衣褶全程零位移,右手在下缘捏住包带(颈链独立);拍2 微活性:开口唱"天青色"——口型大开再收圆,头随乐句摆 3° 向左;拍3 微活性:一次完整慢眨眼+眼球垂向左下,再沿 45° 爬回镜头(眼神路径固定为下-左-回);拍4 微活性:头右回正过中线 2° 回弹,口型收在"等你"尾音闭合,捏带拇指随拍轻叩一下(刘海随头摆延迟半拍;脸占上 2/3 恒定)
- H3:`holding a static bust frame in a blue-floral ivory top, swaying the head a few degrees on the phrase, letting the lips open wide and round through the sustained note, blinking slow and full with the eyes drifting down-left before climbing back to the lens, fingertips pinching the strap at the bottom edge with the thumb ticking the beat`
- 来源:《青花瓷翻唱》00:3.6-7.6s

### K140 唱段收尾·渐暗沉光链(3拍|翻唱自拍·大姿势锁死)
- 入态:句间换气、头正 → 出态:画面近乎全暗、脸右下 15° 沉入剪影
- 分解:拍1 唱"就当我为遇见你伏笔",头向右转 5°、下颌微收,口型轻咬字(乐句尾自然带动);拍2 曝光开始跌落,环境先暗、脸后暗,瞳孔显大,眨眼放缓到一次跨两拍(只剩呼吸起伏可见);拍3 头再右沉 15°、视线落向右下,轮廓与肩上黑环带成为最后可读元素,画面沉入近黑收束(回收顺序:环境光→面部→眼神;机位零移动,纯曝光变化)
- H3:`turning the head five degrees right on the closing phrases, softening the mouth into half-sung syllables, letting the room light dim around the face until only the outline and the shoulder ring stay readable, eyes lowering as the frame fades to near black`
- 来源:《青花瓷翻唱》00:17.6-22.6s

**片<v32> 《上元·戏腔舞台》(古风戏腔演唱会直拍·36.3s·竖屏)**
- 背景人物:淡青主调舞台屏——月洞圆窗+瓦檐纹+"上元"大字;女歌手:银黑羽扇形高冠+银流苏步摇+额间花钿,奶白缎面宽袖长袄(袖口织金纹与水墨镶边),湖蓝百褶裙+红金织花腰封,粉白渐变麦克风。真人舞台直拍(字幕歌词:凤箫声动 光转玉壶/你耳语话更改了我两鬓流苏/生辉盼顾 清风吹拂/觥筹交错举杯美酒欢如注/心无旁骛 相对四目/忽然我就深陷中了你的蛊)。简报"疑似 AI"修正:实为现场直拍。
- 节拍:onset 粗测读法不定(126.3 或半速 63),戏腔慢板倾向 63(推测)。
- 镜头形态:A 一镜到底(直拍长焦变焦)。

### K141 耳语拢发垂袖链(4拍|古风戏腔舞台·手势舞)
- 入态:右手持麦于唇、左臂垂 → 出态:左手收回胸前、袖堆腕上
- 分解:拍1 右手举麦贴唇起唱,左臂随乐句向外荡开,宽袖滑到肘下挂住(肩带臂,袖重拖拽);拍2 左手两指沿鬓角把一缕发别向耳后,头随触点右倾 8°(手势与"你耳语"词点同步——歌词触发实测);拍3 袖面自肘滑脱、整幅垂到腕上堆成玉坠状,指尖仍停在耳后一息(技术峰值:袖坠腕的静帧;缎面袖延迟身体半拍落);拍4 手离耳沿颊侧划下收至胸前,头左回正,冠上银流苏随头摆轻晃(流苏两拍内衰减;镜头从中景推近半身)
- H3:`singing into a lavender mic held at the mouth while the free arm swings out on an embroidered sleeve, tucking a strand behind the ear with two fingers as the head tilts into the touch, letting the wide sleeve slide down the forearm and pool at the wrist, returning the hand to the chest with the sleeve trailing`
- 来源:《上元戏腔》00:5.4-8.8s

### K142 按胸扬掌起身链(3拍|古风戏腔舞台·手势舞)
- 入态:3/4 左身、左掌按于心口 → 出态:手升至颏下、身回正
- 分解:拍1 左掌平贴心口、五指舒展,头沉入左 profile,麦仍稳在唇边(掌根压胸的自压感,肩胛后收);拍2 按压保持整句,指尖随字腹轻颤两次,视线先垂后扬回镜头(微活性:仅指与眼);拍3 掌离胸、指节向内卷收,沿胸线上浮至颏下停住,脊柱节节回正,冠位全程水平不晃(技术峰值:手到颏下与头回正同时到达;回收顺序:头→手→肩)
- H3:`pressing the left palm flat over the heart with fingers spread and the head sinking into profile, holding the press through the line, then peeling the hand off the chest and curling the fingers inward as it rises to the chin, spine lengthening back to vertical with the silver-feather crown staying level`
- 来源:《上元戏腔》00:17.0-19.8s

### K143 双手捧麦羞笑收势链(4拍|古风戏腔舞台·手势舞)
- 入态:右手单持麦,左手做捏指小动作 → 出态:双手合握麦收于胸前、下颌微收定住
- 分解:拍1 左手拇食指相捏、余三指弯成小钩,在胸口高度随"深陷中了你的蛊"词点左右摇滚(歌词触发实测;腕为轴小幅摆);拍2 捏指手上提向脸,右手的麦同步降半掌,双手向中聚合(两手互为归点);拍3 双手一并裹住麦身,宽袖翻下来盖住腕背,头右倾 10° 嵌出羞笑,眼球斜上瞟一瞬再回镜(技术峰值:裹麦+羞笑同帧);拍4 双手裹麦收至胸骨前定住,下颌收 1cm,冠珠与流苏静止,肩沉一口气收束(袖堆在腕上叠出三层;镜头微推至半身)
- H3:`rocking a pinched-finger hand at chest height side to side on the phrase, drawing the hand up toward the face, wrapping both hands around the mic with sleeves draping over the wrists, tilting the head right into a shy smile aimed at the lens, settling hands and mic together at the upper chest with the chin tucked for the close`
- 来源:《上元戏腔》00:29.6-36.0s

**片<v33> 《奇袭白虎团·踩雷》(1972 京剧电影武戏剪辑·109.1s·竖屏内嵌黑边)**
- 背景人物:灰蓝夜外景(山影+松枝+石台)→蓝光夜坑→敌指挥所木屋内景(木桌+电话+窗帘);主角侦察排长严伟才:灰绿军官制服+大檐帽,灰面红里斗篷;侦察兵群:灰制服+白/灰披布+钢盔+步枪;夜袭段主角换白衬衫+深色长裤+鸭舌帽+红袖标,持带刺步枪,敌军官灰制服钢盔。1972 年真实京剧电影胶片质感(颗粒/暗角/宽银幕条框),武打为真实戏曲演员配合;水印"桃白白co bilibili",108.5s"必剪"片尾卡;20-40s 为剪辑留黑段。简报"疑似 AI"修正:实为老电影剪辑。
- 节拍:京剧锣鼓板式驱动,无固定 BPM;锣鼓 onset 实测≈127.7(快板段,格拟合 71ms);板式驱动不变。
- 镜头形态:C 快剪(原片镜头间硬切;跨切动作连续性为组接,按相对拍标注)。

### K144 夜幕踩雷训令链(4拍|京剧武戏·样板戏电影)
- 入态:特写,右臂侧平指、目眦欲裂 → 出态:全身令下、群兵伏地后撤
- 分解:拍1 特写基座——右臂向右侧平伸、五指分张成指物位,斗篷搭肩垂顺,目光钉死画面左(台词"我……踩着地雷了"触发,下颌绷紧只动唇);拍2 特写微活性:眉峰压低 1mm、颈筋显形,臂位纹丝不动(大姿势锁死,只有面部与呼吸);拍3 切全身——臂从侧平位向下向前抡成指挥弧,斗篷随肩转荡起里衬红(腰背拧转带臂,技术峰值:臂挥至前下 45°);拍4 随"迅速后退!"臂再向侧上弹抖一次,身后群兵自蹲踞转伏地倒爬后撤,主角钉在原地成三角站位收势(斗篷下摆随挥臂两拍内摆尽;特写→全身硬切,主角恒居左前景)
- H3:`in a grey officer uniform and red-lined cape pointing one arm straight out with split fingers, glaring hard to the left while only the jaw moves on the line, sweeping the arm down and forward into a command arc, flicking it out on the retreat order as the squad behind scrambles backward into prone crawls, cape hem settling two beats behind the shoulder turn`
- 来源:《奇袭白虎团》00:01-09s

### K145 斗篷旋身穿掌指挥链(5拍|京剧武戏·样板戏电影)
- 入态:群兵一线匍匐 → 出态:主角静立亮相、群兵携枪入场
- 分解:拍1 群兵白披布覆背、一线匍匐爬行横过画面(群像底噪层);拍2 主角红斗篷自石台后切出,斜线奔跑,斗篷平展拖尾,右手前指(蹬地步频,斗篷反向滞后);拍3 收步跺定,右拳举过头顶,斗篷顺势裹上肩(跑动惯性经跺步灌入拳);拍4 斗篷裹身拧半圈——外灰内红双色翻卷成伞状(技术峰值:篷展伞面帧,6fps 密帧实测 49.4-50.4s),拧出即变左掌向前平推成穿掌位(篷角回甩至背后);拍5 全身静止亮相两拍,随后群兵携枪自画面左列队跑过,主角掌位不动送队(回收顺序:身→篷→目光;全身居中,群兵走前景横线)
- H3:`leading a line of prone crawlers across the stage, breaking into a diagonal run with the cape flying, stamping to a stop with a fist raised overhead, winding the cape into a half-turn that opens it like an umbrella, breaking out into a flat palm pushed toward the squad, holding still for the photo pose as the ensemble files past from the left with rifles low`
- 来源:《奇袭白虎团》00:43-56s(旋身细节 00:49.4-51.4s 6fps 密帧)

### K146 排雷腾跃斗篷亮相链(6拍|京剧武戏·样板戏电影)
- 入态:群兵蹲踞作背景石台,主角步出 → 出态:坐地铺篷收势
- 分解:拍1 步出至台心,斗篷垂落体侧,随后屈膝下沉蓄力(膝踝压缩储能);拍2 蹬地腾空——双臂向斜上展开,斗篷内衬红面全部张开成双翼(技术峰值一:空中展篷,6fps 实测 84.3-84.5s);拍3 马步落地,双臂水平端平,篷幅仍保持展开弧——静亮相一拍(回收顺序:腿→臂→篷);拍4 反向拧身,斗篷反裹全身成茧状旋团,白外面朝镜头(篷布缠绕躯干-臂三层);拍5 破茧再腾跃二次展篷,空中身体倒平成水平旋子面(技术峰值二:倒身横空帧,87.3s);拍6 落地顺势坐地,斗篷铺满腿面成扇,上身后仰撑手再蜷坐弹起半次收束(篷角在地面滑移半拍;全身正面恒定,背景群兵蹲姿做石台剪影)
- H3:`sinking to a crouch in front of the rock set, launching into a soaring leap with both arms spread so the cape opens into red wings, landing in a wide horse stance with arms level for the pose, winding the cape around the body through a tight cocoon spin, bursting out into a second leap that inverts horizontal in mid-air, folding into a seated finish with the cape spread over the legs`
- 来源:《奇袭白虎团》00:83-88s(腾跃/倒身细节 00:84.0-87.8s 6fps 密帧)

### K147 夜坑翻滚群像链(3拍|京剧武戏·群体翻扑)
- 入态:坑沿白影自右向左跌落 → 出态:坑底叠伏成堆静止
- 分解:拍1 第一名侦察兵自坑沿抢背翻下,蓝夜光里身体团紧、白披布翻卷包住躯干(前冲惯性+低头抱膝);拍2 连续两三人叠落,半空可见倒插体位、双腿朝天蹬直再团身(技术峰值:倒插帧;披布翻飞滞后身体一拍);拍3 后续队员依次滚压入堆,坑底人堆起伏两次后静止,只剩披布余波(布面颤动两拍;固定全景,跌落方向恒为右→左)
- H3:`rolling down the blue-lit slope into the trench, bodies tucked and tumbling with legs kicking skyward mid-fall, white cloths lagging a beat behind each rotation, successive scouts piling into a heaped stillness on the pit floor with only cloth ripples remaining`
- 来源:《奇袭白虎团》00:88.5-95s

### K148 白衣夜袭枪刺过顶摔链(5拍|京剧武戏·对打)
- 入态:木屋内景,敌兵挺刺、白衣者侧身 → 出态:敌伏地、白衣者立枪亮相
- 分解:拍1 敌兵自左挺枪直刺,白衣者右手横枪格开、左手护胸前,身成弓步对顶(枪杆相击的反冲,两臂三角锁);拍2 敌二度扑进,白衣者沉肩钻入其臂下,双手锁其腰带向上发力(低身进正是全部前提);拍3 技术峰值——把敌兵整体过顶举起,敌体在空中倒插水平,白衣者双臂全伸托举一拍(镜头微仰强化高度);拍4 顺势旋腰把人摔向右前,紧接着一记扫踢把第二名敌兵踢得横飞扑地,枪身随腰拧画出立圆(枪尖余摆两拍);拍5 拖枪收步,枪托顿地,另一手扶枪身中段立枪于体侧,下颌抬起目视前方,背后敌兵伏地不动——定场亮相(回收顺序:敌→枪→身;镜头从近身切全身)
- H3:`deflecting a bayonet thrust with a horizontal rifle sweep in the wood-walled room, ducking under the second lunge to hoist the attacker overhead in a full arm extension, spinning him down with a waist turn, sending the second enemy sprawling with a sweeping kick as the rifle draws an upright circle, then grounding the rifle butt and standing tall over the fallen with the chin lifted for the closing pose`
- 来源:《奇袭白虎团》00:97-108s

**片<v34> 《Genie》(姜杉 Focus 九机位精剪·魔力生日会·K-pop 翻跳·172.1s·竖屏)**
- 背景人物:室内剧场舞台,深色天幕+大屏蓝白圆形光斑/红色丝带/紫蓝条纹三种灯效;台口返送音箱、落地风扇、侧台灯具与线缆入画。人物:姜杉——白色宽松翻领衬衫(七分卷袖、下摆掖入)、黑色高腰紧身短裤、黑色挂绳白色工牌卡套(职场概念)、黑色过膝弹力长靴(方粗跟)、黑棕中分微卷长发披肩、细项链、深色尖甲。队友同款白衬衫,部分系黑小领带/戴墨镜,黑短裤或黑半裙、黑高跟,工牌挂绳同款。
- 直拍特征:九机位快剪,切点密集(约 3-8s 一切),检出切换≈30.5/32.0/34.8/63.2/69.5/89.0/90.8/94.3/96.5/127.3/131.0/149.8/152.3/154.3/156.4s;机位含低角仰拍、面部特写、背面全景、三人横排;0-2s 为字卡。
- 节拍:onset 实测≈120 BPM(强点密度 0.25s=8 分音符层,倍频 240 修正;格拟合 59ms,高置信);拳泵/顶胯周期吻合。
- 镜头形态:C 多机位快剪。

### K149 走秀扬手顶胯-下擦手侧抬腿链(7拍|单人竖条·职场风)
- 入态:蓝光群舞行进,双臂体侧自然摆 → 出态:并步站定,双手收于体前,腕部余摆未消
- 分解:拍1(27-28.5s)群舞行进,髋随步幅左右送,工牌随步左右小荡,白衬衫掖摆稳定(股四头+核心行进);拍2(29-30.5s)右臂向侧甩出掌心向前,左臂屈肘收胸侧,右髋顶出,身体微左倾(肩袖外展+髋侧顶);拍3(30.5-32s)左臂向侧下伸指尖向下,右手收至下颌旁,三连小步交替提膝(30.5/32s 两处切机位);拍4(32-34s)亮相:右手举至头侧五指张开,左手插髋,左髋连顶两下,头随胯小幅左右甩,长发发梢延迟甩动;拍5(34.5-35.5s)双手收至胸前交叠再向两侧打开(34.8s 切暗底圆斑机位);拍6(36-37.2s)技术峰值:右掌从脸侧向下擦过胸前至腰际,同时左腿向左直膝抬起划弧约 45°,上身向右对拉;拍7(37.5-38.5s)收腿落步,双臂顺势向下抖腕甩出(甩毛巾式),惯性使指尖继续下荡,回收=收肩并步;音乐触发=每拍强点对应顶胯/甩腕
- H3:`strutting forward with hips swaying, sweeping one arm out with the palm forward, popping the hip while flashing an open palm beside the head with the other hand on the hip, then sweeping one hand down the chest as the opposite leg lifts and arcs sideways, flicking both wrists downward like shaking off water`
- 来源:《Genie》27.0-38.5s(机位切点 30.5/32.0/34.8s)

### K150 推掌抹胸-双拳拳泵-X 交叉-叉腰高抬膝行进链(8拍|单人居中·可爱力)
- 入态:深红丝带背景中景,双掌举至头侧 → 出态:右拳向上伸直定格,靴筒立起
- 分解:拍1(60-61s)双掌掌心向外自头侧向前下方压掌,膝弹动两次;拍2(61-61.8s)右掌向左前快速抹过脸前(切式),左拳砸向髋侧,短促发力;拍3(61.8-63.2s)双掌贴胸下滑至腰际指尖张开,耸肩,膝内扣半蹲(核心下段+前锯);拍4(63.2-64.5s)双拳高举过头向上顶两下,身体随拳上弹(63.2s 切机位);拍5(64.5-66s)左拳高举定格,右拳于肩侧向下泵一次,髋左顶小步行进;拍6(66-67s)双掌前推(停势)随即双臂胸前交叉成 X(掌心向外),膝外开半蹲;拍7(67-69.5s)双臂自 X 向两侧打开划落,双手插髋左右顶胯各一次(69.5s 切低机位);拍8(69.5-72s)叉腰高抬膝行进:右膝抬至髋高连提两步,挺胸后仰下颌上扬,结尾右拳向上伸直定格;音乐触发=副歌重拍对齐拳顶/膝提;同款组合 120.0-132.0s 重复(漂浮掌→顺腿上摸→拳泵拇指外弹→X 交叉→叉腰高抬膝→双人胯摆,切点 127.3/131.0s),合并件双时间码
- H3:`pushing both palms down from head height, sliding the hands from chest to hips with shoulders raised, punching both fists overhead, crossing the arms into an X then opening them wide, hands on hips popping side to side, and marching with high knee lifts before snapping one fist straight up`
- 来源:《Genie》60.0-72.0s;120.0-132.0s(同款重复)

### K151 拳泵行进-队形背走-低位交叉合手链(6拍|队形变换·利落)
- 入态:三人景拳泵起,深色背景 → 出态:双手松开垂于体侧,笑颜定格
- 分解:拍1(86-88.5s)拳泵行进:双拳交替于肩侧向上泵,步幅小髋随泵左右送(86.5s 切近景);拍2(89-90.5s)队形变换:全队转身背对镜头小步快走至后区,长发披背随步摆动,双臂自然后摆(89.0s 切背面全景);拍3(90.5-91.5s)回身:原地右后转,发梢甩起划弧,双臂向外展开(90.8s 切机位);拍4(91.5-93.5s)低位交叉:双臂于小腹前交叉成低位 X,掌背相对,随节拍摆胯两次,红色丝带背景;拍5(93.5-95s)双臂向两侧打开划半圆下落,掌心向下浮于髋侧(94.3s 切紫底机位);拍6(95-96.5s)双手腹前交握,头右倾肩左顶送髋,笑颜定格,回收=松手垂臂(96.5s 切三人横排机位);音乐触发=预副歌小节切换对齐转身与 X 交叉
- H3:`pumping the fists alternately at shoulder height while marching, turning the whole line to walk away from the camera with hair swaying down the back, spinning back around with a hair whip, crossing both arms low over the belly into an X, then opening the arms in a half circle and clasping the hands in front with a head tilt`
- 来源:《Genie》86.0-96.5s(切点 86.5/89.0/90.8/94.3/96.5s)

### K152 背叉腰后踢走-回身顶胯-三人拳泵收势链(6拍|背影线·收势)
- 入态:侧身小跑切步,低机位仰角 → 出态:右手举至头侧五指张开,三人横排定格
- 分解:拍1(146-147.5s)侧身切步:双拳交替肩侧泵,左肩前送,低角仰拍强化腿部透视;拍2(147.5-149.5s)双手插髋左右顶胯两次,右膝提至髋高再落,头随胯摆(149.8s 切背面全景);拍3(149.5-151.5s)技术峰值:背对镜头叉腰直背,右腿向后伸直点地再踢臀收起,左腿主力,髋部向镜头方向送出,长发全披于背——后伸腿+送髋同拍成大线条;拍4(151.5-153s)原地转身:右肩引导回身,发尾甩出弧线,双手滑至髋骨(152.3s 切蓝底机位);拍5(153-154.5s)指尖卡髋骨左右顶胯各一次,视线过肩回看镜头;拍6(154.5-157s)三人一字排开双拳交替肩侧泵,步幅一致(154.3/156.4s 切机位),结尾姜杉右手举至头侧五指张开收势;音乐触发=桥段末四小节对齐背走,尾拍定格于下一乐句起点
- H3:`marching with alternating shoulder-level fist pumps, hands on hips popping side to side with a high knee lift, walking away on straight legs kicking one heel back while pushing the hips toward the lens, spinning back with a hair whip to hook the fingertips on the hip bones, then closing in a three-person line with fist pumps and one palm fanned open beside the head`
- 来源:《Genie》146.0-157.5s(切点 149.8/152.3/154.3/156.4s)

**片<v35> 《I Love You》(EXID 路演直拍·"服装没到随便穿"·195.2s·竖屏)**
- 背景人物:室内路演舞台(随机舞蹈活动),粉紫色像素风背景板(BZ Boundless Zoom 标识、中文"随机舞蹈"立体字、闪电/音符贴纸)、粉色圆形地贴。被跟拍成员:白色透视宽松长袖衬衫敞开、黑色吊带内搭、黑色紧身短裤、黑色薄丝袜、黑漆皮防水台一字带细高跟(红底),棕色渐变大波浪长发,深色长尖甲——混搭"随便穿"风。队友(背景):红棕发黑抹胸+铆钉黑短裤+红底黑高跟;黑短发黑连体裙+灰丝袜+黑长靴;白衬衫黑背带男装舞者等随机参与者轮换入画。
- 直拍特征:主机位全身固定直拍为主,间以推拉变焦与横摇(101.5s 起男装舞者入画时左摇);检出切镜≈13/20/26/35.3/44s;100-112s 深蹲段为持续固定仰角直拍。
- 节拍:onset 粗测 81.1(倍频不定,户外掌声污染);维持 118(X 交叉 0.5s/拍动作周期吻合),低置信。
- 镜头形态:A 跟拍为主+少量多机位切换。

### K153 X 交叉臂开手滑臂-钟摆摇摆-比心链(6拍|双人前后·X 交叉标志)
- 入态:双臂胸前交叉成 X,宽距半蹲,双人前后错位站 → 出态:全队转身背对镜头走位
- 分解:拍1(1-3s)X 交叉(右臂在上),双腿开立宽于肩膝微屈,掌心向下指尖张开,红棕发队友于后同款;拍2(3-5s)交叉不变,双手沿对侧上臂向外滑开再合回,开合循环两轮,指尖始终张开如扇,膝随节拍屈伸(胸大肌水平内收/外展);拍3(5-6.5s)双臂自 X 解开向前下方伸直推落(峰值=双臂直线甩出);拍4(6.5-7.5s)双手胸前快速合拢成心形指位再向两侧下抹(擦桌面式);拍5(7.5-10s)双臂重新交叉成 X,全身以髋为轴左右钟摆,肩头交替前送,膝随摆加深屈伸,重心左右脚交替;拍6(10-12s)X 保持,右拳自交叉中向前弹出一次随即收回,12s 全队转身背对走位(13s 切机位);音乐触发=副歌"알러뷰"吐字点对齐开手滑臂;同款 X 交叉 172.0-184.0s 重复(体摆+拳弹循环→胸前比心下移至盆骨→下砸拳收→转体,切镜 172-184s 全程连续直拍),按合并件双时间码;另 73.3s、93.3s(总览)亦见 X 交叉定场
- H3:`crossing both arms into an X over the chest in a wide plie, sliding the hands out along the opposite sleeves and back with fingers fanned, unfolding the arms to push straight down, snapping a quick finger heart before a tabletop wipe, then re-crossing and pendulum-swaying the torso hip to hip while popping one fist forward out of the cross`
- 来源:《I Love You》1.0-12.5s;172.0-184.0s(合并件);定场 73.3s、93.3s

### K154 行进摆臂-飞吻交叉抬腿-扑翼摆-发际定格链(7拍|群舞中心·俏皮)
- 入态:行进摆臂,黑短发队友于侧 → 出态:双掌举至面部两侧掌心向外,队列收拢定她为中心
- 分解:拍1(33-34s)行进:双臂体侧大幅摆,步幅大,高跟落脚带踝部微晃(髋屈肌+踝稳定);拍2(34-35s)技术峰值:右手背贴唇向前送吻,左臂后下甩,同时左膝提至髋高前跨——吻与提膝同拍对开,丝袜腿线全展;拍3(35-36.5s)双手滑至髋骨,深蹲幅左右摆胯两次,膝内扣外开切换(35.3s 切三人景);拍4(36.5-39s)扑翼摆:双臂屈肘于体侧上下扑动,膝弹动,头小幅左右甩,两侧队友同拍扑翼(37-38.5s 群舞同步);拍5(39-40.5s)右臂平举前指,收肘回拉一次,小步行进;拍6(40.5-41.5s)定格:右手五指张开贴头侧发际,左手抓短裤下摆,双膝并拢内扣,下颌右偏,长发停摆;拍7(41.5-44.5s)双拳胸前泵两次,队友高踢腿入画(43s),44s 切群景双掌举至面部两侧掌心向外收拢为中心;音乐触发=说唱段语速点对齐扑翼频率
- H3:`striding forward with big arm swings, blowing a kiss off the fingertips while driving one knee up to hip height, sliding the hands onto the hip bones for a deep side-to-side hip sway, flapping bent elbows like wings with a knee bounce, pointing forward, then freezing with one open hand at the temple and the other gripping the shorts hem`
- 来源:《I Love You》33.0-44.5s(切镜 35.3/44.0s)

### K155 爪形挥手-弹指-头顶比心-T 位扑臂-宽距比心链(7拍|单人竖条·手势流)
- 入态:双手举至头侧五指张开 → 出态:双手贴大腿下抹,长发落定
- 分解:拍1(60-62s)爪形挥手:双手举至头侧五指如爪,手腕快速左右摆,肘高抬,长发随腕摆轻晃;拍2(62-63.5s)双掌于面前向下压一次,右手屈腕向上弹指(响指势),左手按于胸口,重心移右脚(63s 切全景);拍3(63.5-65s)双手举至头顶上方合成心形,踝交叉踮立,下颌微收(峰值=心形顶置);拍4(65-66s)耸肩摊掌:双掌两侧摊开掌心向上,双肩交替耸两次,膝并拢弹动;拍5(66-67.5s)双拳收至肩侧向上顶两次,膝深弹,队友左入画(67s);拍6(67.5-69.5s)T 位扑臂:双臂平举成 T 上下小幅扑压三次,踝交叉小步横移(模特台步);拍7(69.5-71.5s)双腿开立深蹲幅,双手先于额前合心再落至盆骨前合小拳心,膝内扣,收势双手贴大腿下抹;音乐触发=副歌尾"lo-lo-love"音节点对齐比心落位
- H3:`waving both claw-spread hands beside the head, pressing the palms down then flicking a wrist snap with one hand on the chest, forming a heart above the head on crossed ankles, shrugging the palms open, pumping fists at the shoulders, flapping flat T-arms while stepping cross-ankled, and closing in a wide plie as the heart slides from the forehead down to the pelvis`
- 来源:《I Love You》60.0-71.5s(切点 63.0s)

### K156 前倾摸背-深前折-甩发深蹲摸踝定格-起身扫腿链(7拍|下腰蹲姿·腿部线标志)
- 入态:踝交叉站姿,右手抚发别耳后 → 出态:展臂小跳站定,长发扬起未落
- 分解:拍1(100-101s)抚发站位:右手把发别至耳后,双腿踝交叉,直拍正身;拍2(101-102.5s)前倾摸背:上身前倾,右手沿腰后滑至臀外侧按住,挺胸抬头看镜头(竖脊肌控制前倾,峰值之一=胸部反弓);拍3(102.5-103.5s)深前折:继续前折至背近水平,双手滑过膝至小腿,头侧转看镜头,臀向后顶——丝袜+高跟腿线全展(腿部 line 标志帧);拍4(103.5-104.5s)甩发起身:头发向前甩再向后撩起,双臂后上展开,臀后坐屈膝入蹲(长发滞后于头约半拍);拍5(104.5-109s)技术峰值:深蹲至臀贴踝,右手下滑摸到脚踝一字带,右膝叠于左膝上,上身挺直看镜头,定格持续约 4 秒(固定仰角直拍);拍6(109-110.5s)借伸膝弹出起身,左腿向侧划弧落地,右手顺大腿外侧下抹至膝,男装舞者左入画(机位左摇);拍7(110.5-111.5s)右腿侧伸成低弓步右手抓握大腿,随即起身双臂大幅展开小跳,长发扬起收势;音乐触发=副歌重拍"나 사랑해"落点对齐甩发,蹲姿定格覆盖 4 个小节长音
- H3:`brushing the hair aside in a crossed-ankle stance, leaning forward sliding one hand along the lower back to the hip with the chest lifted, folding deep until the hands reach the shins with the head turned to the lens, whipping the hair up to rise, dropping into a deep squat resting a hand on the ankle strap for a held four-count, then springing up sweeping one leg out and stroking the thigh before a wide arm-spread hop`
- 来源:《I Love You》100.0-111.5s(全程连续直拍,仅镜头左摇)

**片<v36> 《小情郎》(国风写真 BTS 混剪·15.2s·竖屏)**
- 背景人物:中式戏台婚庆景——深红绸布垂幔、金色大"囍"字圆形浮雕墙、红花球、玫红缎布围台;第二场景室外广场街拍。人物:少女——红色牡丹印花无袖旗袍(膝下+白衬裙露边),A 造型低髻+金色弧形发饰+红绒花、B 造型空气刘海+耳侧珍珠链,珍珠项链、长款耳坠、玉镯,道具黄色绢面折扇;同伴少女全红旗袍+白色流苏披肩+黑长直。实拍(路人目光方向、街景纵深、运动模糊一致)。
- 节拍:(推测 70-80,国风慢板)
- 镜头形态:C 快剪(舞台全景/街拍特写/双人近景≥6 组)

**片<v37> 《骊山手势舞》(卧室手势舞·10.8s·竖屏)**
- 背景人物:粉色少女卧室——白纱床幔、卡通印花床品、窗台长毛玩偶、毛绒玩具堆、白+粉双层窗帘。人物:少女——灰白蕾丝层叠吊带纱裙(lolita,及膝),白色蕾丝发带+黑长直双马尾,白蕾丝腕套、白色及膝袜。标题为《阿房宫赋》文句但画面为实拍卧室(床品褶皱、动作拖影、发丝物理一致,该 AI 疑判不成立)。
- 节拍:(推测 120,手势每 0.5s 一换)
- 镜头形态:A 一镜到底(固定机位自拍)。

### K157 团扇过顶下压凝视链(4拍|国风写真·微活性)
- 入态:台上全身正面,团扇横置头顶后方遮住发冠,右手扣扇柄顶端 → 出态:扇沿下压至颧骨旁半遮脸,头右倾,眼球从扇沿上方滑入镜头
- 分解:拍1(大姿势锁死)双腿在旗袍内锁死,右手虎口扣扇柄置头顶,头从扇沿下露出、眼球对镜头,前景红花球虚化;拍2 微活性 左手五指先后贴上扇面左缘(食指→中指→无名指),扇左倾 10°、头随右倾 15°,眼神不离镜头;拍3 主动作 右肩带发力沿右前弧线把扇下压到下颌高度,峰值=扇沿扫过眉毛瞬间,白衬裙下摆以 1-2cm 延迟晃动(旗袍硬、衬裙软双层);拍4 回收 下巴回 5°、持扇腕再旋 5° 使扇面正对镜头,眼神先到、头后到
- H3:`standing on a red silk stage in a floral red qipao, lowering a round silk fan from above the crown down beside the cheekbone while the eyes slide to the lens ahead of the chin, the under-slip hem lagging one beat behind`
- 来源:《小情郎》00:00-02.5s

### K158 双人折扇开合挑逗链(5拍|国风双人互动)
- 入态:双人胸像,主女折扇收拢高举 → 出态:金扇再开横挡同伴口鼻前、同伴立红团扇遮脸回应,主女眼球回镜头嘴角上挑
- 分解:拍1 右臂举收拢折扇立指向斜上,同伴自右后探入、目光锁扇尖;拍2 腕部爆发抖腕开扇,峰值=扇叶全开瞬间的惯性弹颤,同伴嘴张惊叹、肩前倾 10cm;拍3 手指逐级合拢扇骨变棍状,腕内旋 90° 挑扇尖向同伴面部;拍4 再开扇横挡同伴口鼻,同伴抬红底描金团扇立起遮脸;拍5 双扇对峙定格,回收顺序:肩先松→肘落→扇收至胸前,主女眼神先回镜头
- H3:`snapping a folding fan open beside a companion's head, collapsing it to a stick, re-opening it to cover the companion's mouth while she raises a paddle fan in answer, eyes returning to the lens before the shoulders relax`
- 来源:《小情郎》08.5-10.5s

### K159 收扇指弄低头链(3拍|国风写真·微活性)
- 入态:3/4 站姿,双手在胸骨前持收拢金扇,头低垂视线落扇 → 出态:右拇推扇骨使扇头旋 40°,眼球快速扫镜头一次又落回
- 分解:拍1(锁死)双脚与裙身完全不动,双手持扇于胸骨高度,头低垂;拍2 微活性 右拇指推最外扇骨、扇头绕指尖旋 30-45°,左手指腹沿扇纸滑到扇头再回握,珍珠链随呼吸微晃;拍3 微活性 头角抬 1cm、眼球扫镜头一次即落回(欲看又止),指尖轻拍扇头两下收势
- H3:`standing three-quarters in a red floral qipao, head bowed over a closed gold folding fan at the sternum, rolling the fan head with the thumb in small spins while one eye flicks up to the lens and back down`
- 来源:《小情郎》12.9-15.0s

### K160 颊侧指枪 V 字交替链(4拍|手势舞·节拍链)
- 入态:双臂自上组动作下甩回收至腰侧 → 出态:右指枪贴右颊、左 V 立于左肩外,头右倾 10°
- 分解:拍1 双臂胸前交叉下甩回腰侧(承接惯性),脚跟微弹对拍,发力=前臂甩+膝缓冲;拍2 右食指竖起贴右颊、左手立 V,两手势同拍落定为峰值,头右倾、眼球直视镜头;拍3 手势镜像互换(左指枪/右 V),头回正再左倾,双马尾发梢延迟半拍;拍4 回收 双手胸前收拳再散开下垂,肩落,重心回双脚
- H3:`standing center-frame in a lace dress, alternating a finger-gun to the cheek with a V-sign at the opposite shoulder on each beat, twin tails lagging half a beat, heels bouncing lightly`
- 来源:《骊山》06.0-08.0s(密帧段 05.3-08.2s)

### K161 胸前交叉摆臂荡裙链(3拍|手势舞·大动作)
- 入态:双手身前低握起势 → 出态:摆幅递减静止、头抬起眼神回镜头
- 分解:拍1 双手低握预摆,重心双脚间预移,头随节拍点两下;拍2 双臂胸前交叉成 X 再向两侧下甩(发力=肩带回旋),裙摆荡起 20-30cm 弧度,身体左右倾交替,峰值=甩开瞬间最大摆幅;拍3 惯性延续 双臂递减回摆两次,头发与裙摆滞后回落,双脚原地小垫步对拍,眼神回镜头
- H3:`crossing both arms in front of the chest and flinging them wide down on the beat, layered skirt and long hair swinging half a beat behind, settling back to center stance with heels bouncing`
- 来源:《骊山》02.4-04.7s

**片<v38> 《少女的真心》(宅舞·疑似 AI·15.0s·竖屏 4K60)**
- 背景人物:落地窗白纱帘房间,浅木地板,漫射日光。人物:少女(疑似 AI)——粉色双马尾长卷发+粉白蝴蝶结发饰,粉白 lolita 公主裙(泡泡短袖、胸前蝴蝶结、多层纱裙),白蕾丝颈带+腕套,白花边短袜+粉蝴蝶结玛丽珍。AIGC:疑似 AI 生成或重度 AI 美化(中高置信)——4K60 管线、全程零运动模糊、皮肤无毛孔纹理、腿部比例娃娃化橡胶质感、裙摆惯性偏弱、相邻帧五官与发量微漂移;手部五指正常未见崩坏。
- 节拍:(推测 120-128,宅舞弹跳步频)
- 镜头形态:A 一镜到底。

### K162 递掌双推弹跳链(4拍|AI 宅舞·弹跳步)
- 入态:双臂内收交叉于胸前 → 出态:双掌前推至肩宽、指尖上翘,踮脚尖弹跳停稳
- 分解:拍1 双臂向内收拢交叉(承接上组),双脚并拢跟弹,帧面无运动模糊(AI 特征);拍2 双前臂上翻、掌心朝上自胸前递出如捧物,肘先动腕跟随,重心右脚弹跳移至左脚尖点地;拍3 双掌前推至肩宽,峰值=推掌到位与踮脚同步,粉纱裙摆以弱惯性上扬(物理偏轻);拍4 回收 翻掌朝内收回胸口,下巴微抬看镜头,脚跟落回
- H3:`offering both palms up from the chest and pushing them forward at shoulder height on a pointed-toe bounce, the pink tulle skirt lifting with unnaturally light inertia, chin rising to the lens on the recover`
- 来源:《少女的真心》05.0-06.6s

### K163 高举 V 臂摇摆链(3拍|AI 宅舞·微活性)
- 入态:双臂自胸口沿体侧上举 → 出态:右臂先落、左臂画弧后落,头随倾 10°,双脚开立重心移交
- 分解:拍1 双臂举至头顶成 V,肘伸直过程有 2 段角度停顿(帧间跳变,AI 插值痕迹);拍2 双腕带动手掌同步摆浪、髋反向摆,张嘴跟唱口型,马尾发簇摆幅偏弱;拍3 回收 右臂先落左臂画弧后落,头部随落臂方向倾倒 10°
- H3:`raising both arms into a high V and waving the hands side to side with counter-swaying hips, mouth open singing, arms descending with slightly interpolated pauses, twin tails lagging weakly`
- 来源:《少女的真心》07.5-09.2s

**片<v39> 《春诗》(AI 氛围写真混剪·44.7s·竖屏 4K60)**
- 背景人物:约 12 个场景轮换——画室(灯串/颜料架)、窗边卧室、木地板坐垫区、面包房柜台、衣帽间(红外套)、花园绿植白花、老钢琴房、夜景街道栏杆。人物:黑发凌乱短发少女(AI 同一角色):白 T+军绿背带裤(颜料渍、画笔、脸颊蓝颜料痕)→灰吊带+工装短裤+白头戴耳机→米色睡衣→灰蓝毛衣→米色卫衣+陶杯→红色棒球外套+白吊带(高马尾)→灰绿背带裙+满天星花束→泡泡袖衬衫(弹琴)→针织开衫+深灰长裙(街拍)。AIGC:AI 生成(高置信)——UP 主水印"月亮熊猫AI / Λ MoonPanda Production",跨场景发际线与耳型微漂移,光斑粒子恒定飘散,皮肤过度均匀。
- 节拍:(推测 70-85 慢板,视觉无强拍对齐)
- 镜头形态:C 快剪(约 12 场景,含叠化与虚焦转场)。

### K164 逆光回眸抬颏眼神链(4拍|AI 氛围写真·微活性)
- 入态:身体 3/4 背对镜头,左手持画笔垂放,面部被刘海遮 1/3 → 出态:头停 3/4 位,双眼自刘海下缘全露,下巴抬 1-2cm,慢眨一次
- 分解:拍1(大姿势锁死)背身 3/4、左肩松垂,画笔尖朝下(手始终有任务),短发逆光轮廓光全开,光斑背景;拍2 微活性 头绕纵轴向镜头缓转 40°,眼球先于头型对上镜头,光斑在脸颊滑动;拍3 主动作 下巴上抬 1-2cm、颈线抬升刘海露出双眼,嘴角 2mm 微笑起步,持笔腕轻旋 10°;拍4 回收 眼睑慢眨一次再睁开,蓝色颜料痕入画,头角定位
- H3:`turned away in paint-splattered overalls with a brush hanging from one hand, rotating the head over the shoulder until the eyes catch the lens from under messy bangs, chin lifting one breath, slow double blink in warm backlight`
- 来源:《春诗》00:00-02.4s

### K165 原地转身甩衫回眸链(4拍|AI 氛围·服装物理)
- 入态:背对镜头立于窗边柜前,米白衬衫滑落至双肘 → 出态:3/4 站姿,衬衫半挂右肩,右膝微屈,过肩回眸
- 分解:拍1 背身站立,颈后发际与白色耳机头带可见;拍2 主动作 左脚为轴原地左转 180°,右臂外张平衡,发力=躯干扭转,峰值=衬衫下摆与发梢甩至水平最高点;拍3 惯性延续 衬衫回落但一袖停挂肘弯,头发甩过脸再落,耳机线在胸前划弧;拍4 回收 右膝弹一下,头过右肩回眸对镜头,衬衫重新半挂右肩;镜头轻微手持下沉跟焦
- H3:`spinning 180 degrees on the left foot by a window counter, the cream shirt flying off the shoulders and settling half-hung on one elbow, white headphones swinging on their cord, ending in an over-the-shoulder gaze with a soft knee bounce`
- 来源:《春诗》06.2-07.8s

### K166 花束递镜微笑链(4拍|AI 氛围·POV)
- 入态:双手捧满天星于胸口,头右倾 15°,碎发拂面 → 出态:花束推至镜头前虚化占下 1/3,露齿笑峰值,头倾 20°
- 分解:拍1(锁死)捧花于胸、头右倾 15°,背景绿植白花虚化、光斑粒子飘;拍2 主动作 双肩前推+躯干前倾 5°,花束由胸位升至占满下 1/3 画面;拍3 微活性 花停在近焦点外虚化,手指再收紧一次花纸,头倾至 20°,笑容由抿转露齿(表情峰值);拍4 回收 花降 5cm 露全脸,风将发丝吹过右眼,眼神在花与镜头间往返一次
- H3:`thrusting a bouquet of baby's breath from the chest toward the lens until the flowers blur into the lower frame, smile blooming from pressed lips to teeth, head tilting twenty degrees with hair blowing across one eye`
- 来源:《春诗》28.0-31.2s

**片<v40> 《春日列车》(JK 写真分镜·24.8s·竖屏)**
- 背景人物:日式高架站台(玻璃顶棚、黄色盲道砖、蓝色站牌、白色通勤电车)+车厢内(金属长椅、拉手吊环、行进窗外绿荫)。人物:金发双马尾少女(JK cos):白长袖衬衫+深蓝水手领背心裙(胸前红丝带结+藏青百褶裙),黑过膝袜+棕乐福鞋,粉色卡通印花头戴耳机。实拍可能性较高(站台盲道、车门反射、站牌细节跨帧一致,行走帧有真实运动模糊;判定为重美颜/氛围调色)。
- 节拍:(推测,环境音+轻音乐,无强对拍动作)
- 镜头形态:C 快剪(月台背影/戴耳机特写/低机位脚部/车厢坐姿≥5 镜)。

### K167 月台背身戴耳机链(5拍|JK 写真·分镜)
- 入态:背身向月台纵深行走,右手拎粉耳机于髋侧 → 出态:头带落位,双手指腹捋完双马尾垂回体侧,切低机位脚部静帧
- 分解:拍1 背身走两步远离镜头,百褶裙随步幅开合,右手拎耳机,电车自左侧滑过形成横向遮挡(全身背拍+车体前景);拍2 停步立定,双手举耳机至头顶张开头带;拍3 头带扣入双马尾之间,双手沿头带左右各捋一次,发梢被压出弧度;拍4 微活性 左右各调 5° 松紧,指尖顺马尾捋至发尾;拍5 回收 双手落回体侧,头微低再抬,硬切至低机位脚部静态(盲道砖纹前景)
- H3:`walking away from camera on a sunlit platform, stopping, lifting pink headphones over two blonde twin tails and seating the band with small fingertip adjustments before hands fall back to the sides`
- 来源:《春日列车》00.8-03.6s

### K168 车厢垂眸抬眼链(3拍|JK 写真·微活性)
- 入态:坐姿锁死,双手交叠于膝,头垂向左下、眼睑低 → 出态:视线逐节抬至镜头,头跟转 10°,手指重新交叠
- 分解:拍1(锁死)双膝并拢、双手交叠膝上,头垂左下;窗外绿荫光斑流动(列车行进);拍2 微活性 眼睑缓慢抬起,视线先落前下方再逐节上移入镜头,头部跟转 10° 且滞后于眼球;拍3 微活性 拇指换位重新交叠一次,嘴角 2mm 弧度,躯干随车厢晃动 1-2cm 被动位移
- H3:`seated by a moving train window with hands stacked on the knees, lifting the gaze gradually from downcast to the lens while the head follows ten degrees behind, re-stacking fingers and letting the carriage sway the torso`
- 来源:《春日列车》18.4-21.6s

**片<v41> 《Heli 贵气纱裙》(婚纱品牌展示·13.9s·竖屏 4K)**
- 背景人物:欧式样板间——米金色暗纹壁纸+护墙板,灰白理石地面黑色菱形拼花,水印"MANLIBRIDAL 娜纱"。人物:棕发低髻编发女模特——白色单肩斜肩珠纱礼服(立体褶纹压纱上身+透纱裙罩+开衩,单肩垂白纱长披),珍珠耳钉,白色软底鞋。实拍(透纱层双腿折射关系、大理石倒影、拖尾纱物理跨帧一致;叠化为后期转场)。
- 节拍:(推测 60-70,展示慢节奏)
- 镜头形态:C 快剪(正面行进/背身辫/转身/压褶特写/自抱定帧,含叠化)。

### K169 透纱前行捏纱停驻链(4拍|婚纱写真·服装物理)
- 入态:全身正面朝镜头缓步,裙尾拖大理石地面 → 出态:停步 3/4,右腿顶纱成前凸弧,右手捏起大腿处纱面 3cm,下巴垂、眼先入镜
- 分解:拍1 正面缓步 2 步,右腿自透纱裙罩中跨出(纱内腿型可见),裙尾拖出涟漪,构图柱线居中对称;拍2 第三步加大,纱罩被腿顶出前凸弧度,拖尾滞后半拍滑行,单肩纱带随步颤(纱双面折射+拖尾延迟);拍3 停步重心落右腿,左膝穿纱顶出小弓形,右手收拢捏起大腿处纱面提 3cm;拍4 微活性 下巴垂 10°、眼球先上抬入镜头(眼神先到头后到),指尖捻动纱丝一次
- H3:`walking toward the lens in a one-shoulder sheer-tulle gown that trails on marble, stopping to press one knee through the tulle and pinch the fabric at the thigh, chin dropping while the eyes rise to the lens first`
- 来源:《贵气纱裙》00.4-03.0s

### K170 沿纹压褶滑手自抱链(5拍|婚纱写真·微活性)
- 入态:近景 3/4,双手指腹落于胸前褶纹两侧 → 出态:左臂横抱肋侧、右手指卷收在锁骨窝,头转左侧脸垂头定帧
- 分解:拍1 双手指腹落在立体褶纹两侧(叠化转入),膝顶纱维持;拍2 双手沿褶纹下滑至髂骨,指尖引导掌根随后,身体侧倾 5°、肩线一高一低;拍3 峰值 双手停髋骨外侧、肘外撑成 V,下巴回收、目光自下睫毛上缘入镜;拍4 转位 左臂横抱肋侧(自我环抱),右肘抬高、指卷收于锁骨窝;拍5 回收定帧 头转左侧脸再垂头,视线落左下方,肩后纱披垂坠不动
- H3:`sliding both hands down the ribbed drapery of a couture gown from underbust to hip crests, flaring the elbows into a V, then crossing one arm under the ribs with the other hand curled at the collarbone into a left-profile chin-down pose`
- 来源:《贵气纱裙》05.8-09.2s

**片<v42> 《东京夜舞》(cos 宅舞·22.9s·竖屏 4K60)**
- 背景人物:夜间室外建筑前空地——灰石材墙、绿篱、三柱暖光景观灯(标题"东京街头漫步"实为夜景摆拍地)。人物:银紫短发波波头少女(cos,黑发夹):白色挂脖礼服裙(领口黑色大蝴蝶结+白色短披肩+白蓝高低裙摆、蓝色缎面衬裙),白色腕套,黑连裤袜+白厚底鞋;片尾背身可见背部蓝色蝴蝶结、披肩罩头。实拍(夜景高感光、行走/踢腿运动模糊真实,缎衬惯性正常)。
- 节拍:(推测 120-128,宅舞拍频)
- 镜头形态:A 一镜到底(手持固定机位,开场虚焦拉焦)。

### K171 入场摆裙滑步链(3拍|cos 宅舞·裙撑物理)
- 入态:虚焦光斑中拉焦入像,高低裙行走中蓝色缎衬左右甩 → 出态:并步立定,缎衬两次递减摆幅落定,眼神入镜
- 分解:拍1 焦点自前景光斑拉至人物(呼吸感拉焦),白面蓝衬高低裙行走,缎衬随髋左右甩出 30-40cm 弧,黑连裤袜双腿走直线,机位固定;拍2 双手自裙侧半提裙缘,走改侧向 step-touch 滑步,衬裙甩至最高点(峰值);拍3 回收 放下裙缘,缎衬 2 次递减摆幅落定,右脚并步立定、眼神入镜
- H3:`walking into focus at night in a high-low white dress with blue satin lining, sweeping the lining side to side with a step-touch slide, then letting the flare settle in two shrinking swings into a ready stance`
- 来源:《东京夜舞》00.4-03.6s

### K172 出拳顶髋踢腿链(4拍|cos 宅舞·节拍链)
- 入态:双拳轮替上顶至肩侧、膝弹跳对拍 → 出态:踢腿落并步,手臂收回胸前小拳,头点拍两次收势
- 分解:拍1 双拳轮替上顶("加油泵")、肘外撑,膝盖弹跳对拍,髋随出拳侧顶;拍2 双拳外旋展臂成掌心向前"停掌",重心移左,马尾与裙衬反向延迟;拍3 主动作 右膝提踢、绷脚尖过身前中线,双臂向身后摆,峰值=踢腿顶点与臂后摆同步;拍4 回收 腿落并步,臂收回胸前小拳,头点拍两次收势
- H3:`pumping both fists at shoulder height with hip pops on the beat, opening the arms into palm-out pushes, kicking one pointed toe across the midline while the arms swing back, landing closed with two head nods`
- 来源:《东京夜舞》09.8-13.2s

**片<v43> 《Rather Be 小提琴》(器乐演奏·21.0s·竖屏 4K)**
- 背景人物:灰色水泥墙琴房,挂三张水彩音符装饰画,黑色吸音板、木地板,固定三脚架正面机位。人物:黑长直发+齐刘海,右侧奶油色小熊发夹,雪纺碎花衬衫(泡泡袖、木耳领),浅蓝牛仔背带裤,绿松石串珠手链+细银项链;道具小提琴+琴弓。实拍(60fps 原生运动模糊、琴体反光连续、手指按弦合理)。标签纠偏:标题为《Rather Be》但内容为小提琴演奏而非翻跳。
- 节拍:约 121 BPM(推测,与原曲相符,全弓周期约 0.8s)。
- 镜头形态:A 一镜到底(18.0-19.5s 收琴走近镜头关机,19.5s 后空镜)。

### K173 持琴回旋甩发入场链(2拍|小提琴·开场·长发)
- 入态:正面低举琴站立(左手垂琴、右手持弓侧摆) → 出态:回正面对镜头、长发落肩、微笑准备架琴
- 分解:拍1 头部先导向其左侧带转、肩胯随后做俯视逆时针原地回旋,长发滞后半拍向右横扫过肩(峰值遮住半脸),琴与弓全程不脱手,背对镜头瞬间长发呈扇面展开;拍2 借转体惯性别甩补完 360°,发梢向回摆拢过面,身体微前倾、抬手拨发,裤摆随转身外张后回收
- H3:`leading a full counterclockwise spin with her head while the waist-length hair lags half a beat and whips across her face, violin and bow held low through the whole turn, hair settling back over her shoulder as she snaps to camera smiling`
- 来源:《Rather Be 小提琴》00.0-02.6s

### K174 举琴上肩架弦链(2拍|小提琴·过渡)
- 入态:琴垂左体侧、弓持右手低位 → 出态:琴托肩、下颌扣腮托、弓搭弦起奏
- 分解:拍1 左臂把琴自体侧弧线上提至左锁骨,头部右倾以下颌迎腮托,右臂同步把弓自下方横抬过身前;拍2 弓落弦、左腕内旋手指按弦,肩-颌-手三点支撑成型,重心微右移站定,残余发摆收止
- H3:`raising the violin in a left-hand arc onto her collarbone, tilting the jaw into the chinrest as the right arm sweeps the bow across to land on the strings`
- 来源:《Rather Be 小提琴》03.0-04.6s

### K175 全弓快弓摆体演奏链(2拍循环|弦乐·技术峰值)
- 入态:架弦完成、直立站姿 → 出态:连续分弓中、躯干随弓行左右微摆
- 分解:拍1 右肘开合驱动全弓下行至弓尖,肩带前送,左手指法换把,躯干随弓向右倾约 5°;拍2 弓折返上行全弓,肘关节收拢回落,重心回中向左让摆,快弓段(13.4-14.6s)改腕指主导短分弓,弓杆与手臂出现原生运动模糊,视线在谱与镜头间切换
- H3:`driving full detache bow strokes with elbow lead while the torso sways into each direction change, the left hand shifting positions on the fingerboard, quickening into wrist-driven short strokes with visible motion blur`
- 来源:《Rather Be 小提琴》12.4-14.6s(同型动作遍布 05-17.5s)

**片<v44> 《李珠珢中场舞》(富邦悍将啦啦队现场·86.6s·竖屏)**
- 背景人物:棒球球场内场高架舞台(富邦悍将主场,夜场),满座看台、护网入镜、舞台音箱与设备箱可见,队友浅蓝制服。人物:李珠珢——栗棕长直发+空气刘海,白色短袖翻领衬衫+格纹领带,卡其格纹百褶短裙(腰挂深蓝小包),白色过膝袜+白色运动鞋,入耳式耳返。实拍;后期字幕提示曲目段落切换(9 月 6 日/AOA 怦然心动/轻快)。
- 直拍特征:多机位实拍(护网低机位仰拍/侧杆机位/远景),单镜内无假剪。
- 节拍:130±8 BPM(推测;Heart Attack 段偏快,轻快段稍慢)。
- 镜头形态:C 快剪(多角度切换)。

### K176 坐姿回眸甩发链(2拍|啦啦队·签名·长发)
- 入态:坐于台沿后仰撑手、双腿屈膝抬起、侧脸朝场内 → 出态:正脸对镜头、长发甩过肩落定、歪头笑
- 分解:拍1 头部自左侧向镜头方向回转,长发滞后沿弧线自背后横扫至胸前(峰值盖脸),撑地双手与核心稳定不动,屈膝腿保持上抬;拍2 发梢甩尽回摆至肩后,下巴微抬收势,肩部小幅耸动配笑,身体随台沿轻晃
- H3:`turning her head back toward the camera so the long straight hair sweeps in an arc across her face from behind, planted hands keeping the seated lean stable, the hair settling over one shoulder into a tilted-head smile`
- 来源:《李珠珢中场舞》00.0-01.3s(复现 00:60.0-61.5s)

### K177 抚腿起身大摆臂链(3拍|啦啦队·Heart Attack 段)
- 入态:并膝微蹲、手抚大腿 → 出态:直立、双臂交叉抱肩收势
- 分解:拍1 双手沿大腿下滑抚过裙摆至膝,脊柱逐节前卷、膝内扣并拢(百褶裙随下蹲收拢);拍2 双手贴身线上提经腰至胸,脊柱逐节立直、头最后抬起,双腿伸直重心升高;拍3 左臂向上大开过头顶外划后落,身体后仰再前倾,双臂于胸前交叉抱肩,重心下沉半拍,长发随起身反向甩动
- H3:`gliding the palms down her thighs as the spine rolls into a knee-together dip, undulating back up with the hands tracing up the body, one arm slicing overhead before both arms cross over the chest in the signature pose`
- 来源:《李珠珢中场舞》14.0-17.5s(同型 18.5-20.5s 提膝踢腿延续)

### K178 躬身甩发环绕背靠背链(4拍|啦啦队·双人·技术峰值)
- 入态:站立侧身、右手举至脸侧 → 出态:与队友背靠背、双臂外划镜像摆动
- 分解:拍1 右手在脸侧挥动致意,左膝点提,发随动作右摆;拍2 上身前躬近 90°、整头垂直下甩,长发完全覆盖面部呈瀑布状,双手落向膝盖方向;拍3 直身仰头起,长发自面部向后整体翻越头顶抛至背后,惯性峰值呈横向环状扇面,双臂顺势上扬;拍4 头部左右快摆两次令长发水平环绕,右转体与队友背靠背贴靠,双臂外划镜像波浪,裙摆随转身外张
- H3:`bowing forward to whip the hair straight down into a face-covering curtain, snapping upright so the hair flips all the way back over the crown in a horizontal halo, shaking the head side to side to keep the hair fanned mid-air before backing into a back-to-back duet with her teammate`
- 来源:《李珠珢中场舞》33.5-37.5s

**片<v45> 《打起手鼓唱起歌》(新疆舞翻跳·21.0s·竖屏 4K)**
- 背景人物:夜间城市桥下人行道,砖铺地面、白色桥栏、路灯,社会车辆不时驶过(车灯与湿路面反射时序连续)。人物:深色低髻中分,矢车菊蓝长袖针织上衣,白色高腰阔腿裤,黑白条纹围巾双垂尾,白色板鞋。实拍(围巾/裤摆物理自然、过车与反光连续、标准新疆舞语汇绕腕/移颈/托帽式/点步转身,非 AI)。
- 节拍:约 112 BPM(推测,2/4 欢快)。
- 镜头形态:A 一镜到底(固定机位正面全身,夜景)。

### K179 绕腕托帽移颈链(3拍|新疆舞·翻跳)
- 入态:开立站姿、右手抬至肩侧 → 出态:左手叉腰、右手曲臂于眉前托帽式、颈部侧移定势
- 分解:拍1 右腕由内向外连续绕环,指尖立起带动小臂,头随腕行微侧,重心移至右腿;拍2 右臂折上举过顶做翻腕压腕,左脚侧点步、左胯外顶,围巾双尾随臂摆起落;拍3 左手收落叉腰,右手曲肘收至眉骨上方成托帽式,颈部左右横移两下(移颈),肩位锁定,视线随头
- H3:`rolling the wrist outward in continuous circles that lift the arm overhead with a wrist flick, planting one hand on the hip while the other folds into the brow-height hat-hold pose, sliding the neck side to side Uyghur-style as the striped scarf tails swing`
- 来源:《打起手鼓唱起歌》03.0-05.5s(同型 00.0-02.5s、18.5-20.5s)

### K180 连环转身链(4拍|新疆舞·旋转·围巾物理)
- 入态:双前臂于胸前平交、开立 → 出态:转体回正、右臂上举曲肘定势
- 分解:拍1 双臂胸前平举后拧腰启动 360° 回旋,后脚插步,围巾两端离肩上扬拖后;拍2 旋转过背对位时双臂上折举至头后(围巾自背后扬起过肩),再转经侧位双臂收落横扫;拍3 回正瞬间右手下撩过胸、左手叉腰、胯侧顶做半拍停顿;拍4 右手翻腕上举引身再转,左膝提至腰高点步旋转,阔腿裤摆随转外张,落步开臂收势
- H3:`launching into a chest-level full spin with both scarf tails lifting off the shoulders mid-turn and the arms folding overhead at the back-facing peak, then chaining into a knee-lifted pivot turn with one wrist rolled high before opening the arms to land`
- 来源:《打起手鼓唱起歌》07.8-09.0s(拍 1-3)、15.5-17.0s(拍 4;同型 10.3-11.0s)

**片<v46> 《银月画本》(宫斗演绎口播·22.8s·竖屏)**
- 背景人物:室内木地板,藤编柜+全身镜(镜中背影入画),暖光。人物:黑色长直发,哭妆(眼尾红润挂泪光),黑色一字肩挖肩连衣裙,银手链+戒指,领夹麦入画;道具白狐玩偶"银月"(黑色耳尖、蓝绿异瞳)——与库内片 v13《我是银月呀❤》同一角色新片。兽耳/尾巴说明:本片狐耳为玩偶道具,无独立延迟物理,仅整体受压变形、随抱持移动。实拍(领夹麦、镜面反射、玩偶形变与手指持握自然)。
- 节拍:无固定 BPM(口播断句约 1-2s/句)。
- 镜头形态:A 一镜到底(固定机位高角度俯拍,腰上构图)。

### K181 抚泪哭诉链(3拍|宫斗演绎·哭妆)
- 入态:跪坐、左手搭狐偶、右手捏指于鬓角 → 出态:手落膝上、含泪仰视镜头
- 分解:拍1 右手指尖自右鬓角沿眉骨下滑至颧骨拭泪,头随手右倾,肩微耸,口型持续诉词;拍2 手回鬓角小圈打转第二次,头部轻摇(委屈摆头),跪姿重心后移;拍3 手垂落搭膝,下颌内收后仰眼看镜头,睫毛颤动收势
- H3:`dragging her fingertips from the temple down the cheekbone in a slow tear-wiping stroke while tilting her head, repeating the gesture in a small circle with a grievance head-shake, then dropping the hand to her knee and lifting teary eyes to the lens`
- 来源:《银月画本》00.0-02.5s(同型 04.0-08.5s)

### K182 拾狐抱胸贴脸链(3拍|宫斗演绎·玩偶物理)
- 入态:双手垂拾地上狐偶 → 出态:狐偶贴胸、面颊压偶顶、破涕一笑
- 分解:拍1 双手自地面捧起狐偶至胸口,肘内收把偶体压进怀里(玩偶受压贴胸变形);拍2 头前倾以下颌/面颊压上偶顶,发丝顺肩前垂,肩胛内合做两次小幅安抚式摇晃;拍3 抬头直视镜头渐转微笑,一手轻抚偶头,末帧咧嘴笑收
- H3:`scooping the white fox plush off the floor and squeezing it into her chest so the plush visibly compresses, pressing her cheek down onto its head with two small soothing rocks, then lifting her face into a slow breaking smile while stroking its head`
- 来源:《银月画本》09.4-12.0s(拍 1-2)、20.8-22.3s(拍 3)

**片<v47> 《这舞真有力气》(宅舞·15.1s·竖屏 4K)**
- 背景人物:会展中心室内,水泥地面、玻璃幕墙、蓝白格背景板,保安与围观摄影者入景。人物:棕色长卷发钻卷双马尾,白色蕾丝发箍+兔耳缎带,黑白经典 Lolita JSK+白围裙蕾丝边,大黑领结+皇冠徽章,白色毛绒腕套,白色过膝袜,黑色厚底玛丽珍,腰侧黑缎带垂尾。实拍(磨皮偏重属美颜滤镜,非 AIGC)。
- 节拍:约 128 BPM(推测,0.47s/拍)。
- 镜头形态:A 一镜到底(手持跟摇,构图随舞步横移微调)。

### K183 猫爪抬膝踏步链(2拍|宅舞·漫展·Lolita)
- 入态:并步站立、手垂于侧 → 出态:猫爪手落、单膝高点后踏步回位
- 分解:拍1 一手五指张开摆至颊旁做猫爪腕部小抖,同侧头倾,对侧膝屈提至髋高绷脚下悬,裙摆向提腿侧掀起,钻卷双马尾与兔耳缎带以约 0.2s 延迟跟摆;拍2 踏地反弹小跳,猫爪手收回与另手胸前合拍轻碰,裙摆荷叶边回落,恢复并步
- H3:`popping one hand beside her cheek in a wiggling cat-paw while the opposite knee hikes hip-high with a pointed toe, bouncing the step down into a small hop as the drill twin-tails and headdress ribbons swing a fraction of a second behind, skirt hem flaring with each lift`
- 来源:《这舞真有力气》04.0-05.5s(同型 00.5-02.5s、10.0-10.5s)

### K184 宽站摆胯收拳定格链(3拍|宅舞·技术峰值)
- 入态:宽站微蹲、重心中置 → 出态:食指点太阳穴、歪头定格
- 分解:拍1 双膝弹动下蹲蓄力,单手掌心向上向斜前横扫,胯随重心侧移顶出,裙撑整体向同侧甩出荷叶边浪;拍2 双手交替向下捶收至腰侧,胯回摆,上身随弹跳起伏两次;拍3 双拳自胸口向两侧上击再收至肩,末拍单手食指点向太阳穴、对侧髋同步弹出,歪头 wink 定格
- H3:`bouncing in a wide-stance squat while sweeping one palm across and popping the hip side to side so the petticoat throws ruffle waves, pumping both fists up from the chest, then freezing on a temple-point with a head tilt and wink`
- 来源:《这舞真有力气》09.0-10.0s(拍 1-2)、14.2-15.1s(拍 3)

**片<v48> 《韩立代为师看看》(口播+快剪混排·22.5s·竖屏 4K)**
- 背景人物:开场=米色竖褶幕布前真人(红色短款开衫+红白条纹吊带+奶白花边高腰裤,深色长发),手持"我永远喜欢…"评论梗图板(板面含两张古风人像缩略);3.0s 起=约 16 张古风美人定帧快剪(凡人修仙传女性角色向:紫纱、银蓝、绿衫、执伞、黄绿抹胸、红衣、黑袍等造型)。AIGC:混合——开场段实拍;后半定帧中部分为 AI 生成像(肤质过度均匀+塑料感高光、发丝与背景交界涂抹、瞳形轻微不对称、服饰纹理局部液化,粉/绿配色两张最明显),其余为真实 cos 摄影。
- 节拍:剪辑卡点约 1.1-1.3s/切(约 48-54 BPM 剪辑率;BGM 未核听)。
- 镜头形态:C 快剪(1 个实拍镜头+定帧轮播,画内轻推近/横移)。

### K185 转身递板链(2拍|口播·道具展示)
- 入态:侧身四分之三背对镜头立于幕布前 → 出态:正面对镜、梗图板平举胸前偏左、展臂完成展示
- 分解:拍1 自侧身位置向左转正面对镜头,板子先于身体入画,手臂把板横举胸前;拍2 另一臂向外展开做展示手势,肩线摆正,板面朝镜停留约两拍半,头微歪配合口播,末拍收臂板下移出画(3.0s 硬切入快剪)
- H3:`turning from a three-quarter back stance to face the camera as the meme board swings into frame first, spreading the free arm wide in a presentation gesture and holding the board toward the lens with a head tilt before the hard cut`
- 来源:《韩立代为师看看》00.0-03.0s

### K186 快剪卡点翻图链(4拍|快剪·AI 图混排)
- 入态:开场末帧(板下移出画) → 出态:末张美人定帧后黑场
- 分解:拍1-4 硬切串接约 16 张古风美人定帧,每张停留约 1.1-1.3s 并带轻推近或横移(Ken Burns),切换点卡乐句重拍;图源混合真实 cos 摄影与 AI 生成像,无真人连续动作,镜头几何=画内虚拟运镜+硬切,人物全为胸上近景
- H3:`hard-cutting through a rapid slideshow of guofeng portrait stills, each held about 1.2 seconds with a slow push-in or lateral drift timed to the phrase downbeats, mixing cosplay photos with AI-generated beauties in chest-up framing`
- 来源:《韩立代为师看看》03.0-22.5s(实测切点 07.7/08.8/09.7/10.7/11.8/12.9s,间隔约 1.1-1.3s)

**片<v49> 《成都 KDC 路演》(多人齐舞饭拍·15.0s·竖屏 4K)**
- 背景人物:商场中庭路演舞台,紫色背板印大号字母与"群光广场"横幅,地面紫底白色斑马线条纹(马路主题),白色射灯。舞者 4-5 人轮换居中:A 黑色无袖收腰蓬裙+白色欧根纱内层+白色红底细高跟、半扎黑长发、珍珠项链耳坠;B 白色花瓣层叠吊带短裙、裸色防水台高跟、黑长直;C 黑色无袖百褶蓬裙、黑色漆皮防水台高跟、棕色大波浪;D 白色缎面束身吊带上衣+粉色荷叶边蓬蓬短裤、黑框眼镜、裸色高跟;E 黑色连衣裙+黑漆皮高跟(部分入镜)。无成员名字幕,元子/kuank/开开/呆萌与具体人对应无法从画面证实,按服装代号记录。实拍(手持现场感、遮挡与服装物理自然;UP 主水印"骂版村夫 bilibili")。
- 直拍特征:0-5.3s 黑纱裙 A → 5.0-6.5s 粉短裤 D → 6.7-9.3s 波浪发 C → 9.3-11.7s 黑裙白跟鞋 E → 12.0-14.9s 白裙 B,群舞同步处多时间码合并。
- 节拍:约 126 BPM(推测,按踏步/手势落点)。
- 镜头形态:A 一镜到底(手持横移跟拍,人物保持中央)。

### K187 抬膝踏步行进链(3拍|dance-formation)
- 入态:双人纵队行进、右膝已抬 → 出态:行进至舞台中区、踏步未停
- 分解:拍1 右膝高抬过髋、脚背绷直下点,重心全压左腿,大腿前侧发力上提,双臂自然下垂随步伐前后小摆,下颌过肩回望镜头,黑裙白纱内层随抬腿掀动;拍2 右脚落地瞬间左膝接力抬至同高,双臂反向摆,白纱随换腿荡出,躯干立直仅随步幅微沉;拍3 连续交替抬膝向画面右侧行进,接一次脚跟后踢过渡(红鞋底闪出),镜头同步横移跟住中线,落拍踩重拍
- H3:`marching in line with high knee lifts and pointed toes while the arms swing loosely and she glances back over her shoulder, trading legs on each beat with the white tulle underlayer bouncing under the black skirt, then flicking both heels back into a light traveling jog`
- 来源:《成都 KDC 路演》0-2.0s

### K188 后踢跑位接提膝收拳链(4拍|dance-formation)
- 入态:侧向行进中 → 出态:站定、双拳抵腰、面向镜头
- 分解:拍1 脚跟交替后踢向臀部(鞋底红底高频闪出),小腿后侧发力,双臂自然后摆,身体略前倾向右行进,波浪长发随步频弹跳;拍2 连续两次后踢后急停并步,双脚合拢屈膝下弹缓冲卸力,双手顺势收至裙腰;拍3 左膝向前高提至腰际,髂腰肌发力快提慢放,躯干后仰对冲,双拳收抵腰侧,张嘴对口型;拍4 落膝胯向右顶送,头回正,惯性余摆一拍内收住
- H3:`jogging sideways with heels flicking back toward the hips and arms trailing, halting into a feet-together knee bounce, then popping one knee up to waist height while both fists pull into the waistline and the torso leans back against the lift`
- 来源:《成都 KDC 路演》7.0-8.8s

### K189 抵腰扭胯原地后踢收尾链(4拍|dance-formation)
- 入态:队形归位、双拳已收腰侧 → 出态:并脚定拍、拳留腰侧
- 分解:拍1 双拳屈臂抵住腰侧,胯部画小八字左右扭摆(腰腹带动,膝微屈弹),10.7-11.7s 由黑裙白跟鞋成员居中示范;拍2 换为原地交替后踢:右脚跟后踢向臀,站立腿随节拍微弹,双拳不离开腰位,12.6-13.5s 白裙成员同拍复刻(重复动作合并标注);拍3 换左腿提膝前抬,躯干保持立直,双人动作同步率达帧级;拍4 收势并脚,胯回正定拍,全片在此姿势附近收束
- H3:`holding both fists against the waist while twisting the hips in a small figure-eight, then kicking each heel back toward the seat in place on a bouncy standing leg, alternating front knee lifts in sync and settling into a final feet-together posed stance`
- 来源:《成都 KDC 路演》10.7-14.5s(12.6-14.5s 为 6fps 密帧证实)

**片<v50> 《这么可爱 应该不会咬人吧？》(小恶魔 cos 独舞·14.5s·竖屏)**
- 背景人物:室内练习室/走廊,浅灰米色方格隔断墙板+浅米色地板,顶光均匀。人物:银白色及腰长直发齐刘海,黑色蕾丝蝙蝠翼发箍(兽耳状双耳位),肩后一对黑色膜质蝙蝠翼装饰,黑色漆皮抹胸多层欧根纱蓬蓬裙(白色腰带扣),黑色颈链,右臂过肘黑色蕾丝长手套,双侧黑丝大腿袜带吊带袜扣,黑色厚底蝴蝶结玛丽珍鞋。水印"糕小一 bilibili"。实拍(纱裙褶皱、手套网眼、动态模糊均自然)。
- 节拍:约 120 BPM(推测)。
- 镜头形态:A 一镜到底(固定机位全身,无运镜)。

### K190 恶魔爪手开场链(3拍|dance-cosplay)
- 入态:双脚前后交叉站定、右手蜷爪收在锁骨前 → 出态:宽站屈膝、V 臂定格
- 分解:拍1 右爪手向前下方挥出展开,五指从蜷到张,同时右脚撤步打开至肩宽,双膝微屈下沉,腕部全程放松;拍2 左臂跟进从胸前向左下扫,躯干左倾,肩带转动让蝙蝠翼发箍与背翼完整露出,长发随转体从右肩滑向左肩;拍3 双臂向两侧上抬成 V、手腕下压指尖朝下模仿蝠翼,胯向左顶、左膝内扣,纱裙随重心横移荡向右侧
- H3:`starting from a crossed-feet stance with one hand curled like a claw at the collarbone, sweeping the clawed hand down and open as the feet spread wide, then raising both arms into a drooping-wrist V like bat wings while the hip pushes out and one knee caves inward`
- 来源:《这么可爱》0-1.8s

### K191 V 臂展翅抱头摆胯链(4拍|dance-cosplay)
- 入态:宽站直腿、双臂在体侧 → 出态:双手抱头、肘外扩、胯回中
- 分解:拍1 双臂从体侧向下压划收拢,胯向右撞顶一次(骨盆主动发力,脚跟不动);拍2 双臂直臂上甩成 V、手腕放松下垂,胯改向左顶,左膝弯右膝直形成对角线张力,背翼随胸腔上提弹动;拍3 双手回落绕至脑后抱头,肘尖外扩成框,胯部连续左右大摆两个八分拍,膝随摆动交替屈伸;拍4 纱裙纱层随摆荡起后回落,银发甩向摆动反方向产生延迟跟随,末拍半拍内收胯回中
- H3:`pressing the arms down past the hips with a sharp hip bump, throwing both arms up into a drooping-wrist V, then wrapping the hands behind the head with elbows flared and swinging the hips wide so the tulle skirt flares and the silver hair whips in delayed follow`
- 来源:《这么可爱》5.0-6.9s

### K192 猫爪弹跳拱臂收尾链(4拍|dance-cosplay)
- 入态:直立 → 出态:单臂拱顶、胯左顶定格
- 分解:拍1 屈膝内扣半蹲小弹跳两下(脚跟不离地,踝发力),双爪手蜷在胸前,头随弹跳点动,张嘴对口型;拍2 右爪手举至耳侧,左手按胸口,起身直立,肘部保持弧度;拍3 双手在肩前做爪形下按两下(腕带动指尖拍动,模仿猫爪),膝盖同步弹两下;拍4 左臂弧线拱过头顶、手腕下垂,右手贴胸,胯左顶膝内扣定格,银发与裙纱各晃半拍后静止
- H3:`bouncing in a knock-kneed half squat with cat-claw hands curled at the chest, lifting one paw beside the ear while the other presses the heart, tapping both paws downward twice, then arching one arm overhead with a drooping wrist and popping the hip to freeze`
- 来源:《这么可爱》11.5-13.5s

**片<v51> 《乱码 A·OL 舞》(OL 制服风格独舞·15.2s·竖屏·高度疑似 AIGC)**
- 背景人物:纯色浅米色墙面+白色踢脚线,无其他陈设,正面柔光。人物:棕色大波浪长卷发+空气刘海,蓝白细条纹衬衫(黑纽扣、卷袖至肘、胸口小徽标),黑色高腰紧身包臀短裙,黑色挂绳白色工牌(卡片文字不可辨),细项链。判定为舞蹈类依据:全程连续成套动作、卡点式膝弹与手势编排,非写真摆拍亦非口播。高度疑似 AIGC,依据:皮肤无毛孔级磨皮质感、工牌卡片为不可辨伪文字、腰臀比/腿长比例风格化理想化、发丝与肩线过渡局部发糊、720p/30fps 低规格+乱码文件名;置信度中高,不排除重度美颜实拍,动链仍按帧证提取。
- 节拍:约 128 BPM(推测)。
- 镜头形态:A 一镜到底(固定机位全身,无运镜)。

### K193 背身抖胯转体甩发链(4拍|dance)
- 入态:背对镜头、上身前倾约 30 度 → 出态:面向镜头、双拳收肩、定拍
- 分解:拍1 双手握拳收在胯两侧,胯部快速左右摆振(核心带动,膝深屈弹动),包臀裙随摆绷紧出褶,前 0-0.4s 为侧身高抬腿踏步进入此姿态;拍2 上身直起,双臂向两侧甩开伸展,裙摆回弹;拍3 以左脚为轴左后转体 360 度,手臂收拢减小转动惯量,长发随转身甩成大弧形延迟跟随;拍4 转正落地面向镜头,双拳收至肩侧屈肘,右膝弹一下,微笑定拍,发梢甩至脸侧后归位
- H3:`shaking the hips fast from a forward-hinged back view with fists at the hips and knees bouncing, rising to swing the arms wide, spinning a full turn so the long wavy hair whips around in a delayed arc, and landing facing the camera with both fists popped at the shoulders`
- 来源:《乱码 A·OL 舞》0.5-2.3s(0-0.5s 踏步进入段并入拍 1)

### K194 交替掌浪推拒手势链(4拍|dance-gesture)
- 入态:双手举在胸前、掌心相对 → 出态:双掌朝镜头摊开定格
- 分解:拍1 双手在胸前交替做横向"抹浪"(左手从右向左平抹,右手接力跟进),腕软掌平,肩随手动微转,膝部全程小弹;拍2 左手掌心朝外举至脸侧做"停"手势,右手同时向下拖掌至腹前,躯干左倾胯左顶;拍3 换右手掌心朝外推挡,左手收回胸前,胯回中,重心左右交接干净;拍4 双掌同时朝镜头摊开五指微晃两下(推拒/打招呼混合语),头歪向左肩,工牌随躯干摆动轻荡后静止
- H3:`rolling alternating palm waves across the chest like smoothing water, flipping one palm out beside the face in a stop gesture while the hip juts and the other hand drags down, trading hands, then pushing both spread palms toward the camera with a small wave and a head tilt`
- 来源:《乱码 A·OL 舞》12.0-14.4s(同族掌浪 9.3-11.7s 已出现,合并标注)

**片<v52> 《乱码 B·沙发》(坐姿写真手势短片·4.5s·竖屏·高度疑似 AIGC)**
- 背景人物:室内客厅一角,深灰布艺沙发,灰色外套搭在沙发背,米色抱枕,墙上挂鸟禽图案装饰画。人物:黑长直+空气刘海,白色缎面吊带紧身短裙,白色蕾丝袜口大腿袜(左右袜口不对称),红色细手链,心形吊坠项链。判定为摆拍/手势类依据:无位移、无舞蹈编排,仅上半身微动作与手势。高度疑似 AIGC,依据:皮肤完全无纹理蜡质高光、手指指尖边缘发虚、挂画鸟形解剖扭曲且细节随帧微漂、沙发外套褶皱"融化"感、足踝衔接模糊、4.5s 时长+乱码文件名(典型生成片段规格);置信度高,动链按帧证提取并仅供微动作参考。
- 节拍:无明确重拍(推测为慢速抒情/氛围乐)。
- 镜头形态:A 一镜到底(手持近景,缓慢漂浮感,疑似生成运镜)。

### K195 沙发抚胸歪头倾身链(2拍|gesture)
- 入态:沙发侧坐、双腿交叠、右手五指抚左胸 → 出态:前倾坐姿、手停腹前
- 分解:拍1 右手在胸口轻按揉两下(指腹发力、掌根不离身),头向右歪至肩,露齿笑,眼神直视镜头,长发从左肩整体滑落;拍2 右手沿胸口曲线下滑至腰腹,上身向镜头前倾,重心前移让吊带裙肩带轻微滑落半寸,红手链随腕部下移轻晃
- H3:`sitting cross-legged on the sofa with one hand resting on the chest, kneading it gently while tilting the head into a smile, then sliding the hand down to the waist as the torso leans toward the camera and the long hair slips off the shoulder`
- 来源:《乱码 B·沙发》0-2.3s

### K196 双掌摊开摇手拒接链(3拍|gesture)
- 入态:上身直起、右手已抬 → 出态:双掌朝镜头定格、微笑
- 分解:拍1 右手掌心朝镜头五指张开,手腕左右摆两下(摆幅小、频率快),肘部保持固定;拍2 左掌抬起与右掌并排,双掌同时朝镜头轻晃,指尖自然分开微颤,上身微前倾配合;拍3 双掌向内收半寸再向前推出做"推拒"收尾,头歪向左肩,惯性余晃半拍内静止
- H3:`raising one spread palm to the camera and waving it side to side, lifting the other palm to join it in a double wave, then pressing both hands forward in a soft push-and-hold while tilting the head onto the shoulder`
- 来源:《乱码 B·沙发》2.7-4.5s

**片<v53> 《躺踢变装》(氛围感变装·6.3s·竖屏)**
- 背景人物:暗灰沙发+条纹吸音墙。人物:黑棕大波浪+齐刘海,香槟金丝绸睡衣→黑吊带短裙+黑过膝袜带+红底高跟鞋+黑 choker。AIGC:真人实拍+重度 AI 美化,鞋部疑似 AI 重绘(鞋形帧间不稳)。
- 节拍:(推测)慢板 85-100,跳切点 1.8s。
- 镜头形态:A 一镜到底(高位俯拍 POV,1 处跳切变装)。

### K197 后仰踢腿遮帧跳切变装链(4拍|变装转场·POV 俯拍)
- 入态:沙发边缘坐姿、丝绸睡衣、右手撩发垂眸 → 出态:黑裙红底鞋、屈膝拱腿定格、鞋底朝镜
- 分解:拍1 双手交叠穿发向上撩,下巴垂 15°,肩胯沉进沙发,进入路径=从拨发的松弛态直接接重心后倒;拍2 右手滑到领口压住衣襟,躯干后倒 20°,右大腿启动踢腿(髂腰+股四头),裸脚掌迎镜头放大,运动模糊从踝部向小腿蔓延;拍3 技术峰值=脚掌糊满画面下 1/3 遮住躯干中段的瞬间(1.75s),跳切发生在此糊帧内:丝绸睡衣→黑吊带裙+过膝袜+红底鞋,腿部姿势角度精确延续(踢腿顶点=切点);拍4 落回屈膝拱腿姿,红鞋底正对镜头轻晃 2 次,回收顺序=腿定→手收至下巴→眼神最后入镜
- H3:`slouching on a dark fabric sofa in cream silk pajamas threading fingers through her hair, kicking one bare foot up at the lens so the sole blurs across the frame, jump-cutting mid-kick into a black slip dress and red-sole stiletto whose sole now faces the camera, settling into a knee-up recline with fingertips at her chin`
- 来源:《躺踢变装》00.0-02.0s(切点 1.75-1.875s)

### K198 膝拱红鞋底朝镜微活性链(3拍|定格摆拍·微活性)
- 入态:变装后屈膝拱腿姿 → 出态:同一构图收尾(眼神锁定镜头)
- 分解:拍1 大姿势锁死:后仰靠枕、右膝拱起、鞋底朝镜、左手托颌;微活性=鞋底以踝为轴左右倾旋 5-10°,两次露出鞋跟红底;拍2 托颌手指单次屈伸,下巴随眨眼微点,眼球先动头后动;拍3 发丝从肩头滑落一根、吊带肩带轻微回弹(过膝袜口随大腿转动轻微位移);02.0-06.3s 全程同构
- H3:`holding a knee-up recline on the sofa with the red sole of her stiletto facing the lens, rocking the shoe slowly at the ankle, one fingertip flexing at her chin while the eyes hold the camera and a loose hair strand slides off her shoulder`
- 来源:《躺踢变装》02.0-06.3s

**片<v54> 《选择题御姐》(卡点变装舞·6.1s·竖屏)**
- 背景人物:素灰墙+浅灰石板地,顶部柔光。人物:黑棕大波浪、细框眼镜、金圈耳环;装 A=黑高领+古铜金属光泽包臀迷你裙+灰褐红绑带纹丝袜+黑细带高跟;装 B=同上衣+黑皮质迷你裙+深渔网袜(吊袜带);装 C=裸腿。AIGC:真人实拍+重度 AI 美化(瓷化皮肤、腿部拉长、金属裙涂抹感);跳-落地-前踢重心连贯真实,跳切为剪辑而非 AI 形变。
- 节拍:(推测)86-128 区间,两处跳切间隔 1.4s 卡点。
- 镜头形态:A 一镜到底(2 处卡点跳切)。

### K199 提膝跳切双装接力链(4拍|变装转场·卡点跳切·舞蹈)
- 入态:正面走来、装 A(铜裙红纹袜) → 出态:单腿提膝悬空、装 B(黑裙渔网袜)
- 分解:拍1 0-1.9s 模特步进镜,铜裙随胯摆出高光流动;拍2 2.0-2.25s 右腿提起屈膝、身体 3/4 背转,裙摆离心飞起,手臂张开平衡——遮挡物=抬腿横过裙区+转身+裙摆飞展;拍3 技术峰值=2.25-2.375s 提膝顶点处跳切:铜裙→黑皮裙、红纹袜→渔网+吊袜带,腿部悬空角度连续(切在动作上);拍4 2.375-2.7s 单脚承重落地小跳 2 次,双臂上举画弧平衡,渔网袜随小腿晃出弹性形变,裙摆滞后半拍回落
- H3:`strutting in with a bronze metallic mini skirt, lifting one knee and spinning so the hem flies, jump-cutting at the apex of the raised knee into a black leather mini with garter fishnet stockings, landing hops on the standing leg with arms carving overhead arcs`
- 来源:《选择题御姐》00.0-02.7s(切点 2.25-2.375s)

### K200 单腿跳旋前踢收腿切袜链(4拍|舞蹈动作·变装转场)
- 入态:单腿站立提膝、装 B → 出态:双腿交叉站定、装 C(裸腿)
- 分解:拍1 2.7-3.25s 单腿小跳中右腿屈膝前后点摆,髋部画小圈,手臂一上一下护平衡;拍2 3.375-3.5s 技术峰值=右腿向前踢直(脚背绷直过腰),躯干后仰 10° 对抗,渔网袜网眼拉紧;拍3 3.625s 腿下落交叉收回,双臂胸前合拢(遮挡物=收腿+合臂+运动模糊),3.625-3.75s 跳切:渔网袜→裸腿;拍4 交叉腿站定,重量沉右胯,裙摆与发梢摆动 2 帧后停
- H3:`hopping on one leg with the other knee pumping, snapping into a high pointed front kick that stretches the fishnet taut, then folding the leg down and crossing the arms so the tights vanish into bare glossy legs on the cut, settling into a crossed-leg stand with weight sunk into one hip`
- 来源:《选择题御姐》02.7-04.0s(切点 3.625-3.75s)

### K201 抱臂推镜框微活性链(3拍|定格摆拍·微活性)
- 入态:交叉腿站定、裸腿 → 出态:同构收尾(指尖点颊)
- 分解:拍1 大姿势锁死:双腿踝交叉、左臂横抱腰前、右手抬起;微活性=右手上行推眼镜框上梁一次(4.333s);拍2 指尖滑到颊侧轻点两下,头右倾 10° 再回正,眼球咬镜头;拍3 胯部小幅左右顶 2 次(5.0-5.667s),裙摆随胯微摆
- H3:`standing with ankles crossed and one arm folded at the waist, pushing her glasses up with a fingertip that trails down to tap her cheek, tilting the head while the hips pulse twice and the eyes never leave the lens`
- 来源:《选择题御姐》04.0-06.1s

**片<v55> 《御姐蹲》(高跟鞋蹲拍·8.9s·竖屏)**
- 背景人物:高端楼宇大堂走廊,米色木饰墙、"VIP ENTRANCE"发光字牌、灰大理石地。人物:黑棕长卷发+金圈耳环,黑高领修身短袖+古铜液态金属皮革迷你裙+黑色前中缝线丝袜+黑色 YSL 金跟凉鞋。AIGC:真人实拍+重度 AI 美化/局部重绘(瓷肤、腿比夸张、字牌边缘波动);蹲姿重心物理合理。
- 节拍:(推测)非严格卡点摆拍,切点 2.9/4.4/7.3s,慢板 80-90。
- 镜头形态:C 快剪(3 处姿态跳切,平机位→低机位渐压)。

### K202 交叉步走秀进镜链(4拍|走路链·服装物理)
- 入态:远端正面走起 → 出态:近身收步手搭裙侧
- 分解:拍1 模特交叉步(每步落脚压过中线),胯为发动机左右顶送,前缝线丝袜随步把缝线保持腿正中,手臂低位对摆;拍2 步频加快,头发随步频弹跳,镜头微退跟拍;拍3 收步并腿,右手背擦过裙臀抚平皮革褶皱,下巴微收眼神入镜;拍4 微活性:腰侧手轻拎裙口 1cm 再放下,肩线回正
- H3:`runway-walking in with cross-stepping hips driving a bronze liquid-leather mini, the front seam of her sheer tights staying centered, brushing the skirt hem flat at the hips before locking the gaze to the lens and giving the hem a one-centimeter tug`
- 来源:《御姐蹲》00.0-02.9s

### K203 侧身后坐深蹲凝镜链(5拍|技术动作·重心控制)
- 入态:正面站姿 → 出态:深蹲后坐、双手搭膝、垂睫抬眼凝镜
- 分解:拍1 2.875s 右手离裙,头先转向左(视线领路);拍2 3.0s 身体转正侧 profile,胯向后下推送(髋屈+臀肌离心),双膝前折,双手伸向膝;拍3 3.125-3.375s 技术峰值=连续下蹲至全蹲:脚掌全平贴地(细高跟稳定承重),裙摆沿大腿上滑至髋褶,双手滑过膝盖扣在膝上,发垂两颊;拍4 3.5-4.0s 底点停驻:下巴垂 20°,眼球自下向上先入镜头(下看上瞟),手指在膝上轻叩;拍5 4.0-4.375s 上身再前倾左臂探地,回收=手撑地→膝微展→切出;同款蹲姿 7.3-8.9s(正面版,右膝高顶)
- H3:`turning to full profile and pushing the hips back to fold into a deep squat on stiletto heels, hands sliding over the knees as the leather mini rides up, chin dropping before the eyes cut up to the lens from under the brows, one arm reaching for the floor`
- 来源:《御姐蹲》02.9-04.4s(同族 07.3-08.9s)

### K204 起立甩发切低蹲定格链(4拍|变装转场·姿态跳切·定格摆拍)
- 入态:深蹲底点 → 出态:低蹲单膝高顶定格(手搭膝)
- 分解:拍1 4.5s 切至正面全身:双手深插入后脑发根,双肘外张,胯左顶,头右倾,发从指缝垂落;拍2 4.875-5.667s 指根向前耙发→单侧甩发(发梢划 1/4 圆弧)→手顺发滑到锁骨;拍3 6.0-7.25s 3/4 近身定点:指尖抵下颌-领口缓慢摩挲,眼神锁镜(微活性);拍4 技术峰值=7.25-7.375s 姿态跳切:正面站→正面低蹲(右膝高顶、YSL 金跟踏地、右手搭膝),切点前后构图重心下移半格
- H3:`rising into a full-front stand with both hands buried in her hair, raking it forward into a quarter-arc toss before sliding a fingertip at her collar, then pose-cutting straight down into a low squat with one knee driven high and gold-heel sandal planted, hand riding the knee`
- 来源:《御姐蹲》04.4-08.9s(切点 4.4-4.5s、7.25-7.375s)

**片<v56> 《猎人猎物》(西装跪·黑丝·5.3s·竖屏·高度疑似 AI 合成)**
- 背景人物:深灰竖肋板墙+木地板,椭圆追光;双主体:①前景站立者=黑丝袜长腿+黑漆皮红底细高跟(仅腿入画);②光斑中跪坐者=白短袖衬衫+黑领带+黑百褶短裙+浅口过膝袜,长卷发,左手持矮杯。AIGC:高度疑似 AI 生成合成——0.875s 前景腿落定时光斑内空,1.0s 跪姿人物凭空出现(连续实拍不可能);光源方向/色温不完全一致;膝盖关节形变。
- 节拍:(推测)氛围电子慢板。
- 镜头形态:A 一镜到底,地面超低机位锁定 POV(贴地仰角)。

### K205 黑丝长腿跨立入场合成链(4拍|变装转场·AI 合成·地面 POV)
- 入态:空光斑+鞋尖入画 → 出态:双腿跨立成"权力门框"、跪姿人物现身光斑
- 分解:拍1 0-0.625s 空镜:地面光斑、黑鞋尖缓缓滑入;拍2 0.75s 技术峰值=一条黑丝小腿裹运动模糊横扫过镜头上方(遮挡物=扫镜的腿+糊帧);拍3 0.875-1.0s 该腿落定画面中右,光斑内跪姿人物在 1.0s 凭空补现(合成节点);拍4 1.125-1.5s 第二条腿从画左摆入跨落,双脚分开比肩宽站定,构图完成=前景双腿作画框、跪者居光斑中心
- H3:`from a floor-level POV an empty spotlight waits as a black-stockinged calf sweeps across the lens in motion blur, the leg plants itself framing the right side while a kneeling figure in shirt and tie materializes in the spotlight, the second leg striding in to complete a power-stance gateway`
- 来源:《猎人猎物》00.0-01.5s

### K206 光斑跪仰猎物凝视链(3拍|定格构图·微活性)
- 入态:跨立构图完成、跪者垂头 → 出态:仰首凝视上方站立者,双唇微启
- 分解:拍1 大姿势锁死:跪坐于脚跟、膝头微分、裙摆铺地、左手持杯垂于裙侧;前景双腿微调重心(右踵外旋→左脚尖内扣);拍2 技术峰值=抬头:下颌沿 45° 线抬起,发向后滑,眼睛最后锁定镜头方向(仰视角);拍3 微活性:肩胛后张挺胸 1 次,持杯手指轻收,前景膝盖小幅内扣一次,光斑内发丝受"隐形风"轻摆
- H3:`kneeling back on her heels inside the spotlight with a glass resting at her skirt, lifting her chin along a 45-degree line until the eyes lock upward past the towering stockinged legs, shoulders rolling back once as the foreground feet shift their weight`
- 来源:《猎人猎物》01.5-05.3s

**片<v57> 《钓你上钩》(钓系制服变装舞·10.0s·竖屏·AI 渐变形)**
- 背景人物:深灰摄影幕布。人物:黑棕超长卷发;装序:①oversized 白长衬衫+白泡泡裙摆(裸腿白运动鞋)→②+黑过膝袜→③+黑领带→④修身白短袖衬衫+黑百褶裙+黑漆皮尖头泵。AIGC:高度疑似 AI 视频生成(图生视频类)——三处服装"渐变形"均无剪辑痕迹:袜子在抬腿遮挡下裸→白短袜→黑过膝渐长;领带在挥臂遮挡后一帧浮现;背身转身时宽松衬衫呈半透明纱化中间态收成修身衬衫+百褶裙;白鞋在提腿遮挡下变黑漆皮泵;瓷化皮肤、幕布纹理过度均匀。
- 节拍:(推测)约 100 BPM,变形点 0.9/2.1/3.2/4.3s 间隔约 1.1-1.2s 卡拍。
- 镜头形态:A 一镜到底(AI 形变换装,无剪辑),固定中景平机位。

### K207 旋身渐变形四连变装链(7拍|变装转场·AI 形变)
- 入态:白 oversized 衬衫裙摆臂起舞、裸腿 → 出态:完整制服(修身衬衫+领带+百褶裙+黑过膝袜+黑漆皮泵)
- 分解:拍1 0-0.875s 双臂交替上摆+提膝小跳,衬衫罩裙随胯摆出鼓形;拍2 技术峰值1=0.875-1.125s 右腿抬起交叉,遮挡物=抬腿横过身前+运动模糊,小腿处袜体渐长变形:裸→白短袜→黑过膝(形变中间态可见);拍3 1.125-2.0s 落地继续摆胯,双臂向上画大弧;拍4 技术峰值2=2.0-2.125s 右臂横扫过胸前遮挡瞬间黑领带浮现并甩出离心摆;拍5 2.125-3.0s 带领带续舞,3.0s 起以右肩为轴背身转身(遮挡物=转身+衬衫旋出);拍6 技术峰值3=3.125-3.375s 背身时宽松长衬衫呈半透明纱化中间态,随即收拢变形为修身短袖衬衫+黑色百褶裙,转回正面;拍7 技术峰值4=4.25-4.375s 后勾提腿时白鞋渐变为黑漆皮尖头泵(内里闪红一帧)
- H3:`dancing in an oversized white shirtdress as one lifted leg morphs bare skin into black thigh-highs mid-cross, a black necktie materializing behind a chest-sweeping arm, the loose shirt turning sheer and reshaping into a fitted short-sleeve shirt with a black pleated skirt during a back turn, white sneakers morphing into black patent pumps behind a hooked-up leg`
- 来源:《钓你上钩》00.0-04.4s(形变点 0.875-1.125 / 2.0-2.125 / 3.0-3.375 / 4.25-4.375s)

### K208 制服御姐摇摆舞链(4拍|舞蹈动作·服装物理)
- 入态:完整制服、后勾腿点地 → 出态:双臂低展定格收尾
- 分解:拍1 4.4-5.667s 后勾腿(黑漆皮泵朝天)+胯左右连续顶送,百褶裙摆与胯反相摆动,手臂一手托颌一手平摆波浪;拍2 5.667-7.0s 双臂在体侧交替画"S"波浪,肩部耸落 2 次,头随肩滚 1/2 圈;拍3 7.0-9.0s 胯画小圈,领带随上身扭转甩出弧线,发梢与裙摆滞后半拍;拍4 9.0-10.0s 技术峰值收势=双臂向两侧低位展开,下巴微扬眼神下压镜头,重心沉定定格
- H3:`pumping one hooked leg behind while the hips drive the pleated skirt into counter-swing, arms rolling in alternating S-waves with shoulder pops, the loose tie whipping arcs across each torso twist, closing with arms spread low and the chin lifting over a down-pressing gaze`
- 来源:《钓你上钩》04.4-10.0s

**片<v58> 《地铁 OOTD》(松弛感日常穿搭·8.5s·竖屏)**
- 背景人物:地铁站台(青绿导视、广告灯箱、全高站台门、列车、绿色"候车"地贴)。人物:黑棕长卷发;白色低胸吊带+牛仔短裤+灰色长款开衫(常滑落单肩)+白堆堆袜+白色厚底运动鞋+链条包。AIGC:真人实拍+重度美颜(场景细节真实,皮肤瓷化、腿部拉长)。
- 节拍:(推测)中速流行 ~90-100,快照切点不规律。
- 镜头形态:C 快剪(8 个快照机位),跟拍段手持逆行跟移。

### K209 扶梯垂立下行转站台甩发走链(4拍|走路链·日常感)
- 入态:扶梯上垂眸站立 → 出态:站台小跳步收势
- 分解:拍1 0-1.0s 扶梯下行:双脚并拢站稳一级,左手搭扶带、右手垂持手机,垂眸,身体随梯级自然起伏;拍2 1.333-1.75s 切站台手持跟拍(机位逆行后退):大步走,髋部送步,头发大幅甩摆,开衫滑落右肩一半,链条包随步幅前后荡;拍3 1.75-2.0s 眼神先入镜、下巴内收、嘴角单侧挑起(微活性),步幅不减;拍4 2.0-2.25s 技术峰值=双脚小跳步收势(俏皮双落步),身体前倾向镜定格;同族 5.333-5.667s 近景回眸甩发、6.0-6.667s 屏门前侧身看包回眸
- H3:`riding the escalator with feet together and eyes downcast, then striding toward a retreating handheld camera as her hair swings wide and the cardigan slips off one shoulder, eyes reaching the lens first before finishing with a playful two-foot hop lean`
- 来源:《地铁 OOTD》00.0-02.25s(同族 05.3-06.7s)

### K210 蹲姿系鞋带与托脸深蹲微活性链(4拍|定格摆拍·微活性)
- 入态:小跳步收势 → 出态:托脸深蹲定格
- 分解:拍1 2.375-3.125s 蹲坐系鞋带:右膝高顶、双手指尖系白鞋鞋带,先垂眸盯手,中段抬眼咬镜头,头右倾;拍2 3.333-4.0s 柱前靠站:双腿踝交叉、双手交叠垂于裙前、眼神锁镜(手指交叠摩挲 1 次);拍3 4.333-5.0s 坐上台面:长腿斜伸交叉、一手托颌一手扶台沿、小腿悬空轻晃;拍4 技术峰值=7.0-8.5s 深蹲托脸:全脚掌深蹲贴柜,双掌包住双颊、肘架膝上,头左右缓倾(各 10°),收尾凝镜
- H3:`squatting to tie her sneaker lace before glancing up into the lens, leaning crossed-ankled against a pillar with folded hands, stretching long crossed legs from a display block, then dropping into a full squat cupping both cheeks in her palms with elbows braced on knees, head swaying side to side`
- 来源:《地铁 OOTD》02.3-08.5s(多机位多时间码)

**片<v59> 《薄荷绿》(御姐户外摆拍·7.8s·竖屏)**
- 背景人物:户外广场白瓷砖台面/旱池,白砖墙+涂鸦字母、高层住宅楼、阴天柔光。人物:黑棕长卷发+薄荷绿圆圈耳环+十字项链;黑色抹胸短裙+oversized 黑西装(滑落双肩)+薄荷绿过膝袜+黑漆皮尖头细高跟(内里闪红)。AIGC:真人实拍+重度 AI 美化,局部疑似 AI 补绘(4.5-5.33s 前屈帧发丝与西装边缘"融化"、5.667s 鞋内里异常变红;姿态物理与地面阴影真实)。
- 节拍:(推测)中速流行,切点间隔不规律,摆拍快剪。
- 镜头形态:C 快剪(7-8 个摆拍机位),低机位仰拍与平拍交替。

### K211 坐台伸腿卷袜口链(3拍|服装物理·手部细节)
- 入态:坐台伸腿低角仰拍 → 出态:袜口整平、腿绷直收尾
- 分解:拍1 0.0-1.0s 坐台低机位:双腿向镜头右下伸展占满对角线,一膝屈立、黑尖头泵点台面,眼神俯压镜头;拍2 技术峰值=3.6-4.125s 卷袜口:右腿抬伸悬空,双手钩住薄荷绿袜口向外拉整、指尖逐段卷边,垂眸盯手(遮挡物=抬起的腿+双手全在袜口区),余光两度扫回镜头;拍3 4.125-4.375s 袜口整平贴紧大腿,腿绷直绷脚背,袜面弹性回缩微颤;同族 5.667s 高抬腿亮红鞋里、6.0-6.333s 交叉腿搭膝抚袜
- H3:`seated on a tiled ledge with her stockinged legs driving the low-angle frame, hooking both fingers into the mint over-knee top to tug and roll it snug up her raised thigh, eyes down on the hands before flicking back to the lens, then pointing the toe long`
- 来源:《薄荷绿》00.0-01.0s、03.6-04.4s(同族 05.6-06.3s)

### K212 深蹲托肘凝镜微活性链(3拍|定格摆拍·微活性)
- 入态:矮蹲环膝、发垂遮面 → 出态:深蹲双膝朝镜、肘架膝定格
- 分解:拍1 2.333-3.0s 矮蹲:双膝并拢蹲踞在台面上,西装滑落双肩,双臂环膝,长发前垂遮半面,下颌找膝;拍2 技术峰值=6.75-7.0s 切至地面深蹲:双膝外展正对镜头(薄荷袜膝部为画面最亮反光点),双肘架膝、双手垂悬膝间交握,抬头凝镜;拍3 7.0-7.7s 微活性:头左右缓倾各 10°、指节在膝间微屈、重心以踝为轴微摇 2 次,凝镜定格
- H3:`holding a tight crouch with arms wrapped over her knees and hair curtaining the face, cutting low and wide so both mint-stocking knees face the lens with elbows braced between them, tilting the head slowly side to side while fingers flex and the eyes hold the camera`
- 来源:《薄荷绿》02.3-03.0s、06.7-7.7s

**片<v60> 《尾巴加载》(节奏天国变装·7.4s·竖屏)**
- 背景人物:室内练习角(灰绿墙+木地板),固定全身机位。人物:王羽杉——前段奶白波点睡衣套装+白色厚底玛丽珍,后段红白格纹女仆装(HelloKitty 蝴蝶结胸饰+白围裙短裙+红格臂环)+白蕾丝过膝袜+红漆皮高跟鞋+白蝴蝶结发箍,棕栗大波浪;特效道具:像素橘猫贴纸、白色星光遮挡贴、腰后白毛绒尾巴(合成)。AIGC:真人+重度美颜瘦腿(透视/门框阴影一致;变装为单帧硬切无过渡帧,非 AI 生成)。
- 节拍:约 150 BPM(推测;三处变装间隔 1.65s≈4 拍)。
- 镜头形态:C 快剪(节拍跳切×3:衣 3.2s/鞋 4.85s/尾 6.6s)。

### K213 睡衣节拍猫耳手势链(5拍|节奏舞·像素贴纸)
- 入态:开位直立,右拳抬至胸口 → 出态:双臂下甩、右脚尖侧点,指尖朝上蓄势待变装
- 分解:拍1(0.0-0.4s)双脚开立,右拳胸前抬起,重心坐左胯(基座锁定);拍2(0.4-1.0s)双臂两侧打开至平举后下收,膝微弹两次吃音乐 tick;拍3(1.3-1.7s)技术峰值:双手举至头侧食指上指做猫耳手势,腕外翻两次,肩胛收紧带起上胸,与拍点严丝合缝;拍4(2.0-2.4s)双手合掌胸前、右膝提 90°,落步重心右移;拍5(2.5-3.1s)掌心胸前打开→右手指点颊侧→双臂向下甩出惯性回弹,右脚尖右侧点地,末态指尖朝上为变装拍让位
- H3:`dancing in a cream pajama set and chunky mary janes in front of a grey wall, pumping both fists chest-high, opening the arms wide on the beat, pointing both index fingers up beside the head like cat ears, pressing palms together while lifting one knee, then flicking both arms down as one toe taps out to the side`
- 来源:《尾巴加载》00.0-03.2s

### K214 变装三级跳链(6拍|变装·跳切三连)
- 入态:睡衣指尖上举 → 出态:女仆装+红跟+尾巴齐备的猫爪胯摆
- 分解:拍1(3.125s)变装前末帧定格;拍2(3.2s 跳切)红格女仆装瞬现:双手收至胸前理围裙肩带,右腿正迈步中、白袜未变——服装切换一帧完成、零过渡帧;拍3(4.3-4.8s)双臂两侧摊开掌心向上,展示红格臂环与白蕾丝过膝袜;拍4(4.85s 跳切)红色漆皮高跟鞋瞬现:白袜→红跟仅鞋部变化,胯位步态跨切点保持(匹配剪辑);拍5(6.2-6.5s)猫爪手势:双腕屈指下垂抖动,胯左右摆每拍一次;拍6(6.6s)白色毛绒尾巴贴纸合成入画,根部随胯摆反向荡出弧线,7.3s 收尾——三级变装(衣→鞋→配件)逐级递进全部踩拍
- H3:`beat-synced outfit change dance: pointing both fingertips upward in cream pajamas, cutting instantly into a red gingham maid dress with hands snapping to the apron straps, spreading the arms palms-up to show gingham arm garters and white lace thigh-highs, popping red patent heels on the next cut with the stride unchanged, ending in cat-paw hands while a fluffy white tail overlay swings counter to each hip sway`
- 来源:《尾巴加载》00:3.1-7.4s

**片<v61> 《腿精百褶裙》(通勤学院 OOTD·10.4s·竖屏)**
- 背景人物:黄昏城市天台(玻璃栏杆+浅灰砖地+水景+楼群天际线),固定全身机位。人物:王羽杉——白色收腰短袖衬衫+黑领带+黑色百褶超短裙+黑透肉丝袜+黑色尖头细跟+黑色小手提包;棕栗大波浪;全程肩以下构图、不给正脸。AIGC:疑似 AI 生成/深度 AI 美体嫌疑高(存疑)——腿身比失真、步态平滑略漂浮、玻璃反光无人影;栏杆与建筑透视物理一致。
- 节拍:约 80 BPM(推测;整步周期 0.75s)。
- 镜头形态:C 快剪(步频匹配跳剪:2.0s 手包换手藏于交叉步)。

### K215 直行逼近步频跳剪链(5拍|OOTD·步频跳剪)
- 入态:起步交叉步 → 出态:逼近镜头的直行步态
- 分解:拍1(0.0-0.5s)左脚交叉迈过右脚,黑手包垂左腕随步后荡(顶格裁头构图);拍2(0.5-2.0s)直行三步:每步 0.375s,鞋跟先落、胯随重心微旋,百褶裙摆随步频开合;拍3(2.0s 跳剪)手包从左手换至右手——切点藏于交叉步换脚瞬间,步频节奏完全延续(节拍遮蔽跳剪);拍4(2.0-3.7s)第二段直行:步幅加大,包随右臂前后荡;拍5(3.7-5.0s)逼近镜头:步速不变、透视放大,丝袜网点随腿拉伸;音乐触发:每步一拍
- H3:`walking straight toward a locked camera on a dusk rooftop in a white shirt, black tie and pleated mini skirt with sheer tights, crossing one leg over the other each step while a small black handbag swings at the wrist, the bag switching hands across an invisible stride-matched cut, hips rolling slightly with every heel strike`
- 来源:《腿精百褶裙》00.0-05.0s

### K216 停步摆包定格解锁链(6拍|道具包·摆弧)
- 入态:行进中收拳 → 出态:交叉步站定收尾
- 分解:拍1(5.3-5.8s)行进中左拳收至领口,右臂带包前荡(步态减速上肢加速);拍2(5.8-6.05s)定格点:右臂横伸包甩至体侧、左手撩发别耳,双腿前后交叉锁位静 0.25s(技术峰值前导);拍3(6.05-6.9s)解锁续走:包回落身侧,步频回 0.375s;拍4(8.9-9.5s)包由肩前向身后绕弧;拍5(9.5-9.75s)技术峰值:右臂全展、包荡至体侧最远点,身体左倾对抗配重,双腿剪式交错(腕部圆周甩动的离心力);拍6(9.75-10.37s)包回收至大腿侧,最后一步交叉站定——音乐触发:摆弧顶点落重拍
- H3:`pausing the rooftop walk to flick the handbag out to the side and tuck hair behind the ear in a crossed-leg stance, resuming the 0.375-second step rhythm, then swinging the bag into its widest arc with the arm fully extended and the torso leaning away as counterweight before stepping into a final cross-legged stop`
- 来源:《腿精百褶裙》00:5.3-10.4s

**片<v62> 《白裙慢摇》(金顶天台慢摇·15.5s·竖屏)**
- 背景人物:金色黄昏天台(玻璃栏杆+浅色铺装+楼群天际线),固定全身机位。人物:唐安琪@Angel(创作归属存疑:文件名为王羽杉,G2 组判读为唐安琪)——白色竹节纱一字肩不对称迷你裙+黑丝绒迷你包(黑长飘带)+黑点透肉丝袜;祖母绿耳环;棕栗长发帘式刘海。AIGC:疑似全 AI 生成嫌疑最高(远景楼群无逻辑马赛克重复纹理、腰胯曲线失真、点袜网点不均;裙摆物理与长阴影又一致)。
- 节拍:约 80 BPM(推测;胯摆换边周期 0.75s)。
- 镜头形态:A 一镜到底(15.5s 无切点,J 章微活性示范片)。

### K217 慢摇胯画横 8 链(6拍|慢摇·微活性)
- 入态:右胯外顶开位 → 出态:肩胯反向拧转蓄势
- 分解:拍1(0.0-0.8s)右胯向外顶出,右臂松垂随惯性摆,肩轴反向水平(骨盆-肩对抗);拍2(0.8-1.6s)胯横移左、重心跟移,裙摆下缘荡出斜弧;拍3(1.3-2.0s)右手抬至锁骨勾住领口;拍4(2.3-3.0s)左手指背触下巴,头右倾 15°,胯顶右(微活性:腕颈胯三点活);拍5(3.3-4.0s)胯左顶双臂松垂荡回,裙摆甩向右(轻纱滞后骨盆半拍);拍6(4.3-5.0s)肩-胯反向拧转一次回正;音乐触发:每换边一拍
- H3:`slow-swaying on a golden-hour rooftop in a white off-shoulder mini dress, pushing the hips side to side in a flat figure-eight while the arms hang loose and swing on inertia, hooking one hand into the neckline, tapping a knuckle under the chin with the head tilted, and letting the asymmetric hem swing against each hip shift`
- 来源:《白裙慢摇》00.0-05.0s

### K218 指唇抚颊撩发闭环链(5拍|微活性·手势链)
- 入态:手勾袖口 → 出态:手滑回胸口、胯回中
- 分解:拍1(5.0-5.25s)右手勾袖口上提至胸口,肘先动腕随;拍2(5.375-5.625s)指尖到唇轻点两下,肩胛上提含胸;拍3(5.75-6.0s)指腹滑至右颊,胯同步顶左,裙摆掀起(对侧联动);拍4(6.125-6.375s)手指插入鬓发向后梳,肘外展、胸廓展开(技术峰值:五指入发的发丝位移);拍5(6.5-6.625s)手顺锁骨下滑收、胯回中——微活性完整闭环,全程双脚不动
- H3:`micro-activity gesture chain in a slouchy white mini dress: drawing one hand up from the hem to the collarbone, tapping fingertips on the lips twice, sliding them down the cheek while the hip pops opposite, combing fingers back through the temple hair with the chest lifting, then gliding the hand down the sternum as the hips return to center`
- 来源:《白裙慢摇》00.5.0-06.7s(应为 00:05.0-6.7s)

### K219 肩滚背转回眸链(5拍|肩滚·背转回眸)
- 入态:右手滑向胯侧 → 出态:重心落定、发尾惯性收
- 分解:拍1(8.3-8.675s)右手从胸口滑到胯侧,躯干右拧启动;拍2(8.8-9.05s)双肩向后滚一圈,背 3/4 露出,包带斜跨背心;拍3(9.175-9.3s)下巴越过左肩回望镜头(背转峰值,头部最后回位);拍4(9.425-9.675s)转回正面,手先回胸口、胯跟进,裙摆拖带惯性;拍5(9.8-10.0s)重心落定,发尾摆收;同型复现 11.67-12.33s 侧步版本
- H3:`rolling both shoulders backward while the torso twists into a three-quarter back view with a tiny bag slung across, looking back over the left shoulder with chin leading, then unwinding to face front as the hand lands on the collarbone first and the hips follow, the ruffled hem trailing the turn on inertia`
- 来源:《白裙慢摇》00.8.3-10.0s(同型 00:11.7-12.3s)

**片<v63> 《薄荷绿斜角》(POV 斜角构图·5.7s·竖屏)**
- 背景人物:阴天户外白瓷砖台地,现代住宅楼群,"SHANG ZONE"字样立牌。人物:唐安琪@Angel(同 v62 归属存疑注记)——黑色西装外套(滑肩露锁骨)+黑色抹胸+铆钉腰带黑超短裙+薄荷绿过膝袜+黑尖头细高跟(鞋头薄荷拼色)+祖母绿耳环;红棕长发。道具:POV 前景手持手机。
- 节拍:约 100 BPM(推测;切点间隔 0.6s)。
- 镜头形态:C 快剪(POV/全景闪切交替+白闪 whip+黑帧,三拍位循环两轮)。

### K220 POV 取景斜角让位链(4拍|POV·取景构图)
- 入态:手机入画取景 → 出态:白闪 whip 入下一镜
- 分解:拍1(0.0-0.7s)前景持机手从左下入画,屏幕内她坐倚台阶斜角构图(腿向右上延伸占满对角线,双层构图);拍2(0.7-1.4s)手机沿斜角下移,屏幕画面与实景同构互证;拍3(1.4-2.2s)手机右移让位,露出全身斜角实景:左肘撑台、右手抚领、薄荷过膝袜双腿叠伸(地平线倾斜 10-15°);拍4(2.3-2.45s)白闪 whip 转场糊帧入切(曝光拉白+运动模糊)
- H3:`filming a friend who loves diagonal composition: holding a phone low so the screen frames her seated pose on white tiled steps, sliding the phone down and aside until it reveals the real scene — black blazer, mini skirt and mint thigh-high socks with legs stretched along the frame diagonal — then whipping into a white blur transition`
- 来源:《薄荷绿斜角》00.0-02.45s

### K221 三连拍位闪切循环链(5拍|拍位闪切·三连)
- 入态:坐倚拍位 → 出态:跪坐拍位循环两轮收
- 分解:拍1(2.45-3.2s)坐倚拍位:左掌撑台面、右手抚西装领、双腿向右伸直叠放,头左转看远(拍位静、微活性:指尖捻领、头微沉);拍2(3.2-3.3s)白/黑闪帧切换(1-2 帧 blink);拍3(3.3-3.55s)站立拍位:双臂垂、右胯顶、歪头向右,西装滑肩;拍4(3.575-3.7s)闪切;拍5(3.8-5.1s)跪坐拍位:双膝落地小腿外分、右手抚胸锁骨、左手撑地、仰头 45°——三拍位循环两轮(第二轮 4.0/4.33/4.67s 复现),末帧 5.33s 回坐倚收;音乐触发:每切点一拍
- H3:`rapid pose-cycle montage for a photo dump: holding a seated lean with one palm on the ledge and the other at the blazer lapel, blinking through a white flash into a full-body stand with hips cocked and head tilted, blinking again into a wide-kneel with one hand on the chest and the chin lifted, repeating the three-hero-pose loop twice on the beat`
- 来源:《薄荷绿斜角》00.2.4-05.7s

**片<v64> 《汗流浃背》(坐地变装·7.6s·横屏 60fps)**
- 背景人物:室内墙角(深色木地板+白墙+棕门框),固定机位。人物:王羽杉——前段奶黄睡衣套装+白袜;后段黑色亮片吊带迷你裙(侧腰镂空系带)+珍珠项链+黑色 YSL 凉鞋;黑长卷发。AIGC:疑似深度 AI 美体(小腿非物理褶皱伪影、腿身比失真);变装用甩模糊转场,非 AI 生成。
- 节拍:约 72 BPM(推测;滑腿周期 1.4s,R&B 慢速)。
- 镜头形态:C 快剪(2.9-3.2s 水平甩模糊转场一次)。

### K222 坐地滑腿甩模糊变装链(5拍|坐姿·甩模糊变装)
- 入态:屈膝坐地 → 出态:黑亮片裙贴墙坐定位
- 分解:拍1(0.0-1.0s)坐地右倾,双腿屈膝抬起,左手撑地板,黄睡衣白袜(骨盆+左手两点支撑);拍2(1.0-2.4s)双腿沿墙面向右下伸直滑落,脚跟蹭墙下行,身体后仰至 30°(核心控腿+墙面摩擦);拍3(2.4-2.9s)双腿完全伸直贴墙、脚尖绷直,肩胛触墙定位;拍4(2.9-3.2s)整幅水平甩动模糊转场(遮挡窗口);拍5(3.3-3.8s)黑亮片吊带裙+YSL 跟现:同机位同坐姿,双腿仍贴墙——腿位跨切点完全复刻
- H3:`sitting on a wooden floor in a pale yellow pajama set, sliding both legs down along the wall until they are fully extended with pointed toes, then whipping into a horizontal motion blur that lands in a black sequin mini dress and strappy heels in the identical wall-leaning seat, legs matched across the transition`
- 来源:《汗流浃背》00.0-03.8s

### K223 贴墙足尖磕墙微动链(4拍|贴墙·微活性)
- 入态:亮片裙坐姿定位 → 出态:膝交叠静拍
- 分解:拍1(3.8-5.0s)定位拍:左手撑地后倾,右手食指抵胸,右脚外缘贴墙、左踝搭右踝(基座锁定,踝/颈/腕活);拍2(5.0-5.7s)足尖交替点墙:右踝屈伸两次,鞋跟磕墙与音乐触点对齐(磕墙声=打击点);拍3(5.7-6.7s)右手撩耳后发,头右倾,肩线压低半寸;拍4(6.7-7.6s)换边:左腿屈膝收、右腿伸直压上,膝交叠循环一轮收于静拍——技术峰值在拍 2 踝拍节奏
- H3:`holding a floor pose against the wall in a black sequin dress: propping on one hand behind, pressing a fingertip to the chest, alternating ankle flexes that tap the heels against the wall on the beat, brushing hair behind one ear with the head tilted, then re-crossing the knees into a quiet final hold`
- 来源:《汗流浃背》00.3.8-07.6s

**片<v65> 《理想型》(走廊遮挡变装·8.9s·竖屏)**
- 背景人物:酒店走廊(木饰面墙+黑色条形灯槽+反光石材地面,一点透视),固定机位。人物:王羽杉——前段白色一字肩针织衫+粉色阔腿裤;后段香槟色亮片挂脖吊带长裙+项链+耳环+手链;棕栗大波浪。AIGC:真人+重度 AI 美体(走廊透视与地面反射一致;皮肤零毛孔、腰臀比极端;变装窗口内宽裤 0.4s 内消失物理不可能——衣物遮挡下隐藏跳切)。
- 节拍:约 88 BPM(推测;胯顶换边 0.7s)。
- 镜头形态:C 快剪(1.8-1.9s 遮挡窗口藏切点)。

### K224 背身拢手回眸链(4拍|背身·胯拍)
- 入态:背对镜头站立 → 出态:转身启动、双手抓稳下摆
- 分解:拍1(0.0-0.6s)背对镜头站定,双手于腰后交叠拢住毛衣下摆,胯随拍左右顶;拍2(0.6-1.0s)胯顶左同时头左后转,回眸 3/4 侧脸,长发甩过右肩;拍3(1.0-1.4s)头转回背位,双手把下摆抓得更紧(变装蓄力);拍4(1.4-1.7s)左肩内旋启动转身,双手沿后腰上移
- H3:`standing with the back to the camera in a white off-shoulder sweater and pink wide pants, clasping both hands behind at the hem, pumping the hips side to side on the beat, glancing back over the shoulder in a three-quarter smile with hair whipping across, then gripping the hem tighter as the turn begins`
- 来源:《理想型》00.0-01.7s

### K225 撸衫蒙面旋转变装链(3拍|遮挡变装·旋转)
- 入态:双手抓下摆 → 出态:亮片裙全身现、指尖到位下巴
- 分解:拍1(1.7-1.8s)双手将毛衣下摆向上撸过腰、过胸,衣身罩到领口蒙脸(遮挡物=衣物本体);拍2(1.8-1.9s)衣物蒙面瞬间=换装窗口:毛衣内已穿香槟亮片吊带裙,粉宽裤在遮挡中消失(隐藏跳切/遮挡变装机制);拍3(1.9-2.05s)发鞭横扫落下,亮片裙全身亮相,右手指尖已就位下巴
- H3:`pulling the sweater hem up and over the torso until the fabric covers the face, spinning inside the occlusion so the white top and pink pants swap for a champagne sequin slip dress, letting the hair whip down across the frame as the cloth clears to reveal the full look with one fingertip already at the chin`
- 来源:《理想型》00.1.7-02.1s

### K226 走廊慢摇甩发峰值链(6拍|慢摇·甩发峰值)
- 入态:指唇小腕花 → 出态:单肩胯顶定格
- 分解:拍1(2.05-2.7s)指腹点唇、腕外翻小腕花,胯画横 8;拍2(2.7-4.0s)慢摇循环:骨盆每 0.7s 换边,亮片随胯闪光流动;拍3(5.3-5.55s)右手插入发顶向后拢,肘架高;拍4(5.675-5.8s)技术峰值:头从右后向左前猛抡,整头发横弧扫过镜头、糊帧但无切点(颈旋转+发鞭惯性);拍5(5.9-6.2s)发落定肩前,手指顺发梳下,胯顶回右;拍6(7.0-8.9s)双腕交替外翻腕花两次→8.33-8.67s 单肩胯顶收尾定格——甩发落重拍
- H3:`slow-swaying down a hotel corridor in a champagne sequin midi dress, tapping fingertips on the lips with a little wrist roll, pumping the hips in a flat figure-eight on every beat, raking one hand back through the crown hair and whipping the whole head forward so the hair fans across the frame in a motion-blurred arc, then settling the hair and closing with double wrist rolls into a final hip pop`
- 来源:《理想型》00.2.1-08.9s

**片<v66> 《猜你喜欢》(唐安琪·椅子卡点换装·5.1s·竖屏)**
- 背景人物:暗调室内(黑色木饰面墙+顶部聚光锥+大理石纹地面),黑色现代单椅,固定机位。人物:唐安琪@Angel——五套连换:黑蕾丝吊带+蓝喇叭牛仔裤+银钻凉鞋→白衬衫+黑透肉丝袜+黑绊带跟→红色吊带裙+红点丝袜+黑尖跟→祖母绿缎面抹胸裙+黑丝+绿宝石项链→银色亮面抹胸裙;黑长发中分。AIGC:真人+重度美颜(椅子形变、墙面木纹真实连续;换装为跷腿锚点跳切非 AI 生成)。
- 节拍:约 80 BPM(推测;换装间隔 0.75s=1 拍)。
- 镜头形态:C 快剪(固定机位卡点连切×4,跷腿姿势跨切复刻)。

### K227 跷腿甩鞋遮挡换装链(3拍|跷腿·甩鞋变装)
- 入态:坐椅开位双臂平展 → 出态:跷腿几何不变、服装换为白衬衫黑丝
- 分解:拍1(1.9-2.15s)黑蕾丝吊带+蓝喇叭牛仔裤+银钻凉鞋:双臂向两侧平展打开(翅式),左腿抬离地面(髋屈肌提腿);拍2(2.15-2.3s)左腿跨压右腿成跷腿,右踝同时外翻,银色凉鞋脱脚甩出、鞋在趾尖飞离(变装前导=遮挡物:动作吸引视线);拍3(2.35-2.4s)跷腿姿态完全一致的跳切:白衬衫+黑透肉丝袜+黑绊带跟瞬现——跷腿几何为不变锚点,切点藏于鞋子飞离瞬间(甩鞋落拍)
- H3:`sitting on a chair in a black lace cami and flare jeans, spreading both arms wide like wings, lifting the left leg to cross over the right knee while the right ankle rolls and a rhinestone sandal kicks off the toe mid-air, then cutting on the identical crossed-leg pose into a white shirt, sheer black tights and strappy heels`
- 来源:《猜你喜欢》00.1.9-02.45s

### K228 卡点四连换装锚点链(6拍|卡点四连换装)
- 入态:白衬衫跷腿拍位 → 出态:银色抹胸裙同锚点收
- 分解:拍1(2.9-3.1s)白衬衫拍位:跷腿不动,右足尖垂直点地循环 2 次(基座=骨盆+跷腿完全锁定);拍2(3.1-3.3s)跳切:红色吊带裙+红点丝袜现,左腿 swing 重新跷上、足尖继续点;拍3(3.3-3.85s)红裙拍位:足尖点 2 次、指尖搭膝;拍4(3.85-4.0s)跳切:祖母绿缎面抹胸裙+黑丝+绿宝石项链现(配饰同色联动,系列标志);拍5(4.0-4.35s)绿裙拍位足尖点 2 次;拍6(4.35-4.8s)跳切:银色亮面抹胸裙现,足尖点拍收尾——四套服装同一跷腿锚点,每次切点均落在足尖触地拍上(足尖点地=节拍遮蔽跳切)
- H3:`beat-locked seated outfit cycle on one chair: keeping the crossed-leg pose as the fixed anchor while pointed toes tap the floor on every beat, jump-cutting from white shirt to red slip dress with polka-dot tights, to an emerald satin strapless mini with a chunky green gemstone necklace, to a silver metallic mini, each cut landing exactly on the toe-tap`
- 来源:《猜你喜欢》00.2.9-04.8s

**片<v67> 《听话 OOTD》(唐安琪·御姐 OOTD 多景快剪·6.0s·竖屏)**
- 背景人物:室内玄关/衣帽间——黑色木纹墙板+浅灰大理石地面+白色格栅墙,三处坐具(黑墙角、黑皮沙发、黑色单椅)。人物:唐安琪@Angel——灰色斜纹抹胸紧身包臀短裙、黑色后缝线大腿袜(背部缝线清晰)、黑色网纱 T 字带踝绑高跟凉鞋、红甲;黑长直中分,耳骨夹。实拍+重度美颜(手指关节与指甲形态真实;磨皮+腿部修长滤镜)。
- 节拍:约 120 BPM(推测,切点 1.87/2.9/3.95/5.3 卡点)。
- 镜头形态:C 快剪(5 镜全硬切,切镜后 0.2s 曝光爬升)。

### K229 踩点入画踝特写链(3拍|低机位特写·节奏踩点)
- 入态:黑墙大理石地空镜,腿出画 → 出态:双脚第四位交叉立定于画面纵轴
- 分解:拍1 甩腿入画:右腿自画左上摆入,足背绷直,摆速快带一帧运动模糊;拍2 落定:前掌先触地再压跟,小腿绷直使袜背缝线拉成直线,左腿跟进并拢,双脚交叠成第四位;拍3 微活性:踝骨沿跟腱线内外小幅摆两次踩点,红甲在鞋头开口处闪现(固定低机位,腿占满纵轴)
- H3:`low-angle close-up of bare legs stepping into frame through a swinging arc in black back-seam stockings and mesh T-strap heels, landing toe-first then stacking the feet into a crossed fourth position, ankles ticking side to side twice on the beat against a black door and marble floor`
- 来源:《听话 OOTD》00.0-01.8s

### K230 黑墙蹲踞抱膝凝视链(3拍|定格构图·微活性)
- 入态:黑墙角落深蹲坐 → 出态:指节抵唇凝视镜头
- 分解:拍1 定格锁死:深蹲坐于脚跟,双膝高叠交剪,裙摆绷于大腿面,双臂环叠膝头,下颌收向膝,入点 0.2s 欠曝(曝光爬升);拍2 技术峰值=抬头:下颌沿斜上 45° 线抬起至镜头,锁骨露出,发梢滑落肩前;拍3 微活性:叠膝手指逐根收拢再摊开一次,膝头内扣 1cm 回弹;复现镜头(5.3-6.0s)同一蹲姿加指节抵唇
- H3:`squatting low on her heels against a black wall with knees stacked sideways and arms folded over them, lifting the chin along a diagonal until the eyes lock on camera, fingers assembling and spreading once over the kneecap while a reprise shot adds knuckles pressed to her lips`
- 来源:《听话 OOTD》02.0-02.8s、05.3-06.0s

### K231 沙发后仰抚腿·拨发召手链(3拍|换景复合·POV 召引)
- 入态:黑皮沙发坐定腿高叠 → 出态:单椅上前伸手掌召引
- 分解:拍1 进入:膝上叠膝小腿前伸,身体沿沙发背向后滑,肩胛触背时胸口上挺;拍2 逐拍:掌沿大腿外侧向下滑半掌幅,头后仰发后坠,视线全程回镜头;拍3(切椅景)技术峰值=手召引:肘先抬、小臂鞭打前伸、腕最后抖平,五指张开朝镜头,发随手拨过肩
- H3:`leaning back along a black leather couch with one knee stacked high, palm gliding half a hand-width down the outer thigh as the head tips back and the eyes stay on camera, then flicking the hair off one shoulder and reaching an open palm toward the lens from a chair in a whip of forearm snap`
- 来源:《听话 OOTD》03.0-04.0s、04.0-04.8s

**片<v68> 《薄荷绿车拍》(唐安琪·车内夜拍氛围·6.7s·竖屏)**
- 背景人物:夜间轿车副驾位,车门开启,门外地库黄色氛围灯带,黑真皮座椅。人物:唐安琪@Angel——黑色抹胸紧身短裙、薄荷绿过膝袜(无鞋,足部裸袜)、黑长发。实拍(车内饰缝线/安全带扣/门框反光物理一致;薄荷袜膝弯压力褶自然堆积)。
- 节拍:约 90 BPM(推测,慢句铺陈,切点 2.1/4.45/5.25)。
- 镜头形态:C 快剪(4 镜:拢膝近景→低机位抚胫→后仰握头枕→膝上俯身近景)。

### K232 车座拢膝托腮链(3拍|车内框中框·微活性)
- 入态:上身前倾贴近镜头 → 出态:手收至下颌,膝并拢回正
- 分解:拍1 进入:上身自镜头近处拉回(开机位),膝并拢侧坐,薄荷袜口绷在大腿;拍2 逐拍:指尖自锁骨下滑至下颌,头随行侧倾,门外黄色灯带在腿上扫出一条亮边;拍3 微活性:并拢膝头向镜头方向顶半寸回落,睫毛半掩(门框构成画左黑边=车内框中框)
- H3:`seated sideways in the passenger seat with knees pressed together in mint thigh-highs, pulling back from the lens to let fingertips travel from collarbone to chin as the head tilts, yellow ambient strip light running an edge along the thighs, kneecaps nudging half an inch toward camera once`
- 来源:《薄荷绿车拍》00.0-02.1s

### K233 低机位抚胫·后仰握枕链(3拍|低机位+后仰·POV)
- 入态:低机位侧拍,腿折叠于座椅 → 出态:头枕上仰闭目
- 分解:拍1 进入(切镜入点):硬切至座椅侧低机位,掌已贴胫骨前侧;拍2 技术峰值=抚胫慢滑:掌根发力沿胫骨自膝下向踝推,足背随之绷直,趾节逐根蜷缩再展开;拍3 回收(切后仰景):手越过头顶反握头枕,胸骨上顶,头后仰落枕,眼睑徐徐闭合,下颌线侧向镜头
- H3:`filmed from a low side angle inside the car, palm pushing slowly down the shin from under the knee toward the ankle as the foot points and toes curl then fan, then leaning back to grip the headrest overhead, chest lifting and eyelids sinking shut with the jaw offered sideways to the lens`
- 来源:《薄荷绿车拍》02.1-04.45s、04.45-05.2s

**片<v69> 《薄荷绿不烧心》(展示快剪·6.5s·竖屏)**
- 背景人物:客厅两景——黑色木门+灰地站立位;黑皮沙发+白色格栅墙+黑白格"H"字靠枕。人物:唐安琪@Angel——黑色抹胸连体短裤、薄荷绿过膝袜、黑色漆皮细高跟(红底)、黑色蕾丝颈圈,深棕长卷发。实拍(2.28-2.4s 转场为真实运动模糊,人+机同动;沙发皮面褶皱连续)。
- 节拍:约 125 BPM(推测,快切,切点 1.25/2.28/3.3/4.0)。
- 镜头形态:C 快剪(含 1 处两帧甩移模糊转场,6+ 镜)。

### K234 站姿拧胯绕膝链(3拍|全身站姿·卡点)
- 入态:黑墙前双手叉腰直立 → 出态:膝内绕交叠后重心回正
- 分解:拍1 锁定:双手虎口卡腰侧,肘外撑,重量沉单腿,肩线水平;拍2 逐拍动力:右膝先内拧(膝内扣),胯随之向左推送,双腿绕成剪状交叠,袜口随大腿挤压上顶;拍3 技术峰值+回收:绕膝交叠到位后重心回灌,胯部画小横八字回正踩点,发尾随躯干惯性轻摆
- H3:`standing full-body against a black wall with hands hooked on the hips, screwing one knee inward to push the hip across and scissor the legs over each other in mint thigh-highs, then letting the weight pour back as the hips trace a small flat eight and the hair tips sway with the recoil`
- 来源:《薄荷绿不烧心》00.0-01.25s

### K235 红底抬腿·甩移近景链(3拍|快剪+甩镜·物理峰值)
- 入态:切镜即见沙发一腿高举 → 出态:近景抚膝定格
- 分解:拍1 进入(切镜即动):切至沙发即见小腿垂直上举、鞋红色大底正对镜头(技术峰值),足尖挂高跟,手扶膝;拍2 转场:躯干前扑带动机位横向甩移,两帧全画面运动模糊(人机同动)完成宽景→近景跨景;拍3 落定:近景白墙背景,掌心罩上膝头反复摩挲,袜口上沿露出一截大腿,视线回镜头
- H3:`cutting in mid-motion with one calf raised vertical and the red sole of the stiletto facing the lens on a black couch, then lunging forward into a two-frame whip blur that carries the camera across the room to a close-up where the palm cups and strokes the stocking-top knee while the eyes return to the lens`
- 来源:《薄荷绿不烧心》01.25-01.9s、02.28-02.78s

**片<v70> 《5 秒错过我》(反差变装·5.3s·竖屏)**
- 背景人物:亮色轻奢室内——白色灯带台阶+白色格栅墙+银色镜面 Bearbrick 积木熊摆件+大理石纹地面。人物:王羽杉——白色 oversized 短袖 T、黑色短裤、白色厚底松糕鞋;发型三变:丸子手举发(镜 1)→大波浪散发(镜 2、3);红唇。实拍(黑场为真实压黑转场,银熊镜面反射随人形连续变化,发丝无生成漂移)。
- 节拍:约 100 BPM(推测,卡点落在 1.85 变装切与 4.4 黑场)。
- 镜头形态:C 快剪(3 镜:地板盘坐→台沿散发→台沿并膝,含 1 处黑场转场)。

### K236 地板盘坐举发链(2拍|纯真系·微活性)
- 入态:大理石地板盘坐,右手握发上举 → 出态:发束仍举,整体轻弹
- 分解:拍1 定格:盘坐交叉腿,白色厚底鞋交叠,右拳攥头顶发束高举,腕挂黑发圈,下颌微收盯镜头;拍2 微活性:以腰椎为轴整体前后小弹两次(核心与臀部均摊),发束随弹动上抛半寸,腮边碎发飘起
- H3:`sitting cross-legged on marble tile in an oversized white tee and chunky white sneakers, one fist hoisting the topknot high with a black hair tie around the wrist, bouncing twice from the lumbar spine so the captured hair tosses half an inch and the baby hairs lift off the cheek`
- 来源:《5 秒错过我》00.0-01.85s

### K237 台沿散发斜倚链(3拍|变装后·慵懒斜倚)
- 入态:散发落肩,坐白色台沿 → 出态:手滑至小腿,回眸锁镜
- 分解:拍1 进入(变装切点):大波浪散发已垂至腰,坐台沿腿前伸交叠,身体前倾手搭膝;拍2 逐拍:掌沿小腿正面缓慢拖行,头随掌行方向斜倒,发帘盖过右眼;拍3 技术峰值=回眸:掌行至踝时头沿对角线抬起回正对镜,锁骨窝加深,银熊镜面反射随人形扭动
- H3:`hair released into long waves over a white ledge with legs crossed and extended, palm dragging slowly down the front of the shin while the head tips sideways and bangs cover one eye, then lifting the head back along a diagonal to re-lock on camera as the silver mirror bearbrick bends the reflections`
- 来源:《5 秒错过我》01.85-04.3s

### K238 黑场复活·并膝撩鬓链(3拍|黑场转场·定格)
- 入态:画面压黑 → 出态:并膝坐定,手插鬓发
- 分解:拍1 转场:两至三帧黑场(压黑卡点,无叠化残像);拍2 复活入态:亮起即并膝坐定,左手垂于膝间攥发圈,右手已抬至鬓角;拍3 微活性:指尖在鬓发里梳进半寸停住,身体沿台沿小幅度前顶一次,复亮后红唇饱和度瞬间拉满(调色峰值)
- H3:`dipping through two frames of black into a knee-together seated pose with the left hand holding the hair tie between the thighs and the right hand already buried half an inch into the temple hair, easing the torso forward once on the ledge as the color grade snaps the red lips to full saturation`
- 来源:《5 秒错过我》04.3-05.3s

**片<v71> 《隔屏就撩·海员帽》(直播近景 POV 互动·30.1s·竖屏)**
- 背景人物:直播间胸口以上近景,蓝绿渐变虚化背景。人物:王羽杉——深蓝海军平顶帽(蓝色缎带蝴蝶结)、深蓝抹胸、宽蓝颈圈、白色缎面及肘手套、银十字+珍珠双层项链、蓝色耳返;棕色长直发空气刘海。道具:白色有线耳机线(全程逗弄核心道具)。特效:漂浮光尘粒子。AIGC:直播实时美颜接近"AI 感",但耳机线悬链线弧度与手套细褶符合物理→直播实时滤镜,非生成视频。
- 节拍:约 72 BPM 慢律动(推测,直播无硬卡点)。
- 镜头形态:A 一镜到底(机位固定近景)。

### K239 掌心贴胸慢滑链(3拍|直播近景·POV 互动)
- 入态:白手套掌心摊开贴锁骨下 → 出态:掌滑至胸口中央,头左倾
- 分解:拍1 进入:五指全张压平于锁骨下方,腕骨内旋令掌纹全贴皮肤;拍2 逐拍动力:以指节为引导沿胸口缓慢下滑约一掌幅,头部同步左倾,眼睑半落,唇随唱词开合;拍3 微活性+回收:指尖在终点屈伸一次,肩线上提半寸再沉,白线在掌外侧保持垂直张力,缎面手套随腕旋起细褶
- H3:`pressing a white satin glove flat under the collarbone with fingers spread, sliding one hand-width down the chest as the head tilts left and the lids droop, flexing the fingertips once at the end while the earphone cord keeps a vertical tension beside the wrist against a blue gradient backdrop`
- 来源:《隔屏就撩·海员帽》02.8-04.7s

### K240 耳机线逗唇链(3拍|道具互动·POV)
- 入态:白线垂于胸前 → 出态:线沿下颌收拢,双手合掌托腮收尾
- 分解:拍1 拾线:双手指尖捏线自颈前提起,线呈真实悬链线弧度;拍2 技术峰值=线过唇:线身横搭唇峰,唇肌轻微收缩含住线弧再放开,眼睛先于唇锁向镜头;拍3 惯性+回收:线自唇滑向下颌沿脸缘收拢,头随线端方向缓缓歪斜;末段(27.2-30.0s)线拉成斜对角绷紧,双手合掌托腮,指尖在线上轻弹两次收尾
- H3:`pinching the white earphone cord between both gloved fingertips and lifting it into a hanging catenary across the lips, letting the lip muscles catch and release the curve while the eyes lock first, then trailing the cord down along the jaw as the head follows it sideways, ending with palms pressed together under the chin flicking the line twice`
- 来源:《隔屏就撩·海员帽》09.6-11.3s、22.0-23.9s、27.2-30.0s

**片<v72> 《隔屏就撩·你来啦》(直播全景 POV 互动·18.4s·竖屏)**
- 背景人物:直播间全景——深紫蓝幕布+地面紫色 LED 灯带+白色人体工学直播椅+灰粉靠枕。人物:王羽杉——深蓝丝绒抹胸前拉链紧身短裙、黑色细高跟凉鞋、大圈耳环、白色有线耳机。道具三连:白色瓶装饮品杯、黑色团扇、白色粉盒。实拍(灯带光斑稳定,椅脚反光连续)。
- 节拍:约 65 BPM 慢律动(推测,动作事件间隔 4-5s)。
- 镜头形态:A 一镜到底(固定全景机位)。

### K241 转身撩发踢腿链(3拍|直播全景·惯性峰值)
- 入态:椅子前坐膝并拢 → 出态:腿回叠坐正
- 分解:拍1 转体:肩线先向右拧,头甩向背后(发旋即鞭梢,惯性延至发尾),同时右大腿开始上抬;拍2 技术峰值=踢展:右腿沿水平线向画左踢出伸直锁定,拉链裙被大腿抬升拉紧上滑;拍3 回收:腿以弧线下落,躯干回转对镜,双腿落成交叠位
- H3:`twisting the shoulders right until the head whips behind the back with the hair lagging as a whip tail, extending the right leg into a locked horizontal kick toward frame left as the zip-front dress cinches upward over the thigh, then lowering the leg through an arc and re-crossing it while the torso rotates back to the lens`
- 来源:《隔屏就撩·你来啦》02.0-03.4s

### K242 拾杯托颊·粉盒沉降递送链(3拍|道具链·POV)
- 入态:手垂椅侧 → 出态:粉盒沉落膝前,团扇换手
- 分解:拍1 探取:躯干右前倾,臂探向地面,五指兜住白杯上提(髋屈+背伸链);拍2 托颊展示:杯沿弧线扫至颊侧,肘架起,腕内旋把杯口转向镜头,头侧贴向杯作嗅闻位;拍3 沉降递送(粉盒段):白色粉盒平托掌心自肩高沿体前中线下沉,腕部保持盒面朝镜头(POV 递送语义),至膝前交左手,右手随即拾起团扇
- H3:`reaching down past the chair arm to scoop up a white cup then sweeping it up to the cheek with the wrist rotating the rim toward the lens as the head leans in to sniff, later lowering a white compact flat on the palm down the body midline toward the knees before trading it for the black paddle fan`
- 来源:《隔屏就撩·你来啦》07.2-08.7s、15.8-17.5s

**片<v73> 《美背杀》(书房实景美背展示·6.4s·竖屏)**
- 背景人物:复古书房实景棚——满墙彩色书脊书架、黄铜烛台吊灯(烛焰点亮)、水晶冰柱挂饰、木质格架台。人物:王羽杉——黑色单肩露背紧身衣(深开背至腰骶)、棕色大波浪长发及腰、金属大耳环。实拍(书脊排列磨损随机,烛焰/水晶/抓发物理一致;8fps 密帧发丝无漂移,手指抓握逐帧连续→实拍+重度调色磨皮)。
- 节拍:约 75 BPM(推测,乐句约 3.2s 一循环)。
- 镜头形态:A 一镜到底(固定背面直视机位,微仰角)。

### K243 背面跪坐拢发链(2拍|全背面·进入路径)
- 入态:跪坐书架台,双手扶台,发瀑披背 → 出态:右臂高举攥发束
- 分解:拍1 锁定:直背跪坐,双手掌面平压身侧木台,发瀑盖住整个开背,肩胛藏于发下;拍2 逐抬:右手离台沿体侧外弧上举(肘先行、腕再卷),五指插入后脑发根攥成一束上提,左侧发帘被牵拉滑落露出左肩胛全貌,头随提拉方向微仰
- H3:`filmed straight on from the back, kneeling upright on the wooden shelf ledge with both palms flat on the wood while hair curtains the open back, then sweeping the right arm up along an outer arc to bunch the hair at the crown, pulling it upward until the left shoulder blade fully emerges`
- 来源:《美背杀》00.2-02.6s

### K244 美背撩发倾泻链(3拍|技术峰值·慢惯性质感)
- 入态:双手举发束过头 → 出态:发瀑泻向左肩,手顺发滑落
- 分解:拍1 举定:双臂皆举,发束攥在头顶上方,裸背全露,腰椎前顶形成背沟深影;拍2 技术峰值=释放:五指松开,发团先整体上弹再向左肩泻落,发丝呈三段落差分批落下(上部快、发尾拖),肩胛随释放放松下沉;拍3 回收:右手沿下坠的发外缘向下捋,手到腰际时发尾刚好齐腰落定,左手回扶台面
- H3:`holding the gathered hair overhead with both arms raised and the bare back fully exposed, releasing the grip so the hair bounces once then pours over the left shoulder in three staggered layers, tracing the falling mass down with the right hand until the ends settle at the waist in front of a bookshelf wall and brass chandelier`
- 来源:《美背杀》02.6-04.0s

**片<v74> 《书架露背》(复古书房写真·9.0s·竖屏·AI 写真幻灯)**
- 背景人物:深色木书架复古书房棚(铜烛台吊灯、暖黄壁灯、虎皮纹丝绒扶手椅、鎏金雕花椭圆立镜)。人物:王羽杉——黑色单肩露背连衣裙(大 U 挖空至腰骶),水滴金耳环,栗棕大波浪,钻链脚链+黑细带高跟;中段配貂皮披肩;红唇。AIGC:疑似(高)——2.525s/7.375s 两处单帧重影 morph 转场(图生视频插值特征)、皮肤零噪点、镜面反射文字糊化。
- 节拍:约 76 BPM(推测·慢板)。
- 镜头形态:B 快照幻灯(6 机位经 AI morph 串联,无硬切)。

### K245 书架坐姿双镜位链(4拍|坐姿·背线语义·微活性)
- 入态:壁龛内正面坐定、右腿跨压左腿占对角线 → 出态:背面撑台坐定、头回正、背线全展后二次前倾
- 分解:拍1 0.0-1.1s 正面机位(胸高平拍):右腿跨压左腿向画面右下伸展,左手自胫骨向脚踝分段滑抹,头水平锁定镜头,背后镜面反射棚内人影;拍2 1.15-1.9s 背面机位(肩胛高度,同景切镜):双手宽距撑住书架台沿把髋坐满,露背挖空线自 C7 直通腰骶全展(背线语义:发帘盖背左 1/3,转头即成 reveal 机关),头从左 profile 经正中慢滚,发梢甩扫过背线;拍3 1.9-2.4s 回收=头→肩→髋:头回中、肩胛后收、右手沿台沿内滑半掌;拍4 3.67-5.0s 正面二回(机位更低更近):前倾加深、头右倾 15° 目线压镜头;音乐触发:整链≈4 拍
- H3:`seated inside the dark wood bookshelf alcove with one leg crossed over the other driving toward the lens while a hand glides down the shin, then from behind with palms planted wide on the shelf edge slowly rolling the head from left profile through center so the long waves swing across the fully open back, settling shoulder blades and leaning deeper over the knee on the return`
- 来源:《书架露背》00.0-01.1s、01.15-02.4s、03.67-05.0s

### K246 椭圆镜披肩滑臂回头链(3拍|服装物理·镜像几何·回眸)
- 入态:镜前站立、披肩挂上臂 → 出态:实空间近景、双手抓披肩绕至胸前、下颌微收
- 分解:拍1 5.375-6.0s 镜像内景(机位正对鎏金椭圆镜,实体背影占左下前景双层深度):貂皮披肩自上臂向肘窝滑落(肩主动下沉+重力),顺势滚肩;拍2 技术峰值=6.125-6.75s 回头压镜:头经右肩上方回旋、目光在镜像中直取镜头,披肩恰悬肘弯;拍3 6.875-7.25s 硬切实空间近景:双手自肩后抓披肩两端绕至胸前收拢(机位前推+景别收紧)
- H3:`standing at the gilt oval mirror seen through the glass, sliding the tan fur stole down from upper arm to elbow crook while rolling the shoulder, turning her head back over it to hold the lens inside the reflection, then pulling the stole around to her chest with both hands in a closer cut`
- 来源:《书架露背》05.375-06.75s、06.875-07.25s

**片<v75> 《香槟纱》(礼服写真·17.4s·竖屏)**
- 背景人物:灰色硬包拼接墙角+黑色皮凳,顶光均匀。人物:王羽杉——香槟米色抹胸礼服(上身罗纹收褶、超大朵廓形欧根纱袖、多层纱裙),银色星形吊坠项链,栗棕大波浪+刘海,粉色手机。AIGC:疑似(低),判真拍重磨皮——动作轨迹连续、手机道具跨 13s 形制稳定、无 morph 鬼影;肤质过度磨皮保留低概率。
- 节拍:约 75 BPM(推测·慢板)。
- 镜头形态:A 疑似一镜到底(0-16.7s 同机位)。

### K247 电梯角慢转头扫镜链(2拍|微活性·眼神节奏)
- 入态:左侧脸坐定、手机举于头侧 → 出态:头回正后右倾低垂、目线下沉
- 分解:拍1 2.6-3.4s 灰色硬包墙角坐定,粉色手机自头侧撤出画外,左肩微沉,目线垂向左下;拍2 技术峰值=3.4-4.2s 两拍完成慢转头:头沿水平轴从左侧脸滚向正前(胸锁乳突肌离心控制),目线中途两次触镜(3.475s/3.9s),随后头右倾 15° 目线落回下方(大波浪发尾延迟约 0.3s 摆正);欧根纱袖随呼吸起伏;固定机位无剪切
- H3:`seated against the grey panel corner in the champagne tulle gown, lowering the phone out of frame, drifting from left profile into a slow two-beat head turn that lands her eyes on the lens twice before tipping away down again, tulle sleeve bobbing with each breath`
- 来源:《香槟纱》02.6-05.0s

### K248 捻发下滑别发链(2拍|手部细节·发丝物理)
- 入态:右侧脸坐定、右手抬至锁骨 → 出态:发别回耳后、目线回镜头
- 分解:拍1 8.2-9.6s 指尖捏住胸前发梢(指屈肌捏合),顺发丝全长向下滑抹把卷发拉直,发丝在手下方延展后弹回波浪,垂眸盯手;拍2 技术峰值=9.95-10.575s 别发:腕内旋把整束发拢向耳后,掌根贴颊推压一次,目线在掌根离颊瞬间抬回镜头(眼神节奏=手落眼起)
- H3:`pinching a front strand of hair at chest height in right profile, sliding the fingers down its full length so the wave straightens and springs back, then re-raising the hand to sweep the hair behind her ear with the gaze dropping to the fingers and flicking up to the lens as the palm leaves her cheek`
- 来源:《香槟纱》08.2-10.6s

### K249 捏纱垂眸举机链(2拍|服装物理·道具互动)
- 入态:左侧脸低头、左手持粉色手机垂在裙上 → 出态:手机举至脸高、目线入屏
- 分解:拍1 13.2-15.2s 右手拇指食指捏住胸前欧根纱袖边缘细捻(遮挡物=抬起小臂+纱袖),捻出褶峰再抚平,垂眸盯手;拍2 15.2-15.575s 左手把手机自裙面提至脸高(纱先抚平→手机后举),目线投入屏幕(固定机位,手机占画幅 1/4)
- H3:`bowed in left profile, pinching and worrying the tulle sleeve edge at her chest between thumb and forefinger until the gauze peaks and smooths flat, then lifting the pink phone from her lap up to face level as her eyes drop into the screen`
- 来源:《香槟纱》13.2-15.6s

**片<v76> 《夜桥黑缎》(夜景街拍·9.7s·竖屏)**
- 背景人物:夜景天台/桥(金属栏杆+木地板),螺旋楼体、蓝紫 LED 高楼群、圣诞树、白色弧形沙发床。人物:王羽杉——黑色缎面吊带长裙(胸口银色水钻横带)、银色流苏臂环、栗棕大波浪;中段配奶油色长毛皮草。AIGC:否(真拍·重度美颜)——硬切干净无重影;夜景 LED 为真实光源;4.4-6.2s 抛发发丝级运动模糊自然;臂环跨镜佩戴左右不一致(多套实拍连续性瑕疵,反证非 AI 单源)。
- 节拍:约 96 BPM(推测·中速)。
- 镜头形态:C 快剪(≥7 机位硬切,3.0s 黑帧过渡)。

### K250 夜桥顺发下滑双回链(2拍|手部细节·发丝物理)
- 入态:手埋脑后肘上扬 → 出态:双手落定、重心换后腿、微入半步
- 分解:拍1 0.0-1.4s 夜桥眼高平拍全身:右手自脑后埋入发根,顺头侧滑出经下颌滑到锁骨(肩胛上提→逐节下放),头左倾 20°,髋右送;拍2 1.5-2.6s 硬切 LED 背景:左手自太阳穴梳前发帘向下滑,整束前发甩向对侧肩(惯性甩发),右臂横摆后收,重心换右腿微入半步;两次顺发均收在拍尾
- H3:`standing at the night railing with one hand buried behind her head, letting it slide out and down through the hair past the jaw while the head tilts into it, then after the cut raking the front hair down from the temple and tossing the whole sweep across to the other shoulder with a small step in`
- 来源:《夜桥黑缎》00.0-01.4s、01.5-02.6s

### K251 背影抓发抛落链(3拍|背线语义·发丝物理·背影机位)
- 入态:背面站定、手在体侧 → 出态:手回体侧、发幕贴脊、肩微抖收势
- 分解:拍1 4.4-5.15s 背面全身机位:双臂同时上举插入发根,肘向两侧扬至最高(斜方肌上束+肩胛上回旋),头随之下低;拍2 技术峰值=5.275-5.775s 抓拢释放:十指贴头皮向后脑抓拢整幅发幕,向上提离肩背一掌高后完全松手,发幕整体抛起成波浪再塌落回脊背(全组最重发丝物理点),肘沿两侧弧线坠落;拍3 5.9-6.2s 手落回体侧,双肩快速轻抖一次
- H3:`filmed from behind at the night railing, driving both hands up into the hair at the nape with elbows flared wide, raking the whole curtain up off the shoulders and releasing it so it lifts and crashes back down along the spine in a wave while the hands land at her sides and a quick shoulder shake settles the strands`
- 来源:《夜桥黑缎》04.4-06.2s

### K252 皮草搭臂提裙回眸链(3拍|服装物理·坐姿·回眸)
- 入态:白沙发前俯身、皮草覆双前臂 → 出态:栏杆侧影、裙摆攥在手中、头回旋压镜头
- 分解:拍1 3.9-4.3s 白色弧形沙发机位:奶油皮草整幅搭双前臂,左前臂搁沙发沿,指尖轻敲两下,下颌上抬 10°;拍2 6.3-7.3s 软垫坐姿:右腿跨压左腿,皮草挂双肩,右手把缎面裙边向膝外拨平,裙衩随拨开合一次;拍3 技术峰值=8.0-9.7s 栏杆侧影:右手攥住裙摆向大腿提起一攥(缎面在拳中堆褶),头经肩上回旋直取镜头(回眸)
- H3:`draping the cream fur coat over both forearms on the white curved sofa with fingertips drumming the edge once, then seated cross-legged smoothing the satin hem out over the knee, and at the railing bunching the dress hem up in her fist before spinning her head back over the shoulder to pin the lens`
- 来源:《夜桥黑缎》03.9-04.3s、06.3-07.3s、08.0-09.7s

**片<v77> 《生日粉纱》(少女写真生日房·8.0s·竖屏·AI 高置信)**
- 背景人物:写真馆生日房(白护墙板、黑金"HBD/BIRTHDAY"三角旗串、黑皮沙发、圆镜、花墙布景、金螺旋蜡烛)。人物:粉色抹胸蓬蓬纱公主裙(超大 tulle 裙撑),粉色蝴蝶结头纱,水钻 choker,白色纱袖长手套,粉色手机。道具:奶油三层蛋糕→黑莓果小圆蛋糕(形制突变)。AIGC:是(高置信)——1.0s 人脸+蛋糕双影 morph;4.85s 泛光转场鬼影;5.6s 花瓣粒子凭空生成且前后景深穿插(合成层穿模);6.7s 烛台凭空入画。
- 节拍:约 85 BPM(推测·梦幻慢板)。
- 镜头形态:B 快照幻灯(泛光 morph+粒子特效串联 5 机位)。

### K253 拳掌抛送花瓣生链(3拍|手势·特效触发·道具互动)
- 入态:黑皮沙发坐定、右拳举于颌侧 → 出态:手收回托腮、花瓣环绕持续
- 分解:拍1 4.975-5.475s 黑皮沙发机位:右拳松握举在颌侧,腕放松随节拍轻晃,嘴张开作讶异态;拍2 技术峰值=5.475-5.725s 拳变掌:五指自拳心依次展开成掌心向上的抛送手势推向镜头,5.6s 粉色辉光迸发、花瓣粒子自掌位生成螺旋环绕全身(特效触发点);拍3 5.85-7.4s 手收回,纱手套托腮,头随花瓣微倾三次
- H3:`raising a loose fist beside her chin with a wide-eyed look at the lens, unfurling it into an upward palm-offer toward the camera as pink glow bursts and petal particles ignite and spiral around her, then sinking the hand back to rest her cheek on the sheer glove while the petals keep drifting`
- 来源:《生日粉纱》04.975-05.725s、05.85-07.4s

### K254 镜前比心托腮链(2拍|自拍手势·特效环绕)
- 入态:圆镜前举手机 → 出态:托腮定格、花瓣前后景穿插
- 分解:拍1 2.333-3.475s 圆镜自拍机位(粉手机举于镜前):食指中指比 V 抵下颌侧,头左倾 10°,噘唇作飞吻预备;拍2 5.85-7.4s 黑皮沙发托腮(承接 K253 拍 3 持续态):花瓣粒子在人物前后景深交替穿插(前后遮挡=AI 合成层),目线锁镜头
- H3:`holding the pink phone up to the round mirror for a selfie with a V-finger pressed at her chin and a blown-kiss pout, then resting her cheek into the sheer glove with elbow planted while petal particles pass in front of and behind her and the gaze stays pinned on the lens`
- 来源:《生日粉纱》02.333-03.475s、05.85-07.4s

**片<v78> 《豹纹变装》(室内变装·7.8s·竖屏)**
- 背景人物:极简室内(棕墙+米地板、圆形光池)。Look1:白色短款羽绒服+白微喇裤+白毛毛厚底靴,双手各拎豹纹细带高跟鞋;Look2:黑高领中袖上衣+豹纹缎面包臀迷你裙+同款豹纹高跟鞋。AIGC:否(真拍跳剪变装·疑似 AI 美体拉腿)——3.4s 变装干净硬切、抬腿姿态跨切精确匹配、无 morph;双腿比例超长、膝部过度平滑。
- 节拍:约 128 BPM(推测·变装 drop 卡点)。
- 镜头形态:B 双镜跳剪变装(切点 3.4s;7.5s 渐暗淡出)。

### K255 白套抬腿变装跳剪链(3拍|变装跳剪·道具转移·卡点)
- 入态:白羽绒服套装双手持鞋、单腿横摆 → 出态:豹纹裙踩上同款高跟、猫步第一步启动
- 分解:拍1 2.9-3.4s 体重压右腿,左腿直膝上摆横跨,白毛毛靴绷脚,双手各拎豹纹细带高跟鞋向两侧平展如翼(道具双持);拍2 变装跳剪=3.4s(推测 drop 卡点,硬切无 morph):同一抬腿姿态穿豹纹细带高跟重新入画,脚尖先行点地落下,双臂空手沿原摆动弧线走完——手中鞋"转移"到脚上,变装核心魔术;拍3 3.525-4.15s 落地收势,猫步启动
- H3:`swinging one straight leg up in a crossed lift with the white fuzzy boot pointed and both hands holding the leopard strappy heels out to the sides like wings, cutting on the drop so the same lifted leg re-enters wearing those heels and lowers toe-first while the empty arms finish the swing arc, then gathering weight into the first catwalk stride`
- 来源:《豹纹变装》02.9-04.15s

### K256 豹纹直线猫步抓发链(3拍|台步·抓发·直线借位)
- 入态:猫步第一步启动 → 出态:抓发不放、步频不减、渐暗淡出
- 分解:拍1 4.15-5.6s 直线借位猫步(机位胸高固定):每步膝部几乎互擦(直线借位),高跟先掌后跟落地,髋随重心左右滚动;拍2 5.6-5.975s 右手抓握右肩前发束一整把拉离颈部;拍3 6.0-7.45s 抓发持续走:步频摆髋不减,手把发束向外拉紧再放松两次(6.85s/7.35s);7.475s 渐暗
- H3:`catwalking dead straight toward the lens with each knee brushing past the other thigh and the hips rolling over the heels, gripping a full bunch of hair at the right shoulder and tugging it taut twice through the stride while the left arm counters wide, until the fade`
- 来源:《豹纹变装》04.15-07.45s

**片<v79> 《贴地捡玩具》(居家厨房贴地机位·7.2s·竖屏)**
- 背景人物:家居厨房/餐边(浅木地板、白柜体),镜头贴地约 20cm 仰角固定;道具红黑迷你玩具车前景。人物:王羽杉——黑色金扣西装大衣+黑色短裙内搭,灰透光泽丝袜,黑漆皮尖头细高跟(红底),金大耳环,栗棕大波浪。实拍(1.6-1.75s 坍坐真实运动模糊、漆皮鞋反光实时变化;腿部拉长磨皮)。
- 节拍:约 88 BPM(推测·中慢板)。
- 镜头形态:A 一镜到底(贴地固定机位;6.6s 渐暗)。

### K257 并膝下蹲坍坐悬指链(4拍|蹲姿纪律·贴地机位·眼神反差)
- 入态:画外入走向玩具 → 出态:贴地坐定、指尖悬停玩具上方、目线压镜头
- 分解:拍1 0.6-1.2s 贴地机位:灰丝袜小腿+黑漆皮细跟自画左走入,步幅收小停在玩具上方;拍2 技术峰值=1.2-1.5s 并膝优雅下蹲:双膝全程并拢("拍照从不批腿"纪律)屈膝下沉,一手顺势下抚裙摆压住走光点,另一臂前伸;拍3 1.6-1.75s 快速坍坐(全片最快动作、强运动模糊):蹲位直接落坐地面,一手撑地缓冲;拍4 1.85-3.0s 悬指挑逗:右手五指张开悬停玩具上方 3-5cm 小幅摆动始终不触,目线全程压镜头而非看玩具(眼神反差)
- H3:`walking in over the floor-level lens toward the fallen toy, folding down into a knees-pressed-together squat with one hand skimming the skirt hem down the thigh to hold it, collapsing in one motion-blurred beat to the floor with a palm catching behind her, then hovering splayed fingertips above the toy without touching while the eyes stay locked on the lens`
- 来源:《贴地捡玩具》00.6-03.0s

### K258 贴地伸腿红底弹踢链(3拍|腿部细节·鞋底语义·贴地机位)
- 入态:贴地侧坐、左腿长伸 → 出态:回落后再伸、趾尖缓屈、定格至淡出
- 分解:拍1 4.3-4.55s 贴地侧坐定格:左腿沿地板向画面右下长伸占对角线,大衣下摆铺地成扇面,头倒向镜头;拍2 技术峰值=4.675-4.925s 红底弹踢:左足连小腿快速上撩踢向玩具方向,4.8s 红色鞋底正对镜头闪现一次(鞋底语义=瞬间亮牌);拍3 5.05-6.7s 回落重置:膝弯把腿收回叠好,再重新长伸至镜头前,趾尖约 2 秒一次缓屈缓伸,目线锁镜头;6.6s 渐暗
- H3:`holding the floor sprawl with one stocking leg laid long toward the lens, flicking that foot up fast so the red sole flashes at the camera, retracting it under her in one bend, then re-extending the long leg with slow two-second toe flexes while the gaze stays pinned on the lens until the fade`
- 来源:《贴地捡玩具》04.3-06.7s

**片<v80> 《车库百褶》(地下车库 OOTD·11.7s·竖屏)**
- 背景人物:地下停车场(灰环氧地坪、黄车位线、顶灯管、玻璃隔间、发光出口牌)。人物:王羽杉——黑色修身小高领中袖上衣,灰色百褶迷你裙+黑色双带扣腰带,黑色过膝袜(绝对领域),黑厚底圆头玛丽珍;栗棕大波浪。实拍(车库实景管线/指示牌清晰、硬切无 morph;腿部与袜面 AI 美肤)。
- 节拍:约 100 BPM(推测·中速)。
- 镜头形态:C 快剪(4-5 机位:眼高全身→膝高纯腿→上身近景→纯腿)。

### K259 车库交叉步停格链(3拍|台步·入画对焦·停格站姿)
- 入态:失焦走近 → 出态:X 腿站姿定格、手归位发侧
- 分解:拍1 0.0-0.375s 失焦入画走向镜头,0.25-0.375s 对焦拉实(焦点先于姿态到位);拍2 0.375-1.75s 走近(眼高固定,车库透视线汇聚):左手插鬓角发内,右臂横抱胸下,厚底玛丽珍步频稳,1.25-1.75s 每步落点越过身体中线成交叉步;拍3 技术峰值=1.875-2.375s 停格:重心坐进后腿,前膝内扣成 X 腿,右手鬓边捻发归位,下颌内收目线抬压镜头;2.375s 硬切大腿机位
- H3:`walking toward the garage lens out of focus until the pull sharpens, one hand tucked at the temple and the other arm folded under her chest, crossing each step over her center line before dropping the weight into the back leg and knocking the front knee inward for the held X-leg pose with a chin dip`
- 来源:《车库百褶》00.0-02.375s

### K260 踮脚转踝换向交叉链(3拍|腿部细节·袜品物理·纯腿机位)
- 入态:腿部特写、小腿交叉站 → 出态:反向再交叉、趾尖剪刀步、微弹收
- 分解:拍1 9.45-10.2s 纯腿机位(膝高平拍,百褶裙下缘+过膝袜口+厚底鞋三段构图):双腿小腿位交叉,前脚趾尖点地踮起、足跟离地轻颤两下(小腿三头肌提踵),袜口在大腿压出微褶、袜筒跟部随提踵起皱;拍2 技术峰值=10.325-10.95s 转踝画圈:前足足跟落地为轴,踝内旋让脚尖在地面画小弧,膝随之下探加深;拍3 11.075-11.575s 换向交叉:双腿解开向反方向再交叉,前足搭后足脚背上方成剪刀步,膝部小弹收住
- H3:`in the legs-only cut crossing the shins and rising onto the front toe with the heel lifting to tremble twice, pivoting that heel down to rotate the ankle through a small arc as the knee dips deeper, then uncrossing and re-crossing the other way with the front toe scissored over the instep and one small bounce to settle`
- 来源:《车库百褶》09.45-11.575s

**片<v81> 《恶劣御姐变装》(御姐摆拍变装·8.2s·竖屏)**
- 背景人物:室内单机位,米灰竖条纹吸音墙+暖光顶灯带。人物:王羽杉——棕卷发,白框眼镜,黑高领毛衫裙(白方腰扣)+黑红格纹百褶短裙+黑尖头高跟;腿部装束两次变化(裸腿→黑过膝袜双吊带夹→灰透丝袜),结尾手持摘下的眼镜。AIGC:疑似 AI 修形增强(腿异常细长、膝部蜡质);变装本体为真硬切(3.08→3.20s、5.50→5.62s 相邻帧切换,无过渡形变帧)。
- 节拍:约 95 BPM(推测,慢速 trap/r&b)。
- 镜头形态:C 快剪(同机位两处跳切,手部掩剪)。

### K261 静位跳切袜变装链(3拍|变装跳剪·同机位·手位掩剪·卡点)
- 入态:裸腿交叉腿静位摆拍 → 出态:黑过膝袜同姿态静位
- 分解:拍1 0.0-3.08s 双腿交叉站立(右腿前叠),重心锁死右腿,右手指尖抵下巴、左手背于腰后——纯静位蓄拍;拍2 3.08→3.20s 硬切(8fps 密帧证实相邻帧切换、无过渡形变帧):同机位同景别,裸腿瞬间变黑不透明过膝袜+双吊带夹,手位由下巴滑至鬓角掩剪,交叉腿姿态逐像素复刻;拍3 3.20-5.38s 袜态微摆:肩部呼吸起伏、指尖回落锁骨
- H3:`holding a static crossed-leg pose with a fingertip at the chin then jump-cutting on a small hand-to-hair move so bare legs instantly reappear in opaque black thigh-highs with garter straps while the identical crossed-leg stance repeats`
- 来源:《恶劣御姐》03.08-03.20s(蓄拍 0.0-3.08,延展至 05.38)

### K262 二段换袜摘镜收势链(3拍|变装跳剪·道具上手·连续收势)
- 入态:黑过膝袜抬手位 → 出态:灰透丝袜+手持眼镜收势
- 分解:拍1 5.38-5.50s 黑袜态右手抬至肩高指尖向上、髋左微顶(蓄切姿势);拍2 5.50→5.62s 第二次硬切:黑袜→灰透丝袜(吊带夹消失),抬手轨迹无缝延续至鬓角——切点藏于指尖到达发丝瞬间;拍3 5.75-6.12s 镜内连续摘镜:右手上行捏住白框眼镜沿颧骨向外平抽,离面后挂指间轻荡,头前倾回正——全片唯一镜内连续动作
- H3:`jump-cutting mid hand-raise so opaque thigh-highs become sheer grey tights with the raised hand uninterrupted, then continuously sliding the white glasses off the face and letting them dangle from the fingers as the closing beat`
- 来源:《恶劣御姐》05.50-06.12s

**片<v82> 《高尔夫四宫格》(分屏变装舞蹈·9.3s·竖屏·疑似 AIGC)**
- 背景人物:同一现代室内(木饰面板墙+黑吊灯),画面 2x2 四分屏,四轨=同一动作时间线四条并行素材。初始四轨同装黑色长袖连体短裤;错拍变装后:浅蓝露肩宽松上衣/灰吊带背心+黑短裤/黑连体+棕腰带(基准轨)/黑吊带交叉背带裙,结尾 BR 轨压轴变酒红高领+灰短裙+黑丝+工牌。AIGC:疑似 AIGC 图生视频四分屏(手部挥动粉色涂抹虚影、面部过度平滑、四轨帧级微不同步);变装为分轨真硬切(2.00→2.12s 相邻帧瞬间换装)。
- 节拍:约 120 BPM(推测,四轨变装点互差错拍)。
- 镜头形态:C 快剪(嵌套结构:整片一轨,轨内各自跳切)。

### K263 四宫格错拍跳切变装链(4拍|分屏变装·分轨跳切·错拍卡点)
- 入态:四轨同装黑连体同步起手 → 出态:四轨四装同框定格(职场装压轴)
- 分解:拍1 0.0-2.00s 2x2 四轨同装同步:掩口手→双臂向侧下横扫(1.5-1.9s 高速挥臂成粉色涂抹虚影),躯干启动右转;拍2 2.00→2.12s TL 轨硬切:浅蓝露肩宽松长上衣瞬间替换黑连体,转身相位无位移——第一拍变装;拍3 2.12-7.05s 错拍连环:TR 轨先切黑吊带裙再切灰吊带+黑短裤,BR 轨切黑吊带交叉背带裙,BL 轨保持黑连体+棕腰带作基准轨;拍4 7.33-7.67s BR 轨压轴切酒红高领+灰短裙+黑丝+工牌挂绳,四装同框收尾
- H3:`running four synchronized copies of the same side-turn choreography in a 2x2 grid and jump-cutting each panel into a different outfit on staggered beats — light-blue off-shoulder first, black slip then grey cami with shorts, closing on a burgundy turtleneck office look with a work lanyard`
- 来源:《高尔夫四宫格》02.00-02.12s(机制主证)、02.12-07.67s(错拍延展)

### K264 挥杆扫臂转身背影杀链(3拍|舞蹈·背影·分屏同步·惯性延续)
- 入态:掩口手站姿 → 出态:全背面双手后交定格
- 分解:拍1 1.50-1.90s 掩口手落,双臂合力向右下横扫(高尔夫挥杆式发力:肩胛先行、手腕末端甩出),重心右移;拍2 1.90-4.20s 惯性转身:躯干右转约 90° 经侧对位,胯前顶,四轨同步走完同一弧线;拍3 4.20-7.05s 全背面:双手交叠于体后低处、肩胛收拢,浅蓝轨背部系带在转身惯性中甩出摆动
- H3:`sweeping both arms down and across like a golf swing so the fast hands blur pink, then carrying the momentum through a side profile into a full back view with hands clasped low behind the body as hair and tie-straps settle from the turn`
- 来源:《高尔夫四宫格》01.50-04.20s(背影延展至 07.05)

**片<v83> 《杀杀杀》(评论回复变装舞蹈·20.3s·竖屏)**
- 背景人物:与 w29 同款竖条纹墙板+木地板场景。人物:王羽杉——前期湖蓝色宽松睡衣套装+鲨鱼夹半扎发+十字项链,画面叠后期评论气泡("敢发弄死你"→"给我看看你的手段");变装后黑色蕾丝拼丝绒束身衣+黑色毛呢短裤+白色钻扣腰带、CHANEL 颈链、大圈耳环、金表。AIGC:疑似 AI 增强(皮肤蜡质、腰臀比夸张);变装转场为"撞镜模糊缝合"(5.38-5.62s 全模糊区间换装,判镜内拼接/剪辑缝藏于模糊)。
- 节拍:约 105 BPM(推测,"杀杀杀"挥砍逐拍对位)。
- 镜头形态:C 快剪(一处缝合转场,其余单镜舞蹈+摆姿)。

### K265 交叉挥砍杀杀杀舞蹈链(3拍|舞蹈·发力对位·服装物理)
- 入态:睡衣手扶胯站姿 → 出态:摊手收拍
- 分解:拍1 3.95-4.20s 右手由腰侧提起,双腕交叠于胸前高位成 X,掌心向外——"杀杀杀"起手;拍2 4.20-4.45s 双肘外展,前臂沿对角线下劈至体侧,发力=肩带+背阔,宽松睡衣袖随劈砍滞后鼓起;拍3 4.45-4.83s 双掌翻为掌心向上于腰前摊开,躯干随节拍小幅左右摆(绿色评论气泡以模糊横条滑入,后期 UI)
- H3:`crossing both wrists high in front of the chest then slashing the forearms down along diagonals so the loose pajama sleeves billow behind each cut, and flipping palms up to present open hands at the waist while the torso sways on the beat`
- 来源:《杀杀杀》03.95-04.83s

### K266 撞镜模糊缝合变装链(3拍|变装·撞镜缝合·焦点回落)
- 入态:睡衣双臂落定中景 → 出态:黑束身衣拉出续舞
- 分解:拍1 5.00-5.25s 睡衣双臂落至体侧静止(中景全身);拍2 5.25-5.50s 镜头急推撞向胸口:5.38s 全身涂抹模糊→5.50s 深色发块占满画面,运动模糊掩埋剪辑缝;拍3 5.62-6.38s 拉出即换装:黑蕾丝束身衣+短裤+CHANEL 颈链+金饰已穿好,焦点 0.2s 内回位,双手胸前小跳拍打续接——推拉距离物理上不可能镜内完成,判"模糊缝合"
- H3:`rushing the camera into an extreme close-up of hair and chest so heavy motion blur fills the frame, then pulling straight back to reveal the black lace corset outfit already worn as focus snaps back within a fifth of a second`
- 来源:《杀杀杀》05.25-05.62s(缝合主证)、05.62-06.38s(续舞)

### K267 拇指下滑抚腿摆姿链(3拍|摆姿·视线引导·腿部线条)
- 入态:束身衣竖拇指 → 出态:双手膝上并膝站定
- 分解:拍1 15.40-15.65s 右手竖大拇指于右胸前,肘部架住束身衣上缘;拍2 15.65-15.90s 拇指沿胸口中线向下滑至腰际,四指松开(滑动摩擦引导视线下行);拍3 16.02-16.67s 双手掌心顺大腿前侧下滑停于膝上,双膝并拢微叠,胯向左顶
- H3:`sliding a thumbs-up gesture down the sternum to the waist then gliding both palms down the fronts of the thighs to rest above the knees as the hips cock left with the weight locked on the right leg`
- 来源:《杀杀杀》15.40-16.67s

**片<v84> 《从不批腿》(脚部创意转场+并膝摆姿·6.5s·竖屏·混合)**
- 背景人物:两段。前段:木地板俯拍特写,白罗纹毛线袖套套住小腿足背,红趾甲,绿数据线收纳盒;后段:办公室灰白滚轮椅+条纹墙板,黑蜘蛛印花无袖皮感上衣+黑短裤+过肘皮手套+灰透过膝袜(白袜口)+黑细高跟。AIGC:前段实拍;后段疑似 AI 插帧/增强(5.33s、6.0s 糊化闪烁、袜口与皮肤交界熔化)——全片判混合。
- 节拍:约 90 BPM(推测)。
- 镜头形态:C 快剪(线牵引甩镜缝合两段)。

### K268 脚趾按压拉线开篇链(3拍|足部特写·道具操作·蓄力留白)
- 入态:线盒着地线松弛 → 出态:拉线横贯满绷
- 分解:拍1 0.00-0.67s 木地板俯拍特写:白色罗纹毛线袖套套住小腿足背,红趾甲的趾腹压住浅绿数据线收纳盒,金属拉线松弛弧线拖地;拍2 0.67-1.67s 趾缝发力:拇趾与二趾夹紧盒盖,足弓下压固定,脚尖沿线滑动拨线——线由松弛转为绷直;拍3 1.67-2.20s 足部出画,只剩绷直银线横贯画面(留白蓄转场)
- H3:`pressing a mint cable reel flat against the wood floor with painted toes wrapped in a fuzzy knit legwarmer, gripping the lid between the first two toes as the retractable cable pulls taut across the empty frame`
- 来源:《从不批腿》00.00-02.20s

### K269 线牵引甩镜缝合转场链(3拍|转场·道具牵引·甩镜模糊)
- 入态:绷直的线 → 出态:线系踝+过膝袜坐姿显影
- 分解:拍1 2.20-2.45s 绷直线横贯画面,镜头沿线走向横向甩动(线=甩镜轨迹);拍2 2.45-2.83s 甩镜模糊:地面、椅腿、黑丝小腿 0.3s 内拉成斜向涂抹(真实手持甩镜);拍3 2.83-3.00s 显影收点:灰白办公椅上坐定,灰透过膝袜+黑高跟已穿好,线之彼端以粉白绳结"系"在右脚踝——拉线→系踝的道具逻辑闭合
- H3:`whip-panning along the taut cable so the frame smears across the floor, then settling on her seated on the office chair in grey thigh-highs and black heels as the other end of the cord is now tied around her extended ankle`
- 来源:《从不批腿》02.20-03.00s

### K270 并膝交腿手套抵唇摆姿链(3拍|摆姿·并膝纪律·微摆)
- 入态:椅上半躺举腿 → 出态:交腿定格歪头
- 分解:拍1 3.00-4.80s 半躺椅面,双膝全程并拢抬起,右小腿叠压左小腿(踝交叠而双膝不分开——"拍照从不批腿"纪律语义),黑皮长手套抵下巴;拍2 4.80-5.42s 微摆:胯部随节拍小幅起伏、膝位锁死,仅脚踝沿轴心小旋转;拍3 5.42-6.33s 两次糊化闪烁(疑似 AI 插帧)后定格:交腿不变,头歪向左肩,手套指尖勾住袜口
- H3:`reclining on the office chair with both knees clamped together and only the ankles crossed, keeping the knee gap closed while the hips pulse on the beat and a long black opera glove rests against the chin until the fingers hook the stocking top`
- 来源:《从不批腿》03.00-06.33s

**片<v85> 《杭州入夏腿》(POV 拖箱+影子秀·14.5s·竖屏·约 22fps)**
- 背景人物:户外白天广场/街道,灰砖+黄盲道+回字纹铺装+黄路障,强投影。人物(全程未露脸):红趾甲、裸色绑带平底凉鞋、白花边裙摆+黄花短裙、右手拖黄色 24 寸行李箱、长发(由影子证实)。实拍(真实阴影、行李箱拖动物理、手持抖动,无磨皮与形变)。
- 节拍:约 110 BPM(推测,轻快 vlog BGM,步频松对位)。
- 镜头形态:A 一镜到底(手持 POV 连续,中段仅上摇)。

### K271 拖箱 POV 步态链(3拍|POV 行走·道具物理·空间推进)
- 入态:低头 POV 起步 → 出态:回字纹铺装区连续行走
- 分解:拍1 0.00-1.02s 低头 POV:左脚先落(红趾甲+裸色绑带凉鞋),右臂垂直拖黄色行李箱,箱体每步磕碰一次地砖(声点物理),白花边裙摆+黄花裙沿画框下缘晃动;拍2 1.02-2.33s 步态周期:右腿蹬地→左腿前摆交替,步幅约 0.7 身位,裙摆随髋滞后半拍扬起;拍3 2.33-5.50s 连续行走:灰砖→黄盲道→回字纹,镜头随步频自然点头
- H3:`walking forward in a first-person downward view as bare legs in strappy sandals alternate strides, one hand dragging a yellow suitcase that knocks the pavement each step while the ruffled skirt hem sways half a beat behind the hips`
- 来源:《杭州入夏》00.00-02.33s(周期主证),延展至 05.50

### K272 抬镜影子秀转场链(3拍|转场·无切上摇·剪影构图)
- 入态:看脚 POV → 出态:影子全身同步行走
- 分解:拍1 5.50-5.88s 行走中镜头上摇,视线由脚尖转向前方地面,中段迈步无切;拍2 5.88-6.62s 影子渐入:阳光把全身影投上回字纹地砖,镜头上摇至影子全身入画(长发、收腰、拖箱臂剪影);拍3 6.62-14.33s 影子行走展示:影子与真实脚步逐帧同步,行至黄路障小幅绕行,结尾影子站定双手扶箱拉杆
- H3:`tilting the camera up from the feet to reveal her own full-body shadow stretching across the patterned pavement, then walking so the long-haired suitcase-pulling silhouette strides in sync with the real steps`
- 来源:《杭州入夏》05.50-06.62s(转场主证)、06.62-14.33s(延展)

**片<v86> 《腿精》(蓝椅变装腿部展示·9.6s·竖屏·疑似 AIGC)**
- 背景人物:现代客厅,米灰条纹墙板+壁挂 TV+蓝色潘顿式 S 椅(全片唯一道具)。人物:王羽杉——棕长直发+刘海,米白高领紧身上衣不变;下装两次变化:奶白工装阔腿裤+白厚底鞋→金色缎面短裙+裸腿+裸色铆钉缠绕细高跟;开场右手拎黑色 YSL 高跟鞋。AIGC:疑似 AIGC 图生视频——4.50s/7.22s 双重人像叠影、椅影漂移、腿比拉长;变装本体为踢腿掩剪真硬切(2.65→2.77s)。
- 节拍:约 90 BPM(推测,慢摇)。
- 镜头形态:C 快剪(三段机位,段间 AI 变形缝合)。

### K273 起身踢腿掩剪变装跳剪链(4拍|变装跳剪·道具转移·踢腿掩剪)
- 入态:蹲椅持鞋工装裤 → 出态:金裙+铆钉高跟落腿收势
- 分解:拍1 0.00-2.15s 蹲踞蓝 S 椅座面:米白高领+奶白工装裤+白厚底鞋,右手拎黑 YSL 高跟,左手撩发蓄势;拍2 2.15-2.65s 臀部滑下坐定,双腿向前踢出(鞋底朝镜),手中鞋随下沉荡至膝侧;拍3 2.65→2.77s 硬切(切于踢腿最高帧):工装裤+运动鞋→金缎短裙+裸腿,手中 YSL 鞋"转移"为脚上裸色铆钉高跟,双腿沿同一前伸轨迹落下;拍4 2.77-3.30s 落腿收势:双腿并拢直伸搁椅沿、绷脚尖,鞋跟悬空轻晃
- H3:`kicking both legs out from the chair seat in white sneakers and jump-cutting at the top of the kick so the cargo pants become a gold satin mini skirt with the held pumps now strapped onto her feet as the legs descend along the same arc`
- 来源:《腿精》02.15-02.77s(切点主证)、02.77-03.30s(收势)

### K274 举腿 V 位-交腿落姿链(4拍|腿部线条·AI 变形过渡判别)
- 入态:后仰举腿 V 位 → 出态:正面交腿"腿精"构图
- 分解:拍1 3.00-4.38s 后仰靠椅,双腿并拢伸直举成 V 位(足跟高于椅背)、绷脚背(侧低机位+椅面高度拉出全腿线,技术峰值);拍2 4.38-4.62s AI 变形过渡帧:4.50s 双重人像叠影、椅沿复制——非真实运动模糊,判 AI 图生视频过渡(与真跳切判别依据);拍3 4.62-5.67s 落姿:双腿沿体前下落成交叠位,上身回正、左手滑至颈侧;拍4 6.85-7.35s 第二次 AI 变形(7.22s 肢体复制鬼影)后切正面全景
- H3:`reclining to raise both straight legs into a V above the chair back with pointed toes, then lowering through an AI-morphed ghost frame into a knee-over-knee cross with one hand sliding to the neck and the long leg line facing camera`
- 来源:《腿精》03.00-04.62s(V 位主证)、04.62-05.67s、06.85-07.35s(落姿与二次过渡)

**片<v87> 《纯欲手搓变装》(单镜搓脱变装·6.4s·竖屏)**
- 背景人物:与 w29/w31 同场景系列(竖条纹墙板+木地板)。人物:王羽杉——棕长发中分,钻链 choker,初始 oversized 白 T(下衣失踪+裸腿);变装后金色香槟亮片网面紧身吊带短裙(预穿在 T 内),左手腕表。AIGC:单镜连续实拍布料操作+重度 AI 美颜;3.40-3.52s 全屏白糊为布料扫过镜头的运动模糊而非 AI morph——密帧证实布料位置逐帧连续。
- 节拍:约 120 BPM(推测,"搓脱完成"对重拍)。
- 镜头形态:A 一镜到底(变装在镜内以真实布料操作完成)。

### K275 白 T 搓脱单镜变装链(4拍|单镜变装·布料物理·预穿揭幕)
- 入态:白 T 下衣失踪站定 → 出态:金亮片裙全裸露+白布罩头
- 分解:拍1 1.90-2.40s 双手捏住宽松白 T 两侧衣摆向上向外拉——金色亮片紧身裙自 T 内露出上沿(预穿揭幕);拍2 2.40-3.02s 连续上搓:双臂沿躯干卷推衣身,T 恤罩过面部(2.90s 全遮脸),金裙完全裸露,肘外张;拍3 3.15-3.52s 甩头脱出:T 恤自头顶翻脱,白布扫过镜头形成全屏运动模糊(布半透可见身形)——单镜无切,密帧逐帧连续证实布料位置;拍4 3.65-4.15s 白布圈套过头顶落至双肩成披肩,双臂高举过顶 V 形拉伸
- H3:`gripping the oversized white tee hem and rolling it up the torso over the face to reveal a gold sequin mini dress worn underneath, throwing the shirt off the head in one continuous take so the flying fabric blurs across the lens and lands draped over both shoulders`
- 来源:《手搓变装》01.90-04.15s

### K276 甩布收势胯摆链(3拍|收势·服装物理·卡点定格)
- 入态:白布披肩双臂高举 → 出态:右手提布胯摆定格
- 分解:拍1 4.15-4.65s 白披肩自双肩向右臂滑脱,右肘下沉接布、左手落至腰侧;拍2 4.65-4.90s 右手收布成团垂于体侧,肩线回正;拍3 4.90-6.00s 定格收势:金裙胯部随节拍左右小摆两次,右手提布轻晃,choker 与裙面钻光收尾
- H3:`sliding the white shirt off both shoulders down the right arm to gather it in one hand at the side, then swaying the hips twice in the gold sequin dress as the closing pose`
- 来源:《手搓变装》04.15-06.00s

**片<v88> 《黑丝纯欲》(御姐摆拍·7.97s·竖屏)**
- 背景人物:现代开放厨房/吧台区——深色大理石岛台、暖黄灯带、微波炉+奶油色水壶、深灰双开门冰箱、绿帘。人物:王羽杉——红棕大波浪+空气刘海;黑色紧身无袖高领上衣+黑色双排扣腰带短裙+灰紫油光裤袜+黑漆皮红底细高跟;金手镯金表水滴耳环;墨镜与透明框眼镜轮换。AIGC:真人实拍+重度美颜美体,非全 AIGC(手部五指正常、厨房道具几何与镜面反射稳定;腿长/腰臀比切点前后突变=拉腿液化);8fps 密帧证实全部姿态切换为硬跳切、无 AI 渐变形帧。
- 节拍:~75-90 BPM 慢速律动(推测,切点 1.1/2.2/3.1/4.5/6.5s 落拍不规则)。
- 镜头形态:C 快剪(同景 5 段固定机位跳切)。

### K277 吧台坐姿交叉腿甩发链(3拍|御姐摆拍·定妆开场·发浪惯性)
- 入态:端坐吧台沿、右腿叠左腿、头左倾蓄力 → 出态:发落披肩、双臂侧下延展定妆
- 分解:拍1 0.00-0.33s 颈部发力向左甩头,发浪自右肩抛出,右手抬至发根借力——先转头带发;拍2 0.33-0.67s 发浪惯性越过左肩继续左前弧线(技术峰值:发梢扬至肩上 30cm),右臂向体侧下打开,叠腿与坐骨锚点纹丝不动——发力只在上半身;拍3 0.67-1.05s 发丝回落披散,双臂落至台面高度指尖向外延展,下颌回正对镜,墨镜反光定格;回收顺序"先臂后头再视线"
- H3:`sitting on a marble kitchen island with legs crossed, whipping long auburn hair from right to left in a slow arc while both arms extend down to the countertop and settle into a glam pose`
- 来源:《黑丝纯欲》00.00-01.05s

### K278 跳切换姿五连机制链(6拍|御姐摆拍·同装跳切·眼镜轮换)
- 入态:坐姿定妆 → 出态:抱膝坐定妆(第五站)
- 分解:拍1 1.05→1.18s 硬切 A(8fps 主证):坐姿→台面青蛙跪,墨镜→透明框眼镜同步换款,切点前后无过渡帧;拍2 1.18-2.20s 跪姿单手扶红底鞋跟、回眸看镜;拍3 2.20→2.33s 硬切 B:跪→侧卧台面,双腿向镜头纵深伸展;拍4 3.10→3.33s 硬切 C:侧卧→背身站立抬手拢发;拍5 4.50→4.67s 硬切 D:站→台面深蹲;拍6 6.40→6.67s 硬切 E:深蹲→抱膝坐收尾——五段同装同景,仅姿态/景别/眼镜款轮换,变装机制=纯后期跳切;音乐触发:各切点落慢鼓拍(推测)
- H3:`jump-cutting through five static glam poses on one kitchen counter — seated, kneeling, side-lying, standing and deep squatting — swapping tinted sunglasses for clear frames on every hard cut while the black outfit stays identical`
- 来源:《黑丝纯欲》01.05-01.18s(机制主证)/02.20-02.33s/03.10-03.33s/04.50-04.67s/06.40-06.67s

### K279 深蹲拢发放落链(4拍|御姐摆拍·发型打开·俯仰角切换)
- 入态:台面深蹲双膝外展、双手举顶 → 出态:单手扶膝、俯视镜头定妆
- 分解:拍1 4.67-5.00s 双手举过头顶十指插发向后拢(肱三头肌上举),重心沉进红底鞋跟;拍2 5.00-5.33s 指根松开发团凭重力垂落,头主动左偏让发从右侧泻下——技术峰值:发瀑展开瞬间;拍3 5.33-6.00s 右手捋发到胸前把玩,左手下滑扶膝,躯干前倾;拍4 6.00-6.40s 手落膝侧,视线由俯视转直视镜头定格
- H3:`squatting on the countertop in stiletto heels, gathering her hair overhead with both hands then releasing it to cascade down while one hand slides to the knee and the torso leans into the camera`
- 来源:《黑丝纯欲》04.67-06.40s

**片<v89> 《我的发》(御姐遮手变装·5.2s·竖屏)**
- 背景人物:素色木纹墙单景。人物:王羽杉——红棕长卷发;段一碎花黑底睡衣套装+CHANEL 字母颈链;段二黑色蕾丝束胸衣+钻扣大腰带黑短裤+裸腿;颈链贯穿两段。烟雾贴图自胸口升起。AIGC:真人实拍+美颜+后期贴图(烟雾/暗角/模糊脉冲),非全 AIGC(睡衣花纹帧间稳定;烟雾层边缘发硬且不遮挡颈链=贴图证据;变装 1.425s 仍睡衣、1.55s 已束衣,无混合帧)。
- 节拍:~100-110 BPM(推测,切点 1.5s、脉冲 3.7s)。
- 镜头形态:C 快剪(2 镜+贴图特效)。

### K280 拢发遮手跳切变装链(4拍|遮手变装·明暗掩护·衣料物性突变)
- 入态:碎花睡衣松身正面站 → 出态:黑蕾丝束胸衣+钻扣短裤,手已举过头顶
- 分解:拍1 0.00-0.67s 睡衣垂坠态双臂自体侧抬至肩高、掌心朝前,袖口花边随腕抖动;拍2 0.67-1.00s 右手横扫过面前(遮脸手位=遮挡物就位),左手向左下甩出,袖口拖出残影;拍3 1.00-1.425s 右手停在发际撩发、左手落胯侧,肩线随呼吸起伏——遮挡窗口开启;拍4 1.425→1.55s 硬切变装(8fps 主证):碎花睡衣→黑蕾丝束胸衣+短裤,背景亮度突降+暗角压边+烟雾贴图升启,手位"撩发→举过头顶"无缝衔接,衣料物性瞬间由松坠变紧贴——机制:手部遮挡+明度差掩护的真跳切
- H3:`sweeping one hand across the face in an oversized floral pajama set and jump-cutting mid-gesture into a black lace corset with rhinestone-buckled shorts as the background darkens and smoke drifts in`
- 来源:《我的发》01.425-01.55s(机制主证)/00.00-01.425s(进入路径)

### K281 手扶头烟雾定妆+模糊脉冲链(3拍|御姐摆拍·烟雾贴图·节拍失焦)
- 入态:变装落地、手举头顶 → 出态:同位定妆收尾
- 分解:拍1 1.55-2.67s 左肘架起手背贴发顶(遮阳定妆位),右臂垂持细带,烟雾贴图沿胸前上升扩散,腰胯 0.3s 周期小幅左右摆——以静制动;拍2 3.55-3.85s 全画失焦脉冲:0.3s 内模糊峰值后回焦,姿态保持连续(拼条验证:模糊无位移跳变)——脉冲为后期特效非切点;拍3 3.85-4.87s 烟雾渐散,发量视觉增厚(液化),骶骨微顶定格;音乐触发:模糊脉冲对齐副歌重拍(推测)
- H3:`holding one hand over the head like a salute while smoke drifts across the chest and the hips sway subtly, the whole frame briefly pulsing out of focus on the beat before sharpening back into the pose`
- 来源:《我的发》03.55-03.85s(脉冲主证)/01.55-04.87s

**片<v90> 《桌子底下有什么》(反差梗合成·4.87s·竖屏)**
- 背景人物:木格栅墙+暖光带房间,白色雕塑椅,低机位仰拍。人物(同一人两 shot 合成):前景=灰紫油光裤袜+黑漆皮红底高跟双腿;背景/正面=白色泡泡袖短外套+黑抹胸包臀裙+黑透丝+黑高跟+无框眼镜+黑皮文件夹+签字笔。AIGC:真人双机位合成(抠像拼接)+美颜拉腿,疑似 AI 抠像辅助,非全 AIGC——1.45s 背景空椅→1.575s 失焦层中人物淡入(125ms 内不可能真人走入)、前景腿在地板上无接触阴影、巨腿与背景人物比例违反透视(梗设计)。
- 节拍:~100 BPM(推测,揭秘 1.5s、切正面 2.7s)。
- 镜头形态:C 快剪(2 真实镜头+合成层)。

### K282 低机位入场走腿链(4拍|腿精入场·超低仰角·红底闪现)
- 入态:低机位空景(白椅+暖光带) → 出态:双腿跨立满框
- 分解:拍1 0.00-0.33s 地面仰拍空景定场:白色雕塑椅居中,画面顶端只露红底鞋尖(画外入画);拍2 0.33-0.67s 左腿入画一步跨过机位上方,鞋底红底正对镜头闪现(技术峰值:红底占屏瞬间);拍3 0.67-1.00s 右腿落地并步,小腿拉长比例占满画幅 2/3,鞋跟触地落点即拍点;拍4 1.00-1.45s 双腿左右分开站定,裤袜高光随腿转动呈竖条流动
- H3:`filming from floor level as glossy grey-stockinged legs in red-soled stiletto heels stride into the empty room and settle into a wide stance filling the frame`
- 来源:《桌子底下》00.00-01.45s

### K283 巨腿框景揭秘接面试官坐姿链(5拍|框景合成·焦点牵引·反差揭秘)
- 入态:双腿跨立框住空椅 → 出态:正面坐姿持笔抵唇定妆
- 分解:拍1 1.45-1.575s 前景双腿纹丝不动,背景空椅清晰;拍2 1.575-1.825s 焦点自前景腿拉向纵深,失焦中"坐姿人物层"淡入(白外套+黑包裙+黑透丝),前景腿退为虚化边框——合成层借失焦掩护淡入,125ms 内完成(合成主证),地板上前景腿无接触阴影;拍3 1.825-2.35s 背景人物跷二郎腿、右手抬笔、左手持黑皮文件夹,巨腿框景构图成立(比例违反透视=梗本体,技术峰值);拍4 2.35→2.8s 硬切正面:同一人坐白色雕塑椅、腿交叠、笔尖抵唇;拍5 2.8-4.87s 笔从唇边移开、向外摊手示意,头微歪定格;音乐触发:揭秘与切点均落重拍(推测)
- H3:`keeping two giant stockinged legs as a foreground frame while focus racks to reveal the same girl sitting far behind on a white chair, then cutting frontal to her seated interview pose tapping a pen against her lips`
- 来源:《桌子底下》01.575-01.825s(合成淡入主证)/02.35-02.8s(硬切)/02.8-04.87s

**片<v91> 《后裔摇》(旗袍摇·10.63s·竖屏)**
- 背景人物:红墙红地纯色房间(唯一背景),固定平视机位。人物:王羽杉——黑长发及腰;无袖黑蕾丝提花短旗袍裙(挂脖钥匙孔领、裙摆不规则)+黑丝袜+高跟;垂坠耳环。AIGC:真人实拍+重度美颜美体(体型液化),非全 AIGC——红墙/地角线几何稳定、转身连贯真动;蕾丝花纹贴附局部游移(液化贴图不稳)、腰臀比帧间突变;0s 与 2.67s 全画模糊为后期脉冲特效(模糊内含连续动作轨迹,非切点)。
- 节拍:~120 BPM(推测,顶胯约 0.25-0.3s/次=半拍律动)。
- 镜头形态:A 一镜到底(带后期模糊脉冲)。

### K284 背影顶胯转身甩发链(5拍|旗袍摇·背影开场·180 度转体)
- 入态:背身站立双手垂 → 出态:正面站定双臂垂
- 分解:拍1 0.33-1.00s 背影:双手裙后捏住蕾丝裙摆向外轻拉,骨盆左右顶胯各一次(0.3s/次)——先摆胯后转体;拍2 1.00-1.30s 左手松裙抬至腰侧,头部先行左转带动发梢(转身顺序:头→肩→髋);拍3 1.30-1.675s 原地左后转体,右脚跟为轴,长发甩出弧面盖住侧脸(技术峰值:发浪遮脸瞬间);拍4 1.675-2.05s 转完面朝镜头,发浪惯性继续左前飘再回落,挂脖钥匙孔领露出;拍5 2.05-2.2s 双臂垂落体侧站定;服装物理:蕾丝层随顶胯局部纹理游移(液化痕迹);音乐触发:转体起点对齐小节首拍(推测)
- H3:`starting with a back-view hip pop while gripping the hem of a sheer black lace qipao dress, then pivoting 180 degrees on one heel with long hair whipping around to face the camera`
- 来源:《后裔摇》00.33-02.2s(8fps 01.30-02.30s 逐拍验证)

### K285 遮眼摇胯后裔摇标准件(3拍|后裔摇·锚定上肢·骨盆半拍律动)
- 入态:正面站定 → 出态:手落肩高转体衔接
- 分解:拍1 2.2-3.0s 右臂屈肘上举、手掌横遮眉弓(招牌遮眼位),肘尖斜上——上肢锚定即入位;拍2 3.0-6.33s 核心循环 8-10 拍:双膝内扣微屈充当弹簧,骨盆左右交替顶出(每拍约 0.25-0.3s),顶左时左腿承重右膝松、顶右反向,上半身与遮眼手完全锁定,仅髋部横移约±15°——技术峰值在第 4-5 拍胯幅最大;拍3 2.67s 与 5.9s 前后两次全画失焦脉冲(0.2-0.3s),模糊中胯部摆动轨迹连续可见——脉冲为特效非切点;镜头几何:固定平视、膝上裁构放大髋部位移;音乐触发:每顶胯踩半拍(推测 120BPM)
- H3:`performing the signature hand-over-brow hip sway dance, popping the pelvis alternately left and right on each beat while bent knees act as springs and the upper body stays locked in the salute pose`
- 来源:《后裔摇》03.00-06.33s(循环主证)/8fps 04.30-05.30s 逐拍验证

### K286 点胸拳平指摆臂收尾链(6拍|后裔摇·手臂组合·定格收尾)
- 入态:遮眼位 → 出态:单手扶顶、胯右送定妆
- 分解:拍1 6.33-6.67s 右手自眉弓下落至肩高——回收遮眼位;拍2 6.67-7.33s 双臂体侧钟摆式大幅摆荡(先左后右),躯干反向微倾对冲;拍3 7.33-8.00s 右臂屈肘拳心朝内轻点胸口锁骨下两次,头随点动微颔;拍4 8.00-8.67s 右拳变掌向右侧平摊推出再收回,胯同步右送;拍5 8.67-9.0s 双手收至胸前指尖朝上猫爪抖动,9.0s 一次全画模糊脉冲(特效);拍6 9.0-10.33s 左手举顶扶发、右臂垂落,重心右移胯顶住,头低垂看斜下方定格收尾;音乐触发:点胸双下对齐鼓点双跳(推测)
- H3:`dropping the salute hand into a pendulum arm swing, tapping the collarbone twice with a loose fist, flashing one flat palm sideways, wobbling cat-paw hands at the chest and finishing with one hand on top of the head and hips pushed right`
- 来源:《后裔摇》06.33-10.33s

**片<v92> 《强者出片》(洗手间摆拍快剪·10.37s·竖屏)**
- 背景人物:公共洗手间——白瓷砖墙地、镜墙、洗手台、格间门。人物:王羽杉——黑高领紧身短袖上衣+黑牛仔超短裙+灰黑透丝+黑漆皮红底高跟;白色挂绳工牌(卡片无清晰文字=道具)。AIGC:真人实拍+重度美颜拉腿+后期转场贴片,非全 AIGC(镜面反射几何正确、地板砖缝透视一致;工牌文字糊化、1.35-1.475s 方向性模糊内背景砖缝拖影=后期贴片证据)。
- 节拍:~85-95 BPM(推测,甩镜 1.35s、黑场 8.4s 落重拍)。
- 镜头形态:C 快剪(7 站点硬切)。

### K287 甩镜模糊快剪摆拍机制链(7拍|环境摆拍·双掩护转场·七站点)
- 入态:走廊甩发侧身定位 → 出态:镜前地板跪坐收尾
- 分解:拍1 0.00-1.22s 白砖走廊侧身甩发定位;拍2 1.22→1.60s 甩镜转场 A(8fps 主证):1.35-1.475s 两帧强方向运动模糊覆盖硬切,从走廊位跳至镜墙拐角位——背景砖缝拖影而人物姿态直接换位,证实模糊为后期贴片掩护真跳切;拍3 1.60-3.00s 拐角站姿:右腿屈膝抬起、手举额侧;拍4 3.00→4.33s 硬切:台前深蹲→台面坐跷腿;拍5 5.33-6.33s 硬切:地板背镜坐,双腿向斜下伸展、镜中倒影成双影;拍6 6.33-8.33s 站回镜前背镜半转身,双手捏高领拉链下拉(唯一连续动作段);拍7 8.33→8.67s 压暗过渡 B:0.25s 后切至墙角跪坐,镜面反射完整,定格收尾——机制:七站点全硬切,两种掩护=方向模糊贴片+压暗,转场落点均在重拍(推测)
- H3:`jump-cutting through seven restroom photo stations — hair-flip entrance, wall lean, deep squat, counter sit, floor sit against the mirror, back-to-mirror zipper pull and final floor crouch — with whip-blur overlays and quick dips to black masking each hard cut`
- 来源:《强者出片》01.22-01.60s(甩镜主证)/08.33-08.67s(黑场主证)/03.00-08.33s(站点多时间码)

### K288 背镜拉衣跷腿摆链(4拍|镜面双影·拉领细节·重心锚定)
- 入态:背对镜子半转身 → 出态:拉链下拉定妆
- 分解:拍1 6.33-6.67s 背对镜站立,躯干右转 3/4 朝镜,双腿膝下交叉;拍2 6.67-7.33s 右手捏住高领中缝向下拉拽约一掌宽,领口撑开锁骨露出,头后仰配合——技术峰值:拉拽最低点;拍3 7.33-8.00s 松领,手沿身侧下滑至胯侧,胯左顶,膝部交叉角度加深;拍4 8.00-8.33s 保持交叉腿微调重心,镜中倒影全程镜像同步;服装物理:高领弹力布随下拉产生横向褶皱、松手回弹
- H3:`standing back to the mirror with legs crossed at the shins, tugging the mock-neck zipper down a hand width while tilting the head back, then releasing it and cocking the hip toward the mirrored double reflection`
- 来源:《强者出片》06.33-08.33s

**片<v93> 《哇咔哇咔杀回来了》(元气啦啦队·9.97s·竖屏)**
- 背景人物:素色木纹墙+浅木地板练习室,固定机位。人物:王羽杉——黑棕长发半扎;白蓝阿根廷球衣裁短款(胸前 Footba…/背后 10 号)+墨绿白竖条百褶超短裙+白色三道黑杠长筒袜+白运动鞋;金色手镯+黑手绳。AIGC:真人实拍+重度美颜,非全 AIGC(背景墙地纹理稳定、转身/拍手连贯自然;裙褶数量帧间不守恒=布料贴图游移、腿比超模化)。
- 节拍:~120-127 BPM 热舞曲(推测,拍手即拍点)。
- 镜头形态:A 一镜到底(首尾淡入淡出)。

### K289 背身入场原地回旋链(4拍|元气风·裙摆离心·素景回旋)
- 入态:背身站立(虚焦淡入) → 出态:正面开手站定
- 分解:拍1 0.00-0.33s 全画虚焦淡入清晰:背身站,裁短球衣背后 10 号可见;拍2 0.33-0.67s 以左脚为轴原地左后回旋,长发随转向左前方甩出弧面;拍3 0.67-1.00s 转体过 3/4 相位,百褶裙摆随旋转离心展开一瞬(技术峰值:裙摆最大张角),右手向体侧微张;拍4 1.00-1.30s 正面朝镜,双臂自体侧张开半掌宽,发落肩,微笑定妆;音乐触发:回旋起点对齐前奏鼓入(推测)
- H3:`fading in from blur standing back to the camera in a cropped Argentina jersey and pleated mini skirt, then spinning 180 degrees in place with the hair swinging and arms half-opening into a front-facing cheer pose`
- 来源:《哇咔哇咔》00.00-01.30s(8fps 0.50-1.30s 逐拍验证)

### K290 拍手斜举哇咔摇摆链(7拍|元气热舞·拍手即拍·一镜到底)
- 入态:正面开手站定 → 出态:双手胸前合十收尾(渐黑)
- 分解:拍1 1.30-2.00s 双臂体侧摆荡两下,膝部屈-伸-屈弹动;拍2 2.00-2.50s 双手向内交叉相拍合于左肩上方(拍手 1),躯干左倾,合掌沿对角线滑向右肩(拍手 2)——技术峰值:斜举合掌;拍3 2.50-3.33s 合掌胸前小幅上下搓摩三次,肘部架平;拍4 3.33-6.33s 循环组"开掌-交叉拍-斜举滑掌"×2-3 轮,百褶裙摆随胯摆出波浪,白袜黑杠随膝弹;拍5 6.33-7.67s 双掌摊开体侧耸肩摆,掌心朝上挑腕两次;拍6 7.67-9.0s 双手举至脸侧猫爪抖动,再变 OK 手势左右各一次;拍7 9.0-9.33s 双手合十收于胸前,渐黑淡出;音乐触发:拍手即拍点(推测 120-127BPM)
- H3:`dancing the waka-waka cheer combo in one continuous take — clapping palms diagonally over each shoulder, rubbing clasped hands at the chest, shrug-swaying with open palms, wiggling cat paws and OK-signs beside the face before closing with hands together`
- 来源:《哇咔哇咔》02.00-03.33s(拍手主证)/06.33-09.33s(手势组)

**片<v94> 《红色高跟鞋》(卡点变装·6.23s·竖屏)**
- 背景人物:深灰木格栅墙+条形暖光灯+木地板。人物:王羽杉——红棕长卷发;段一米白罗纹高弹连体衣裸足(红甲油);段二黑底奶油斜纹抹胸包臀超短裙+灰透丝裤袜/黑过膝长筒袜交替+黑高跟;大圈耳环+项链。AIGC:真人实拍+美颜+硬切卡点剪辑,非全 AIGC(裸足持鞋手部/足部互动物理合理、鞋底红底连续;袜类切换全部为硬切;腿比夸张系液化)。
- 节拍:~100 BPM(推测,变装 2.05s、袜切 2.65/3.7/5.2s 踩军鼓)。
- 镜头形态:C 快剪(3 镜+袜类交替跳切)。

### K291 裸足持鞋逗鞋链(5拍|道具互动·裸足开场·鞋即主角)
- 入态:背身裸足单手持鞋 → 出态:鞋贴脸颊、指尖敲鞋头
- 分解:拍1 0.00-0.33s 背身站,米白罗纹连体衣裸足,右手拎黑红底高跟鞋于胯侧——道具先于动作入画;拍2 0.33-0.67s 左后转体带发浪,双手各持一鞋向两侧摊开示物;拍3 0.67-1.00s 右鞋提至右颊旁、鞋尖朝上红底正对镜头,头向左让位(技术峰值:鞋贴脸构图);拍4 1.00-1.33s 鞋跟轻点锁骨窝,视线顺鞋身下移再抬眼看镜;拍5 1.33-1.6s 双鞋并至左手,右手食指中指并拢在鞋头轻敲两下;音乐触发:敲鞋对齐打击乐(推测);鞋的红底为全片唯一高饱和色块
- H3:`turning around barefoot in a cream ribbed catsuit holding a pair of red-soled pumps, kissing one shoe against the cheek and tapping its toe with two fingers like a playful prop tease`
- 来源:《红色高跟鞋》00.00-01.6s

### K292 抬腿甩鞋遮切变装+袜类交替卡点链(8拍|动作遮掩变装·袜类卡点·同装异袜)
- 入态:双手双鞋并举 → 出态:抱臂交叉腿定妆
- 分解:拍1 1.60-2.00s 右腿裸足屈膝上提(火烈鸟位),双鞋向两侧甩开带残影——遮挡窗口开启;拍2 2.00→2.125s 硬切变装(8fps 主证):连体衣裸足→黑条纹抹胸包臀裙+灰透丝+高跟已穿,抬腿相位衔接为交叉腿站姿、手位延续——动作遮掩真跳切;拍3 2.125-2.65s 交叉腿左右重心各移一次;拍4 2.65s 硬切换袜:灰连裤袜→黑过膝长筒袜(袜口大腿中段露腿根);拍5 3.0-3.7s 长筒袜版抱臂交叉腿定格两拍;拍6 3.7s 硬切回灰连裤袜版同姿;拍7 5.2s 再切长筒袜版提腿一拍;拍8 5.2-6.2s 切回连裤袜版,双臂抱胸、胯左顶、头右歪定格收尾——机制:同裙装+两类丝袜交替即"卡点换装"(2.65/3.7/5.2s 三切点),全部硬切;音乐触发:每次切袜踩军鼓重拍(推测)
- H3:`lift-kicking one bare leg while swinging both shoes wide and jump-cutting into a striped bandeau mini dress with heels on, then hard-cutting on every snare between sheer grey pantyhose and black thigh-high stockings while the pose carries over`
- 来源:《红色高跟鞋》02.00-02.125s(变装主证)/02.65s、03.7s、05.2s(袜类交替多时间码)

**片<v95> 《请选择你的主队》(世界杯啦啦队 AI 变装·9.4s·竖屏)**
- 背景人物:会议室式白墙+灰地毯,墙挂大电视循环播放足球比赛回放(屏显"央视频/小红书/回放"角标、记分牌、场边 McDonald's 广告牌)。人物:AI 御姐模特,红棕长卷发挑染,5 套球衣啦啦队装(①蓝白条纹 10 号抹胸+白百褶裙+蓝条纹白过膝袜 ②黄绿条纹短袖+黄裙绿腰封 ③白短袖+蓝白百褶裙 ④红蓝 Football 印花短袖+红蓝百褶裙 ⑤蓝一字肩+黑短裙),全程白色三条纹板鞋;道具:足球随变装换色。AIGC:疑似 AI(高)——球衣号码/广告牌/记分牌文字乱码、球面 logo 跨帧熔变、皮肤蜡质、腿比拉长。
- 节拍:≈128 BPM(推测;4 次变装点 2.0/3.8/5.6/7.7s,间隔≈1.85-1.9s)。
- 镜头形态:A 一镜到底(换装全部由生成端形变完成,无真切口)。

### K293 肩球换手展示摇(4拍|啦啦队·道具锚定·骨盆横移)
- 入态:侧身站定、球压左肩 → 出态:右手托球前伸展示、重心回正
- 分解:拍1 0.0-0.7s 双脚并拢锚定,左臂屈肘把黑白足球压在左肩峰,髋部小幅左右摆预热;拍2 0.7-1.4s 重心左→右转移,左臂伸直让球沿体侧滚落至左手托住,髋随重心横移约±10°,百褶裙随摆扬起滞后半拍回落;拍3 1.4-2.0s 左手把球平举胸前贴手递向右侧,右手接球水平右伸至肩宽外、掌心托球面朝镜头,头右转追球——技术峰值为贴手滚递水平线;拍4 右臂屈肘收球至肩,身体回正,髋部两次递减摆吸收惯性;复现:03.90-05.50s、06.00-07.60s 同链异装
- H3:`standing with a soccer ball resting on the shoulder, rolling it down the arm and passing it across the body to the other hand while swaying the hips on each beat, then presenting the ball toward the camera as the head follows it`
- 来源:《请选择你的主队》00.00-02.00s / 03.90-05.50s / 06.00-07.60s

### K294 抛球落手摆胯(3拍|啦啦队·抛接停顿·屈膝缓冲)
- 入态:双手托球胸前 → 出态:球合抱落回腰前、屈膝弹回中
- 分解:拍1 2.8-3.0s 双手把黄蓝足球向上轻抛离手约 0.3m,双臂上送、提踵;拍2 3.0-3.3s 球悬最高点(半拍停顿),双臂上举迎球,视线锁球,髋同步向左顶出;拍3 3.3-3.7s 球落入胸前双手合抱缓冲,膝盖微屈弹一次、骨盆回中
- H3:`tossing a soccer ball overhead with both hands and catching it at the chest on the next beat while popping the hip to one side, knees bouncing softly to absorb the catch`
- 来源:《请选择你的主队》02.80-03.70s

### K295 旋糊/瞬换/白光三式变装机制链(5拍|AI 变装机制·同机位换装)
- 入态:上一套服装结束姿势 → 出态:下一套服装同机位新姿势
- 分解:拍1 1.95-2.10s 变装①旋身糊:左脚为轴原地快速旋身 180-360°,手臂收拢减小转动惯量,整帧被定向涂抹模糊覆盖,服装与球在糊内同步换色,背景屏幕内容随糊切换——模糊为生成涂抹而非真实快门拖影;拍2 2.10-2.20s 糊散出态,跨糊姿态跳变,无任何布料过渡帧;拍3 3.75-3.90s 变装②瞬换:相邻两帧服装+球+屏幕内容直接替换,身体姿态近乎连续,判定生成端硬切;拍4 5.55-5.95s 变装③二次旋糊,方向与①相反;拍5 7.60-7.80s 变装④白光竖条纹涂抹:全身被过曝白色纵向拉丝吞没再显影为蓝一字肩+黑裙抱球——技术峰值:四式机制统一实现"同机位零切口连续换装"
- H3:`snapping into a new outfit through a single-frame motion-blur whip spin, an instant silent swap, and a white-out vertical smear while the camera stays frozen and the pose jumps across the blur`
- 来源:《请选择你的主队》01.95-02.20s / 03.75-03.90s / 05.55-05.95s / 07.60-07.80s

**片<v96> 《辣妹球衣》(天台球衣摆拍·10.0s·竖屏·AI 中高)**
- 背景人物:城市高楼天台,玻璃栏板+灰石地+藤边日床,远景城市天际线。人物:棕褐长卷发,蓝色 oversize 球衣(QATAR AIRWAYS 胸印+背面 10 号),牛仔短裤、白色三条纹板鞋,卧姿段赤足。AIGC:疑似 AI(中高)——背面 10 号印刷上缘粘连变形、发丝与衣料/手指蜡质融合、腿身比极端、靠垫边缘跨帧微漂移;正面字母清晰,不能完全排除真人重度美颜。
- 节拍:≈100 BPM(推测;切点间隔 2.2-4.5s,弱拍感摆拍)。
- 镜头形态:C 快剪(低角仰拍卧姿→侧坐→正面中景→远景背影→站立→床沿坐,真跳切约 1.25/2.15/5.85/8.45s)。

### K296 卧起撩发锁骨点摆拍链(3拍|天台摆拍·核心侧屈·发丝惯性)
- 入态:低角仰躺日床手扶发 → 出态:侧坐指尖点锁骨目视镜头
- 分解:拍1 0.0-1.2s 仰躺日床,双腿向画面左下伸直叠放,左手插发根托头、右手搭腹,下颌微收看镜(核心侧屈+头部自重);拍2 1.3-2.2s 腹肌发力缓慢撑起过渡侧坐,右手滑出发间经颈侧停在锁骨、指尖随拍轻点两下,发丝因起身惯性甩过肩落胸前;拍3 2.2-5.8s 坐姿循环:右手过顶绕后脑撩发→下移遮眉弓→五指插回发根侧拉一缕松手回弹,同步骨盆小幅摆;oversize 球衣下摆随起身从大腿滑至臀线
- H3:`lying back on a daybed with one hand buried in the hair, slowly sitting up to a side perch tapping the collarbone on the beat, then looping overhead hair lifts and side hair pulls with gentle pelvic sway`
- 来源:《辣妹球衣》00.00-05.80s

### K297 背影甩发转身埋发链(3拍|天台摆拍·W 框肘架·半拍骨盆)
- 入态:全背影球衣 10 号对镜 → 出态:正面双手埋发定格、床沿坐姿收尾
- 分解:拍1 5.90-6.30s 全背影站玻璃栏前,长发全披,髋左右小幅摆让衣摆轻晃;拍2 6.30-6.60s 切正面半侧身,双手插进两侧发根向外翻开花,下颌右偏看镜(肩带外展+腕翻转);拍3 6.60-8.40s 双手留发中,指尖沿发缕下滑至肩再回耳后循环 2-3 次,膝内扣微屈当弹簧、骨盆每拍交替顶出(±10°)——技术峰值:肘尖外撑的 W 形框发构图;尾镜 8.47-10.00s 真跳切床沿并膝坐,手叠膝静态微晃收场
- H3:`standing back to the camera in an oversized jersey, flipping to face forward with both hands buried in the hair, fingertips sliding down the strands and back while the pelvis pops side to side, closing on a kneed perch with hands folded`
- 来源:《辣妹球衣》05.90-08.40s / 08.47-10.00s

**片<v97> 《蓝裙氛围感》(蓝蕾丝户外氛围摆拍·9.1s·竖屏·AI 高)**
- 背景人物:户外园区,蕨类灌木+灰步道+景观岩石+苔藓绿墙+紫花境,远景玻璃幕墙办公楼。人物:深棕长卷发,宝蓝蕾丝透视抹胸长裙(腰际挖空、细金链交叉背带、裙身堆叠大腿),金链颈饰、绿松石耳坠、裸色高跟。AIGC:AI(高)——腰臀腿比例超人体极限、蕾丝与皮肤纹理互融、裙堆无重力垂坠、0.55-0.95s 白糊涂抹形变跨姿态跳变。
- 节拍:≈110 BPM(推测)。
- 镜头形态:C 快剪(背身跪→旋转 90°躺石→正面站→旋转跪弓→岩面侧坐→跪蹲,6 机位硬切,含 1 处涂抹形变)。

### K298 背身跪姿顶胯撩发链(4拍|蓝裙氛围·背身 S 曲线·涂抹形变)
- 入态:白糊中显形背身跪 → 出态:单臂侧伸、臀后翘定格
- 分解:拍1 0.00-0.30s 涂抹模糊中显形:背对镜头跪坐步道边,臀后翘对镜,蓝蕾丝抹胸+同料裙堆胯上,细金链交叉勒出裸背——入态即最大 S 曲线;拍2 0.30-0.55s 左臂屈肘上举插发撩起整片头发再松手,发丝回落扫背,髋向后上顶一次(顶胯峰值)、肩胛内收;拍3 0.55-0.95s 全身再次被白糊涂抹覆盖约 3-4 帧,姿态跨糊从左臂上举跳变为右手屈肘胸前——AI 形变接缝;拍4 1.00-1.67s 右臂体侧平伸展示、头低垂,骨盆保持后翘微摆;服装物理:蕾丝裙堆臀下不滑落、高跟鞋尖点地(违反垂坠,AI 特征)
- H3:`kneeling with the bare back and hips toward the camera in a sheer blue lace dress, lifting and releasing the hair with one arm while popping the hips back, morphing through a white smear into an arm-extended display pose`
- 来源:《蓝裙氛围感》00.00-01.67s

### K299 旋转躺石伸展链(3拍|蓝裙氛围·旋转构图·指扇慢展)
- 入态:90° 旋转构图侧卧岩面 → 出态:岩沿交叠腿侧坐手抚膝
- 分解:拍1 2.00-3.33s 整幅画面逆时针旋转 90°(人物与岩面横置),身体沿岩面斜线躺伸:双腿顺岩面向上交叠伸展、单手支地、另一手自脸颊向外展开发散五指——技术峰值为手指扇形慢展;拍2 3.40-4.60s 真跳切回正向构图:正面站姿抚颌、指尖点唇,随后切入第二个旋转构图:跪地后弯弓身(桥式变体)手插发;拍3 5.30-6.00s 弓身过渡到岩沿侧坐,双腿交叠斜伸、骨盆每拍小幅倾;服装物理:蕾丝裙侧躺贴体不坠、褶皱跨帧漂移(AI);镜头几何:正向/旋转双机位硬切
- H3:`stretching along a rock in a rotated frame with legs extended up the stone and fingers fanning open in slow motion, then arching into a kneeling bridge and settling into a crossed-leg rock-edge sit with subtle pelvic tilts`
- 来源:《蓝裙氛围感》02.00-03.33s / 03.53-04.60s / 04.65-06.00s

**片<v98> 《嘉桐摇》(黑衣慢摇指舞·9.3s·竖屏·AI 高)**
- 背景人物:室内纯色浅棕木纹墙,无家具、无踢脚线、人物无接地投影;画框止于膝下。人物:深棕超长卷发,黑色 U 领紧身长袖(左胸红蝴蝶结胸针),黑色紧身短裤,细银项链。AIGC:AI(高)——背景无投影、指节粘连指长异常、脊柱反弓 S 曲线超限、双脚全程锚定仅骨盆平移(AI 摇特征)。
- 节拍:≈120 BPM(推测;摆胯周期 0.45-0.5s)。
- 镜头形态:A 一镜到底(固定机位慢摇)。

### K300 指地画圈飞吻摇胯链(4拍|嘉桐摇·食指画圈·双脚锚定胯平移)
- 入态:正面站立右手抬胸 → 出态:指手收胸、飞吻定格
- 分解:拍1 0.90-1.10s 右手五指微张抬至胸前,腕翻掌心朝下、食指伸向镜头前下方(指地位),肘先抬、腕后翻、指最后点;拍2 1.10-2.40s 核心循环:食指指尖对镜头画小圈(直径≈10cm,1 圈/拍≈0.45s),同步骨盆左右平移(±8°,双脚全程钉地仅胯平移——AI 摇特征),肩线锁定;拍3 2.40-2.65s 技术峰值:指尖画完收向唇前,双唇拢起对镜飞吻一次,眼波右抛;拍4 2.65-2.80s 手指松开回落握拳于胸前,骨盆两下递减摆回中;紧身长袖随骨盆平移在腰侧出横向拉褶
- H3:`pointing one index finger down toward the camera and drawing small circles on every beat while the pelvis slides side to side on planted feet, then pulling the finger to the lips to blow a kiss`
- 来源:《嘉桐摇》00.90-02.80s

### K301 腰际手波侧展掌链(4拍|嘉桐摇·托盘掌·手指波)
- 入态:指拳收胸 → 出态:双手腹前指花收势定格
- 分解:拍1 4.80-5.30s 甩头换边:右手落体侧、头右甩发浪,身体右转 3/4;拍2 5.30-5.80s 左臂体侧平伸、掌心翻上成托盘位,头顺手向看出,右髋同向顶出(背阔带动大臂外展);拍3 5.80-6.70s 左掌回收划经腰际,五指在腹前依次波浪(2 波/拍),骨盆改前后微送;拍4 6.70-8.67s 左臂再展再收(幅度递减 30%)、双肩交替耸落,双手腹前指尖相对做小花开合收势
- H3:`extending one arm sideways with the palm up like presenting a tray, pulling it back to roll a finger wave across the belly while the hips pulse forward and back, then repeating smaller and closing with fluttering fingertips at the waist`
- 来源:《嘉桐摇》05.30-08.67s

**片<v99> 《莫多莫多》(四格同步变装卡点·9.3s·竖屏·AI 确证级)**
- 背景人物:整帧为 2×2 四格拼贴(每格 540×960),格内同一酒店走廊式场景;四格为同一 AI 人物模板的不同生成样本:深棕超长卷发,服装各格独立切换——白裙/酒红无袖高领+灰铅笔裙+工牌/金米色蕾丝束腰+黑缎短裙/黑一字长袖+黑短裤/金抹胸+金金属包臀裙+大耳环。AIGC:AI(确证级)——四格同房间同人体模板、动作同步而服装阶段错位(真人拍摄不可实现)、工牌挂绳无物理垂坠、花纹跨帧漂移、换装均为单帧瞬换无布料过渡。
- 节拍:≈120 BPM(推测;换装卡点 2.4/5.9/6.3/7.3s 落重拍)。
- 镜头形态:特殊:格内各自 A 一镜到底,四格级联换装卡点(格间动作模板一致、逐帧细节有生成样本漂移)。

### K302 开场挥手拳胸摇(3拍|莫多莫多·四格同步·高位挥摆)
- 入态:双手上举掌心向外 → 出态:双拳收胸前、手落腰际
- 分解:拍1 0.00-1.50s 双臂抬至头侧、前臂竖立掌心朝镜头,手腕带动双手左右同步挥摆(1 摆/拍≈0.5s),肘高位锁定,骨盆随摆微送;拍2 1.50-2.20s 双手握拳回落胸前、拳面相对小幅上下捶两次,膝盖屈伸弹性缓冲;拍3 2.20-2.70s 双手滑落腰际指尖相对,身体微右转预备展臂;本链在 2×2 四格内同步执行
- H3:`waving both raised palms side to side toward the camera on each beat, then dropping into loose fists to pump them twice at the chest with a soft knee bounce before sliding the hands to the waist`
- 来源:《莫多莫多》00.00-02.70s(四格同步)

### K303 四格级联换装卡点机制链(4拍|AI 变装机制·四格拼贴·重拍连击)
- 入态:四格同穿白裙同步起舞 → 出态:四格四装抱胸收势
- 分解:拍1 2.40-2.50s 左上格率先单帧瞬换装(白裙→酒红高领+灰铅笔裙+挂绳工牌),其余三格保持白裙,无布料过渡;拍2 4.00-6.00s 四格同步展臂顶胯:单臂体侧摊开掌心向上、髋向展臂侧顶出,接转身背对 3/4 摆胯回正——同一动作模板四格并行渲染、逐帧细节各有样本漂移;拍3 5.90-7.50s 级联连击:左下格瞬换黑一字长袖+黑短裤(≈5.9s),右上格瞬换金米色蕾丝束腰+黑缎短裙(≈6.3s),右下格最后瞬换金抹胸+金色金属包裙(≈7.3s),每次换装落一个重拍;拍4 7.50-9.30s 四格(四装)同步双手交叠按胸→落腹前小幅弹跳收势——技术峰值:级联完成瞬间四格色彩四分对撞
- H3:`four identical synchronized dance panels in one 2x2 grid where each quadrant snaps to a different outfit one card-point apart in a cascading swap while all four keep sweeping one arm out and popping the hip in unison`
- 来源:《莫多莫多》02.40-02.50s / 05.90-06.00s / 06.30-06.50s / 07.20-07.50s / 07.50-09.30s

**片<v100> 《jumpstyle》(白衫跳步变装黑袜·6.0s·竖屏·AI 高)**
- 背景人物:极简展廊,灰木纹格栅墙+暖光带+浅灰地坪(人物镜像倒影)。两套装:①白荷叶边无袖上衣+浅蓝阔腿牛仔裤+白球鞋 ②黑无袖高领连体短裤+黑丝袜+棕细腰带+黑细高跟;深棕长卷发。AIGC:AI(高)——丝袜灰白横带伪影跨帧漂移、腿比极端、0s 白糊入场、3.0-3.15s 单帧瞬换装、跟部反光与地面倒影不一致。
- 节拍:≈128 BPM(推测;跳步 1 跳/拍、交叉点地 2/拍)。
- 镜头形态:A 一镜到底(白糊入场+单帧换装,无真切口,末段压暗收场)。

### K304 开手举臂入场链(4拍|jumpstyle·开肩→W 举臂)
- 入态:白糊显形正面站立 → 出态:单臂高举、重心左移预备跳
- 分解:拍1 0.00-0.30s 白糊中显形,双臂向体后下张开、掌心朝后开肩;拍2 0.30-0.60s 双手沿体侧前摆至髋、指尖触腰骨、肘外撑;拍3 0.60-1.00s 双肘上提,前臂面前交叉成护栏位随即打开,双臂沿头侧上举过头、手腕放松下垂轻晃——技术峰值:过头 W 框架;拍4 1.00-1.40s 右臂保持高举、左臂屈肘回收,重心左移,右腿提膝预备跳步
- H3:`emerging from a white smear into a shoulder-opening stance, sliding the hands up to the hip bones and raising both arms overhead with loose wrists before holding one arm high to load a hop`
- 来源:《jumpstyle》00.00-01.40s

### K305 jumpstyle 双脚跳交叉踢步链(4拍|jumpstyle·腾空弹跳·剪刀摆臂)
- 入态:单臂高举预备 → 出态:并脚屈膝弹动收势
- 分解:拍1 1.40-1.90s 双脚同时蹬地小跳(jumpstyle 基础弹跳,1 跳/拍),屈膝收腿腾空约一脚高,双臂自上向外下张开压拍,前脚掌落地屈膝缓冲;拍2 1.90-2.40s 落地即起:左右腿身前快速交替交叉点地(2 点/拍),手臂低位随步伐自然对摆;拍3(技术峰值)2.40-2.90s 交叉步中插正踢:右腿向前上方踢出、绷脚离地约膝高,同侧臂前摆、对侧臂后摆成剪刀摆,落地接左腿反向踢——踢腿节奏 1 腿/拍卡重拍;拍4 2.90-2.95s 末次落地双脚并拢微屈膝弹两下回正;服装物理:阔腿牛仔裤随跳跃甩出宽裤口波浪;镜头几何:固定全身正面无跟摇,地面倒影强化腾空判读
- H3:`performing jumpstyle hops with both feet leaving the floor on every beat, crossing the legs in quick alternating taps, and snapping straight front kicks with scissor-swinging arms before landing back into a bounce`
- 来源:《jumpstyle》01.40-02.95s

### K306 卡点瞬换装高跟鞋摆胯收势链(4拍|AI 变装机制·跳切换装·幅度衰减)
- 入态:白装并脚站定 → 出态:黑袜高跟摆胯归静、画面压暗
- 分解:拍1 2.95-3.15s 单帧瞬换装:相邻两帧间整套装替换(白上衣+牛仔裤+球鞋→黑无袖高领连体短裤+黑丝袜+棕细腰带+黑细高跟),发型由侧披变全披,姿态近乎连续、≤1 帧过渡残影——生成端卡点硬切;拍2 3.15-4.50s 换装即接慢摆:双脚钉地,骨盆左右交替顶出(±10°,1 顶/拍),膝微屈当弹簧;拍3 4.50-5.40s 摆幅衰减,改为重心脚交替踮跟起伏,单手指尖沿裤腰滑行;拍4 5.40-6.00s 摆幅递减至静止站立,画面亮度线性压暗至近黑收场;服装物理:丝袜高光 AI 灰白横带跨帧漂移、跟部反光与倒影不一致;镜头几何:换装前后构图零位移
- H3:`snapping from the jeans outfit into a black bodysuit with sheer stockings and stiletto heels between two frames on the beat, then rocking the pelvis side to side on planted feet with fading amplitude until the lights dim to black`
- 来源:《jumpstyle》02.95-06.00s

**片<v101> 《紧身连衣裙》(金钻裙慢摇手势·9.1s·竖屏·AI 高)**
- 背景人物:酒店走廊式室内,灰木纹墙板+顶部暖黄光槽+浅木地板,顶棚垂两根无源细线缆(AI 伪影);画框止于膝下。人物:深棕长卷发,金色香槟水钻抹胸紧身迷你裙,钻颈链。AIGC:AI(高)——无源线缆、墙板线条贴人物边缘弯曲、水钻纹理整片喷涂跨帧漂移、0-0.3s 与 4.95-5.15s 白糊涂抹形变、指节畸形。
- 节拍:≈120 BPM(推测)。
- 镜头形态:A 一镜到底(含 2 处 AI 涂抹形变作隐形接缝,无真切口)。

### K307 下颌收手捏指摆胯链(4拍|金钻裙慢摇·护脸拳位·指尖捏点)
- 入态:白糊显形侧身 S 态 → 出态:正面捏指招手定格
- 分解:拍1 0.30-1.00s 金钻抹胸紧身裙侧身站定,双手空拳收至下颌两侧(护脸位),髋向左后顶出、身体 C 形曲线、膝右内扣——入态即锁定上肢、只留胯自由度;拍2 1.00-2.30s 双手沿体前中线交叉下落再开至腰侧,五指捏合状在腰际上下两点(1 点/拍),骨盆每拍左右交替顶(±10°),上肢锁位仅腕指动;拍3(技术峰值)2.30-3.67s 右手上提胸前做指尖捏合+慢腕转(展示位),左手插回胯侧;拍4 3.67-4.80s 双手胸前交替招手两次,膝弹性屈伸;服装物理:水钻裙无褶皱位移、钻面反光跨帧漂移(AI);镜头几何:固定全身正面微仰,顶棚两根无源线缆入画(AI 伪影)
- H3:`holding both curled fists by the chin in a skin-tight rhinestone dress with the hip pushed out, then pinching the fingertips at the waist on each beat and lifting one hand for a slow show-off wrist turn while the pelvis pops side to side`
- 来源:《紧身连衣裙》00.30-04.80s

### K308 白糊形变接缝扭胯展臂收势链(4拍|AI 变装机制·对角拉弓·摊手定格)
- 入态:正面招手中段 → 出态:双臂摊开掌心向上定格
- 分解:拍1 4.80-5.15s 全身被白色纵向涂抹模糊吞没约 0.3s,姿态跨糊从正面招手跳变为左侧身,墙缝与线缆连续无切——AI 形变接缝(同装同景的隐形段间拼接);拍2(技术峰值)5.15-6.60s 出糊即接侧身扭胯:右臂向斜下伸直展开,髋向左顶出成对角拉弓曲线,头看镜头,上肢与骨盆对角张力最大化;拍3 6.60-8.00s 身体逐帧回正,双臂收经胸前向脸颊两侧打开、五指张成爪形轻晃两次、肩耸落;拍4 8.00-9.10s 双臂体侧平摊、掌心向上定格,骨盆两下递减摆,视频结束;服装物理:裙体贴身如喷涂,扭胯时腰侧出现油漆式拉长变形;音乐触发:形变落重拍、摊手定格对乐句尾
- H3:`morphing through a white vertical smear into a side stance with one arm extended low and the hip counter-popped, unwinding to claw hands beside the cheeks and closing with both palms shrugging upward`
- 来源:《紧身连衣裙》04.80-09.10s

**片<v102> 《黑色系御姐》(慢律动坐姿摆拍·8.0s·竖屏)**
- 背景人物:现代风客厅,深灰布艺沙发+浅灰木地板,竖条纹吸音板墙+暖光灯槽。人物:王羽杉——棕黑长卷发中分,黑色紧身半高领短袖连衣裙(包臀),灰黑高光透肉丝袜,黑色尖头细高跟(红底大底),细手链。道具:智能手机(锁屏壁纸为同女白色系精修照)+单只红底高跟鞋,由前景之手持入。AIGC:真拍+重度滤镜精修(前景手机光学畸变、手指关节、甩镜整帧模糊真实;皮肤"玻璃肌"重度美颜,锁屏内人像本身即 AI 风精修)。
- 节拍:约 75 BPM(推测,动作循环周期约 1.3s)。
- 镜头形态:C 快剪(前景特写→揭示→甩镜遮切共 3 段,焦点牵引)。

### K309 手机锁屏+红底鞋前景引导揭示链(4拍|道具引导·焦点揭示)
- 入态:全帧虚焦,前景手机屏(锁屏人像)+红底高跟占据画面中心,背景人物虚坐 → 出态:前景道具完全出画左缘,焦点落在沙发前人物全身,姿态锁定交腿坐
- 分解:拍1 0.00-0.65s 前景手托手机屏居中,红底鞋斜倚其右,背景虚焦人物已就位(静态锚点)——构图层级:道具屏>鞋>人;拍2 0.65-0.90s 手持双道具整体向左平移,鞋身翻转露出红底大底(道具展示峰值),焦点开始后拉;拍3 0.90-1.10s 道具滑出左缘,焦点牵引完成,人物由虚转实,灰丝反光先于面部清晰(视线引导到腿);拍4 1.10-1.40s 人物微调坐姿入态,双手落膝,交腿相位与屏中人像形成"同人对镜"暗示
- H3:`holding a phone lockscreen photo and a red-soled pump in the blurred foreground, then sliding both props out of frame left while racking focus onto the woman seated behind in a black dress and glossy grey pantyhose`
- 来源:《黑色系御姐》00.00-01.40s

### K310 地板倚沙发交腿延伸摆拍链(6拍|坐姿摆拍·脚尖循环)
- 入态:背靠沙发前缘坐于地板,双腿向镜头交叠延伸,手搭膝 → 出态:单手插入发内、头倾肩,腿型维持交叉延伸
- 分解:拍1 1.40-2.00s 交腿延伸态,上腿脚尖做"绷—勾—绷"循环(丝袜高光随绷脚沿胫骨滑动),发力来源为踝背屈肌群,髋不动;拍2 2.00-2.67s 双手下滑撑地,髋微后坐加深腿的镜头延伸感(透视拉腿);拍3 2.67-3.33s 上腿小幅上下点动两次,膝角变化±10°,惯性延续到小腿末端颤动;拍4 3.33-4.30s 双手交叠压膝,肩线向镜头微转,下颌内收(技术峰值:全身线条在镜头轴上最直);拍5 4.30-4.60s 预备动势——肩向后带、重心上提;拍6 4.60-4.65s 动势切断进入甩镜(移交 K311)
- H3:`sitting on the floor against the sofa with crossed legs extended toward camera, cycling toe point-and-flex so the glossy grey pantyhose sheen slides along the shin, then pressing hands over the knee and lifting the chest right before the whip transition`
- 来源:《黑色系御姐》01.40-04.65s

### K311 甩镜遮切转场链(3拍|转场机制·动态模糊遮切)
- 入态:地板倚坐宽机位构图 → 出态:沙发坐面中近机位新构图,交腿高抬,手入发
- 分解:拍1 4.65-4.73s 镜头/身体快速动势启动,帧内出现方向性拖影(整帧模糊开启遮挡窗口);拍2 4.73-4.85s 模糊峰值帧——主体不可辨,机位在此窗口内完成"地板低位→沙发坐面中近位"的构图替换(真切点藏在模糊内,非连续运镜);拍3 4.85-5.10s 模糊收敛,新场景浮现:她已坐上沙发坐面,双腿交叉高位向镜头,第一清晰帧即锁定交腿相位(甩镜遮切成立判据);惯性延续:5.10-5.60s 手顺势插入发内、头倾,回收顺序为手→头→肩
- H3:`whipping the camera into a full-frame motion blur that hides the cut from the wide floor-lean setup to a closer sofa-seat framing, resolving the blur already locked on crossed legs high toward camera before trailing one hand up into the hair`
- 来源:《黑色系御姐》04.65-05.60s

**片<v103> 《拿下你》(学妹反差双变装·7.5s·竖屏·AI 渐变实锤)**
- 背景人物:室内木饰面素墙,正面固定机位。人物:王羽杉——棕发长卷发+黑色蝴蝶结发箍。三套造型:①黑色背带连衣裙罩白泡泡袖衬衫+条纹领带;②白色翻领针织短袖+白色百褶迷你裙+黑色 choker;③黑色蕾丝吊带+酒红短裙披膝+黑底碎花蕾丝过膝袜+黑红底细高跟+choker,坐白色雕塑感异形椅,手持黑色多股皮鞭道具。AIGC:AI 渐变实锤——变装 1 3.63-3.88s 半透明双态叠影且右侧多出一只"鬼影指向手臂"(五指结构畸形);变装 2 4.95-5.65s 白/黑两整态反复闪变振荡、叠影帧肢体错位;编辑器交叉溶解必单调推进,不可能回摆,判:AI 生成转场(AI 视频或 AI 重绘后期)。
- 节拍:约 88 BPM(推测)。
- 镜头形态:C 快剪(AI 渐变衔接,三段同构图对齐)。

### K312 学妹装理带展臂链(4拍|入场摆拍·反差铺垫)
- 入态:正面直立,右手捏领带贴胸 → 出态:双臂向侧下展开后回收扶带,恢复端立
- 分解:拍1 0.00-0.66s 捏带贴胸静态,头微歪(乖巧态标定);拍2 0.66-1.33s 右手顺带面向下滑半程,肩随手上提;拍3 1.33-2.33s 双臂向侧后方展开至裙摆高度再划回,发力来源为背阔肌内收;拍4 2.33-3.30s 双手扶带整理,肘抬至肩高再落,末帧与变装 1 入态对齐(3.30-3.55s 保持静止利于渐变对齐)
- H3:`standing square to camera in a schoolgirl pinafore and striped tie, sliding a hand down the tie, flaring both arms out and back in, then adjusting the tie with elbows high before holding still for the transition`
- 来源:《拿下你》00.00-03.55s

### K313 AI 渐变双段变装链(6拍|AI 变装机制·渐变+振荡)
- 入态:学妹黑装端立 → 出态:白色系站姿 OK 手势态(第一段)/黑蕾丝椅坐态(第二段)
- 分解:拍1 3.55-3.63s 黑装末态静止,渐变窗口开启;拍2 3.63-3.88s 单调溶解中态:黑裙透明度下降、白裙同位浮现,右侧生成鬼影指向臂(畸形五指)——AI 重绘痕迹帧;拍3 3.88-4.90s 白装整态稳定:双手轮流在脸侧比 OK 圈,choker 跨装延续(身份锚点),每圈约 0.5s 踩点;拍4 4.90-5.05s 渐变窗口二次开启,白装边缘开始透明;拍5 5.05-5.65s 振荡闪变:白站态↔黑椅坐态整帧反复交替(5.12/5.51 黑、5.25/5.32 白回摆),叠影帧出现多腿与鞭带错位——生成插值时序不稳,峰值帧 5.05s(双态各半透明);拍6 5.65s 后黑蕾丝椅坐态锁定,手位与白装 OK 手势同相位衔接
- H3:`cross-dissolving AI-style from the schoolgirl outfit into the white polo set with ghost-arm artifacts, flashing OK-signs at the face, then flickering back and forth between the white standing and the black lace seated versions with double-exposed limbs before settling seated`
- 来源:《拿下你》03.55-05.65s(变装 1 主证 03.63-03.88s/变装 2 主证 04.95-05.65s)

### K314 椅坐蕾丝袜甩鞭链(4拍|坐姿御姐·红底鞋展示)
- 入态:白雕塑椅端坐,黑蕾丝过膝袜交腿,手持鞭带 → 出态:腿前伸点地亮红底,鞭带垂落身侧
- 分解:拍1 5.65-6.10s 椅坐定态:酒红裙披膝抚平,鞭带在右手划小圈(道具动能保持);拍2 6.10-6.60s 上腿向前下方蹬伸至半直,脚背绷直,红底鞋底朝镜头闪现(技术峰值:鞋底红面全露约 0.3s),蕾丝袜筒随小腿拉伸下滑半寸(袜口物理);拍3 6.60-7.10s 腿回收交叠,鞭带绕腕收短;拍4 7.10-7.50s 双腿交叠静置,鞭梢垂落裙侧摆动两次后静止,下颌抬,御姐终态
- H3:`sitting on the sculptural white chair in floral lace thigh-highs, circling the black strap whip in hand, kicking the top leg into a pointed extend that flashes the red sole at camera, then re-crossing the legs and letting the whip tails settle`
- 来源:《拿下你》05.65-07.50s

**片<v104> 《梦的翅膀》(出画换装+流苏浅跳·18.6s·竖屏)**
- 背景人物:走廊式室内,浅米墙+深色竖条吸音板+顶部黄色灯带,木地板+灰色地垫,固定三脚架宽机位。人物:棕黑长卷发。三套造型:①白色缎面衬衫(胸前垂系带)+白色阔腿裤;②黑色斜肩挂颈上衣(领口银钻链)+黑高腰短裤+灰黑透肉丝袜+黑高筒靴+大圈银耳环;③白色钩织流苏挂脖迷你裙。AIGC:非全 AI——两处变装均为"人物走出画→干净空镜→新装回入画"(空镜帧无叠影),实拍剪辑逻辑;判:真拍+重度滤镜。
- 节拍:约 120 BPM(推测,手势动作成对踩拍,段界≈2 小节)。
- 镜头形态:C 快剪(固定机位,出画/入画隐藏切点)。

### K315 出画换装双轮回入画链(8拍|走位变装机制·空镜交接)
- 入态:白缎套装立于画面中央 → 出态:流苏裙入画至中央,手势相位延续
- 分解:拍1 1.73-2.35s 白装食指竖唇"shhh"态,小步左移启动;拍2 2.35-2.73s 左行出画,末帧仅剩衣角(出画完成判据 2.73s 全空);拍3 2.73-3.10s 干净空镜 0.4s(换装时间被剪除的交接窗,切点藏于空镜内);拍4 3.23s 黑装自画左回入画,首帧即举臂过头——臂位与出画前抬手动势同相位(跨空镜姿态延续);拍5 3.60-5.60s 黑装抚额敬礼式→手落扶髋→顶髋摆动,右转身;拍6 5.73-6.23s 右行出画,6.23-7.10s 空镜 0.9s;拍7 7.15-7.60s 流苏裙自画右回入画,首帧手势为指捏式,与黑装出画前手位相位对齐;拍8 7.60-8.00s 行至中央手势起舞(移交 K316)。机制总结:两轮均为"同侧出、同侧入",出入方向左/右交替
- H3:`walking out of frame left in the white satin set, holding a clean empty-room beat, re-entering left in the black halter outfit with the raised arm already in phase, then exiting right and re-entering right in the fringe dress with finger gestures carrying over`
- 来源:《梦的翅膀》01.73-08.00s(轮 1 02.35-03.23s/轮 2 05.73-07.15s)

### K316 流苏裙手势浅跳链(8拍|手势浅跳·流苏物理)
- 入态:中央站定窄距,双手胸前起势 → 出态:双臂交替冲拳高位,弹动律动建立
- 分解:拍1 8.03-9.03s 胸前指尖交替捏放(每拍一指),重心随指左右微移;拍2 9.28-10.03s 单臂侧伸摊掌"展示位"→收回划腰际波浪(流苏层随臂摆向外荡开 30°);拍3 10.53-11.28s 肘折叠横扫+胸前立圈绕腕(滚拳),发力来源前臂旋前肌群;拍4 11.28-12.28s 双拳交替上泵两次,每次泵送膝弹一次(拍点密度峰值);拍5 12.53-13.53s 左右交替上冲拳,拳峰过耳,髋反向顶(交叉发力);拍6 13.78-14.53s 臂斜下甩腕(马蹄腕花),流苏甩出残影;拍7 14.78-15.53s 双手胸前剪刀开合两轮,步距不动(脚下零位移,纯上半身浅跳);拍8 15.78-16.00s 双臂向上预提,进入收尾(移交 K317);惯性延续:每拍手势末梢余摆 0.1-0.15s 与下拍首帧叠接
- H3:`doing an upper-body-only gesture dance in the tiered fringe dress — alternating finger pinches, palm-up presenting sweeps, forearm rolls, double fist pumps with knee bounces, crisscross punches and wrist flops — while the fringe swings outward on every arm stroke and the feet never leave the narrow stance`
- 来源:《梦的翅膀》08.03-16.00s(拳泵主证 11.28-12.28s)

### K317 交叉腕上举 V 收尾链(3拍|ending 定格·慢旋腕)
- 入态:双臂提至肩上 → 出态:双臂上举交叉腕 V 形定格,头侧倾笑
- 分解:拍1 16.00-16.67s 双臂沿体前上行过头顶,前臂交叉、双手互握腕;拍2 16.67-17.40s V 形撑满,腕互绕慢旋两周(技术峰值:上举最高点+旋腕),流苏裙摆随身体小幅螺旋回转;拍3 17.40-18.60s 保持 V 形微旋,头右侧倾至肩,目视镜头定妆,末帧静止至片尾
- H3:`raising both arms overhead into a crossed-wrist V, slowly winding the wrists around each other at the top while the fringe skirt coils, then tilting the head onto the shoulder and holding the pose to the end frame`
- 来源:《梦的翅膀》16.00-18.60s

**片<v105> 《风格多变》(办公椅四连跳切换装·5.0s·竖屏)**
- 背景人物:会议室风,浅木地板+深色竖条纹墙板+黄色氛围灯带,白灰网布滚轮办公椅。人物:王羽杉(前段脸部贴"？"白色圆形遮挡贴,Cut1 后揭面)。五套造型:①黑色短外套+卡其工装阔腿裤+白色厚底解构 sneakers;②蓝色缎面抹胸+金胸饰+浅蓝亮面丝袜(菱纹微光)+蓝色漆皮尖头细高跟;③棕褐后缝线透肉丝袜+棕色绑带高跟+橄榄色缎面吊带;④紫红碎花蕾丝连裤袜+黑色连体短裤;⑤裸腿+黑色细带高跟+豹纹西装外套。AIGC:非全 AI——四个切点两侧均为单一清晰态、零叠影,抱臂与交腿相位跨切精确衔接(剪辑台同姿跳切);判:真拍+重度滤镜(疑似腿部比例后期拉长)。
- 节拍:约 90 BPM(推测,切点间隔 0.63/0.75/0.62s)。
- 镜头形态:C 快剪(固定机位微仰角,五段同构图跳切)。

### K318 办公椅搓手亮底鞋链(5拍|变装前段·道具铺垫)
- 入态:端坐椅中,双手交握于膝 → 出态:抱臂+单腿高举亮鞋底,sneaker 悬荡
- 分解:拍1 0.53-1.10s 双手在膝上互相搓捻(指尖交叠小循环),坐姿下沉;拍2 1.10-1.90s 双臂交叉抱胸,肩耸起,"？"贴纸遮面;拍3 1.90-2.20s 右腿屈膝上提至胸口高度,脚掌翻转令厚底 sneakers 鞋底正对镜头(亮底峰值);拍4 2.20-2.45s 提腿落成交叠,鞋跟脱离脚跟悬荡两次(鞋类"半脱"态展示);拍5 2.45-2.52s 抱臂交腿静止,与下段蓝装入态完全同相位(跳切对齐帧)
- H3:`sitting in the office chair rubbing the hands together, crossing the arms, then hoisting one leg up to flash the chunky sneaker sole at camera and letting the heel dangle off the toe before locking the crossed pose for the jump cut`
- 来源:《风格多变》00.53-02.52s

### K319 同姿四连跳切换装链(8拍|袜鞋交替卡点·抱臂锚定)
- 入态:抱臂交腿(工装裤+sneakers) → 出态:豹纹装裸腿交腿笑定
- 分解:拍1 2.52s 硬切①→②:卡其裤→浅蓝亮面丝袜+蓝漆皮尖头跟,缎面抹胸+金胸饰,抱臂角度与交腿相位帧级衔接(真跳切,无叠影);拍2 2.585-3.085s 蓝装段:交腿脚尖慢绷两次,鞋跟脱离悬荡一次,"？"贴纸消失露脸;拍3 3.15s 硬切②→③:棕褐后缝线袜+棕绑带跟,腿型换为"交叠+前伸"延长位;拍4 3.335-3.835s 棕褐段:前伸腿脚尖四拍小循环(绷—勾—绷—绷),单手抬至锁骨再落;拍5 3.90s 硬切③→④:紫红碎花蕾丝连裤袜+黑连体短裤,回到屈膝交叠位;拍6 3.96-4.46s 紫段:握拳抵膝捶按两次+脚掌上下点动(蕾丝花纹随点动变形回弹);拍7 4.52s 硬切④→⑤:裸腿+黑细带高跟+豹纹外套,腿前伸交叠;拍8 4.585-5.03s 豹纹段:双手叠膝,脚尖慢绷定格,末帧微笑定妆——五态共用"抱臂/交腿"骨架,仅换袜鞋与上衣(变装机制:同姿跳切+袜鞋轮替)
- H3:`holding crossed arms and crossed legs while hard jump-cutting through four looks on the same office chair — glossy light-blue patterned tights with blue patent pumps, back-seam tan stockings with brown strappy heels, purple floral lace tights with a black romper, then bare legs with black strappy heels and a leopard blazer — cycling toe points and heel danglers on every look`
- 来源:《风格多变》02.52-05.03s(切点 02.52/03.15/03.90/04.52s)

**片<v106> 《热舞计划》(背身入画+逐件上装+船长制服浅跳·6.9s·竖屏)**
- 背景人物:极简灰墙+木地板,无陈设,正面固定机位全身景。人物:王羽杉。四段造型:①白色宽松一字肩罩衫+黑白格纹灯笼裤,赤足(背身);②白色短上衣+藏青迷你裙+灰黑透肉丝袜+黑高跟;③同上+腰间黑色织带束具(工具腰带);④船长制服终态:白色船长帽(金边徽章)+藏青水手领巾+白色收腰短上衣(中腹镂空)+黑色腰束具垂带+藏青高腰热裤(侧挂条纹小领带)+灰黑透肉丝袜+黑高跟。AIGC:非全 AI——三处切点均为硬切无叠影,背身行走/转身发丝甩动自然;重度美颜+疑似液化身形。判:真拍+重度滤镜液化。
- 节拍:约 128 BPM(推测,手势 0.33-0.5s 一动)。
- 镜头形态:C 快剪(固定机位,四段跳切)。

### K320 背身行走转身回眸链(4拍|开场走位·发丝惯性)
- 入态:背对镜头远端行走 → 出态:正面站定,手抬至胸前,发丝落定
- 分解:拍1 0.03-0.53s 背身向画内远端走,灯笼裤随步幅左右荡(低位鼓荡),赤足点地;拍2 0.53-0.78s 右后转身 180°,长发随转体甩出弧形残影(发丝惯性峰值),罩衫下摆随转拖带;拍3 0.78-1.03s 面向镜头小退半步站定,手自体侧抬至胸前;拍4 1.03-1.09s 抬手至脸侧定相位,与变装后挥手位对齐(跳切衔接帧)
- H3:`walking away from camera in a white slouchy tee and gingham balloon pants, pivoting 180 degrees with the long hair whiplashing around, stepping back to a stand and raising one hand to the face as the pose locks for the cut`
- 来源:《热舞计划》00.03-01.09s

### K321 逐件上装三连跳切链(6拍|渐进变装机制·单件增量)
- 入态:白衫+藏青裙+灰袜+高跟(挥手位) → 出态:船长帽+领巾+热裤+束具全套,单腿屈膝亮相
- 分解:拍1 1.09s 硬切①→②:格纹灯笼裤→藏青迷你裙+灰黑丝袜+黑高跟,手掌外翻挥动位跨切延续;拍2 1.155-1.655s 裙装段:掌心向镜头摆两拍,髋随摆左右递;拍3 1.72s 硬切②→③(单件增量:仅加腰间黑色织带束具),手位仍为胸前位——逐件上装节奏点;拍4 1.78-1.905s 束具段:手向右侧平展引视线至腰(束具垂带摆动);拍5 1.94s 硬切③→④(单件增量×3:船长帽+水手领巾+裙换热裤一次性落齐);拍6 2.03-2.15s 终态亮相:单腿屈膝提踵、脚尖点于支撑腿后,手指捏合于颊侧——制服全态首帧即舞蹈起手位(移交 K322);机制总结:0.85s 内三切逐件上装,手位相位全程连续
- H3:`hard jump-cutting the costume on piece by piece while the waving hand never breaks phase — pants swap to a navy mini skirt with sheer tights and heels, then a black utility belt snaps on, then captain hat with neck scarf and hot pants land all at once before the leg-lift reveal`
- 来源:《热舞计划》01.09-02.15s(切点 01.09/01.72/01.94s)

### K322 交叉腿站姿手势波链(7拍|站姿浅跳·腕指序列)
- 入态:交叉腿提踵站架,指尖捏合 → 出态:双臂落回体侧,正身定妆
- 分解:拍1 2.15-2.53s 交叉腿站架(前膝叠于后膝前、前脚掌点地)固定,右手食指指天→指侧→指前(三连指,每指 0.13s);拍2 2.70-3.20s 掌心外翻高位摆→腕花下落,站架重心小幅左右递;拍3 3.36-3.87s 前臂立滚(拳轮绕腕两周)→掌心向上腰前"托盘"展示位;拍4 4.03-4.53s 耳侧快摆掌两轮→单臂斜下 45° 甩出(发梢随肩带出余摆);拍5 4.70-5.20s 双臂体侧半展、手腕同步甩摆(鸟翼腕,左右各两拍);拍6 5.36-5.87s 双臂回收落体侧(回收顺序:肘→腕→指);拍7 5.90-6.87s 正身站定,肩线回平,下颌微收定妆至片尾——全链脚下零位移,纯上肢+骨盆浅跳(时间窗完整:每手势在一个 0.33-0.5s 拍窗内起收闭合,无烂尾动作)
- H3:`holding a crossed-leg lifted-heel stance while waving through a finger-point triple, palm flicks, forearm rolls, a tray-presenting pose, ear-level flicks, diagonal arm throws and synchronized wrist flops, then folding the arms back to the sides and settling square to camera`
- 来源:《热舞计划》02.15-06.87s

---

## L. 成品 T2VA 范本与续写提示词收录(外部项目全文并入 · 2026-11-09)

> 收录原则:外部反推/续写项目的完整可粘贴提示词**全文并入**,原文不改。L2 为 L1 的密帧深化修订版(道具窗修正:大厅两侧白色方块,非黑椅;以 L2 为准)。各 Job 时长 ≤15s,块自带共享 DNA 段;`<Audio 1>` 未挂接(声音走块外 postproduction_copy 交接,见各文档 PART C)。忠实度 L1(director's plan),非帧级复刻。

### L1 Miniskirt(AOA)7 人办公室翻跳 — H3 T2VA 详细反推(12 Jobs)·基础版

```text
FIDELITY TIER: L1 (director's plan). Based on ~78 source frames (global + two dense
batches at ~2.5s spacing); NO per-frame skeleton tracking and NO audio onset detection.
Timings approximate (0.1s precision); a directorial plan, not a frame-accurate
reproduction. Visual evidence: source-video frames only, no stock images.
SCOPE: main dance program only, 0.00–150.53s; the ending credits/blooper reel
(~150.5–254s) is excluded per user. FILM TYPE: C — multi-shot MV montage with hard-cut
named setups; audio unverified, cut-to-downbeat claims inferred from picture rhythm.
```

源文件 SHA-256：`f0aeed79425db69b8788c926c8027ef833234fbe4d92c5e10f9a9b9344b29097`
画幅：854×384（宽幅，约 2.22:1，画面内为宽银幕构图），30fps。声音：音轨存在、内容未核听（`N/A`，原声交接见文末）。

---

# PART A — 共享视觉 DNA（全片适用，各 Job 引用）

## A1. subject_definitions（七名舞者，按造型与当前位置区分，不固定个人编号）

```text
Seven female dancers, tracked by current position and look rather than a fixed name,
since they exchange places. One BLONDE dancer (short chin-length blonde bob, straight
bangs) is the visual anchor and frequently takes center; the other six have long dark
hair (black or brown, straight or wavy, some half-tied up, some worn down), fair skin,
defined eye makeup, small earrings and delicate necklaces.
OFFICE LOOK (the dominant program): white or fine-striped fitted shirts, some with
black suspenders, a short black mini-skirt, sheer black stockings, black stiletto
heels, and a lanyard ID badge on a black strap; hair mostly down.
HALL LOOK: tight black mini-dresses with cut-out / open-back / halter details, black
stockings with garter belts, black stilettos; some sequences use black chairs.
All seven keep the same costume within each scene; the blonde stays blonde throughout.
```

## A2. environment_definition

```text
OFFICE: a bright modern open-plan office with a pale blue-grey floor, large floor-to-
ceiling windows in soft daylight, glass-block walls, a curved archway and a round
ceiling light; desks, office chairs, computers and a cylindrical column fill the
background; clean, cool and airy.
HALL: a grand warm-lit hall with a black-and-white checkerboard floor, tall white
columns, a white paneled double door, a chandelier, wall sconces and curtains; a warm
amber glow from the sides; black chairs are used for the chair-dance section.
The wide frame is letterboxed; no on-screen text is required to be generated.
```

## A3. lighting_definition

```text
OFFICE: soft cool daylight from the large windows, even and diffuse with gentle fill,
pale neutral-to-cyan color temperature, soft shadows and clean specular highlights on
the smooth floor and the sheen of stockings.
HALL: warm amber key from side wall lights, harder and more directional, deep warm
shadows on the checkerboard floor, a chandelier overhead; strong rim light separates
the black outfits and bare skin.
Lighting stays constant within each scene and switches only on the hard scene cuts;
subtle film grain, no random flicker.
```

## A4. named camera setups

```text
WIDE FRONTAL (WF): eye-level full-body wide, whole ensemble and floor visible —
  dominant, establishes formation.
LOW ANGLE (LA): camera near the floor looking up, legs and stilettos emphasized,
  figures read long; glossy floor in the foreground.
HIGH ANGLE (HA): elevated (not fully vertical) framing of layered or bent formations.
MEDIUM CLOSE (MC): chest-up framing for facial and hand gestures, shallow depth.
INSERT (INS): tight detail — legs, heels, hem, hands at the lips, hair.
WHIP / WIPE (WB): fast motion-blur move or a body/hair occlusion used as a motivated
  bridge between setups.
Use only the assigned setup per beat; no unmotivated camera moves.
```

## A5. body_mechanics（K-pop 性感舞蹈力学）

```text
GROUNDING & FORCE: in stilettos the weight stays over the balls of the feet; every
move initiates from the floor and travels hip -> lumbar -> chest -> shoulder -> arm.
A small breath or counter-wind-up precedes each release.
HIP & WAVE: pelvic sways and body rolls are driven by the hips with the knees soft;
the wave passes sequentially through belly, chest and shoulders, never as one rigid
tilt. SQUATS: the center of mass drops over the heels, knees tracking over the toes,
back elongated, then the hips drive the rise.
FLOOR WORK: in the lying pose the body lowers with controlled support, the spine
arcing on the floor; hands frame the head, legs extended, no collapsed weight.
CHAIR DANCE: the chair is a stable prop; weight sits into the hips, legs extend and
cross, hands trace the thighs and back while the torso stays lifted.
HEAD & EYES: gaze follows the leading hand; on turns the head arrives last; faces stay
composed and confident, expressions controlled, no constant smile.
```

## A6. costume_hair_physics

```text
Nothing animates independently. Long hair, the loose shirt hems and the short skirt
lag slightly behind each hip or body acceleration and settle with a soft secondary
motion; on turns hair flares and on squats the skirt and stocking lines follow the
thighs. The ID lanyard swings with a small lag. Fabrics keep a natural body-to-cloth
gap and fold at the waist and knees; no plastic stiffness, no clipping through the
body, chairs, heels or other dancers; garter straps and stocking seams stay aligned.
```

## A7. CONTINUITY GUARD（七人，全片适用）

```text
- exactly SEVEN dancers at all times: no duplicated or extra bodies, no half-formed or
  fused limbs;
- each dancer keeps her own identity and look: NO face swap, NO costume or accessory
  transfer, the blonde stays the only blonde, including during crossings, occlusion,
  back views and floor work;
- position changes occur ONLY via the described continuous paths — NO teleportation,
  NO instant side-swaps, NO two dancers occupying one point or merging;
- when hair or a body occludes the lens, identities and costumes remain unchanged
  behind it; identity continuity takes priority over completing a move;
- office vs hall changes are SCENE/COSTUME cuts only at the stated boundaries; inside
  one scene the outfits never change.
```

---

# PART B — 12 个 Job 详细时间线（本地时钟从 00:00 重置）

## Job 01 — 源 00:00.00 → 00:13.07（13.07s）｜黑场 → 冷开场大厅预告

```text
integrated_multimodal_description: [Shot 1] A pure black frame holds with only the small fixed platform watermark in the upper corner, no subject and no motion. [Shot 2] At 00:02.300, a hard cut reveals the grand warm hall as a cold-open teaser: the seven dancers in black mini-dresses and stockings on the checkerboard floor, three seated low on the floor with hands planted while four stand behind them, the blonde among the standing group; warm amber light and columns frame the confident pose. [Shot 3] At 00:05.500, the picture begins rapid montage cuts between the hall group and brief cool office flashes, each hard cut landing on a new pose — a hand at the lips, a hip turned, a back-view turn — building anticipation without a continuous camera move.

camera_direction: Shot 1 locked off on black. Shot 2 wide frontal held steady to establish the seven. Shots 3 onward are discrete hard-cut setups (WF/MC), each near-locked, with only small motivated framing; the fast changes come from editing, not a drifting or orbiting camera.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 02 — 源 00:13.07 → 00:24.13（11.06s）｜办公室开场 → 地面躺卧

```text
integrated_multimodal_description: [Shot 1] A hard cut into the bright cool office; the dancers begin to move into position among the desks and windows. [Shot 2] At 00:03.100, the program settles and a long-haired dancer lowers into a floor pose: she lies on the smooth floor in a white sleeveless knit top and black skirt, spine arcing, long hair spread around her, both hands framing her head while one leg extends; another dancer's legs in heels stand on a desk softly behind her. She holds the reclined pose with controlled support, gaze toward the camera.

camera_direction: Shot 1 wide frontal with a small slow move as they take position. Shot 2 low angle close to the floor, held near-locked on the lying dancer with a tiny slow push, motivated by her lowering to the ground; the background legs stay in frame. No tilt drift, no orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 03 — 源 00:24.13 → 00:35.70（11.57s）｜办公室队形 → 近景

```text
integrated_multimodal_description: [Shot 1] Back in standing formation, the seven move through synchronized hip sways and soft arm gestures in the office, knees relaxed, weight over the balls of the feet. [Shot 2] At 00:06.500, the framing tightens toward a few dancers as one hand sweeps the hair and the torso rolls through a body wave. [Shot 3] At 00:08.000, a closer chest-up framing catches the confident expression and a hand gesture, the bright windows and desks soft behind.

camera_direction: Shot 1 wide frontal with a small lateral follow of the hip movement, motivated by their sway. Shot 2 medium close with a small slow push as the hand sweeps the hair. Shot 3 near-locked chest-up; every move is motivated by the named body action, no autonomous push or orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 04 — 源 00:35.70 → 00:50.00（14.30s）｜七人全景 → 金发特写

```text
integrated_multimodal_description: [Shot 1] A wide office shot shows all seven in a clean line, executing a synchronized pelvic sway with hands traveling from the waist outward, the blonde at one side. [Shot 2] At 00:08.100, the camera cuts into a closer formation as the dancers turn and let long hair flare. [Shot 3] At 00:12.500, a medium close frames the blonde dancer turning over her shoulder, fingers drawing to her lips in a confident hush gesture, the office windows glowing behind her while another dancer moves in the foreground.

camera_direction: Shot 1 wide frontal held steady on the line. Shot 2 medium framing with a small follow of the turn and hair flare. Shot 3 medium close with a small slow push toward the blonde, motivated by her hand moving to her lips; no zoom beyond the face, no orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 05 — 源 00:50.00 → 01:04.63（14.63s）｜办公室队形快切

```text
integrated_multimodal_description: [Shot 1] The office formation continues with the seven stepping through a hip-driven sequence, arms crossing and opening. [Shot 2] At 00:02.100, a quick cut to a tighter angle catches a body wave and a hand tracing the waist. [Shot 3] At 00:03.500, another hard cut shows the group turning, hair and skirt hems flaring. [Shot 4] At 00:04.300, a closer framing holds the confident face. [Shot 5] At 00:12.000, the view returns to a wide office line as they drop into a bent-knee move and rise on the hip.

camera_direction: Shot 1 wide frontal. Shots 2-4 are discrete medium/insert hard cuts, each near-locked, motivated by the wave, turn and facial gesture; Shot 5 wide frontal with a small follow of the drop and rise. The density comes from editing, not a continuous rush or orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 06 — 源 01:04.63 → 01:19.00（14.37s）｜办公室 → 内部机位快切

```text
integrated_multimodal_description: [Shot 1] A wide office shot carries the seven through synchronized sways and arm arcs. [Shot 2] At 00:03.600, a medium framing follows a turn with hair flare. [Shot 3] At 00:10.400, a rapid burst of internal cuts: hard cut to a back-view, then a side profile, then a hand at the hip, each landing on a distinct pose while the location stays the same office. [Shot 4] At 00:13.100, the group settles into a line facing the camera.

camera_direction: Shot 1 wide frontal with a small lateral follow. Shot 2 medium follow of the turn. Shot 3 three near-locked hard-cut setups (WF/MC/INS) with no motion blur between them, motivated by the back turn, profile and hand gesture; Shot 4 wide frontal held. No LOCK/BURST effect, no orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 07 — 源 01:19.00 → 01:27.67（8.67s）｜办公室双人 → 全景

```text
integrated_multimodal_description: [Shot 1] A medium two-shot in the office shows two dancers standing back to back, one dark-haired and one brown-haired, each tracing a hand to the neck and rolling the shoulder. [Shot 2] At 00:02.100, a small cut widens as they turn away. [Shot 3] At 00:05.000, the view opens toward the full ensemble beginning the next formation.

camera_direction: Shot 1 medium two-shot near-locked with a tiny push on the shoulder roll. Shot 2 small framing change as they turn. Shot 3 a gentle pull-out to wide frontal, motivated by the group opening up; no orbit, no handheld drift.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 08 — 源 01:27.67 → 01:42.67（15.00s，内部 15s 拆分点）｜办公室全景

```text
integrated_multimodal_description: [Shot 1] A wide office shot shows all seven in mixed orientations, some facing the camera and some turned, moving through a layered hip sequence with arms extending outward. [Shot 2] At 00:07.000, they bend forward in unison, hands traveling down the thighs, long hair falling forward, then drive the hips back up through a body wave. [Shot 3] At 00:13.300, they settle into a front-facing line, the blonde at one side, holding the closing pose.

camera_direction: Shot 1 wide frontal held with a small follow of the layered moves. Shot 2 the camera dips slightly with the forward bend and rises with the wave, motivated by the body. Shot 3 near-locked wide frontal. No unmotivated push, no orbit; the 15-second boundary is an internal split, so the next Job continues from the same pose.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 09 — 源 01:42.67 → 01:55.63（12.96s）｜办公室末段 → 大厅切换

```text
integrated_multimodal_description: [Shot 1] The office program continues with the seven in formation, bending forward in unison as hands travel down the thighs and hair falls, then rising through a hip wave. [Shot 2] At 00:07.700, a small cut holds the office line. [Shot 3] At 00:09.500, a hard scene cut reveals the grand warm hall: the seven now in black mini-dresses with cut-out backs and garter belts, the blonde centered, standing in a confident line on the checkerboard floor under warm amber light. [Shot 4] At 00:13.000, they begin the first hall hip sequence.

camera_direction: Shot 1 wide office with a small dip and rise following the bend. Shot 2 near-locked office line. Shot 3 wide frontal hall held steady on the new costume and formation, the hard cut carrying the change. Shot 4 small lateral follow of the hip move. No orbit, no dissolve across the scene change.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 10 — 源 01:55.63 → 02:09.87（14.24s）｜大厅椅子舞

```text
integrated_multimodal_description: [Shot 1] In the hall, the seven move around black chairs in mixed orientations, some seated and some standing, the blonde at the center. [Shot 2] At 00:02.200, a hard cut shows them seated on the chairs, legs extending and crossing while hands trace the thighs and the back of the chair, torsos lifted. [Shot 3] At 00:08.200, the view opens to a wide hall line as they rise and turn, hair flaring, moving into a standing hip sequence.

camera_direction: Shot 1 wide frontal with a small follow around the chairs. Shot 2 medium framing near-locked on the chair poses, motivated by the leg and hand lines. Shot 3 a gentle pull-out to wide frontal as they rise, then a small follow of the turn; no orbit, no handheld drift.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 11 — 源 02:09.87 → 02:24.53（14.66s）｜大厅椅子舞 → 斜排

```text
integrated_multimodal_description: [Shot 1] The hall chair sequence continues with the seven in varied seated poses, one dancer turning her back to the camera while others extend a leg. [Shot 2] At 00:08.900, they rise and spread into a diagonal line, the blonde at one end, arms extending. [Shot 3] At 00:10.800, a closer framing catches the blonde and a neighbor facing the camera. [Shot 4] At 00:14.700, the wide hall line drops into a synchronized squat and rises on the hip.

camera_direction: Shot 1 medium/wide near-locked on the chair poses. Shot 2 wide frontal with a small follow as the diagonal forms. Shot 3 medium close with a tiny push. Shot 4 wide frontal dipping and rising with the squat, motivated by the body; no orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 12 — 源 02:24.53 → 02:30.53（6.00s）｜大厅末 → 回办公室收束

```text
integrated_multimodal_description: [Shot 1] A final wide hall line holds the seven in the black dresses on the checkerboard floor. [Shot 2] At 00:01.500, a hard cut returns briefly to the cool office, the dancers in white shirts and black skirts moving through a closing hip gesture. [Shot 3] At 00:03.700, they settle into a front-facing line and hold the final confident pose as the main dance program ends.

camera_direction: Shot 1 wide hall held steady. Shot 2 hard cut to wide office with a small follow of the closing gesture. Shot 3 near-locked wide frontal on the final pose; the ending credits are excluded and begin immediately after this boundary. No orbit, no drift.

overall_soundscape: N/A

non_diegetic_music: N/A
```

---

# PART C — 原声交接（audio_handoff，块外，不进入 H3 三字段）

```yaml
method: postproduction_copy
source:
  path: d:\Users\Administrator\Downloads\女人的身体为什么这么美妙 _  Miniskirt-AOA｜短裙的权威我后知后觉_P1_Miniskirt.mp4
  sha256: f0aeed79425db69b8788c926c8027ef833234fbe4d92c5e10f9a9b9344b29097
  audio_stream_index: 1
  audio_start_s: 0.0
audio_status: unavailable   # 音轨存在但未核听，未写歌词/曲风
retained_range_s: [0.0, 150.53]   # 仅正片，片尾 150.53–254 不沿用
route_maps:
  - {source_range: [0.0, 150.53], assembly_range: [0.0, 150.53], copies: 1}
postproduction_copy:
  - 生成全部 12 个视觉 Job 后，移除各 Job 自带的生成音轨；
  - 从源文件按同一时间戳只铺回一次原始音频 0.0–150.53，跨 Job 硬切处不重启、不重复；
  - 保留源开头到首个画面之间的原始状态，不另加静音或淡入。
sync_risks:
  - 未做音频 onset 检测，"切点挂重拍"仅据画面节奏推断，需后期核对；
  - 独立生成的嘴型不会自动对齐原曲，口型/节拍未测，若要贴合需改用 Ref2VA 音频驱动；
  - 若后续重排或改时长，本一比一映射失效，需重新设计声音方案。
```

# PART D — 装配说明（assembly）

```text
1. 12 个 Job 按序硬切拼接，总时长 150.53s；Job 之间不做叠化，仅 Job 08→09 为内部 15s 拆分的同姿态延续。
2. 场景/造型切换只发生在：Job01 冷开场（大厅）、Job02 起办公室、Job09 切大厅、Job12 短暂回办公室。
3. 椅子舞集中在 Job10–11（约 115–138s），黑椅作为稳定道具，不生成多余椅子。
4. 冷开场（Job01）先给大厅高潮再回办公室，保留预告式结构，不调整为正序。
5. 字幕、成员名、credits 与平台水印均为后期叠加层，不要求模型渲染任何中文/文字，避免乱码；本次范围本就不含片尾。
6. 保持宽幅（约 2.22:1）与 letterbox，不裁切、不改画幅。
```

# PART E — 局限与诚实声明

```text
- L1 忠实度：仅基于媒资参数与约 78 个稀疏真实帧（~2.5s 间隔），未做逐帧骨骼追踪，
  段落时间为近似值（0.1s 精度），不构成帧级复刻。
- 抽帧信息缺失：关键帧之间的迈步、旋转、换重心无法仅靠联系表精确还原，已按连续运动
  描述并标注，未把关键帧当独立姿势拼贴。
- 声音未核听：未跑 onset/BPM，未写歌词、曲风、配器；三字段声音为 N/A，原声以块外
  postproduction_copy 交接，口型/节拍未测。
- 提示词 ≠ 生成结果：模型仍可能出现人数漂移、换脸、服装转移、穿模或场景回退，需按
  七人连续性保护逐段验收。
- 本片为文件名带 _P1_ 的分段，是否存在 P2 未知；本次仅覆盖该文件正片。
```

## 12 Job 时长校验

| Job | 源范围 | 时长 | 场景/造型 |
|---|---|---|---|
| 01 | 0.00–13.07 | 13.07 | 黑场+大厅冷开场 |
| 02 | 13.07–24.13 | 11.06 | 办公室（躺地） |
| 03 | 24.13–35.70 | 11.57 | 办公室 |
| 04 | 35.70–50.00 | 14.30 | 办公室（金发特写） |
| 05 | 50.00–64.63 | 14.63 | 办公室 |
| 06 | 64.63–79.00 | 14.37 | 办公室 |
| 07 | 79.00–87.67 | 8.67 | 办公室 |
| 08 | 87.67–102.67 | 15.00 | 办公室（内部拆分） |
| 09 | 102.67–115.63 | 12.96 | 办公室→大厅 |
| 10 | 115.63–129.87 | 14.24 | 大厅椅子舞 |
| 11 | 129.87–144.53 | 14.66 | 大厅椅子舞 |
| 12 | 144.53–150.53 | 6.00 | 大厅→办公室 |
| 合计 | | **150.53** | |

### L2 Miniskirt(AOA)7 人办公室翻跳 — H3 T2VA 深化反推(12 Jobs,密帧版)·修订版

```text
FIDELITY TIER: L1 (director's plan, dense-frame pass). Now based on ~206 source frames:
the original ~78 plus two new dense batches at ~1.2s spacing (128 frames). Still NO
per-frame skeleton tracking and NO audio onset detection; timings approximate (0.1s).
A directorial plan, not a frame-accurate reproduction. Visual evidence: source frames
only, no stock images. SCOPE: main dance program 0.00–150.53s; ending credits excluded.
FILM TYPE: C — multi-shot MV montage, hard-cut named setups; cut-to-downbeat claims
inferred from picture rhythm. This revision refines movement paths, formation order and
camera setups, and corrects the prop window: the only props are white cube blocks at the
hall sides, used in selected setups and cross-cut with standing/squatting formations,
not a continuous seated routine and no black chairs.
```

源文件 SHA-256：`f0aeed79425db69b8788c926c8027ef833234fbe4d92c5e10f9a9b9344b29097`
画幅：854×384（宽幅，约 2.22:1，letterbox），30fps。声音：音轨存在、未核听（`N/A`，交接见文末）。

---

# PART A — 共享视觉 DNA（全片适用）

## A1. subject_definitions

```text
Seven female dancers, tracked by current position and look rather than a fixed name,
because they exchange places. One BLONDE dancer (short chin-length blonde bob, straight
bangs) is the visual anchor and frequently takes center; the other six have long dark
hair (black or brown, straight or wavy, some half-tied or ponytailed, some worn down),
fair skin, defined eye makeup, small earrings and delicate necklaces.
OFFICE LOOK (dominant): white or fine-striped fitted shirts, some with black suspenders,
a short black mini-skirt, sheer black stockings, black stiletto heels, and a lanyard ID
badge on a black strap; hair mostly down.
HALL LOOK: tight black mini-dresses with cut-out / open-back / halter / chain details,
black stockings with garter belts, black stilettos; white cube blocks at the sides are
used in selected setups only. All seven keep the same costume within a scene; the blonde stays blonde.
```

## A2. environment_definition

```text
OFFICE: bright modern open-plan office, pale blue-grey smooth floor, large floor-to-
ceiling windows in soft daylight, glass-block walls, a curved archway and a round
ceiling light; desks, office chairs, computers and a cylindrical column in the
background; clean, cool, airy.
HALL: grand warm-lit hall, black-and-white checkerboard floor, tall white columns, a
white paneled double door, a chandelier, wall sconces and curtains; warm amber side
glow; fixed white cube blocks beside the column bases are used in selected setups.
Wide letterboxed frame; no on-screen text is to be generated.
```

## A3. lighting_definition

```text
OFFICE: soft cool daylight from the windows, even and diffuse with gentle fill, pale
neutral-to-cyan color temperature, soft shadows, clean specular highlights on the smooth
floor and the sheen of stockings.
HALL: warm amber key from side wall lights, harder and more directional, deep warm
shadows on the checkerboard floor, chandelier overhead; strong rim light separates the
black outfits and bare skin.
Constant within each scene, switching only on hard cuts; subtle film grain, no flicker.
```

## A4. named camera setups

```text
WF  WIDE FRONTAL : eye-level full-body, whole ensemble and floor — dominant.
LA  LOW ANGLE    : near the floor looking up, legs and stilettos emphasized, glossy
                   foreground floor.
HA  HIGH ANGLE   : elevated (not fully vertical) framing of layered or bent formations.
MC  MEDIUM CLOSE : chest-up facial and hand gestures, shallow depth.
INS INSERT       : tight detail — legs, heels, hem, hands at the lips, hair.
WB  WHIP/WIPE    : fast motion-blur move or body/hair occlusion as a motivated bridge.
Use only the assigned setup per beat; no unmotivated camera moves.
```

## A5. body_mechanics

```text
GROUNDING & FORCE: in stilettos the weight stays over the balls of the feet; every move
initiates from the floor and travels hip -> lumbar -> chest -> shoulder -> arm. A small
breath or counter-wind-up precedes each release.
HIP & WAVE: pelvic sways and body rolls are driven by the hips with soft knees; the wave
passes sequentially through belly, chest and shoulders, never as one rigid tilt.
SQUATS: center of mass drops over the heels, knees tracking over the toes, back
elongated, then the hips drive the rise.
FLOOR WORK: in the lying pose the body lowers with controlled support, spine arcing on
the floor; hands frame the head, legs extended, no collapsed weight.
CUBE BLOCK (selected setups): the white cube is a fixed stable prop beside the column;
dancers perch on it with weight in the hips, legs extending, hands tracing the thighs
while the torso stays lifted, then leave it for standing or floor-squat moves.
HEAD & EYES: gaze follows the leading hand; on turns the head arrives last; faces stay
composed and confident, no constant smile.
```

## A6. costume_hair_physics

```text
Nothing animates independently. Long hair, loose shirt hems and the short skirt lag
slightly behind each hip or body acceleration and settle with a soft secondary motion;
on turns hair flares and on squats the skirt and stocking lines follow the thighs. The ID
lanyard swings with a small lag. Fabrics keep a natural body-to-cloth gap and fold at the
waist and knees; no plastic stiffness, no clipping through the body, cube blocks, heels or
other dancers; garter straps and stocking seams stay aligned.
```

## A7. CONTINUITY GUARD

```text
- exactly SEVEN dancers at all times: no duplicated or extra bodies, no half-formed or
  fused limbs;
- each dancer keeps her own identity and look: NO face swap, NO costume or accessory
  transfer, the blonde stays the only blonde, including during crossings, occlusion,
  back views and floor work;
- position changes occur ONLY via the described continuous paths — NO teleportation,
  NO instant side-swaps, NO two dancers occupying one point or merging;
- when hair or a body occludes the lens, identities and costumes remain unchanged;
  identity continuity takes priority over completing a move;
- office vs hall changes are SCENE/COSTUME cuts only at the stated boundaries; inside
  one scene the outfits never change.
```

---

# PART B — 12 个 Job 深化时间线（本地时钟从 00:00 重置）

## Job 01 — 源 00:00.00 → 00:13.07（13.07s）｜黑场 → 大厅冷开场

```text
integrated_multimodal_description: [Shot 1] A pure black frame holds with only the small fixed platform watermark in the upper corner, no subject, no motion. [Shot 2] At 00:02.300, a hard cut reveals the grand warm hall as a cold-open teaser: all seven in black mini-dresses and stockings on the checkerboard floor, three seated low with hands planted and legs extended while four stand behind them, the blonde among the standing group turned partly away; warm amber light and columns frame the confident pose. [Shot 3] At 00:05.500, a hard cut to a tighter hall angle catches a hand on the hip and a turned shoulder. [Shot 4] At 00:06.500, another cut shows a back-view turn with hair flaring. [Shot 5] At 00:09.700, a brief cool office flash appears. [Shot 6] At 00:11.500, the hall group returns in a layered pose, building anticipation.

camera_direction: Shot 1 locked off on black. Shot 2 wide frontal held steady to establish the seven. Shots 3-6 are discrete near-locked hard-cut setups (WF/MC/INS), each with only small motivated framing; the fast changes come from editing, not a drifting or orbiting camera, and no dissolve links them.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 02 — 源 00:13.07 → 00:24.13（11.06s）｜办公室开场 → 地面躺卧

```text
integrated_multimodal_description: [Shot 1] A hard cut into the bright cool office; the dancers move into position among the desks and windows. [Shot 2] At 00:03.100, the program settles and a long-haired dancer lowers into the floor pose: she lies on the smooth floor in a white sleeveless knit top and black skirt, spine arcing, long hair spread around her, both hands framing her head while one leg extends; another dancer's legs in heels stand on a desk softly behind. She holds the reclined pose with controlled support, gaze toward the camera, then begins to gather for the rise.

camera_direction: Shot 1 wide frontal with a small slow move as they take position. Shot 2 low angle close to the floor, held near-locked on the lying dancer with a tiny slow push, motivated by her lowering; the background legs stay in frame. No tilt drift, no orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 03 — 源 00:24.13 → 00:35.70（11.57s）｜办公室队形 → 近景

```text
integrated_multimodal_description: [Shot 1] Back in standing formation, the seven move through synchronized hip sways and soft arm gestures, knees relaxed, weight over the balls of the feet. [Shot 2] At 00:06.500, the framing tightens as a hand sweeps the hair and the torso rolls through a body wave. [Shot 3] At 00:08.000, a chest-up framing catches the confident expression and a hand gesture, the bright windows and desks soft behind.

camera_direction: Shot 1 wide frontal with a small lateral follow of the sway, motivated by the hip movement. Shot 2 medium close with a small slow push as the hand sweeps the hair. Shot 3 near-locked chest-up; every move is motivated by the named body action, no autonomous push or orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 04 — 源 00:35.70 → 00:50.00（14.30s）｜七人全景 → 单人近景

```text
integrated_multimodal_description: [Shot 1] A wide office shot shows all seven in a clean line, executing a synchronized pelvic sway with hands traveling from the waist outward. [Shot 2] At 00:08.100, the camera cuts closer as the dancers turn and let long hair flare. [Shot 3] At 00:12.500, a medium framing holds the brown-haired dancer wearing thin-frame glasses as she sways her hips, one hand traveling down the thigh and settling near the hem while the long hair sweeps across her shoulder; a dark-haired dancer moves in the same line and the bright windows glow behind, no hand raised to the lips.

camera_direction: Shot 1 wide frontal held steady on the line. Shot 2 medium framing with a small follow of the turn and hair flare. Shot 3 medium framing held near steady with a tiny follow of the hip sway, motivated by the hand traveling down the thigh; no push toward the face, no orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 05 — 源 00:50.00 → 01:04.63（14.63s）｜办公室队形快切

```text
integrated_multimodal_description: [Shot 1] The office formation continues with the seven stepping through a hip-driven sequence, arms crossing and opening. [Shot 2] At 00:02.100, a tighter angle catches a body wave and a hand tracing the waist. [Shot 3] At 00:03.500, a hard cut shows the group turning, hair and skirt hems flaring. [Shot 4] At 00:04.300, a closer framing holds the confident face. [Shot 5] At 00:12.000, a tight close-up centers on the blonde dancer: she turns over her shoulder, draws one index finger to her lips and winks, a dark-haired dancer soft behind her, holding the confident hush pose through the end of the Job.

camera_direction: Shot 1 wide frontal. Shots 2-4 are discrete near-locked medium/insert hard cuts, motivated by the wave, turn and facial gesture; Shot 5 tight close-up near-locked on the blonde with only a tiny push toward the face, motivated by the finger moving to the lips and the wink. The density comes from editing, not a continuous rush or orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 06 — 源 01:04.63 → 01:19.00（14.37s）｜办公室内部机位快切

```text
integrated_multimodal_description: [Shot 1] A wide office shot carries the seven through synchronized sways and arm arcs. [Shot 2] At 00:03.600, a medium framing follows a turn with hair flare. [Shot 3] At 00:10.400, a rapid burst of internal cuts: hard cut to a back-view, then a side profile, then a hand at the hip, each landing on a distinct pose while the location stays the same office. [Shot 4] At 00:13.100, the group settles into a line facing the camera.

camera_direction: Shot 1 wide frontal with a small lateral follow. Shot 2 medium follow of the turn. Shot 3 three near-locked hard-cut setups (WF/MC/INS) with no motion blur between them, motivated by the back turn, profile and hand gesture; Shot 4 wide frontal held. No LOCK/BURST effect, no orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 07 — 源 01:19.00 → 01:27.67（8.67s）｜办公室近景 → 全景

```text
integrated_multimodal_description: [Shot 1] A medium close framing holds three dancers in the office, hands traveling to the hip and neck as they roll through a hip sway. [Shot 2] At 00:02.100, the view widens to a multi-orientation full-ensemble shot with a leg-lift insert. [Shot 3] At 00:05.000, a two-dancer close-up shows them offset front-to-back rather than back-to-back, one drawing a hand behind her neck, before the framing pulls out toward the full ensemble.

camera_direction: Shot 1 medium close near-locked with a tiny follow of the hip sway. Shot 2 wide framing with a small follow of the leg lift. Shot 3 a gentle pull-out to wide frontal, motivated by the group opening; no orbit, no handheld drift.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 08 — 源 01:27.67 → 01:42.67（15.00s，内部 15s 拆分点）｜办公室全景

```text
integrated_multimodal_description: [Shot 1] A wide office shot shows all seven in mixed orientations, some facing the camera and some turned, moving through a layered hip sequence with arms extending outward. [Shot 2] At 00:07.000, they bend forward in unison, hands traveling down the thighs, long hair falling forward, then drive the hips back up through a body wave. [Shot 3] At 00:13.300, they settle into a front-facing line holding the closing pose.

camera_direction: Shot 1 wide frontal held with a small follow of the layered moves. Shot 2 the camera dips slightly with the forward bend and rises with the wave, motivated by the body. Shot 3 near-locked wide frontal. No unmotivated push, no orbit; the 15-second boundary is an internal split, so the next Job continues from the same pose.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 09 — 源 01:42.67 → 01:55.63（12.96s）｜办公室末段 → 大厅切换

```text
integrated_multimodal_description: [Shot 1] The office program continues with the seven in formation, bending forward in unison as hands travel down the thighs and hair falls, then rising through a hip wave. [Shot 2] At 00:01.600, a small cut holds the office line. [Shot 3] At 00:07.700, another office framing carries the closing gesture. [Shot 4] At 00:09.500, a hard scene cut reveals the grand warm hall: the seven in black mini-dresses with cut-out backs and garter belts, the blonde standing in the center of a front-facing line on the checkerboard floor under warm amber light, and they begin the first hall hip sequence within this same shot.

camera_direction: Shots 1-3 wide office near-locked with a small dip and rise following the bend. Shot 4 wide frontal hall held steady on the new costume and formation, the hard cut carrying the change, then a small lateral follow of the hip move. No orbit, no dissolve across the scene change.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 10 — 源 01:55.63 → 02:09.87（14.24s）｜大厅横排

```text
integrated_multimodal_description: [Shot 1] In the hall the seven form a clean line, all turned sideways with hands reaching forward to connect, the blonde among them, open-back dresses and garter belts visible. [Shot 2] At 00:02.200, a hard cut to a centered framing shows the blonde facing the camera with arms extended while neighbors turn away or back. [Shot 3] At 00:08.200, the wide hall line moves through a synchronized hip sequence with hair flaring.

camera_direction: Shot 1 wide frontal held steady on the connected line. Shot 2 medium framing with a small slow push toward the center, motivated by the arm extension. Shot 3 wide frontal with a small lateral follow of the hip move; no orbit, no handheld drift.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 11 — 源 02:09.87 → 02:24.53（14.66s）｜大厅分层（白色方块）→ 斜排

```text
integrated_multimodal_description: [Shot 1] A layered hall formation: one dancer stands centered in the foreground, two crouch low directly on the checkerboard floor, and two more perch on the fixed white cube blocks at the sides, hands tracing the thighs and cube tops, torsos lifted. [Shot 2] At 00:08.900, they rise and spread into a diagonal standing line, arms extending, while the cube blocks stay fixed at the edges. [Shot 3] At 00:10.800, a closer framing catches the group turning, long hair flaring.

camera_direction: Shot 1 wide/high angle near-locked on the layered floor-and-cube poses. Shot 2 wide frontal with a small follow as the diagonal forms. Shot 3 medium close with a tiny push on the turn; the white cube blocks are used only in these selected setups, cross-cut with standing and floor-squat formations, not a continuous seated routine. No orbit.

overall_soundscape: N/A

non_diegetic_music: N/A
```

## Job 12 — 源 02:24.53 → 02:30.53（6.00s）｜大厅末 → 回办公室收束

```text
integrated_multimodal_description: [Shot 1] A final wide hall line holds the seven in the black dresses on the checkerboard floor. [Shot 2] At 00:01.500, a hard cut returns briefly to the cool office, the dancers in white shirts and black skirts moving through a closing hip gesture. [Shot 3] At 00:03.700, they settle into a front-facing line and hold the final confident pose as the main dance program ends.

camera_direction: Shot 1 wide hall held steady. Shot 2 hard cut to wide office with a small follow of the closing gesture. Shot 3 near-locked wide frontal on the final pose; the ending credits are excluded and begin immediately after this boundary. No orbit, no drift.

overall_soundscape: N/A

non_diegetic_music: N/A
```

---

# PART C — 原声交接（audio_handoff，块外）

```yaml
method: postproduction_copy
source:
  path: d:\Users\Administrator\Downloads\女人的身体为什么这么美妙 _  Miniskirt-AOA｜短裙的权威我后知后觉_P1_Miniskirt.mp4
  sha256: f0aeed79425db69b8788c926c8027ef833234fbe4d92c5e10f9a9b9344b29097
  audio_stream_index: 1
  audio_start_s: 0.0
audio_status: unavailable
retained_range_s: [0.0, 150.53]
route_maps:
  - {source_range: [0.0, 150.53], assembly_range: [0.0, 150.53], copies: 1}
postproduction_copy:
  - 生成全部 12 个视觉 Job 后，移除各 Job 自带的生成音轨；
  - 从源文件按同一时间戳只铺回一次原始音频 0.0–150.53，跨 Job 硬切处不重启、不重复；
  - 保留源开头到首个画面之间的原始状态，不另加静音或淡入。
sync_risks:
  - 未做音频 onset 检测，"切点挂重拍"仅据画面节奏推断，需后期核对；
  - 独立生成的嘴型不会自动对齐原曲，口型/节拍未测，若要贴合需改用 Ref2VA 音频驱动；
  - 若后续重排或改时长，本一比一映射失效，需重新设计声音方案。
```

# PART D — 装配说明

```text
1. 12 个 Job 按序硬切拼接，总时长 150.53s；Job 08→09 为内部 15s 拆分的同姿态延续。
2. 场景/造型切换只在：Job01 冷开场（大厅）、Job02 起办公室、Job09 切大厅、Job12 回办公室。
3. 道具仅为大厅两侧的固定白色方块，只在 Job11 等部分机位（约 130–138s）被舞者靠坐，
   与站立、蹲地队形交叉剪辑；不生成黑色椅子，不生成多余方块。
4. 冷开场保留预告式结构，先给大厅高潮再回办公室，不调整为正序。
5. 字幕、成员名、credits 与水印均为后期叠加层，不要求模型渲染任何中文/文字。
6. 保持宽幅（约 2.22:1）与 letterbox，不裁切、不改画幅。
```

# PART E — 局限与诚实声明

```text
- L1 忠实度：基于约 206 个真实帧（含 1.2s 密帧），仍未做逐帧骨骼追踪，段落时间为
  近似值（0.1s 精度），不构成帧级复刻。
- 抽帧信息缺失：帧之间的迈步、旋转、换重心无法仅靠联系表精确还原，已按连续运动
  描述，未把关键帧当独立姿势拼贴。
- 声音未核听：未跑 onset/BPM，未写歌词、曲风、配器；三字段声音为 N/A，原声以块外
  postproduction_copy 交接，口型/节拍未测。
- 提示词 ≠ 生成结果：模型仍可能出现人数漂移、换脸、服装转移、穿模或场景回退，需按
  七人连续性保护逐段验收。
- 本片为文件名带 _P1_ 的分段，是否存在 P2 未知；本次仅覆盖该文件正片。
```

## 12 Job 时长校验

| Job | 源范围 | 时长 | 场景/造型 |
|---|---|---|---|
| 01 | 0.00–13.07 | 13.07 | 黑场+大厅冷开场 |
| 02 | 13.07–24.13 | 11.06 | 办公室（躺地） |
| 03 | 24.13–35.70 | 11.57 | 办公室 |
| 04 | 35.70–50.00 | 14.30 | 办公室（近景） |
| 05 | 50.00–64.63 | 14.63 | 办公室 |
| 06 | 64.63–79.00 | 14.37 | 办公室 |
| 07 | 79.00–87.67 | 8.67 | 办公室 |
| 08 | 87.67–102.67 | 15.00 | 办公室（内部拆分） |
| 09 | 102.67–115.63 | 12.96 | 办公室→大厅 |
| 10 | 115.63–129.87 | 14.24 | 大厅横排 |
| 11 | 129.87–144.53 | 14.66 | 大厅分层（白色方块） |
| 12 | 144.53–150.53 | 6.00 | 大厅→办公室 |
| 合计 | | **150.53** | |

### L3 8s 性感宅舞卡点提示词(BPM 132·主动续写·配 8.06s mp3)

> 依据 AnimateDiff 片(片 v17) onset 实测网格(BPM132,强拍 1.03/1.95/2.86/3.77/4.68/5.60/6.50/7.42,弱拍 7.86,音频止于 8.06s);链位全部取自本库性感系:K70/K45/K72/K73 + B1 持续层 + K74 收束;`<Picture 1>` 锁人物,零外貌文字。

```text
H3 ALL-PURPOSE REFERENCE PROMPT — 8s SEXY-GENKI DANCE — MODE: all-purpose reference (NOT T2VA, NOT a first-frame anchor). Vertical 9:16. Target duration 8.0s, exactly matching <Audio 1> (8.06s).

subject_definitions: <Subject 1> is the exact girl in <Picture 1>; sole all-purpose authority for face, hairstyle, makeup, proportions, costume, accessories and shoes; zero appearance description here. She performs a confident, flirtatious street-idol dance. Exactly one performer; no second person anywhere.

environment_definition: A night city street with warm neon signage melting into bokeh behind her, asphalt under her feet, a few trees as dark silhouettes; the background stays soft and out of focus the whole time.

lighting_definition: Cool streetlight base with warm neon rim-light on her hair edges and shoulders; consistent for all 8 seconds; no light change.

audio: <Audio 1> is the sole authority; fully_copy with original pitch, tempo, dynamics and exact length. BPM 132.0; beat 0.4545s; strong downbeats every 0.91s at 1.03 / 1.95 / 2.86 / 3.77 / 4.68 / 5.60 / 6.50 / 7.42, one syncopated accent at 7.86; audio ends at 8.06. Add no new music or sound effects.

integrated_multimodal_description: One locked hip-height camera, tiny sway always present. A continuous hip figure-eight engine (B1) runs under every phrase on the offbeats, never stopping.
[Pickup · 0.00-1.03] static prep: weight sunk on her right hip, one hand at her neck, eyes into the lens, holding still for a full beat.
[Downbeat 1.03] K70: one palm covers her mouth while the other hand flicks out toward the lens, hip twisting right on the hit.
[Downbeat 1.95] the flicking arm sweeps a wide arc across the frame with heavy motion blur as the torso follows it around.
[Downbeat 2.86] K45: an open palm sweeps slowly across her eyes dragging the hair with it, then slides out of frame — the reveal lands with a smirk.
[Downbeat 3.77] K72: both elbows rise high and wide, fists loose beside her ears, hips popping right-left twice under the beat.
[Downbeat 4.68] the hands slide down from her ears to her collar, one knee bending deeper on the accent while the hips keep popping.
[Downbeat 5.60] K73a: one palm slides up her torso along the centerline to her cheek, a slow self-touch line, eyes holding the lens.
[Downbeat 6.50] K73b: cat-paw hands flash beside her face, one crisp clap in front of her chest as the head tips back laughing — clap and chin land on the same frame, the peak of the take.
[Downbeat 7.42] K73c: pressed palms sway side to side, hips leading and arms following, the swing already decaying.
[Syncopation 7.86] one knee lifts and crosses with one hand on it, the other arm extending out, settling into the final pose.
[8.06] END — the pose holds as the audio stops.

camera_direction: Locked hip-height framing, full body in frame the whole take; no push, no orbit, no cuts; tiny handheld sway only.

editing: No cuts; one continuous take; final state: settled knee-cross pose at 8.06s when the audio ends.

performance: Flirtatious but precise — every downbeat lands a shape, offbeats carry the hip engine; the 7.86 accent is the last flourish, nothing after it; no lip-sync.

costume_hair_physics: Hair and hem lag the hits by half a beat; the ponytails whip on every head move and settle into the final pose; fabric never floats independently.

negative_constraints: Exactly one performer as in <Picture 1>, zero redesign; no second person, no crowd, no hands entering frame; no camera cuts, no digital zoom, no slow motion; no lip-sync; every downbeat shape lands exactly once as written; no motion after 7.86 beyond the settling pose.

overall_soundscape: Audio 1 only; add no traffic, wind, crowd or voiceover unless already present.

non_diegetic_music: fully_copy <Audio 1>; the palette is a guide, not permission to layer a replacement.
```

---

## 报告库索引（reports/ · 双 skill 全量档案 · 零丢失架构）

> 库 md 只存索引与动链；每片完整信息（叙事确认/取证档案/画面分析逐段时间轴/运镜流程时间轴/节奏对账/状态表/完整复刻提示词/声音交接/缺口清单）存独立档案。模板：`reports/_REPORT_TEMPLATE_v2.md`（11 章槽位+置信标记体系+双 skill 分工）。

| 报告 | 片 | 内容 |
|---|---|---|
| `_REPORT_TEMPLATE_v2.md` | — | 报告库模板 v2（11 章槽位） |
| `D001_鸣潮变装.md` | v107 | 鸣潮变装 9.1s：两段式单帧变装机制实锤+环境光调色+T2VA 复刻词；链 K323-324（待入 K 章） |
| `SUPPLEMENT_chat_recovery_v1.md` | — | **会话信息回收补遗**：rA/rB 完整复刻范本对（单动作循环解剖+六段编舞）、《至情至圣》MV 七幕时间线+21 帧量化色值表、batch2 18 片 onset 实测数据表、流程经验教训 7 条、遗留登记 |

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
*来源视频:《双倍可爱❤️甜蜜暴击》(47.4s)、宅舞vs抖舞分屏(238.6s)、《与你提酒》(118.4s)、《皇上》(77.5s)、录舞运镜权威(61.5s)、《うみたがり》4人(222.5s)、《BLESSING》4人(96.8s)、向阳 BDF2021 队形版(144.9s);由八份逐拍反推报告提炼,动链合计 70+ 条;另并入 13 支 I2VA 单人成品范本(H 章,2026-10);《绝世舞姬》混剪(82.9s/44镜,E6 转场章+C36-C47+G 补充,2026-10-02);双人弧形运镜 16.8s(E7)+醉酒式镜头母规则(E8,2026-10-03);《三种袜子》右入换装 5.9s(E9)+三姿态原位换装系列 18.4s(E10:站姿侧身/深蹲抱膝抖腿/提裙站姿,onset 卡点实测,2026-10-05);2026-10-30 并入 K 章 74 条(15 支新片+2 图,短标题↔原片名:《绫华的锻炼时间》10.4s、《saber白礼服》9.6s(原片含书名号前缀"成为士郎的剑")、《saber下腰挑战》8.2s(原片《saber下腰动作挑战》)、《奥黛塔变装》153.4s(原片《花3000为奥黛塔制作视频后，最终决定放弃她.......》)、《夏天结束了》16.1s(原片《夏天结束了——做了四次不同情绪的撩头发》)、《橘福福》27.6s(原片《如此绝美的 橘福福 之后再也没见到》)、《薇薇安》60.6s(原片《好女孩——薇薇安（测试）》)、《维琳娜》75.0s(原片《这维琳娜对....对吗？》,鸣潮维里奈 cos)、《两个御姐合拍》14.9s(原片《两个御姐~格格巫和月月的合拍合集~_P1_好想谈恋爱》)、《请pick西施吧～》32.7s、《I Got Your Back》154.3s(原片【ILLIT】金丝眼镜水手服)、《依赖姐姐》72.0s(原片《依赖姐姐一辈子也不是什么坏事吧》)、《我是银月呀❤》18.1s、《活动饭拍》11.6s(原文件 ANbHNypfOZ8EhWqP)、《旗袍夜景》16.8s(原文件 AWsiPVCcHGVFeJGL)、《狐耳白发六宫格》写真图、《蓝水手服走廊截图》单帧);2026-11-08 追加 K75-K84:《潛行吧！奈亞子！W》宅舞翻跳(97.8s,一镜到底固定机位,变身点 24s,双马尾甩转签名×7,力竭躺倒彩蛋收尾);2026-11-09 并入:《AnimateDiff-补帧》8s AI 宅舞(K85-K88,BPM132 onset 实测)+Miniskirt(AOA)12 Jobs T2VA 两版(L1/L2,外部项目全文)+8s 性感宅舞卡点续写(L3);2026-11-10 追加 K89-K156(18 片):K-pop 直拍批(Hwiseo/tripleS《ANDLESS》双机位/Liz/李真率/咲良饭拍/姜杉《Genie》九机位/EXID)+内娱舞台批(黄诗予生日SP/王心凌《彩虹的微笑》深圳+长春/《第一次爱的人》宁波)+饭拍营业件+《上元》戏腔手势舞+1972 京剧《奇袭白虎团》武戏五件+婚纱换装写真件;v14 编译合集与 v15 全场直拍按用户指示未反推。*
