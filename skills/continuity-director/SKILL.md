---
name: continuity-director
description: Design shot-to-shot continuity and match transitions for AI video. Use when inheriting motion, gaze, body orientation, occlusion, camera state, environment state, props, acting state, wind, light, sound, or a moving connector from the previous shot and when preparing a clean exit for the next shot.
---

# Continuity Director

负责镜头之间“状态怎样真实继承”，尤其是动接、遮挡接、视线接、连续运镜与多镜头内部连续性。

## Seedance 跨片硬接口

当目标为 Seedance 2.0 或 2.5 时，上一片的 `[结束状态·供下一片承接]` 必须逐字复制为下一片的 `[起始状态]`，并把上一片实际导出的末帧设为下一片第一优先承接参考。两项缺一不可。

这里的逐字复制只针对边界状态段，不复制整份旧 Prompt；下文 Context isolation 继续用于剔除已离场人物、已结束道具、无关旧参考和制作笔记。

当前方法吸收 `../practical-case-skills/cinedance-v4/SKILL.md` 的 multi-shot continuity 与 `../practical-case-skills/acting-system/SKILL.md` 的 state inertia 实操经验。

## 入口检查

记录上一镜结尾：

- 当前真正出镜的角色 / 参考有哪些；
- 连接物是什么；
- 它在画面中的位置；
- 屏幕运动方向；
- 速度与加速度趋势；
- 摄影机是否正在运动；
- 摄影机位于主体哪一侧；
- 主体姿态、身体朝向与视线；
- 手部与道具状态；
- 人物之间的距离；
- 疲劳、疼痛、紧张、呼吸等表演状态；
- 风、雾、雨、光线等环境状态；
- 声音是否连续。

本镜开头不要无故把这些状态重置成默认静止。

## 动接原则

1. 若上一镜有运动中的连接物，本镜直接继承同方向、相近速度与画面位置。
2. 摄影机状态也要继承：上一镜正在跟随、下降、横移时，本镜不能默认从完全静止空镜开始，除非明确切断。
3. 遮挡接要说明遮挡物何时覆盖画面、何时揭开，以及揭开后空间关系。
4. 视线接要保证人物视线方向与下一镜被看对象的屏幕位置一致。
5. 身体朝向与眼睛方向分开继承；切镜不能把“身体仍朝前、眼睛看右侧”的状态重置成整个人完全转向右侧。
6. 手里的物体、接触状态、门开合、武器位置、设备是否修好等物件状态不能切镜后重置。
7. 环境连续性只保留真正会被观众感知的状态，不要堆无关参数。
8. 本镜落幅必须为下一镜留下可继承的真实画面状态。

## Multi-shot continuity

同一条视频内部发生切镜时，每个新镜头继续继承：

- active character list；
- location geography；
- screen direction；
- camera side（除非明确换轴 / 换侧）；
- gaze targets；
- body orientation；
- lighting direction；
- wardrobe；
- wounds / dirt / sweat / water / fire / smoke 等可见状态；
- props 与 hand state；
- object state；
- emotional / physical progression。

切镜不等于时间重置，也不等于角色瞬移。

如果距离、姿势、道具位置发生变化，必须有足够时间和动作过程解释。

## 表演状态惯性

强刺激、疲劳、疼痛、尴尬、紧张、呼吸紊乱等状态不会因为剪辑而自动归零。

例如上一镜角色刚跑完：

- 下一镜呼吸仍应受影响；
- 身体仍有 settling；
- 说话节奏不能瞬间变成完全平稳。

上一镜刚受到惊吓：

- 下一镜眼神、呼吸或重心仍应保留残余状态；
- 直到有新的可见事件让状态真正改变。

## Context isolation

连续性不等于把上一镜所有文字复制进下一镜。

下一镜只继承**仍然可见、可听或会改变当前画面的状态**。

不要把：

- 已离场人物；
- 已结束道具；
- 无关旧参考；
- 上一镜制作笔记；

继续塞进当前 Prompt。

## 精确度分级

- **高精确动接：**优先使用上一镜结尾帧，并写明连接物方向、速度、位置、人物姿态、视线与摄影机状态。
- **中等连续：**没有结尾帧时，用文字明确上述状态。
- **普通切镜：**只需保证角色、场景、时间、方向、道具状态与表演进度不矛盾。

## 输出

```text
【衔接要求】
上一镜仍然有效的角色 / 参考：
上一镜继承状态：
本镜入口：
身体朝向 / 视线：
连续运动 / 遮挡：
道具 / 手部 / 环境状态：
表演状态惯性：
必须保持不变：
本镜出口：
下一镜可继承状态：
```

不要在这里重写完整镜头内容，只处理跨镜状态。
