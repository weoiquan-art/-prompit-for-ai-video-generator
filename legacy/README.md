# legacy：旧版内容归档（不加载）

状态：归档，不加载，不删除。2026-10 知识整合之前的全部内容，按原目录结构整体放在这里。新入口见 [SKILL.md](../SKILL.md)，主题文件见 `topics/`，证据见 `evidence/`；旧 → 新的去向与"未收录的规则及原因"见 [knowledge-map](knowledge-map.md)。标签 `pre-knowledge-consolidation`（main 的 08e8aad）是整合前的完整状态，可随时回退。

## 改动说明
- 文件文字没有改，只修正了跨目录的相对链接与路径，共 32 处，分布在 14 个文件：指向 `assets/clean-template.md`、`skills/practical-case-skills/` 的链接，`sample-findings.md` 里指向样本文件的路径，以及 `SKILL.v1.md` 里指向 clean-template 的 1 处链接。
- 旧的根 `SKILL.md` 改名为 `SKILL.v1.md`，避免与新入口同名。
- 没有移动：`agents/openai.yaml`、`assets/icon.svg`、`assets/clean-template.md`（只加了状态头）、`skills/practical-case-skills/`（只读，不加载）。
- 旧文里对路径的纯文字提及（如旧路由表里的 `references/…`）保持原样；它们在 `legacy/` 下能对应到同名文件，只有 `assets/clean-template.md` 仍在原处。

## 旧路径清单（被移动的全部文件）
用来在 `chibi-`、`sera-universal`、`JIN-Story-Development` 里搜索失效链接。GitHub 链接形态是 `https://github.com/weoiquan-art/-prompit-for-ai-video-generator/blob/main/<旧路径>`；要搜的字符串可以用 `-prompit-for-ai-video-generator/blob/main/` 或 `-prompit-for-ai-video-generator/tree/main/` 加下面表里的旧路径或旧目录（`references/`、`skills/`、`research/`、`assets/samples/`）。

