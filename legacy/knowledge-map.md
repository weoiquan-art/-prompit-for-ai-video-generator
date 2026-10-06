# 旧 → 新 去向表

旧内容整体在 `legacy/`，不加载、不删除，只修正了跨目录的相对链接（见 [README](README.md)）。本表保证没有丢失：每个旧文件要么并入新条目，要么只留历史参考；**没有收进主题文件的规则，在 F 节逐条列出原因**。条目编号见 [evidence/README](../evidence/README.md)：C＝新知识卡（C01–C41；JIN 之后确认的 C42 待补入），O＝旧仓经验并入（O01–O24）；"C01 组"指标题含该编号的合并条目。

## A 文件级去向

| 旧路径 | 大小 | 新位置 | 并入条目 | 说明 |
|---|---|---|---|---|
| SKILL.md | 26.1 KB | legacy/SKILL.v1.md（逐字副本，改名避免同名）；新入口 [SKILL.md](../SKILL.md) | 见 B 节 | |
| agents/openai.yaml | 0.5 KB | 原位不动 | — | |
| assets/icon.svg | — | 原位不动 | — | |
| assets/clean-template.md | 3.6 KB | 原位保留，仅加状态头 | — | 旧格式备选；正文未改 |
| assets/scene-sequence-plan-template.md | 2.6 KB | legacy/assets/ | O22（T9 末尾有指针） | 表格式留原文 |
| assets/samples/（14 个文件，13 MB） | — | legacy/assets/samples/ | — | 样本视频与图，仅历史参考 |
| references/action-scene-writing.md | 11.9 KB | legacy/references/ | O14、O10、C09 组、C05 组 | JIN 2026-10-01 确认的方法，压缩并入；见 F9 |
| references/annotated-template.md | 7.5 KB | legacy/references/ | C14 组、C20 组、C21、O22、O23 | 只为旧格式服务；见 F4 |
| references/director-thinking.md | 5.1 KB | legacy/references/ | O02、O04、O22 | 见 F5 |
| references/original-prompt-*.md（5 个） | 13.8 KB | legacy/references/ | — | 样本原文，冻结，仅历史参考 |
| references/sample-findings.md | 18.3 KB | legacy/references/ | C01 组、C05 组、C14 组、C15、C21、O05、O08·O18、O20、O23 | 见 F1 |
| references/seedance-version-routing.md | 7.2 KB | legacy/references/ | 入口"版本备注"、O04、O17、C14 组、O08·O18 | 见 F2 |
| references/sera-current-video-template.md | 5.0 KB | legacy/references/ | O19、O03、O05 | 见 F7 |
| references/short-drama-direction.md | 10.6 KB | legacy/references/ | O22 | T9 末尾有指针；见 F16 |
| references/storyboard-workflow.md | 3.5 KB | legacy/references/ | C14 组 | T9 末尾有指针；见 F6 |
| references/validated-camera-causality-and-pov-body-anchors.md | 9.9 KB | legacy/references/ | C38、C09 组、C05 组 | 与 C38／C39 同源，已合并；见 F8 |
| references/visible-facts-and-duration-examples.md | 5.2 KB | legacy/references/ | C35、C15、O22 | 见 F3 |
| research/claude-opus-shot-duration-three-rounds.md | 5.2 KB | legacy/research/ | — | 讨论包，仅历史参考 |
| skills/asset-director/SKILL.md | 9.5 KB | legacy/skills/asset-director/ | O04、O05、C10·C19、C14 组、O17 | 见 F14 |
| skills/continuity-director/SKILL.md | 6.1 KB | legacy/skills/continuity-director/ | O23、O16 | 见 F13 |
| skills/failure-diagnostics/SKILL.md | 8.9 KB | legacy/skills/failure-diagnostics/ | O20、O21 | 见 F15 |
| skills/idea-parser/SKILL.md | 6.0 KB | legacy/skills/idea-parser/ | O02、O01 | 见 F10 |
| skills/idea-parser/references/rough-idea-intent-fidelity.md | 16.9 KB | legacy/skills/idea-parser/references/ | O01、O02 | 见 F10 |
| skills/idea-parser/references/intake-understanding-and-spatial-confirmation.md | 13.5 KB | legacy/skills/idea-parser/references/ | O02、O15、O24 | 见 F10（战斗功能表已收进 T3f） |
| skills/performance-director/SKILL.md | 10.8 KB | legacy/skills/performance-director/ | O16、C22 组、C09 组、O10、O12 | 见 F12 |
| skills/performance-director/references/physical-plausibility-pass.md | 10.0 KB | legacy/skills/performance-director/references/ | O12、C40 | |
| skills/preproduction-director/SKILL.md | 9.8 KB | legacy/skills/preproduction-director/ | O22、O04、O02 | T9 末尾有指针；见 F16 |
| skills/scene-sequence-director/SKILL.md | 9.7 KB | legacy/skills/scene-sequence-director/ | O22、O07、O14、C15、C05 组 | T9 末尾有指针；见 F16 |
| skills/shot-designer/SKILL.md | 17.3 KB | legacy/skills/shot-designer/ | C01 组、O07、O08·O18、C38、O13、C05 组、O14 | 见 F11 |
| skills/sample-learning/SKILL.md | 7.8 KB | legacy/skills/sample-learning/ | O20，治理并入入口 | 见 F17 |
| skills/sample-learning/references/combat-video-0-15-display-task-case.md | 3.5 KB | legacy/skills/sample-learning/references/ | O15 | |
| skills/practical-case-skills/（README＋3 个 SKILL） | 23 KB | 原位不动（只读） | — | 外部实践来源，不加载 |

