---
name: sample-learning
description: Learn reusable AI video prompting methods from paired original prompts and generated videos without overgeneralizing from one sample. Use when studying successes, failures, or repeated behaviors across examples and deciding whether to update a workflow, template, or rule.
---

# Sample Learning

把“原始提示词 + 生成结果”当作证据，目标是提取可复用方法，而不是事后凭感觉改写提示词。

## 证据纪律

1. 保留原始提示词、参考资产和成片，不先改写证据。
2. 对每个观察标记来源：提示词明确要求、参考图提供、模型自行补全、无法判断。
3. 区分：
   - 稳定复现；
   - 偶然成功；
   - 明确失败；
   - 未知来源。
4. 一个样本中的偶然现象不要升级成通用规则。
5. 多个样本重复出现相同因果关系后，才考虑进入主流程。

## 分析维度

按需检查：

- 镜头任务是否单一；
- 起幅 / 过程 / 落幅是否真实执行；
- 摄影机位置与运动是否被模型理解；
- 前中后景是否按预期揭示；
- 角色微表演是否可见；
- 参考资产承担了哪些稳定性；
- 参考污染或人物复制是否发生；
- 镜头间运动、方向、遮挡或视线是否连续；
- 声音是否跟随画面；
- 禁止项是否真正阻止了高风险错误。

## 更新优先级

新发现优先按以下顺序落地：

1. 修改某个独立 Skill 的判断规则；
2. 修改模板格子职责或输出顺序；
3. 增加一个经过验证的新模块；
4. 最后才修改总 orchestrator。

避免把案例细节写死成全局规则。例如“坐姿侧背影角色图”背后的规则应写成“按本镜真正可见角度和姿态选择定向资产”。

## 输出

```text
【样本观察】
- 现象：
- 证据来源：
- 可信度：稳定 / 偶然 / 失败 / 未知

【可复用结论】
- ...

【暂不升级为规则】
- ...

【建议修改位置】
- skill / template / orchestrator：修改理由
```
