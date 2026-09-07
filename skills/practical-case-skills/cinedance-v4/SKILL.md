---
name: cinedance-v4-practical-branch
description: Preserved practical-method branch distilled from the user-provided CINEDANCE V4 Seedance/Higgsfield Skill. Use as hands-on evidence for spatial blocking, first-frame control, optics, physics, lighting, references, continuity, and prompt QA. Do not automatically override JIN rules.
---

# CINEDANCE V4 — Practical Branch

来源：用户提供的 `CINEDANCE HIGGSFIELD SKILL.md`。原方法定位是把任意场景输入转换成可直接生成的 Seedance / Higgsfield 视频提示词，并通过空间 blocking、镜头、物理、灯光、参考图控制和静默 QA 提高一次生成成功率。

本分支保留它最重要的生产结构与工作逻辑，供 JIN 视频体系随时读取。它是**实操 Skill 证据**，不是抽象理论。

## 1. 核心工作顺序

CINEDANCE 的核心不是先写“电影感”，而是先拆当前镜头并找出真正需要控制的事实：

- 当前可见角色与有效参考；
- 当前场景与地标；
- 第一可见帧；
- 人物站位与空间层级；
- 身体朝向与视线；
- 移动路径；
- 摄影机一侧、距离、高度和运动；
- 镜头 / optics 的可见结果；
- 动作时间；
- 物理与接触；
- 灯光方向与曝光；
- 声音；
- 本镜真正需要的失败保险。

原则：**空间规则先于摄影风格，关键站位不能埋进风格段落。**

## 2. Context isolation

最终提示词只保留当前镜头真正可见或可听见的内容。

删除：

- 未出镜角色；
- 未使用参考标签；
- 旧场景信息；
- 上一镜残留 Prompt；
- `same as before / previous / continues from / as above` 等依赖旧上下文的说法；
- 当前镜头看不到也听不到的制作笔记。

把最终 Prompt 当成一个**密封的当前镜头文件**。

## 3. Location Map

当场景复杂或人物位置容易漂移时，先把场景参考转成实用地图：

- camera position；
- camera facing direction；
- foreground / midground / background；
- 地标位置；
- 角色位置；
- 移动路径；
- 灯光方向；
- 深度关系。

场景参考主要提供：地理、材质、氛围、地标、必要时的灯光方向。

**不要默认继承场景参考原本的机位和构图，除非明确要求。**

## 4. First-frame occupancy

如果人物应该从第一帧就存在，要直接锁定：

- 第一可见帧已经包含必要人物；
- 人物在正确位置；
- 空间关系第一帧就能读懂；
- 不自动先生成无人物的 establishing shot；
- 不让必要角色延迟入画。

只有剧情明确需要空镜时才允许空开场。

## 5. Spatial Blocking

重要主体需要用简单物理语言说明：

- screen-left / screen-right；
- foreground / midground / background；
- 与地标或另一角色的物理距离；
- torso / body facing direction；
- gaze direction；
- movement direction。

当距离重要时，弱词如 `near / around / somewhere` 不够稳定，应改成可执行关系，例如：

- 距离车门约 1 米；
- 背靠墙；
- 手已经在把手上；
- 站在标志正下方；
- 与某角色保持一个明确的前后层级。

## 6. Body orientation 与 gaze 分开

身体方向和眼睛看的方向是两个控制量。

可分别写：

- torso faces X；
- eyes stay on X；
- head turns toward X；
- back faces camera；
- profile faces screen-left。

角色可以身体仍朝前，但眼睛先到目标，头部之后才跟随。

## 7. Single take / Multi-shot

先决定：

- `SINGLE CONTINUOUS TAKE`
- 或 `CONTROLLED MULTI-SHOT SEQUENCE`

默认不让模型自己发明随机切镜。

需要多镜时，每次切镜都应明确：

- 本镜持续时间；
- 摄影机；
- 第一帧主体；
- blocking；
- 动作；
- cut 类型；
- 下一镜继承的空间与状态。

切镜后不能重置：角色、地理关系、左右方向、视线、服装、道具、伤势、环境状态与动作进度。

## 8. Optics：优先写可见结果

