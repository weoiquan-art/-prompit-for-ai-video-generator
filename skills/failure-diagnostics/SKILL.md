---
name: failure-diagnostics
description: Predict and diagnose high-impact AI video generation failures from the current shot, references, and prompt. Use to derive a short task-specific guard list instead of a generic negative-prompt dump, or to study why a generated result failed.
---

# Failure Diagnostics

只处理“本次任务最可能怎样崩，以及怎样用最少限制拦住它”。

## 先找冲突源

检查：

- 参考图之间是否互相冲突；
- 图片中的高辨识度细节是否与文字相反；
- 场景图是否包含不该复制的人物、白底、文字或旧构图；
- 同一角色是否可能因多份参考被生成两次；
- 当前镜头是否可能提前执行下一镜动作；
- 运镜、人物动作和环境动作是否在同一时间争夺过多变化；
- 术语是否容易被误解为另一种物体、伤势、设备或事件；
- 背影镜头是否被强行生成不可见的正脸；
- 空间左右、视线、屏幕方向是否矛盾。

若问题来自错误资产，优先建议修正资产，而不是用长篇否定词与图片对抗。

## 风险分类

从实际任务中选择少量高破坏性风险：

- 身份重复或人物增殖；
- 参考污染；
- 动作串台；
- 类型／术语误读；
- 表演过度；
- 空间与方向错误；
- 角色外观漂移；
- 不合理肢体或物体交互；
- 文字、logo、界面或平台常见伪影。

## 写法

1. 每个禁止项对应一个可预见的具体失败。
2. 单镜局部风险尽量放回该镜头，不把所有限制塞到全局。
3. 不复制固定的超长 negative prompt。
4. 能用正向状态说清楚时优先正向，例如“黄兜帽男只出现一次，始终坐在亭内栏杆旁”，而不是连续十条“不要重复人物”。
5. 生成结果已经失败时，区分：提示词设计问题、资产问题、模型随机失败、未知来源。

## 输出

```text
【高风险失败】
- 风险：原因 → 最小修正

【禁止】
- 只保留 3–6 条高破坏性限制
```