## B 旧 SKILL.md 分节去向

| 旧章节 | 去向 |
|---|---|
| 职责边界；Q 版、Sera、动作迁移分流 | 新入口首段 |
| 两种制作入口与合作边界；外部仓库读取说明 | O02、O22 |
| 上下文预算与模块路由表（旧版强度最高） | 新入口"主题索引"（是流程，不是经验，无把握） |
| 东坡肉理论（本轮输入范围） | O03 只传所需材料 |
| 接收阶段的理解、空间与战斗确认 | O02；战斗功能表等 → O24 |
| 从粗糙想法到完整 Prompt | 新入口"流程"、O22 |
| 不变量 1 先守住故事事实 | O01 |
| 不变量 2 强制写可见事实 | C35（中高，进入"每次必读"） |
| 不变量 3 镜头由变化决定 | C05 组 |
| 不变量 4 多镜先锁共享锚点 | O07 |
| 不变量 5 策划秒数与模型时间控制分层 | C15 |
| 不变量 6 动作必须有过程 | O10 |
| 不变量 7 声音参与分镜，限制保护关键结果 | C20 组、C21 |
| 不变量 8 摄影名称与风格标签落到可见功能 | O08·O18 |
| 资产职责覆盖原则；多参考图职责门禁；现行资产分类 | O04、C14 组、C10·C19 |
| 从理解需求到成片复盘（8 步） | 新入口"流程"、O02、O04、O05、O20 |
| 输出与统一模板 | [slot-template](../assets/slot-template.md)（默认）、[clean-template](../assets/clean-template.md)（旧格式备选） |
| 明确弃用的默认做法 | O08·O18、C15、C05 组；两条未收见 F18 |
| Seedance Skill 修改治理（旧版强度最高） | 新入口"修改治理"（JIN 指定的流程，内容不变） |

## C 旧版里强度最高的条目：怎样改标

