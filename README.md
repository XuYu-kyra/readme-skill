# Job Portfolio README Skill

[English](#english) · [中文](#中文)

A reusable Codex skill for turning real GitHub repositories into **evidence-based bilingual portfolio READMEs**. It helps inspect repository evidence, clarify personal contribution and upstream attribution, select a project-specific structure, and keep internal audit findings out of public-facing copy.

This is an instruction-and-reference skill: it does not require an API key, external service, or runtime dependency.

## English

### Why this skill exists

Portfolio READMEs often fail in one of two directions. Some are only installation notes and never explain the project's value or the author's contribution. Others sound polished but overstate ownership, invent results, or publish security and repository-hygiene observations that belong in a private review.

This skill defines a repeatable workflow for a better middle ground:

- inspect code, documentation, results, media, licences, and attribution before writing;
- build claims from repository evidence instead of filling a generic template;
- distinguish **implemented**, **adapted**, **integrated**, **extended**, and **team-owned** work;
- choose a different information structure for research, robotics, RAG, automation, web, portfolio, and model-integration projects;
- write complete, natural Chinese and English editions from the same fact model;
- separate the recruiter-facing README from private security, provenance, and cleanup notes;
- review the final draft against a 100-point quality rubric and automatic-failure checks.

### Is a skill just a large prompt?

`SKILL.md` is the instruction core, so it is prompt-like—but a skill is a small reusable workflow package rather than one long message. Codex first sees the skill's name and description, loads the full instructions when the task matches, and then follows linked references only when needed.

In this repository:

- `SKILL.md` defines the trigger conditions, workflow, output boundaries, and non-negotiable rules;
- `references/quality-rubric.md` provides scoring and automatic-failure criteria;
- `references/project-archetypes.md` provides project-specific structures without enforcing one template;
- `references/bilingual-style.md` defines Chinese/English parity and ownership vocabulary;
- `agents/openai.yaml` supplies display metadata and a default invocation prompt.

The result is easier to maintain, inspect, and reuse than a single copy-pasted prompt.

### Workflow

```text
resolve audience and scope
          │
          ▼
inspect repository evidence
          │
          ▼
build a private claim ledger
          │
          ▼
identify the portfolio thesis
          │
          ▼
choose a project archetype
          │
          ▼
draft natural Chinese and English editions
          │
          ▼
score the public README and check attribution
          │
          ▼
publish README + deliver private findings separately
```

Three reading depths guide the public README:

1. **15 seconds:** project value, strongest evidence or demo, and personal role.
2. **2 minutes:** architecture, contribution, technology roles, and results.
3. **Technical follow-up:** decisions, trade-offs, evaluation, reproduction, and attribution.

### Public README vs. private review

| Public README | Private delivery report |
|---|---|
| Project value and user/research outcome | Credential rotation and historical exposure |
| Personal contribution and ownership boundary | Repository cleanup and hygiene observations |
| Architecture and meaningful decisions | Missing production-hardening suggestions |
| Verified results, demos, and artifacts | Unverified claims and provenance questions |
| Setup, usage, and concise attribution | Follow-up work that should not become public copy |

This separation prevents a portfolio README from turning into an audit report or apology while keeping the private review honest.

### Installation

Codex skills can be installed for one user under `~/.codex/skills/` or scoped to one repository under `.codex/skills/`. The folder containing `SKILL.md` is the skill package.

#### User-scoped installation

macOS/Linux:

```bash
git clone https://github.com/XuYu-kyra/readme-skill.git \
  ~/.codex/skills/job-portfolio-readme
```

Windows PowerShell:

```powershell
git clone https://github.com/XuYu-kyra/readme-skill.git `
  "$env:USERPROFILE\.codex\skills\job-portfolio-readme"
```

#### Repository-scoped installation

Run from the target repository:

```bash
git clone https://github.com/XuYu-kyra/readme-skill.git \
  .codex/skills/job-portfolio-readme
```

Start a new Codex conversation after installation so the skill metadata is included in the new session.

### Usage

Invoke it explicitly:

```text
Use $job-portfolio-readme to inspect this repository and rewrite README.md
as a bilingual portfolio README. Base every claim on repository evidence and
keep security or cleanup findings in the private delivery report.
```

Or describe a matching goal naturally:

```text
Rewrite this robotics project README for job applications. Make my ROS 2
perception contribution clear, preserve team attribution, and write natural
Chinese and English editions.
```

The skill is intended for public repositories used in job applications, portfolio reviews, and technical interviews. It is not intended to replace API documentation, contributor guides, or security audit reports.

### Repository structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── quality-rubric.md
    ├── project-archetypes.md
    └── bilingual-style.md
```

### Design principles

- **Evidence before copy:** the old README is a claim source, not final authority.
- **Ownership before promotion:** stronger marketing never justifies weaker attribution.
- **Structure follows project type:** a research experiment should not read like a web prototype.
- **Technology needs a role:** a useful stack section explains what each technology does.
- **Bilingual means equal substance:** Chinese is not a shortened translation of English.
- **Packaging is selection, not fabrication:** present the strongest true facts and omit unsupported claims.

### Example applications

The workflow was developed while revising a mixed portfolio containing robotics research, ROS 2 system integration, RAG, workflow automation, Django prototypes, an AI model-integration product, and a Jekyll portfolio site. Examples include:

- [BARNnavigation](https://github.com/XuYu-kyra/BARNnavigation) — research question, paired experiment design, and measured results;
- [robotic-systems-design](https://github.com/XuYu-kyra/robotic-systems-design) — ROS 2 perception responsibility and team attribution;
- [LB](https://github.com/XuYu-kyra/LB) — upstream OOTDiffusion attribution and mini-program product integration;
- [Facial_music](https://github.com/XuYu-kyra/Facial_music) — accurate separation of inherited FER code and application-layer work.

### References

- [OpenAI: Skills](https://developers.openai.com/plugins/concepts/skills)
- [OpenAI: Testing Agent Skills Systematically](https://developers.openai.com/blog/eval-skills)

---

## 中文

这是一个用于 Codex 的求职作品集 README skill，目标是把真实 GitHub 仓库整理成 **有证据、有技术深度、归属清楚的中英文项目介绍**。它会先检查代码、文档、实验结果、媒体、许可证和署名，再决定公开 README 应该写什么，而不是直接套用一份通用模板。

这是纯指令与参考资料组成的 skill，不依赖 API key、外部服务或额外运行环境。

### 为什么做这个 skill

用于求职的项目 README 很容易走向两个极端：一种只记录安装命令，看不出项目价值和个人工作；另一种虽然“包装感”很强，却可能夸大 ownership、编造结果，甚至把密钥整改、仓库缺点和产品化待办直接写给招聘者看。

这个 skill 将 README 重写整理为一套可复用流程：

- 写作前检查源码、文档、结果、演示、许可证和 attribution；
- 所有重要结论都从仓库证据出发，而不是填充固定模板；
- 明确区分 **本人实现、基于上游适配、系统集成、继续扩展和团队共同完成**；
- 根据研究、机器人、RAG、自动化、Web、作品集和模型集成等项目类型选择不同结构；
- 从同一份事实模型分别写自然、内容完整的中文和英文版本；
- 将招聘者看到的 README 与安全、来源和仓库清理意见分开；
- 使用 100 分质量量表和自动失败条件检查最终稿。

### Skill 是不是一个大型 prompt？

`SKILL.md` 是核心指令，因此它确实具有 prompt 的性质；但完整 skill 更像一个小型、可复用的工作流包，而不是一次性长提示词。Codex 会先读取 skill 的名称和描述，在任务匹配时加载完整指令，再按需读取引用的规则文件。

这个仓库中：

- `SKILL.md` 定义触发场景、执行流程、公开/私下输出边界和硬性规则；
- `references/quality-rubric.md` 提供评分标准与自动失败条件；
- `references/project-archetypes.md` 提供不同项目类型的结构选择，但不强制统一模板；
- `references/bilingual-style.md` 约束中英文内容对等、自然度和 ownership 用词；
- `agents/openai.yaml` 提供显示信息和默认调用提示。

这种拆分比复制一段超长 prompt 更容易维护、检查和迭代。

### 工作流程

```text
确认受众与修改范围
        │
        ▼
检查仓库证据
        │
        ▼
建立私下 claim ledger
        │
        ▼
提炼项目的核心定位
        │
        ▼
选择适合的项目结构
        │
        ▼
分别撰写自然的中英文版本
        │
        ▼
评分并检查结果、ownership 与 attribution
        │
        ▼
发布 README，私下交付审计与待确认事项
```

公开 README 同时考虑三种阅读深度：

1. **15 秒：** 看懂项目价值、最强证据或演示，以及个人角色；
2. **2 分钟：** 了解架构、个人贡献、技术作用和结果；
3. **技术追问：** 能继续讨论设计决策、取舍、评测、复现和 attribution。

### 公开 README 与私下审查

| 公开 README | 私下交付报告 |
|---|---|
| 项目价值和用户/研究结果 | 凭据轮换和历史泄露处理 |
| 个人贡献和 ownership 边界 | 仓库清理与 hygiene 问题 |
| 架构与有意义的工程决策 | 缺失的生产化能力建议 |
| 已验证的结果、演示和产物 | 未验证事实与来源疑问 |
| 运行方式和简洁 attribution | 不应出现在公开文案中的后续工作 |

这条边界既能避免把求职 README 写成审计报告或道歉信，也不会牺牲私下检查的真实性。

### 安装

Codex skill 可以安装到 `~/.codex/skills/`，供当前用户使用；也可以放在项目的 `.codex/skills/` 中，只作用于该仓库。包含 `SKILL.md` 的目录就是一个完整 skill 包。

#### 当前用户安装

macOS/Linux：

```bash
git clone https://github.com/XuYu-kyra/readme-skill.git \
  ~/.codex/skills/job-portfolio-readme
```

Windows PowerShell：

```powershell
git clone https://github.com/XuYu-kyra/readme-skill.git `
  "$env:USERPROFILE\.codex\skills\job-portfolio-readme"
```

#### 单个仓库安装

在目标仓库根目录运行：

```bash
git clone https://github.com/XuYu-kyra/readme-skill.git \
  .codex/skills/job-portfolio-readme
```

安装后开启一个新的 Codex 对话，使新会话能够读取该 skill 的元数据。

### 使用方式

可以直接点名调用：

```text
使用 $job-portfolio-readme 检查这个仓库，并把 README.md 重写成用于求职的
中英文项目介绍。所有结论以仓库证据为准，安全或清理问题放在私下交付报告中。
```

也可以直接描述符合触发条件的任务：

```text
把这个机器人项目的 README 重写成求职版本。说明我负责的 ROS 2 感知工作，
保留团队 attribution，并分别写自然、内容完整的中文和英文版本。
```

这个 skill 适合求职项目、作品集审查和技术面试准备，不用于替代 API 文档、贡献者手册或安全审计报告。

### 仓库结构

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── quality-rubric.md
    ├── project-archetypes.md
    └── bilingual-style.md
```

### 设计原则

- **先找证据，再写文案：** 原 README 只是 claim 来源，不是最终事实；
- **先说清归属，再做包装：** 更强的宣传不能以弱化 attribution 为代价；
- **结构服从项目类型：** 研究实验不应该和网页原型使用同一套叙事；
- **技术栈必须说明作用：** 不只列技术名称，还要说明它在项目中负责什么；
- **双语必须内容对等：** 中文不能只是英文的压缩摘要；
- **包装是选择事实，不是创造事实：** 呈现最强的真实内容，删除没有证据的说法。

### 实际应用

这个流程是在整理一组混合型求职作品集时形成的，覆盖机器人研究、ROS 2 系统集成、RAG、数据工作流、Django 原型、AI 模型集成产品和 Jekyll 作品集。例如：

- [BARNnavigation](https://github.com/XuYu-kyra/BARNnavigation)：研究问题、配对实验设计与量化结果；
- [robotic-systems-design](https://github.com/XuYu-kyra/robotic-systems-design)：ROS 2 感知职责与团队 attribution；
- [LB](https://github.com/XuYu-kyra/LB)：OOTDiffusion 上游归属与小程序产品集成；
- [Facial_music](https://github.com/XuYu-kyra/Facial_music)：准确区分已有 FER 代码和本人完成的应用层工作。

### 参考资料

- [OpenAI：Skills](https://developers.openai.com/plugins/concepts/skills)
- [OpenAI：系统化测试 Agent Skills](https://developers.openai.com/blog/eval-skills)
