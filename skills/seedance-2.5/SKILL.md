---
name: seedance-2-5-prompt-engineer
description: "为 Seedance 2.5 选择合法 method、处理参数互锁、组织多模态参考，并用事件切片和真实末帧承接生成最长 30 秒的切片或更长成片。不要用于 Seedance 2.0。"
---

# Seedance 2.5 Prompt Engineer

只负责 Seedance 2.5 的合法切片与多切片拼接。生成前读取 `../../references/event-slice-contract.md`。

## 当前运行时合同

| 项目 | 2.5 合同 |
|---|---|
| duration | 5 / 10 / 15 / 20 / 25 / 30 秒 |
| resolution | 480p / 720p / 1080p |
| audio 参考 | ≤10 |
| image 参考 | ≤30 |
| video 参考 | ≤10 |
| 参考总数 | 0..50 |
| elements | 支持 |

单次 60 秒不存在。任何超过 30 秒的成片必须拆成合法切片生成，再剪辑拼接。

这些是 2026-09-11 Notion 基线。调用前根据当前接口 schema 再校验；若发生变化，以实际 schema 与错误为准。

## method 与参数互锁

先确定 method，再准备参考和参数；不得为了“补齐字段”传入必须省略的参数。

| method | 类型 | 参考 | 必须省略 |
|---|---|---|---|
| `text_to_video` | — | — | — |
| `image_to_video` | frames | image ×1 | `aspect-ratio` |
| `first_last_frame_to_video` | frames | image ×2 | `aspect-ratio` |
| `multimodal_reference_to_video` | reference | 多个 | 无；aspect 可用 |
| `reference_video_to_video` | edit | video ×1 | `duration`、`aspect-ratio` |

frames 模式传 `aspect-ratio` 会失败。edit 模式不要补 duration 或 aspect-ratio。

## 长视频拆片

60 秒可优先按 20 / 25 / 15 秒分配叙事职责：建立情境与第一个变化 → 主事件 → 结果与钩子。这是推荐配重，不是唯一拆法。

每片执行：

1. 生成并检查当前片；
2. 导出真实末帧；
3. 把当前片结束状态逐字复制为下一片起始状态；
4. 把真实末帧设为下一片 `@Ref1`；
5. 分别检查身份、空间、动作因果、光线方向和声音同步后再拼接。

动作紧密咬合且单张承接帧不足时，使用 `first_last_frame_to_video`。

## 输出前检查

- method 已先确定且参数省略正确；
- duration 只取 5 / 10 / 15 / 20 / 25 / 30；
- resolution 只取 480p / 720p / 1080p；
- audio、image、video 和总参考数分别合法；
- 超过 30 秒的目标已经拆片；
- Prompt 没有时间码式状态模板；
- 每份参考只有一个主要职责；
- 以动词写清唯一主要变化；
- 后续切片同时继承末态文字和真实末帧。