| 旧条目 | 证据 | 新位置与把握 |
|---|---|---|
| 强制写成当前画面可见的事实（shot-designer、SKILL.md 不变量 2） | 多处独立复述，且与 C35 的 Chibi 记录、乱雪、外星人同向 | C35，中高，进入"每次必读" |
| 资产分类：场景＝无人干净底图 | JIN 2026-09-17 的流程决定，多个样本 | O04，中 |
| 资产分类：同一道具多形态状态组 | 单案例（乱雪），JIN 确认 | C14 组〔多形态资产的状态组〕，低 |
| 资产分类：中心事件承载结构用完整初始状态 Scene Plate | 推理为主 | C10·C19，低 |
| 多参考图职责门禁 | 台阶重逢等样本，单次；新版 08 把 C31、C33 调到中 | C14 组〔参考分工〕，中 |
| 复盘门禁（Prompt → 执行单元 → 成片归因） | 单案例（乱雪）方法，JIN 确认 | O20，中 |
| 场景门禁（关键 Scene Plate 缺失先停在资产交接） | JIN 的流程决定 | O04，中 |

## D 42 张卡 → 26 条

| 条目（文件） | 原卡 | 把握 |
|---|---|---|
| 第一帧锚点（t1a） | C01、C02、C36 | 中 |
| 具体压过抽象（t1a） | C35 | 中高 |
| 前景局部入画与高低关系（t1a） | C27 | 中低 |
| 场景资产范围（t1b） | C10、C19 | 低（C10 句〔中高〕） |
| 构图执行者（t2） | C38 | 中 |
| 观察目标（t2） | C04 | 中低 |
| 主观视角与反打（t2） | C28 | 中 |
| 质感词与摄影机身份词（t2） | C41 | 中 |
| 镜头术语（t2） | C34 | 中 |
| 接触与持有闭合（t3） | C09、C16、C39 | 中 |
| 力与反应方向（t3） | C08 | 低到中 |
| 下坠方向证据（t3） | C03 | 中 |
| 材质进入因果（t3） | C40 | 中低 |
| 打斗节奏（t3f） | C06、C07、C42 | 低（C42 未测） |
| 站姿回落（t3f） | C17 | 低 |
| 表演与视线（t4） | C22、C26、C30 | 中低 |
| 声音与对白（t4） | C20、C29 | 中低 |
| 参考与身份（t5） | C14、C24、C31、C33 | 低（句内：参考分工〔中〕、多人〔中〕、多视图与重复角色〔低〕、多形态资产的状态组〔低〕） |
| 指令与资产不矛盾（t5） | C11 | 低 |
| 风格与光线（t6） | C13、C32 | 中低 |
| 阶段密度与节拍（t7） | C05、C12、C37 | 低 |
| 时间写法（t7） | C15 | 中低 |
| 限制条件（t7） | C21 | 中 |
| 转场（t7） | C23 | 低 |
| 一次只改一层（t8） | C25 | 中低 |
| 镜头层稳动作层脆（t8） | C18 | 中 |

JIN 的 9 条合并建议全部采用；C11、C35 未并——并了会把 C35 的"中高"拉到"低"。合并时，"注意"里改变应用方式的前提（如 C14 的官方 2.0 建议与多视图成功样本并存、C37 的"上限提醒不是配额，只是相关性"）保留在"避免"里。

## E 更早的草稿与来源提示词

| 旧输入 | 新位置 | 并入条目 |
|---|---|---|
| 01 逐段槽位模板 | 骨架 → [slot-template](../assets/slot-template.md)；字段值、3 次测试、张力 → evidence/slot-template-evidence.md | 使用提醒并入 slot-template 用法 |
| 02 词典：打斗页 §0–7 | evidence/dictionary-fight-v0.md | 运镜值表 → O09；动作链公式 → O14；特效传播 → O13；道具状态链 → C09 组；观察目标 → C04；S2 二级运动、S5 节奏处理、S7 落幅只留 evidence，部分并入 O14 |
| 02 §8–9 红蓝 v1–v3 | evidence/case-red-blue.md | C08、C09 组、C13 组、C15 的红蓝证据 |
| 03 词典：动作力学页 | evidence/dictionary-action-mechanics-v0.md | 五拍点、发力顺序 → O10；接触类型与舞台格斗来源 → O11；R1–R4 → C08；R5–R6 → C09 组；节奏、距离 → O14 |
| 04 作者提示词（乌鸦发饰） | evidence/author-prompt-guwu-crow.md | — |
| 05 狗尾巴草逐项分类 | evidence/foxtail-prompt-classification.md | — |
| 08 卡 v0 | evidence/agent-cards-v0.md | 合并前快照 |
| 09 证据档 | evidence/sources-and-limits.md、case-luanxue-sc38.md、case-alien-resigned-lead.md、cards-evidence.md | 逐字拆分 |

