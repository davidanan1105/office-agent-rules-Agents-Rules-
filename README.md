# Office Agent Rules

这是一套面向综合职能人员的 AI 办公任务全局规则。

它适用于 HR、行政、财务、法务、运营、培训、项目管理、综合管理等岗位，用来约束 AI 在处理文档、表格、材料、流程、数据和轻量自动化任务时的工作方式。

它的目标不是让使用者学习开发，而是让 AI 在办公任务中做到：

- 不乱改事实；
- 不臆造口径；
- 不覆盖原文件；
- 不把简单事情复杂化；
- 能说明改了什么、检查了什么、还有什么风险。

## 来源与关联

本项目受到 [`forrestchang/andrej-karpathy-skills`](https://github.com/forrestchang/andrej-karpathy-skills) 启发。

`andrej-karpathy-skills` 是一个面向 Claude Code / 编程 Agent 的行为规则项目，其 README 将自身定位为：一个用于改善 Claude Code 行为的 `CLAUDE.md` 文件，并说明其来源于 Andrej Karpathy 对 LLM 编码常见问题的观察。该项目把这些问题收敛为四个核心原则：

1. Think Before Coding：先澄清假设与不确定性，再动手。
2. Simplicity First：优先使用简单、直接、不过度设计的方案。
3. Surgical Changes：只修改任务必要范围，不做无关重构。
4. Goal-Driven Execution：把任务转化为可验证的目标，并围绕验证结果迭代。

本项目不是 `andrej-karpathy-skills` 的官方中文版，也不是对其内容的直接翻译，而是一个面向“非开发者 / 职能人员办公任务”的改写版本。

它把上述工程化原则转换为办公场景下更容易理解和使用的规则：

| 原工程原则 | 办公场景改写 |
| --- | --- |
| Think Before Coding | 先理解任务、材料、对象和边界，再处理文件 |
| Simplicity First | 不把简单的文档、表格、材料任务复杂化 |
| Surgical Changes | 只改该改的内容，不擅自改事实、数字、口径和原始材料 |
| Goal-Driven Execution | 每次交付都说明已检查范围、未检查范围和剩余风险 |

因此，`office-agent-rules` 可以理解为：

> 一个把 Karpathy-style coding agent rules 降维改造成 office agent rules 的职能办公版本。

## 适用场景

- 文档整理、改写、归档；
- Excel / 表格数据处理；
- 制度、通知、流程说明整理；
- 汇报材料结构化；
- 项目资料清洗与交接；
- 简单 Markdown / HTML 页面生成；
- AI Agent / Codex / Claude Code / Cursor 的全局规则配置。

## 快速使用

把 `AGENTS.md` 中的内容复制到你的 AI 工具全局规则、项目规则或工作区规则中。

如果你已经有自己的全局规则，可以只复制其中这些部分：

- 工作方式；
- 执行原则；
- 文件与数据安全；
- 验证要求；
- 输出格式。

## 文件说明

```text
.
├── README.md
├── AGENTS.md
├── LICENSE
├── templates/
│   ├── task-card.md
│   └── handoff-summary.md
└── examples/
    └── prompt-examples.md
```

说明：

- `README.md`：项目说明。
- `AGENTS.md`：可直接复制到 Codex / Claude Code / Cursor 等工具中的职能版全局规则。
- `templates/task-card.md`：给使用者填写任务需求用。
- `templates/handoff-summary.md`：用于任务结束时做交接和总结。
- `examples/prompt-examples.md`：常见办公任务的提示词示例。

## 设计原则

这套规则借鉴了工程任务中的几个通用原则：

1. 先理解任务，再动手。
2. 优先使用简单、可维护的方案。
3. 只改该改的地方。
4. 保护原始文件和原始事实。
5. 交付必须可检查、可验收、可交接。

## 推荐启动语

在每次任务开始时，可以加一句：

```text
请按 AGENTS.md 的规则执行。先说明理解、计划、涉及文件和验收方式；不要覆盖原文件，不要擅自改动事实、数字和业务口径。
```

## 推荐仓库名

```text
office-agent-rules
```

## License

MIT
