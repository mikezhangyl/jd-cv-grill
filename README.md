# JD CV Grill / JD 简历深挖

> Bilingual JD-to-resume skill for tailoring a CV/resume to a job description through evidence-first questioning, ATS keyword mapping, and interview-ready resume bullets.

`jd-cv-grill` helps an AI agent turn a job description into a targeted, credible CV or resume. It guides the agent to interview the candidate one question at a time, extract project evidence, map experience to JD requirements, identify ATS and recruiter keywords, and rewrite resume bullets without fabricating achievements.

`jd-cv-grill` 是一个面向中英文求职场景的简历优化 skill：根据招聘 JD、职位描述、目标岗位、现有简历/CV、LinkedIn/profile 或项目经历，逐轮追问候选人的真实贡献、项目证据、指标和取舍，然后生成更贴合岗位的简历内容。

## Search Keywords / 搜索关键词

Use this skill when searching for:

```text
JD resume, job description resume, tailor resume to job description, resume polish,
CV polish, CV rewrite, resume rewrite, ATS resume, ATS keywords, resume bullets,
job application, LinkedIn profile, interview preparation, career story,
简历优化, 简历润色, JD改简历, 根据JD改简历, 岗位匹配, 求职简历,
英文简历, 中文简历, CV优化, ATS关键词, 经历挖掘, 项目经历提炼
```

## What It Does

- Analyzes a JD, job posting, role description, or target company profile.
- Extracts hard requirements, hidden hiring signals, ATS keywords, and recruiter screening logic.
- Interviews the candidate one question at a time instead of asking for a long form.
- Builds an evidence table: JD requirement, candidate proof, strength, missing details, and resume placement.
- Rewrites resume/CV bullets around confirmed facts, personal contribution, scope, impact, tools, and constraints.
- Flags weak evidence, unconfirmed metrics, confidentiality risks, and claims that should not be exaggerated.

## 中文能力

- 根据招聘 JD 拆解岗位画像、硬性要求、隐性标准和 ATS 关键词。
- 通过一轮一问深挖项目经历、个人贡献、业务影响、技术取舍和可验证证据。
- 输出岗位定制版简历 bullet、个人简介、技能映射、缺口补偿策略和待确认事实。
- 支持中文 JD、英文 JD、中文简历、英文简历和中英混合求职场景。

## Install

```bash
npx skills add mikezhangyl/jd-cv-grill -a codex
```

Manual Codex install:

```bash
git clone https://github.com/mikezhangyl/jd-cv-grill.git
mkdir -p ~/.codex/skills/jd-cv-grill
cp -R jd-cv-grill/SKILL.md jd-cv-grill/agents ~/.codex/skills/jd-cv-grill/
```

## Usage

Trigger with prompts like:

```text
使用 $jd-cv-grill 根据这份 JD 追问我的经历，并为我定制简历。
```

```text
Use $jd-cv-grill to tailor my resume to this job description and identify missing evidence.
```

```text
使用 $jd-cv-grill 帮我根据这个岗位优化英文简历，重点处理 ATS 关键词和项目 bullet。
```

You can provide a JD, an existing CV/resume, LinkedIn/profile text, portfolio notes, or local files. The skill tells the agent to inspect available materials first, ask only one high-value question at a time, avoid fabricating experience, and label weak or unconfirmed evidence.

## Best For

- Tailoring a resume or CV to a specific job description.
- Turning vague project experience into strong resume bullets.
- Preparing an English resume from Chinese career notes, or vice versa.
- Mapping candidate evidence to ATS keywords and recruiter expectations.
- Stress-testing whether a resume claim can survive interview follow-up.

## Skill Structure

```text
SKILL.md
agents/openai.yaml
```

## License

MIT