## F 未收录的规则及原因

下列规则**没有进入主题文件**，原文都在 `legacy/`。"建议"一列只标我认为可能值得收的，由 JIN 定。

### F1 references/sample-findings.md（18.3 KB，主要是历史参考）
| 未收录的规则或观察 | 原因 | 建议 |
|---|---|---|
| 场景图里已有角色可由提示词直接驱动、后入画角色才补资产（含 5 秒窗外攀谈样本的"场景角色继承"） | 2026-09-17 起已停用，文件自己写明"不再是当前生产规则"；现行做法是无人干净场景＋独立角色资产 | 不收 |
| "声音是画面完成后的后端补充" | 被后来的规则取代：声音参与分镜（已并入 C20 组） | 不收 |
| 候选风格预设 stylized animated cinematic / semi-real stylized character / painterly realistic environment（三层职责） | 单个样本；文件自己把"风格预设的跨题材稳定性"列入"尚不能升级" | 不收 |
| 治疗台 15 秒、7 秒样本的逐镜观察（切点、机位偏低带倾斜、四镜没有执行）；"右下角 LibTV 水印要区分平台叠加与生成错误" | 针对一份具体提示词的单次观察；水印是平台特定 | 不收；其中规则部分已收：时间不足减镜、后续动作不得提前发生（C05 组、C21） |
| 三个职责格子（【衔接要求】管镜间连续、【画面结构】管空间揭示、【画面动作】管分秒事件） | 只服务旧格式；内容已并入 O23、O07 | 不收 |
| 台阶重逢样本里的"焦点转移没有形成强烈拉焦""风和飘叶提供连续动势" | 单次观察 | 不收；故事板作为时间与空间结构资产、面部与服装资产分工、旧时长标签要对齐已收（C14 组、C15） |
| 凉亭动接样本里"肩膀先动、头再跟随"只部分执行 | 单次观察 | 不收；"文本时间轴写到 4 秒而成片 7 秒"已收（C15） |
| "当前样本支持的规则"第 2 条（场景搭建成功不代表时间流程成功）、第 6 条（角色参考与情绪塑造分工） | 前者已被 O20 的"导演层与逐项分开验收"覆盖；后者已被"每张参考图提供什么、不采用什么"覆盖 | 不另收 |
| 大司命凝光湖：视频中的电影观感是否全来自资产、"4K、顶级 TVC 导演"等词是否必要 | 文件自己写"暂不能断言" | 不收；"资产已统一美术风格时只写少量质感词"的候选已收一行（O08·O18） |
| 乱雪 30 秒复盘的逐时间段结论（0–2.5 秒 … 26.5–30 秒）与三条语言链的案例细节 | 案例观察；证据在 evidence 的乱雪页 | 不收；要点已收（C01 组、C09 组、O14） |
| "尚不能升级为通用规则的项目"六条 | 本身就是"不升级"清单 | 不收，原样保留 |

### F2 references/seedance-version-routing.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| "JIN 默认：2.0"与"JIN 默认：2.5"两套路径（最小生成单元 vs 15–30 秒连续叙事、2.0 对文字组织较敏感等） | JIN 2026-10：两版差别不大，不分两套；文件自己写明是 JIN 默认、不是官方结论 | 不收；差异只留入口"版本备注" |
| "选择时只问这些"（5 问）、"不使用的固定结论"（6 条否定） | 只服务版本分流；新入口不作这些主张 | 不收 |
| "事实等级"四类、"用户指定优先" | 新入口用把握和证据标签表达同一件事；版本无独立规则 | 不收 |
| 已收 | 资产容量取舍（O04）、2.0／2.5 关键道具写法（合并为 O17）、2.5 多参考资产分工（C14 组）、摄影与风格标签测试设计（O08·O18）、官方入口链接（evidence/version-facts） | — |

