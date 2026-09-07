---
name: lira-practical-branch
description: Preserved practical-method branch distilled from the user-provided LIRA image-prompt Skill for Higgsfield image workflows. Use as hands-on evidence for task routing, prompt compactness, camera anchors, reference discipline, asset editing, and model-specific image production. Do not automatically override JIN rules.
---

# LIRA — Practical Branch

来源：用户提供的 `LIRA SKILL.md`。它是一套已经用于 Higgsfield / 图像资产生产的 Prompt 优化与路由方法，负责把角色、场景、道具、编辑、纹理修复等不同任务分开处理。

本分支保留它最重要的实操逻辑。平台特定模型路由继续作为来源方法保存，但 JIN 主 Skill 只抽取可迁移的生产原则。

## 1. 4-D 工作方法

### Deconstruct

先确认：

- 用户真正要生成什么；
- 当前是新生成还是已有图编辑；
- 主体与上下文；
- 已有参考；
- 缺失信息；
- 平台参数与输出限制。

### Diagnose

检查：

- camera angle 是否模糊；
- lighting 是否模糊；
- palette 是否缺失；
- subject count 是否容易错误；
- framing 是否不清；
- 是否存在 illustration drift、文字纹身伪影、多角色崩溃或 Prompt 过长风险。

### Develop

根据任务类型选择不同方法，不用一套 Prompt 解决全部任务。

### Deliver

提示词先交付，解释保持短；复杂任务只补必要说明。

## 2. 任务路由优先

来源 Skill 会把工作拆成：

- Character；
- Location / environment；
- Prop；
- Existing-frame edit；
- Texture cleanup；
- Fine local edit；
- Location view change。

核心思想不是“所有模型都一样”，而是：**先判断任务，再把它交给擅长该任务的工具 / 模型。**

LIRA 原始 Higgsfield 路由包括 Soul 2.0、Soul Cinema、Cinema Studio AI Cast、Nano Banana Pro、Seedream 4.5、GPT Image 2。这些具体路由属于来源 Skill 的平台经验，JIN 不默认把它们推广到其他模型。

## 3. Precision beats verbosity

LIRA 的重要实践：

- coherent natural prose 优于 keyword stacking；
- Prompt 不要为了“完整”无限变长；
- 只保留真正控制画面的 anchors；
- 装饰性词越多，不代表控制越强；
- 参考已经明确的信息不要在 Prompt 里反复描述。

来源 Skill 给出的经验目标是紧凑提示词优于散乱长提示词；JIN 主 Skill 吸收的是“**控制密度优先于字数**”，而不是强制固定字符数。

## 4. Positive control first

生成任务优先说明想要的状态，而不是堆叠 NOT 列表。

例如：

- `empty deserted street` 比长串 `no people` 更直接；
- `clean dry skin` 比围绕皮肤问题写大量禁止项更稳；
- `plain unbranded wrapper, blank matte surface` 比在 Prompt 中反复提品牌并否定它更干净。

编辑任务允许明确写 remove，但要同时说明移除后由什么填补。

## 5. Camera anchor：简单物理语言优先

在 location / environment 生成中，镜头锚点是最容易漂移的部分。

来源 Skill 的经验是：

- `high angle three-quarter wide shot`
- `camera high above the room`
- `looking diagonally down at 45 degrees`

这类直接语言往往比 `CCTV / fisheye / extreme corner` 等抽象标签更稳定。

核心可迁移原则：

> **先说明摄影机在哪里、从什么方向看、画面看多少，再补风格词。**

## 6. 材质与灯光写具体结果

比起 `dramatic cinematic lighting` 这类泛词，更偏向写：

- 光源位置；
- 方向；
- 明暗比；
- falloff；
- 具体材质 + 表面状态。

例如：board-formed concrete、oxidized copper、matte surface、fabric weave 等。

但不要因为掌握了更多材质词就机械堆满 Prompt。

## 7. 参考与身份不要被文字覆盖

角色一致性应由平台真正支持的身份锚点 / reference system 承担，文字只补当前画面真正需要的可见 anchors。

来源 Skill 在 Higgsfield 里依赖 Soul ID；JIN 抽象后的原则是：

> **平台 / 参考资产已经能稳定提供身份时，不用长篇 prose 再重建一次角色。**

## 8. 编辑：Minimal CHANGE + exhaustive PRESERVE

已有图片编辑时，一次只改一个主要变量。

推荐结构：

```text
Edit the image: [one-line goal].

CHANGE: [only the single thing that changes].

PRESERVE EXACTLY:
- face / identity
- wardrobe
- props
- subject positions
- camera angle
- existing shadows
- color grade / palette / contrast / grain

ONLY CHANGE: [restate the one change]. 100% identical otherwise.
```

关键经验：

> 用户说“改太多了”，通常不是要写更多新东西，而是要缩小 CHANGE、加强 PRESERVE。

## 9. Location view change

同一场景换到反打 / 新机位时，不要只说“换一个角度”。

如果工具容易打乱几何关系，应明确新视角下主要物体的新位置：

- 原本画面右侧的物体，在反打后应出现在哪里；
- 原本摄影机后方的门，在新机位是否进入画面；
- 主要家具、门窗、地标的左右和前后关系。

这与视频空间 blocking 的逻辑一致：**新视角不是重新随机搭场景，而是同一空间的另一个观察点。**

## 10. 图像资产作为视频上游

场景图、角色图、姿态图、道具图和关键帧，不只是单张漂亮图片；它们是后续视频的视觉事实载体。

因此资产生产重点是：

- 清楚；
- 角色一致；
- 角度有用；
- 关键细节可见；
- 构图职责单一；
- 后续引用时不会和其他资产冲突。

## 11. States not transitions（来源 Skill 的视频附注）

来源 Skill 同样记录：视频模型对明确的动作状态往往比冗长过渡描述更稳定，例如 mid-punch / mid-jump 等。

这一条在 JIN 中与 ACTING 分支一起理解，不单独把它升级成“所有动作都必须只写状态”的硬规则。

## 与 JIN 的关系

LIRA 最适合强化 JIN 的：

- `image-asset-generator`；
- `asset-director`；
- 生图 Skill / GPT Image 上游资产生产；
- Prompt 密度控制；
- 参考资产职责；
- 局部编辑与场景换角度。

平台特定参数、具体模型能力与固定 UI 设置继续留在本实践分支，不自动写进通用视频导演规则。
