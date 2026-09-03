---
name: idea-parser
description: Turn rough natural-language video ideas into a compact director brief without forcing the user to fill a formal template. Use when the input is fragmentary, emotional, visual, or only describes what should happen before/after a shot.
---

# Idea Parser

把用户的自然语言碎片整理成导演可以执行的最小 brief，不提前写完整提示词。

## 目标

从粗糙输入中提取：

- 上一镜怎样结束；
- 本镜唯一事件；
- 角色状态或情绪怎样变化；
- 摄影机最终必须让观众看见什么；
- 本镜怎样结束；
- 下一镜准备从哪里继续；
- 大概时长、画幅、平台；
- 已有参考图、视频、故事板或关键帧。

## 规则

1. 接受一句话、零散画面、情绪描述、截图说明或不完整故事，不要求用户先懂景别、机位、运镜术语。
2. 把抽象情绪翻译成“可见变化目标”，但不要在本 Skill 中设计完整表演细节。
3. 每个候选镜头必须能说清楚：起点 → 过程 → 结果。
4. 若一个想法包含多个独立结果，标记为可能需要拆镜；不要强行在一个镜头里塞完。
5. 只有缺失信息会改变镜头数量、角色身份、核心动作、衔接方向或结尾时才提问。
6. 若缺失信息仍可合理推断，做最小假设继续。

## 输出

输出一个简短 director brief：

```text
【镜头意图】
上一镜入口：
本镜唯一事件：
角色变化：
摄影机必须看见：
本镜落点：
下一镜出口：
时长 / 画幅：
已有素材：
不确定项：
```

不要在这里输出冗长理论、负面词库或完整镜头提示词。