### F3 references/visible-facts-and-duration-examples.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| Sera 城门失守的整场共享锚点、"约 9–15 秒"镜头组合表、"约 20–30 秒"扩展表 | 非 Canon 的导演练习，是示例不是规则；"景别要看得见所写证据"已收（C35） | 不收 |
| 官方能力与导演选择要分开 | 已收：C15 与入口版本备注 | 已收 |

### F4 references/annotated-template.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 字段背后的决定表（本次生成／参考素材职责／全局要求／镜号时长景别拍法／画面／台词声音／出片要点各由哪个模块负责、缺失怎么处理） | 只解释旧格式 clean-template 的字段，新格式没有这些字段；旧模块已不再是独立流程 | 不收 |
| "画面：把设计合成一条时间线"的构图／动作／表演／环境／时间关系 | 已被 O14、C35、O10 覆盖 | 不另收 |
| 已收 | 参考素材职责（C14 组）、声音与字幕权限（C20 组）、禁止项对应具体风险（C21）、连续性验收（O23） | — |

### F5 references/director-thinking.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 【粗糙想法】6 行输入模板、导演拆解 6 步（镜头任务／衔接要求／画面结构／画面动作／表演要求／声音与禁止）、输出顺序 5 步 | 旧格式字段名 | 不收 |
| 已收 | 素材提醒、场景门禁（O04） | — |

### F6 references/storyboard-workflow.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 两段可复制说辞：给 GPT 把手绘整理成"导演控制故事板"、给视频模型的"故事板说明" | 2.6 KB，只在做故事板时用；"故事板只锁什么"已收（C14 组） | 不收；用到时读 legacy 原文（T9 末尾有指针） |

### F7 references/sera-current-video-template.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 净水渠案例包、LibTV《第 0 层》节点案例的结论与链接 | 项目案例证据（外部仓库），不是规则 | 不收，链接留 legacy |
| "可复用的默认制作顺序"7 步 | 与通用条目重复（O03、O05、C14 组、C35、O20 等） | 不另收 |
| 已收 | 成女 Sera 的视觉边界与第一帧基线（O19） | — |

### F8 references/validated-camera-causality-and-pov-body-anchors.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 案例 A（环绕跟拍）、案例 B（POV 递接）的原始提示词转录与成片观察 | 案例证据；要点已收 C38、C09 组、C05 组（"10 秒塞入过多状态被合并"） | 不收原文；原文留 legacy |

### F9 references/action-scene-writing.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| "最终文本不夹带导演理由、证据等级、内部检查表、'模型会理解为'的解释" | 输出格式规则，不是动作知识；已转入 slot-template 用法 | 不进主题文件 |
| 写作自检 7 项、虚构长杆示例句、"案例招式作为有条件的表达方式"（柔性武器鞭击与束缚拉拽的区别） | 自检已由入口自检 8 行覆盖；示例是虚构句法；招式条件是案例特定 | 不收 |
| 已收 | 编排攻防、画面证据、先后重叠延续、速度与观察机会（O14）；高密度写法（C05 组） | — |

