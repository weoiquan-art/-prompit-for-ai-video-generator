---
name: jin-video-director-flow
description: "为 Seedance 2.0/2.5 设计可生成、可承接的 AI 视频提示词与多切片工作流。先选择版本和合法 method/参数合同，再用 Reference Role Map、事件切片、首尾状态与末帧承接组织镜头；按需叠加资产、摄影、表演、连续性、故障诊断及 Q 版社交短视频模块。非 Seedance 平台只使用通用导演模块，不套用 Seedance 参数。"
---

# JIN Video Director Flow

这是总导演与路由 Skill。Notion 中的 Seedance 2.0 / 2.5 实战合同是生成地基；仓库内其他模块负责导演增强，不能覆盖版本能力、参数互锁或跨片承接规则。

## 规则优先级

发生冲突时按以下顺序裁决：

1. 用户本轮明确要求与运行端当前 schema / 报错；
2. 对应 Seedance 版本模块；
3. `references/event-slice-contract.md` 的共同生成合同；
4. Q 版、项目风格和真实样本经验；
5. 资产、摄影、表演、连续性与故障诊断建议。

不要混用 2.0 与 2.5 的参数。运行时 schema 与仓库记录不同时，以实际接口为准，并把差异标为待更新的操作参数。

## 第一步：选择运行时

| 需求 | 路由 |
|---|---|
| Seedance 2.0、4K、4–15 秒短镜头、不需要视频改视频 | 读取 `skills/seedance-2.0/SKILL.md` |
| Seedance 2.5、最长 30 秒切片、大量参考、首尾帧或视频改视频 | 读取 `skills/seedance-2.5/SKILL.md` |
| 超过单次上限的成片 | 使用 2.5 合法切片并通过文字状态和真实末帧双重承接 |
| 未指定模型，且版本会改变参数或素材组织 | 先给选型建议，只询问这一项必要问题；不得猜参数 |
| 非 Seedance 平台 | 不读取 Seedance 参数表；仅使用通用导演模块 |

## Seedance 共同地基

选定版本后读取 `references/event-slice-contract.md`，并遵守以下硬规则：

- Prompt 描述当前切片发生的**一个主要变化**，不用时间码分段堆状态。
- 参考采用 Reference Role Map：与当前切片确实有关的参考是加法，但每份只承担一个明确职责；不设置“四张参考”的人为上限。
- “相关参考全给”不等于机械制造资产。先用 `asset-director` 判断相关性；一旦确认相关，就不因模板示例或习惯上限删掉它。
- 上一片的 `[结束状态·供下一片承接]` 必须逐字复制为下一片 `[起始状态]`；只复制边界状态，不复制整份旧 Prompt。
- 同时把上一片实际导出的末帧设为下一片第一优先承接参考。文字连续但没有真实末帧，不算精确承接。
- 画幅、时长、分辨率放在生成参数，不混入 Prompt 正文。
- 负向词只进入运行端独立 negative prompt 字段；没有该字段时改写成正向可见约束。

## 导演模块路由

只读取当前任务需要的模块：

- 粗糙想法、零散画面、情绪碎片 → `skills/idea-parser/SKILL.md`
- 判断现有参考与缺失资产 → `skills/asset-director/SKILL.md`
- Astra 分镜、Blender 白膜、previs、blocking、Mocap 或 VFX 载体 → `skills/astra-video-asset-prep/SKILL.md`
- 机位、景别、空间、运镜、焦点及起落幅 → `skills/shot-designer/SKILL.md`
- 把情绪变成可见表演 → `skills/performance-director/SKILL.md`
- 跨镜与跨片状态继承 → `skills/continuity-director/SKILL.md`
- 预测或诊断生成故障 → `skills/failure-diagnostics/SKILL.md`
- 从提示词和成片证据更新规则 → `skills/sample-learning/SKILL.md`
- Q 版 / 拟人化、9:16、约 8–15 秒社交短视频 → `skills/qversion-social-short-video/SKILL.md`

复杂整场设计或综合审片才读取 `references/director-review-layer.md`。Leo 式六岗位只作为导演会诊与质检视角，不是 Seedance 参数来源，也不应阻塞用户明确要求的直接提示词交付。

## Q 版分支兼容规则

Q 版长期实测经验继续作为内容与表演基线。若目标是 Seedance 2.0 / 2.5：

1. 保留其角色固定层、行为差异、POV 动机、道具连续性、错峰声音与高价值内容结构；
2. 把 `0–Xs` 等时间段改写为 `[起始状态] → [本片发生的变化] → [结束状态]` 的因果事件；
3. 由所选 Seedance 版本模块决定时长、参考上限、method 与参数省略规则；
4. 不让 Q 版模板中的模型名、比例或惯例值覆盖用户选择。

## 执行流程

1. 确认目标平台与版本，读取唯一对应的运行时模块。
2. 从用户输入提取当前切片的起始状态、唯一主要变化和结束状态。
3. 盘点已有参考，建立 Reference Role Map；只有具体缺口才建议新增资产。
4. 按需叠加镜头、表演、连续性和声音设计，解决冲突后再编译 Prompt。
5. 超长成片先拆成合法切片，逐片生成、检查末帧，再继续下一片。
6. 使用 `assets/clean-template.md` 交付；只保留当前任务需要的栏目。
7. 运行对应版本自检，再做少量任务特定的失败保险。

## 输出要求

默认先给可直接复制的结果：

1. `生成参数`：版本、method、合法参数与明确省略项；
2. `Reference Role Map`：每份参考的唯一职责；
3. `事件切片 Prompt`：按共同合同输出；
4. 多切片任务附 `承接记录`：上一片末态文字、真实末帧引用及下一片入口；
5. 只有用户要求解释时才补导演分析。

保留已知事实、导演推断与待核验项的边界。不得把单个成功样本升级为跨项目永久规则，也不得把当前模型参数写成通用导演原则。


