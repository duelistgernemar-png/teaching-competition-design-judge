# Teaching Competition Design Judge Skill

一个面向中小学教学比赛“教学设计”文本的 Codex skill。它只评价教学设计材料本身，不根据课堂实录、课堂表现或教学反思做推断性打分。

## What It Does

This skill helps Codex act as a Chinese K-12 teaching-design reviewer. It can:

- 自动识别上传材料的学段与学科。
- 按教学设计专项维度给出 30 分制评分。
- 提供 100 分诊断折算分，方便定位修改优先级。
- 按学段学科切换评价模式，例如小学英语、高中生物、初中数学、高中地理等。
- 对教学过程进行逐环节评审，指出每个活动的学生任务、可见产出、学科思维、评价证据和修改方向。
- 给出可直接替换进教学设计的核心问题、问题链、评价量规或活动表述。

## When To Use

Use this skill when you have:

- 教学比赛教学设计 PDF、DOCX 或文本。
- 需要模拟评委视角的教学设计专项评价。
- 需要按不同学段、不同学科给出有差异的修改建议。
- 只有教学设计，没有课堂视频或教学反思。

Do not use it to score live teaching performance, classroom recording quality, teacher language, classroom control, or reflection-video quality unless separate evidence and rules are provided.

## Output Structure

默认输出为中文，通常包括：

1. 学段学科识别
2. 总体竞争力判断
3. 教学设计专项评分表
4. 学科化高分证据
5. 教学过程逐环节评审
6. 获奖作品画像对照
7. 优先修改清单
8. 可直接替换文本

## Scoring Basis

The default score is a 30-point teaching-design score:

| Dimension | Points |
|---|---:|
| Background analysis, learning objectives, methods and strategies | 10 |
| Problem framework | 5 |
| Teaching process and activity design | 15 |

For detailed diagnosis, the skill may also provide a 100-point converted score. The 100-point score is only a revision aid, not an official score.

## Subject And Stage Coverage

The skill includes subject-stage pattern references for common Chinese K-12 categories, including:

- Primary: Chinese, Math, English, Science, Morality and Law, Art, Calligraphy, Music, PE, Dance, Psychology, Information Technology, Integrated Practice
- Junior secondary: Chinese, Math, English, Physics, Chemistry, Biology, Geography, History, Morality and Law, Art, PE, Psychology, Information Technology
- Senior secondary: Chinese, Math, English, Physics, Chemistry, Biology, Geography, History, Ideology and Politics, Morality and Law, PE, Psychology

Each subject-stage mode translates the general rubric into discipline-specific review priorities.

## Example Prompt

```text
调用 teaching-competition-design-judge，评价这份教学设计。请识别学段学科，给出教学设计专项评分，并重点拆解教学过程。
```

```text
Use $teaching-competition-design-judge to evaluate this Chinese K-12 lesson design. Score only the lesson design, audit the teaching process activity by activity, and give concrete revision text in Chinese.
```

## Installation

Clone this repository into your Codex skills directory or any skill path that your Codex setup loads:

```bash
git clone https://github.com/duelistgernemar-png/teaching-competition-design-judge.git
```

Then restart or reload Codex so the skill list can refresh.

## Repository Layout

```text
teaching-competition-design-judge/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── official_design_rubric_10th.md
    ├── discipline_output_contract.md
    ├── teaching_process_audit.md
    ├── corpus_sample_index.md
    └── subject_stage_patterns/
```

## Notes

- This repository contains evaluation instructions and reference patterns, not private teaching-design PDFs.
- The skill is designed to avoid making unsupported claims from missing classroom video evidence.
- If the uploaded lesson design contradicts a filename or folder label, the lesson-design text itself should be trusted.
