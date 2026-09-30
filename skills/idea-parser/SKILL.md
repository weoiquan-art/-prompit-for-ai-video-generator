---
name: idea-parser
description: Turn rough natural-language video ideas into a compact director brief and expose missing spatial facts before prompting. Use for fragmentary story input, multiple characters/key props with missing spatial facts, or confrontation/combat missing purpose, duration, ending, or rhythm. Exclude footage diagnosis, sample learning, asset acceptance, and iteration after a confirmed spatial table.
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
5. 缺失信息会改变镜头数量、角色身份、核心动作、衔接方向、结尾或空间关系的故事读法时，须确认；对抗／打斗缺目的、总时长、结尾或节奏时也触发。理解、空间与战斗统一使用下述接收流程，不各问一轮。
6. 可提出最小执行假设；触发接收确认时先展示事实、假设与待确认项，确认后再继续。明确跳过时展示空间与节奏假设后继续，不逐项追问，也不编造战斗缘由或胜负。

## 统一接收确认

空间确认、动作来由、表格上限及意图保真沿用 [零散想法的意图保真解析](references/rough-idea-intent-fidelity.md#统一接收确认)。对抗／打斗触发时读取 [理解、空间与战斗的接收补充](references/intake-understanding-and-spatial-confirmation.md)，由同一入口提供功能表、提问优先级、招式提醒与收尾关系；目的与结尾都为 [待确认] 时只给 3–4 行粗骨架，回答后再展开。共用一份 brief 和每轮最多 3 问，不替代下游设计。

## 输出

先用一句话复述理解，再输出正文最多 10 行的 director brief；空间触发时附空间表和一张示意，战斗触发时并附功能表，提问合计最多 3 个。目的与结尾在现有字段中记录，不为战斗增加正文行数：

```text
上一镜入口：
本镜唯一事件 / 战斗目的：
角色变化：
摄影机必须看见：
本镜落点 / 结尾与收尾关系：
下一镜出口：
时长 / 画幅：
已有素材：
空间与位置：见空间表；战斗时并附功能表（确认状态与来源）
不确定项：
```

不要在这里输出冗长理论、负面词库或完整镜头提示词。


## 零散想法的意图保真解析

当用户只提供几个角色、场景、动作、情绪或结尾时，不把“补全执行信息”变成“自由改写故事”。先保留用户已经确定的人物、事件、顺序、道具与结束位置，再只补齐让这些内容能够被摄影机看见、在指定时长内完整发生所必需的导演信息。

需要实际执行这种解析、判断哪些内容可以补齐、哪些内容不得擅自增加，或需要查看这一能力从 Q版短视频中产生的用户原话与海盗船实例时，读取：

`references/rough-idea-intent-fidelity.md`

该参考文件是通用方法，不会把 Q版角色、15秒结构或具体案例固化为其他视频类型的规则。Idea Parser 仍只输出最小 director brief；后续完整视频提示词由总导演继续路由到对应模块完成。
