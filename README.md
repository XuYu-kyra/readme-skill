# Job Portfolio README Skill

[English](#english) · [中文](#中文)

Turn a real GitHub repository into a polished bilingual README for job applications and technical portfolios—without inventing results, overstating ownership, or forcing every project into the same template.

## English

### What it does

`job-portfolio-readme` helps Codex inspect a repository and create or revise its public README. It can:

- inspect source code, dependencies, documentation, tests, results, demos, licences, and attribution;
- identify the strongest evidence-backed project story;
- distinguish personal, team, adapted, and upstream work;
- choose a structure suited to the project type;
- explain technologies through their actual role in the system;
- write complete, natural Chinese and English editions;
- keep security and repository-cleanup notes out of public-facing copy;
- review the result with a recruiter-focused quality rubric.

### Supported projects

- Research and experimental projects
- Robotics and ROS systems
- Automation and data workflows
- AI and RAG applications
- Products built around upstream models
- Web and course projects
- Portfolio and static sites
- Libraries and developer tools

The structure changes with the project. Research READMEs lead with the question, method, and results; robotics READMEs focus on system context and interfaces; model-integration projects separate the upstream model from the product and integration work.

### Install

Codex discovers skills from folders containing a `SKILL.md` file. Install this repository for your user account or inside one project.

#### User-scoped

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

#### Repository-scoped

Run from the repository you want Codex to work on:

```bash
git clone https://github.com/XuYu-kyra/readme-skill.git \
  .codex/skills/job-portfolio-readme
```

Start a new Codex conversation after installation.

### Use

```text
Use $job-portfolio-readme to inspect this repository and rewrite README.md
for job applications. Write complete Chinese and English editions, and base
every claim on repository evidence.
```

You can also specify the emphasis:

```text
Use $job-portfolio-readme to improve this ROS 2 project README. Make my
perception and system-integration work clear, preserve team attribution,
and include the verified experiment results.
```

```text
Use $job-portfolio-readme to rewrite this AI application's README. Clearly
separate the upstream model from the API, backend, and UI work I completed.
```

The skill supports three modes:

| Request | Behaviour |
|---|---|
| Review | Analyse the current README and report specific improvements |
| Draft | Produce a replacement without modifying the repository |
| Direct edit | Update the authorised README and verify the result |

### What you receive

The public README can include:

- project purpose and value;
- personal role and ownership boundaries;
- architecture or workflow where useful;
- technology stack with real responsibilities;
- verified results, demos, screenshots, or artifacts;
- setup and usage supported by the repository;
- concise upstream and collaborator attribution;
- natural Chinese and English editions.

The delivery summary reports changed files, evidence checked, validation performed, and any facts or attribution that still require confirmation. Security or cleanup findings remain separate from the public README.

### Quality rules

The skill will not:

- invent measurements, deployment status, users, training, or ownership;
- describe an upstream model as original work;
- weaken collaborator attribution to make a project sound stronger;
- expose credentials or remediation notes in public copy;
- publish a generic list of missing production features;
- shorten the Chinese edition into a summary of the English version;
- reuse one rigid structure for unrelated projects.

### Package structure

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

This is an instruction-only skill. It has no runtime dependencies and requires no API key.

See [OpenAI's Skills documentation](https://developers.openai.com/plugins/concepts/skills) for the underlying format.

---

## 中文

`job-portfolio-readme` 用于把真实 GitHub 仓库整理成适合求职和技术作品集展示的中英文 README。它会先检查仓库证据，再组织项目价值、个人贡献、技术实现和结果；不会编造数据、夸大 ownership，也不会让所有项目使用同一套模板。

### 可以做什么

- 检查源码、依赖、文档、测试、实验结果、演示、许可证和 attribution；
- 找出项目中最值得优先展示且有证据支持的内容；
- 区分本人实现、团队工作、上游代码和集成工作；
- 根据项目类型选择合适的 README 结构；
- 说明每项技术在系统中的真实作用；
- 分别撰写自然、内容完整的中文和英文版本；
- 将安全问题和仓库清理建议留在私下交付说明中；
- 使用面向招聘阅读的质量标准检查最终结果。

### 支持的项目

- 研究与实验项目
- 机器人和 ROS 系统
- 自动化与数据工作流
- AI 与 RAG 应用
- 基于上游模型的集成产品
- Web 与课程项目
- 个人作品集和静态网站
- Library 与开发者工具

不同项目会采用不同重点。研究项目优先说明问题、方法和结果；机器人项目强调真实运行环境、接口和系统协作；模型集成项目明确区分上游模型与本人完成的 API、后端、前端和产品链路。

### 安装

Codex 会从包含 `SKILL.md` 的目录中发现 skill。可以安装到当前用户，也可以只安装到某个项目。

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

#### 单个项目安装

在需要处理的仓库根目录运行：

```bash
git clone https://github.com/XuYu-kyra/readme-skill.git \
  .codex/skills/job-portfolio-readme
```

安装后开启新的 Codex 对话。

### 使用

```text
使用 $job-portfolio-readme 检查这个仓库，并把 README.md 重写成求职版本。
分别写完整的中文和英文内容，所有结论都以仓库证据为准。
```

也可以说明希望强调的方向：

```text
使用 $job-portfolio-readme 优化这个 ROS 2 项目的 README。重点说明我负责的
感知与系统集成工作，保留团队 attribution，并加入有证据支持的实验结果。
```

```text
使用 $job-portfolio-readme 重写这个 AI 应用的 README。明确区分上游模型，
以及我完成的 API、后端和前端工作。
```

支持三种工作方式：

| 请求方式 | 行为 |
|---|---|
| 审核 | 检查当前 README，并给出具体修改建议 |
| 起草 | 生成替换稿，但不修改仓库文件 |
| 直接修改 | 更新授权的 README，并检查最终结果 |

### 最终交付

公开 README 可以包含：

- 清楚的项目目标与价值；
- 个人职责和 ownership 边界；
- 必要的架构或工作流程；
- 说明实际作用的技术栈；
- 已验证的结果、演示、截图或产物；
- 与仓库一致的安装和使用方式；
- 简洁准确的上游与团队 attribution；
- 自然且内容对等的中英文版本。

交付摘要会说明修改文件、检查过的证据、完成的验证，以及仍需确认的事实或 attribution。安全和仓库清理问题不会混入公开 README。

### 质量规则

这个 skill 不会：

- 编造指标、部署状态、用户量、模型训练或个人 ownership；
- 把上游模型描述成本人原创；
- 为了包装效果弱化团队成员或原作者署名；
- 在公开 README 中写入凭据或密钥整改说明；
- 公开罗列项目尚未完成的生产化功能；
- 把中文版压缩成英文版的摘要；
- 对不同类型项目重复使用僵硬的统一结构。

### 目录结构

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

这是一个纯指令型 skill，不需要额外运行依赖或 API key。

关于 skill 的基础格式，可参考 [OpenAI Skills 文档](https://developers.openai.com/plugins/concepts/skills)。

