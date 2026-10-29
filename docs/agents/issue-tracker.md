# Issue tracker: Local Markdown

本仓库的规格和任务以 Markdown 文件保存在 `.scratch/` 下。

## 文件约定

- 每个功能一个目录：`.scratch/<feature-slug>/`。
- 规格：`.scratch/<feature-slug>/spec.md`。
- 实现任务：`.scratch/<feature-slug>/issues/<NN>-<slug>.md`。
- 每个任务独立一个文件，从 `01` 开始编号。
- 分诊状态写在文件顶部附近的 `Status:` 行，
  状态名称见 `triage-labels.md`。
- 评论和讨论追加到文件末尾的 `## Comments` 下。

## 发布与读取

技能要求“发布到任务跟踪系统”时，在对应功能目录创建文件。
技能要求“获取任务”时，读取用户指定路径或编号对应的文件。

## Wayfinding

- 决策地图：`.scratch/<effort>/map.md`，
  记录 Notes、Decisions-so-far 和 Fog。
- 决策任务：`.scratch/<effort>/issues/<NN>-<slug>.md`。
- `Type:` 为 research、prototype、grilling 或 task。
- 决策任务的 `Status:` 为 open、claimed 或 resolved；
  这组执行状态与分诊状态分开使用。
- `Blocked by: NN, NN` 记录阻塞任务编号。
- 所有阻塞任务均为 resolved，当前任务才可开始。
- 从 open 且无阻塞的任务中按编号选择。
- 开始工作前，先保存 `Status: claimed`。
- 完成后，在 `## Answer` 下追加结论，
  更新为 `Status: resolved`，
  并将结论摘要和链接追加到地图的 Decisions-so-far。
