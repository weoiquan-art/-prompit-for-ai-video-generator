---
name: continuity-director
description: Design shot-to-shot continuity and match transitions for AI video. Use when inheriting motion, gaze, occlusion, camera state, environment state, wind, light, sound, or a moving connector from the previous shot and when preparing a clean exit for the next shot.
---

# Continuity Director

负责镜头之间“状态怎样真实继承”，尤其是动接、遮挡接、视线接和连续运镜。

## 入口检查

记录上一镜结尾：

- 连接物是什么；
- 它在画面中的位置；
- 屏幕运动方向；
- 速度与加速度趋势；
- 摄影机是否正在运动；
- 主体姿态与视线；
- 风、雾、雨、光线等环境状态；
- 声音是否连续。

本镜开头不要无故把这些状态重置成静止。

## 动接原则

1. 若上一镜有运动中的连接物，本镜直接继承同方向、相近速度与画面位置。
2. 摄影机状态也要继承：上一镜正在跟随、下降、横移时，本镜不能默认从完全静止空镜开始，除非明确切断。
3. 遮挡接要说明遮挡物何时覆盖画面、何时揭开，以及揭开后空间关系。
4. 视线接要保证人物视线方向与下一镜被看对象的屏幕位置一致。
5. 环境连续性只保留真正会被观众感知的状态，不要堆无关参数。
6. 本镜落幅必须为下一镜留下可继承的真实画面状态。

## 精确度分级

- **高精确动接：**优先使用上一镜结尾帧，并写明连接物方向、速度、位置和摄影机状态。
- **中等连续：**没有结尾帧时，用文字明确上述状态。
- **普通切镜：**只需保证角色、场景、时间、方向和事件状态不矛盾。

## 输出

```text
【衔接要求】
上一镜继承状态：
本镜入口：
连续运动 / 视线 / 遮挡：
必须保持不变：
本镜出口：
下一镜可继承状态：
```

不要在这里重写完整镜头内容，只处理跨镜状态。
