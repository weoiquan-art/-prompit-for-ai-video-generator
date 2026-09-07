---
name: sample-learning
description: Learn reusable AI video prompting methods from paired original prompts and generated videos, or from hands-on production Skills that have been used in real Higgsfield/Seedance workflows, without overgeneralizing from one source. Use when studying successes, failures, practical methods, or repeated behaviors and deciding whether to update a workflow, template, or rule.
---

# Sample Learning

把“原始提示词 + 生成结果”当作最直接证据；同时允许把**已经用于真实生产的实操 Skill**当作另一类实践证据。

目标是提取可复用方法，而不是事后凭感觉改写提示词，也不是把所有外部方法全盘照搬。

## 证据类型

### A. 原始 Prompt + 参考资产 + 成片

这是最直接的生成结果证据。

### B. 实操型 Production Skill

例如：

- 贤者实操案例；
- CINEDANCE；
- LIRA；
- ACTING SYSTEM；
- 其他明确用于 Higgsfield / Seedance / 实际生成流程的工作 Skill。

这类材料**不是纯理论或“画大饼”**。它们代表已经被某个生产流程实际采用的方法，因此值得单独保留和研究。

但“被实操使用”不等于“其中每条规则都适合 JIN 的所有模型与所有项目”。平台特定参数、固定 FOV、固定模型路由等仍需要区分适用范围。

当前保留分支：

`../practical-case-skills/`

## 证据纪律

1. 保留原始提示词、参考资产、成片或实操 Skill，不先改写证据。
2. 对每个观察标记来源：提示词明确要求、参考图提供、模型自行补全、实操 Skill 明确规则、无法判断。
3. 区分：
   - 稳定复现；
   - 实操方法；
   - 偶然成功；
   - 明确失败；
   - 未知来源。
4. 一个样本中的偶然现象不要升级成通用规则。
5. 实操 Skill 中的平台专用规则，不自动升级成通用规则。
6. 多个样本重复出现相同因果关系，或实操 Skill 与 JIN 自己的成功样本互相印证后，再考虑强化为主流程。

## 规则变更必须经过创作者过目

分析样本或实操 Skill 时可以主动提出新的规则候选、模板改法或模块建议，但**不得仅因为 AI 自己判断“值得加入”就直接写进 Skill**。

执行原则：

1. 用户已经明确要求加入或明确认可的修改，可以直接落地。
2. AI 自己从案例中推导出的新增规则，先作为**候选建议**说明：准备加什么、为什么、会影响哪个 Skill。
3. 等创作者过目并明确同意后，再正式修改对应 Skill、模板或 orchestrator。
4. 创作者认为“不需要升成规则”的案例做法，保持为案例经验，不为了体系完整而强行制度化。
5. 不得趁其他已批准修改时夹带未经讨论的新规则。

目标是让 Skill 持续学习，但最终方法论的升级权由创作者保留。

## 分析维度

按需检查：

- 镜头任务是否单一；
- 第一可见帧是否正确；
- 起幅 / 过程 / 落幅是否真实执行；
- 摄影机位置与运动是否被模型理解；
- Spatial blocking 是否清楚；
- 前中后景是否按预期揭示；
- 身体朝向与视线是否正确；
- 角色微表演是否可见；
- 角色行为是否来自目标 / 刺激，而不是只有情绪脸；
- 参考资产承担了哪些稳定性；
- 参考污染或人物复制是否发生；
- 镜头间运动、方向、遮挡、视线、道具与表演状态是否连续；
- 声音是否跟随画面；
- 禁止项是否真正阻止了高风险错误；
- Prompt 是否因为过长、旧上下文或装饰性词造成控制稀释。

## 更新优先级

新发现优先按以下顺序提出修改建议：

1. 修改某个独立 Skill 的判断规则；
2. 修改模板格子职责或输出顺序；
3. 增加一个经过验证的新模块；
4. 最后才修改总 orchestrator。

以上只是**建议落点顺序**；若修改内容不是用户已经明确批准的事项，仍必须先经过创作者过目再落地。

避免把案例细节写死成全局规则。例如“坐姿侧背影角色图”背后的规则应写成“按本镜真正可见角度和姿态选择定向资产”。

同样，不把某个外部 Skill 的平台特定做法直接推广为 JIN 全局规则。例如某个固定 FOV、固定模型路由、固定语言输出，只在它的实践分支里保留，除非后续被明确认可。

## 输出

```text
【证据类型】
- Prompt+成片 / 实操 Skill / 其他

【样本观察】
- 现象：
- 证据来源：
- 可信度：稳定 / 实操方法 / 偶然 / 失败 / 未知

【可复用结论】
- ...

【暂不升级为规则】
- ...

【候选 Skill 修改（需创作者过目）】
- 想增加 / 修改什么：
- 理由：
- 预计修改位置：skill / template / orchestrator
```