| 旧路径 | 现路径 |
|---|---|
| `SKILL.md` | `legacy/SKILL.v1.md` |
| `assets/samples/pavilion-leaf-transition-7s.mp4` | `legacy/assets/samples/pavilion-leaf-transition-7s.mp4` |
| `assets/samples/pavilion-role-reference-ui-mismatch.jpg` | `legacy/assets/samples/pavilion-role-reference-ui-mismatch.jpg` |
| `assets/samples/pavilion-scene-reference.jpg` | `legacy/assets/samples/pavilion-scene-reference.jpg` |
| `assets/samples/scene-reference-empty.png` | `legacy/assets/samples/scene-reference-empty.png` |
| `assets/samples/scene-reference-occupied.png` | `legacy/assets/samples/scene-reference-occupied.png` |
| `assets/samples/stair-reunion-7s.mp4` | `legacy/assets/samples/stair-reunion-7s.mp4` |
| `assets/samples/stair-reunion-character-a.jpg` | `legacy/assets/samples/stair-reunion-character-a.jpg` |
| `assets/samples/stair-reunion-face-b.png` | `legacy/assets/samples/stair-reunion-face-b.png` |
| `assets/samples/stair-reunion-outfit-b.jpg` | `legacy/assets/samples/stair-reunion-outfit-b.jpg` |
| `assets/samples/stair-reunion-scene.jpg` | `legacy/assets/samples/stair-reunion-scene.jpg` |
| `assets/samples/stair-reunion-storyboard.jpg` | `legacy/assets/samples/stair-reunion-storyboard.jpg` |
| `assets/samples/treatment-scan-15s.mp4` | `legacy/assets/samples/treatment-scan-15s.mp4` |
| `assets/samples/treatment-scan-7s.mp4` | `legacy/assets/samples/treatment-scan-7s.mp4` |
| `assets/samples/window-dialogue-5s.mp4` | `legacy/assets/samples/window-dialogue-5s.mp4` |
| `assets/scene-sequence-plan-template.md` | `legacy/assets/scene-sequence-plan-template.md` |
| `references/action-scene-writing.md` | `legacy/references/action-scene-writing.md` |
| `references/annotated-template.md` | `legacy/references/annotated-template.md` |
| `references/director-thinking.md` | `legacy/references/director-thinking.md` |
| `references/original-prompt-dasiming-shaosiyuan-lake-dialogue.md` | `legacy/references/original-prompt-dasiming-shaosiyuan-lake-dialogue.md` |
| `references/original-prompt-pavilion-leaf-transition.md` | `legacy/references/original-prompt-pavilion-leaf-transition.md` |
| `references/original-prompt-stair-reunion-storyboard.md` | `legacy/references/original-prompt-stair-reunion-storyboard.md` |
| `references/original-prompt-treatment-scan.md` | `legacy/references/original-prompt-treatment-scan.md` |
| `references/original-prompt-window-dialogue.md` | `legacy/references/original-prompt-window-dialogue.md` |
| `references/sample-findings.md` | `legacy/references/sample-findings.md` |
| `references/seedance-version-routing.md` | `legacy/references/seedance-version-routing.md` |
| `references/sera-current-video-template.md` | `legacy/references/sera-current-video-template.md` |
| `references/short-drama-direction.md` | `legacy/references/short-drama-direction.md` |
| `references/storyboard-workflow.md` | `legacy/references/storyboard-workflow.md` |
| `references/validated-camera-causality-and-pov-body-anchors.md` | `legacy/references/validated-camera-causality-and-pov-body-anchors.md` |
| `references/visible-facts-and-duration-examples.md` | `legacy/references/visible-facts-and-duration-examples.md` |
| `research/claude-opus-shot-duration-three-rounds.md` | `legacy/research/claude-opus-shot-duration-three-rounds.md` |
| `skills/asset-director/SKILL.md` | `legacy/skills/asset-director/SKILL.md` |
| `skills/continuity-director/SKILL.md` | `legacy/skills/continuity-director/SKILL.md` |
| `skills/failure-diagnostics/SKILL.md` | `legacy/skills/failure-diagnostics/SKILL.md` |
| `skills/idea-parser/SKILL.md` | `legacy/skills/idea-parser/SKILL.md` |
| `skills/idea-parser/references/intake-understanding-and-spatial-confirmation.md` | `legacy/skills/idea-parser/references/intake-understanding-and-spatial-confirmation.md` |
| `skills/idea-parser/references/rough-idea-intent-fidelity.md` | `legacy/skills/idea-parser/references/rough-idea-intent-fidelity.md` |
| `skills/performance-director/SKILL.md` | `legacy/skills/performance-director/SKILL.md` |
| `skills/performance-director/references/physical-plausibility-pass.md` | `legacy/skills/performance-director/references/physical-plausibility-pass.md` |
| `skills/preproduction-director/SKILL.md` | `legacy/skills/preproduction-director/SKILL.md` |
| `skills/sample-learning/SKILL.md` | `legacy/skills/sample-learning/SKILL.md` |
| `skills/sample-learning/references/combat-video-0-15-display-task-case.md` | `legacy/skills/sample-learning/references/combat-video-0-15-display-task-case.md` |
| `skills/scene-sequence-director/SKILL.md` | `legacy/skills/scene-sequence-director/SKILL.md` |
| `skills/shot-designer/SKILL.md` | `legacy/skills/shot-designer/SKILL.md` |

## 路径没变、但内容变了的
- `SKILL.md`：现在是新入口（约 6 KB），旧内容在 `legacy/SKILL.v1.md`。指向 `SKILL.md` 的链接仍然有效，但读到的是新入口。
- `assets/clean-template.md`：只在文件开头加了状态说明。

## 新增的路径
`assets/slot-template.md`、`topics/`（13 个主题文件）、`evidence/`（13 个证据文件）、`legacy/`。
