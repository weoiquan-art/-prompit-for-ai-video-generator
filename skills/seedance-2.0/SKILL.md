---
name: seedance-2-0-prompt-engineer
description: "为 Seedance 2.0 编译合法的 4–15 秒视频生成参数、参考职责与事件切片 Prompt。需要 4K 短镜头或使用 2.0 时调用；不要用于 Seedance 2.5，也不要提供视频改视频参数。"
---

# Seedance 2.0 Prompt Engineer

只负责 Seedance 2.0。生成前读取 `../../references/event-slice-contract.md`，不得复制或推断 2.5 参数。

## 当前运行时合同

| 项目 | 2.0 合同 |
|---|---|
| duration | 4..15 秒 |
| resolution | 最高 4K |
| audio 参考 | ≤3 |
| image 参考 | ≤9 |
| video 参考 | ≤3 |
| 参考总数 | 0..15 |
| elements | 支持 |
| edit / `reference_video_to_video` | 不支持 |

这些是 2026-09-12 Notion 基线。调用前根据当前接口 schema 再校验；若发生变化，保留实际错误证据并更新本表。

## 选型

适合短镜头高分辨率，且不需要视频改视频。需要超过 15 秒单片、大量参考或视频改视频时改用 2.5，不得把 2.5 字段带进来。

## 参考取舍

建立 Reference Role Map，不人为限制为四张。超过 2.0 图片容量时按以下优先级删减：

1. 上一片真实末帧承接；
2. 主角身份；
3. 场景结构；
4. 构图静帧；
5. 次要角色、道具、补充视角与状态。

## 输出前检查

- duration 在 4..15 秒内；
- 不包含 `reference_video_to_video` 或其他 2.5 专用字段；
- audio、image、video 和总参考数分别合法；
- 画幅、分辨率、时长只在生成参数中；
- Prompt 没有时间码式状态模板；
- 每份参考只有一个主要职责；
- 以动词写清唯一主要变化；
- 跨片时末态文字逐字复制，并使用真实末帧承接。


