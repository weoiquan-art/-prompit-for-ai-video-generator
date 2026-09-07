---
name: failure-diagnostics
description: Predict and diagnose high-impact AI video generation failures from the current shot, references, spatial blocking, performance and prompt. Use to derive a short task-specific guard list instead of a generic negative-prompt dump, or to study why a generated result failed.
---

# Failure Diagnostics

只处理“本次任务最可能怎样崩，以及怎样用最少限制拦住它”。

当前检查吸收 `../practical-case-skills/cinedance-v4/SKILL.md` 的第一帧、空间、参考上下文和镜头漂移实操经验，以及 `../practical-case-skills/acting-system/SKILL.md` 的木偶表演故障观察。

## 先找冲突源

检查：

- 参考图之间是否互相冲突；
- 图片中的高辨识度细节是否与文字相反；
- 场景图是否包含不该复制的人物、白底、文字或旧构图；
- 同一角色是否可能因多份参考被生成两次；
- 当前 Prompt 是否残留上一镜未使用的角色、参考、道具或场景信息；
- 第一可见帧是否可能变成无人物空镜；
- 必要角色是否可能延迟出现；
- 当前镜头是否可能提前执行下一镜动作；
- 运镜、人物动作和环境动作是否在同一时间争夺过多变化；
- 术语是否容易被误解为另一种物体、伤势、设备或事件；
- 背影镜头是否被强行生成不可见的正脸；
- 空间左右、屏幕方向、身体朝向与视线是否矛盾；
- 摄影机是否可能跑到错误一侧；
- 场景参考是否可能错误覆盖当前需要的机位 / 构图；
- 镜头语言是否只写器材名，却没有可见的 optics 结果；
- 关键空间规则是否被埋在大量风格形容词里；
- 表演是否只有“情绪脸”，没有真实行为、反应或 eye life。

若问题来自错误资产，优先建议修正资产，而不是用长篇否定词与图片对抗。

## 无白膜时的空间风险

当当前平台无法使用 Blender 白膜 / previs 时，空间漂移风险提高。

此时先检查 `shot-designer` 是否已经明确：

- 第一帧；
- screen-left / screen-right；
- foreground / midground / background；
- 人物身体朝向；
- gaze direction；
- 移动路径；
- 摄影机一侧；
- 与地标 / 道具的距离或接触关系。

如果这些信息缺失，优先补**正向 spatial blocking**，不要先堆 generic negatives。

## 表演故障

如果成片人物像木偶，优先判断：

- 是否直接要求角色“演出悲伤 / 愤怒 / 紧张”，却没有行为目标；
- 是否等刺激结束后才突然切表情；
- 是否眼睛、头、肩、手和身体同时机械启动；
- 是否整镜只有一种动作节奏；
- 是否停顿里什么都没发生；
- 是否强事件后立刻恢复中性状态；
- 是否近景表情动作过多；
- 是否眼睛冻结，没有自然 gaze shift / blink / attention change。

这类问题优先交回 `performance-director` 修正行为，不靠 negative prompt 解决。

## 风险分类

从实际任务中选择少量高破坏性风险：

- 第一帧错误 / 人物延迟出现；
- 身份重复或人物增殖；
- 参考污染或旧上下文泄漏；
- 动作串台；
- 类型／术语误读；
- 表演过度或木偶感；
- 空间与方向错误；
- camera side / optics 漂移；
- 角色外观漂移；
- 不合理肢体或物体交互；
- 文字、logo、界面或平台常见伪影。

## 写法

1. 每个禁止项对应一个可预见的具体失败。
2. 先写正确状态，再决定是否补一句局部禁止。
3. 单镜局部风险尽量放回该镜头，不把所有限制塞到全局。
4. 不复制固定的超长 negative prompt。
5. 能用正向状态说清楚时优先正向，例如“黄兜帽男只出现一次，始终坐在亭内栏杆旁”，而不是连续十条“不要重复人物”。
6. 生成结果已经失败时，区分：提示词设计问题、资产问题、模型随机失败、平台能力限制、未知来源。
7. 如果失败来自 Prompt 太长，先删掉不参与当前画面的角色、参考、旧场景、装饰性形容词和重复规则，再考虑增加新限制。

## 输出

```text
【高风险失败】
- 风险：原因 → 最小修正

【正向锁定】
- 当前真正需要明确的状态

【禁止】
- 只保留 3–6 条高破坏性限制
```