### F10 skills/idea-parser/（SKILL＋2 份参考）
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 战斗接收的功能段落表（策划秒数｜功能｜强度｜场景变化）、目的与结尾都未定时只给 3–4 行粗骨架、场景变化清单（谁触发 → 变成什么 → 保留／复原）、提问优先级 | 已收进 T3f（O24，约 0.7 KB），JIN 批准只放这四项 | 已收 |
| 招式提醒（可选、不占额度）的单独说明 | 只在提问优先级里留名字；其余是低频细节 | 不收 |
| 两种 brief 模板（短片段 9 项／完整短剧 10 项） | 格式模板；O02 留"≤5 行复述" | 不收 |
| 因果理解（为什么行动 → 要完成什么 → 遇到什么 → 怎样应对 → 改变什么）、不为日常动作强加冲突 | 属故事层职责（JIN Story Development）；视频层只记已有项 | 不收 |
| 意图保真的三层解析（明确事实／动作功能清单：建立信息、转移注意、揭示、反应、反转、情绪回报、结束出口／可补齐清单）、"从零散想法到最终提示词"11 步、海盗船实例、用户原话引语 | 要点已收 O01、O02；功能清单与 11 步是细则，实例与引语是历史 | 不另收 |
| 已收 | [已说]／[假设]／[待确认] 标记与关键时刻表（O02）、"低强度段"候选（O15） | — |

### F11 skills/shot-designer/SKILL.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| "多角色同框的动作主次"候选（一段一个主要目标、谁发起谁承受） | 文件自己标"写作自检候选，没有对照证据"；与 C05 组"每阶段一个主要可见目标"部分重合 | 不收 |
| 内部镜头卡骨架（15 项）、两种工作模式 A／B（有无白膜时是否重复几何信息）、"景别／水平角度／纵向角度各自回答什么"等摄影通识 | 旧格式的内部核对表与通识；无白膜写法已收 O07 | 不收 |
| 已收 | 第一帧占位与身体朝向视线分开（C01 组）、构图执行者（C38）、操机与光学（O08·O18）、技能特效载体（O13）、高密度打斗（C05 组）、动作戏正向写作（O14） | — |

### F12 skills/performance-director/（SKILL＋物理推演）
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| Beat 的触发条件（新信息进入、原方法失败、目标达成、权力或距离变化、做出新决定）；Status 与 proxemics（更稳定更少动作＝高 status） | 表演理论细节；Status 来自 ACTING SYSTEM 实操 Skill，JIN 只在合适时用，不做公式 | 不收 |
| 输出模板【表演要求】11 行 | 旧格式内部核对表 | 不收 |
| 已收 | 行为优先、先眼后头、eye life、business、被打断的动作、状态惯性、多角色反应（O16、C22 组）；接触闭合（C09 组）；高难动作关键状态（O10）；物理推演（O12） | — |

### F13 skills/continuity-director/SKILL.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 输出模板【衔接要求】10 行；精确度分级（高精确动接用末帧／中等连续用文字／普通切镜只保证不矛盾） | 格式模板；精确动接用末帧已收 O23 | 不收 |

### F14 skills/asset-director/SKILL.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 输出模板（已有／必须补充／当前不需要／交接 Image EXP）；"平台无法使用白膜时"三步 | 格式与低频流程；白膜替代写法已收 O07 | 不收 |
| 已收 | 资产四问与分类（O04）、实际资产验收（O05）、多形态状态组（C14 组）、承载结构 Scene Plate（C10·C19） | — |

### F15 skills/failure-diagnostics/SKILL.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 成片复查输出模板（7 行）；风险分类 11 项里与 O21 重复的部分 | 格式；已覆盖 | 不收 |

### F16 preproduction-director、scene-sequence-director、short-drama-direction.md、scene-sequence-plan-template
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 模块交接与返回表（8 个职责）、整片方案细节表、各自的输出顺序与表格、preproduction 的"第 0 步可见性核对""第 1 步来源分层""第 6 步自检 11 项" | T9 只留要点（≤4 KB）；其余按 T9 末尾的指针读 legacy 原文 | 不收 |

### F17 skills/sample-learning/
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| 证据类型 A／B、证据纪律 6 条、分析维度 15 项、更新优先级 4 级、输出模板 | 样本学习流程，低频；核心（复盘链、导演层与逐项分开、规则变更须 JIN 过目）已收 O20 与入口"修改治理" | 不收；学习样本时读 legacy |
| 0–15 秒展示任务案例 | 已收 O15（把握低） | 已收 |

