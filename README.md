# project-worklog · 项目工作台账

一个面向 Codex 的中文 Markdown 技能，用于交接长期项目。它把长期规则、最近核实的状态和逐项工作证据分开，让新对话能快速找到上次做到哪、下一步做什么，以及还有哪些地方需要核实。

适合本地环境维护、部署、实验和研究。台账以普通 Markdown 文件保存，可以只在本地使用，也可以配合 Git 保存版本。

## 三个入口

| 文件 | 内容 |
| --- | --- |
| `AGENTS.md` | 长期规则、授权边界和项目资料入口 |
| `STATUS.md` | 最新事实、未关闭工作及恢复条件、简短历史索引 |
| `logs/<工作ID>.md` | 续接摘要、逐轮记录、证据和恢复步骤 |

状态页分别记**配置、运行观察和功能验收**。比如，脚本已指向新版、上次观察到新版运行、隔离环境验证通过，这三条信息各有自己的时间和证据。历史快照留在原日志，接手时先看状态页和相关工作摘要。

## 安装到 Codex

1. 从 GitHub 仓库的 **Code** 菜单下载 ZIP，或克隆仓库。
2. 将文件复制到下列任一位置，目录命名为 `project-worklog`。确保 `SKILL.md` 直接位于该目录内，并保留 `agents/`、`assets/` 和 `references/`。
   - 个人使用：`~/.agents/skills/project-worklog/`。Windows 对应用户目录下的 `.agents\skills\project-worklog\`。
   - 项目共享：`<项目根目录>/.agents/skills/project-worklog/`。
3. 在 Codex 的技能选择器中选择 `project-worklog`，或在对话中输入 `$project-worklog`。若技能未出现，确认目录位置和层级，再重启 Codex。 [Codex 技能说明](https://learn.chatgpt.com/docs/build-skills)

## 开始使用

**首次采用**

> 使用 $project-worklog 为当前项目建立轻量台账。先检查已有资料，保留项目规则。本次只整理文档。

**交给新对话续接**

> 继续这项工作。先读 STATUS.md 的未关闭工作，再从对应日志的续接摘要开始。先告诉我上次验证到哪里。

**迁移已有台账**

> 使用 $project-worklog 把现有台账整理为轻量版。保留工作 ID、历史日志路径和证据，先核对暂停项能否续接。

技能只在明确选用时启用。采用台账、迁移现有文件、建立 Git 仓库和操作运行环境各按用户授权执行。

## 工作方式

- **轻量记录**。讨论和低风险只读核对可合并记录来源、结论和限制。文件变更与高风险操作保留实际参数、验收、备份和恢复方法。
- **按任务续接**。同一目标跨对话沿用工作 ID。可以独立暂停或验收的工作另立关联项，暂停时写明恢复条件和当前占用。
- **可选 Git**。先确定纳管范围，再保存基线和审阅差异。台账继续记录变更原因和实际验收。大附件与私有材料按项目边界存放。 [Git 工作指南](references/git-workflow.md)

[技能规则](SKILL.md) · [项目规则模板](assets/AGENTS.template.md) · [状态模板](assets/STATUS.template.md) · [工作日志模板](assets/work-log.template.md)
