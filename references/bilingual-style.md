# Bilingual Style

Write Chinese and English from one verified fact model. Do not create a full
English README and mechanically shorten it into Chinese.

## Content parity

Both editions should preserve:

- project purpose and outcome;
- personal contribution and ownership boundaries;
- architecture and important engineering decisions;
- measurements, sample scope, demos, commands, and links;
- upstream and collaborator attribution.

Section order may differ slightly for natural reading, but neither edition is a
summary of the other.

## English

- Prefer clear subject-verb-object sentences.
- Use precise verbs such as *implemented*, *integrated*, *adapted*, *designed*,
  *evaluated*, and *measured*.
- Avoid repeated “I built,” generic self-praise, and interview-facing filler.
- Explain trade-offs directly.
- Keep spelling conventions consistent.

## Chinese

- Write like a Chinese engineer describing real work, not like translated
  marketing copy.
- Prefer “我负责完整的感知链路及其与导航、机械臂的接口” over unnatural phrases
  such as “我拥有感知边界.”
- Prefer “这是我的 MSc Robotics 毕业论文项目” over “毕业论文级别项目.”
- Keep established technical names when that is clearer than forced translation.
- Avoid long noun stacks and slogan-like fragments.
- Preserve reasoning and evidence; do not compress the Chinese edition.

## Ownership vocabulary

| Meaning | English | Chinese |
|---|---|---|
| Original implementation | implemented / designed | 实现 / 设计 |
| Built on upstream code | adapted / extended | 基于…适配 / 扩展 |
| Connected components | integrated | 集成 / 打通 |
| Candidate-owned scope | I was responsible for | 我负责 |
| Shared team work | jointly developed / team-owned | 共同完成 / 团队负责 |

## Packaging examples

Internal audit wording:

> The prototype lacks queues, monitoring, locked dependencies, and production
> storage.

Recruiter-facing wording:

> I connected the mini-program flow to the inference service and turned the
> upstream model into an end-to-end interactive prototype.

Overclaimed ownership:

> I wrote the CNN that powers the application.

Evidence-safe ownership:

> I adapted and integrated the existing CNN inference code into the Django
> application, then implemented the upload, prediction, and result-page flow.

## Final bilingual review

- Read each edition independently for naturalness.
- Compare every number, link, command, result, and attribution.
- Remove literal translations that a native speaker would not use.
- Confirm both editions answer “what did you personally do?” with equal clarity.