### F18 旧 SKILL.md
| 未收录的规则 | 原因 | 建议 |
|---|---|---|
| "明确弃用的默认做法"中的"每镜固定写 3–5 句""为不同视频平台重复生成内容相同的版本" | 针对旧 clean-template 与多平台出片；新流程没有这两条约束 | 不收；其余（装饰性质量词、配额、秒数等同时间戳、30 秒默认）已收 |

### F19 样本原文、媒体与讨论包
original-prompt-*.md（5 个）、assets/samples（14 个）、research/：冻结基线、样本证据、讨论包，不是规则，整体留 legacy。

### F20 旧版的最高强度标签
新仓不再使用；旧条目的强度按证据改标把握，见 C 节。

### F21 42 张卡补丁（C1c）里没有采用的内容
| 未采用的内容 | 原因 | 建议 |
|---|---|---|
| 研究报告里的七条说法：正加侧面图保真度高 52%；前 20–30 词加权最重、中文 30–100 词最好；多次生成相似度 90% 以上；CFG Scale=7 等采样参数；专业术语是美学奖励模型高频标签；2.0 支持 3–5 张多角度参考图；情绪词过强让瞳孔发光 | 09 的"来源与边界"已标未证实（无出处、营销文、与官方冲突，或 JIN 经验相反），不进卡片 | 不收；清单在 evidence/sources-and-limits |
| 没有好来源、要实测的空白：三人以上站位走位视线；Q 版和风格化角色表情；既快又稳的打斗写法；相机品牌与 8K 实际效果；多人对话正反打视线匹配；豆包当前参考数量上限 | JIN 的决定：通过实测解决，不靠猜 | 不收；做成实测任务时再记 |
| 旧 C31 的"两个角色最可控、三个可行、更大群体拆分镜"（小云雀转述） | 新版 C31 已删，来源没核实；只保留"人数多时拆成几组分镜再剪"与"2.5 推荐主体 1–8 个"的官方转载说法 | 不收 |

## G 小结

**重复（旧仓里同一知识出现多处，各并为一条）**
- 可见事实：旧 SKILL 不变量 2、shot-designer、scene-sequence、visible-facts、preproduction 第 4 步＋C35 → C35。
- 第一帧与朝向：shot-designer＋C01／C02／C36 → C01 组。
- 构图执行者、递接闭合：validated-camera、shot-designer、performance-director＋Chibi 记录 C38／C39 → C38、C09 组。
- 表演行为优先：performance-director、failure-diagnostics＋C22／C26／C30 → C22 组与 O16。
- 摄影标签：旧不变量 8、routing 末节、shot-designer＋C13／C32／C41 → O08·O18、C13 组、C41。
- 高密度：action-scene-writing、shot-designer、sample-findings＋C05／C12／C37 → C05 组。
- 多参考：旧门禁、asset-director、routing、annotated、storyboard＋C14／C24／C31／C33 → C14 组。
- 场景资产、时间控制、禁止项、复盘：各并入 C10·C19／O04、C15、C21／O21、O20／C25／C18。

**冲突（7 条）**：C14 多视图（已按 JIN：改称"多视图与重复角色"，待判断、低，2.0 的多视图问题暂不处理）、C37 阶段密度、时间写法（已按 JIN：2.5 用整数秒时间段，也可只写"镜头N"，2.0 可不写秒数；模板每段仍标"镜头N｜起-止秒"）、模板头部默认值（已按 JIN：保留为默认，标待测，JIN 指定时可整行省略）、模板无参考职责字段、06 准则 5／7 与旧"每轮 3 问／直接交付"、2.0／2.5 分流。

**互补**：新卡补旧仓没有的——观察目标 C04、下坠证据 C03、力与反应 C08、指令与资产 C11、站姿回落 C17、声音与对白 C20／C29、转场 C23、前景入画 C27、主观视角 C28、镜头术语 C34、材质 C40、质感词 C41、回弹变速 C42；旧仓补新卡没有的——接收与提问、资产验收、跨段连续、成片复查、预检、场戏与整片编排。
