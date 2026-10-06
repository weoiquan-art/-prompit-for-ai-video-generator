# Claude Opus 三轮讨论包：几秒／几十秒分镜与整场导演方法

> 用途：把三次 Opus 对话用于独立研究、压力测试和最终总结。Claude 只分析与提出建议，不修改 GitHub；其结论带回本项目讨论后，才决定是否另行申请 Skill 修改。

请在**同一个 Claude 对话**里依次发送三轮。不要一次把三轮全发出；上一轮回答会成为下一轮上下文。

## 第 1 轮：阅读官方案例并建立独立观点

请作为 AI 视频导演研究员工作。先完整阅读以下材料：

1. Seedance 2.0 官方提示词指南：https://docs.volcengine.com/docs/82379/2222480?lang=zh
2. Seedance 2.5 官方提示词指南：https://docs.volcengine.com/docs/82379/2607689?lang=zh
3. 总导演 Skill：https://github.com/weoiquan-art/-prompit-for-ai-video-generator/blob/main/SKILL.md
4. 整场戏编排 Skill：https://github.com/weoiquan-art/-prompit-for-ai-video-generator/blob/main/skills/scene-sequence-director/SKILL.md
5. 单镜设计 Skill：https://github.com/weoiquan-art/-prompit-for-ai-video-generator/blob/main/skills/shot-designer/SKILL.md
6. 可见事实与 Sera 城门示例：https://github.com/weoiquan-art/-prompit-for-ai-video-generator/blob/main/references/visible-facts-and-duration-examples.md
7. Q版 Claude 原始方法论（只学习“怎样保存原始观点”，不要把 Q版规则复制到成女或通用导演）：https://github.com/weoiquan-art/chibi-/blob/main/references/claude-original-methodology.md
8. 成女 Sera 故事与世界观：https://github.com/weoiquan-art/sera-universal/blob/main/SKILL.md（视频执行改由通用 Video Director 接收 Story Package）

若任何链接无法访问，请明确说出具体哪一项没有读到，不要假装已读。

重点研究官方案例实际怎样使用“镜头1／镜头2”、时间区间、时间点、相对时间、30 秒多镜头、延长与分段素材。请把以下三类内容严格分开：

- 官方文档明确写出的事实；
- 你从官方案例推导出的导演判断；
- 仍需生成测试才能确认的生产假设。

然后形成你自己的第一版观点，回答：策划者预估的几秒与模型 Prompt 中的时间戳应该是什么关系？3–8 秒单镜、8–15 秒片段、15–30 秒叙事各适合承担什么？什么时候一次生成，什么时候拆成多个片段剪辑？

本轮不要建议直接改仓库。输出：初步原则、证据对照、你认为当前 Skill 最值得保留的部分、冲突／空白、下一轮必须压力测试的问题。

## 第 2 轮：用 Sera 城门场戏压力测试

现在不要顺着第一轮结论，请主动寻找它的漏洞。以这个非 Canon 练习为共同测试题：Sera 在城门内侧，前景能看到她，远景城门逐步失守；门破瞬间切到能同时看清脸、遮挡手臂与身体支撑的高角度，她先回避眼睛、抬臂挡尘，再通过脚、膝、髋和躯干抵抗从门外涌入的风尘，最终站稳。成女 Sera 可以说完整台词，但是否说、说多少由当前故事需要决定。

请分别设计并比较：

1. 约 6–8 秒极短版；
2. 约 10–15 秒标准短版；
3. 约 20–30 秒展开版；
4. 由多个几秒／几十秒生成片段剪成约 45–60 秒的版本；
5. 一次连续生成约 30 秒的版本。

每版都说明：镜头职能、制作预估秒数、每镜必须可见的事实、共享锚点、切镜触发、哪些内容同段生成／独立生成、模型 Prompt 是否需要精确时间控制，以及最可能的失败方式。特别解释官方 2.0 倾向不强制每段时长、2.5 又支持时间戳并展示 30 秒案例时，怎样形成按任务与版本分流的判断，而不是二选一口号。

最后反驳你自己的方案：哪些判断只是审美偏好，哪些是模型执行风险，哪些必须靠 A/B 生成样本验证？本轮仍不修改仓库。

## 第 3 轮：输出可带回讨论的 Claude 原始方法论

综合前两轮，输出一份自包含的中文 Markdown 文档，标题为《Claude 原始方法论：整场戏、几秒／几十秒分镜与生成单元》。它将被带回另一个 AI 对话，与用户共同讨论；不是自动生效的 Skill。

必须包含：

1. 核心观点摘要；
2. 官方事实／你的导演推论／待验证假设三栏证据表；
3. 3–8 秒、8–15 秒、15–30 秒、45–60 秒组装的决策矩阵；
4. 单次连续生成与分段生成的选择树；
5. 策划秒数与模型时间控制的明确分工；
6. 共享场景锚点的最小集合；
7. 抽象叙事转可见事实的方法；
8. Sera 城门的几秒版与几十秒版完整注释示例；
9. 对当前总导演 Skill、整场戏 Skill、Shot Designer 与成女 Sera 支线的评审；
10. 建议保留、建议调整、需要 A/B 测试的内容分别列出；
11. 你与现有方法仍然不同意或没有把握的地方。

保持你自己的判断，不为了迎合现有 Skill 而同意。所有修改建议只写成讨论清单，不直接改文件，也不要把建议冒充已验证规则。末尾给出一段可直接复制回本项目继续讨论的 200–400 字摘要。