CINEDANCE 的重要实践是：**不要只依赖焦段、光圈、镜头品牌等 metadata 作为主要控制。**

镜头控制优先说明：

- 摄影机与人物的实际距离；
- 视野是自然、广角展开还是长焦压缩；
- 主体大小；
- 背景是否保持可读；
- 背景是否被压缩并柔化；
- 前景是否被放大；
- 是否存在明显畸变；
- 景深和焦点结果。

原 Skill 有一套具体 FOV 角度模板（如标准、广角、长焦、超长焦）；这些数字属于来源 Skill 的实操工具，保留为参考，但 JIN 主 Skill 不强制每镜使用固定角度。

## 9. Camera 写成摄影机实际行为

优先写：

- camera height；
- camera distance；
- camera side；
- camera angle；
- subject size；
- screen placement；
- camera movement；
- focus behavior；
- depth of field；
- handheld 的真实操机感。

避免只写“电影感运镜”。

Handheld 更适合描述为：呼吸造成的细微 settling、肩扛重量、人体重心修正，而不是数字 jitter 或随机 shake。

## 10. Physics

动作要有因果和重量：

- gravity；
- mass；
- inertia；
- friction；
- contact；
- weight transfer；
- collision；
- follow-through；
- cloth / hair delay；
- 武器重量；
- 液体黏度与重力；
- 粒子受风向影响。

不要出现漂浮身体、无重量武器、无摩擦脚步、道具瞬移或橡胶式 CG 运动。

## 11. Lighting 是优先约束，不是装饰词

需要稳定灯光时明确：

- primary light source；
- light direction；
- camera 位于光源哪一侧；
- 主体哪一侧在暗部 / rim light；
- 背景亮度；
- 曝光优先级；
- 允许的高光。

例如逆光镜头，重点是人物是否真的处于摄影机和亮背景之间，而不是只写 `dramatic backlight`。

## 12. Action Timing

用时间块写可执行事件，每段只承载有限任务：

- 主体位置；
- 动作；
- 摄影机行为；
- 道具状态；
- 必要物理；
- 必要声音。

一个时间块不要塞互相矛盾的动作。

## 13. Reference hierarchy

不同资产承担不同职责：

- identity reference → face / body / proportions / costume / unique anchors；
- location reference → architecture / materials / geography / atmosphere / landmarks；
- prop reference → shape / scale / material / contact / state；
- style reference → 不应覆盖身份、blocking、动作、镜头和灯光。

参考图已经明确的内容，不用长篇文字重新覆盖。

## 14. Prompt density

高密度只放在真正会导致失败的地方：

- identity；
- first frame；
- blocking；
- gaze；
- hand / prop state；
- timing；
- optics；
- lighting；
- physics；
- dialogue。

低密度处理：

- 泛用美化；
- 已经由参考图提供的服装细节；
- 不参与当前动作的背景物；
- 装饰性形容词。

**更强的信号比更长的 Prompt 更重要。**

## 15. Failure locks

默认先写正向状态，再补局部失败保险。

例如：

- 人物第一帧已在正确位置；必要时再补“不要空开场”；
- 人脸保持逆光暗部；必要时再补“不要平光”；
- 当前只使用这些参考；必要时再补“不要旧标签”。

不要默认堆大型 generic negative block。

## 16. Silent QA

交付前内部检查：

- 当前参考是否都真的使用；
- 第一帧是否正确；
- 人物位置是否明确；
- gaze 与 body orientation 是否明确；
- camera side 是否明确；
- optics 是否与画面任务一致；
- 灯光有没有漂成平光；
- 道具是否在正确手中；
- 动作是否物理可行；
- 时间块是否一致；
- 是否残留旧场景上下文。

## 与 JIN 的关系

当白膜 / previs 无法被当前视频平台直接输入时，本分支尤其重要：它提供一套**文字版空间 blocking** 方法，用 Prompt 把本来可由三维预演承担的站位、方向、第一帧和机位关系说清楚。

当未来平台可以直接使用有效白膜或预演资产时，JIN 可以减少重复的空间文字，把 Prompt 预算留给动作、表演、物理、灯光与声音。
