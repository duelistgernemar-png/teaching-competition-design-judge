# Agent Entry Guide

This repository defines a portable review workflow for Chinese K-12 teaching-competition lesson designs. If an agent is given this GitHub URL and asked to use it, follow the instructions below.

## Primary Instruction

Read `SKILL.md` first and treat it as the main operating instruction. This repository is not a software package to run; it is an instruction-and-reference bundle for evaluating lesson-design documents.

## Task Scope

Only evaluate the teaching design evidence provided by the user. Do not invent or score:

- classroom recording performance
- live teacher language
- classroom management
- student reactions not shown in the design
- teaching reflection quality

If the user provides only a lesson-design PDF/DOCX/text, score only the lesson design.

## Required Reading Order

1. `SKILL.md`
2. `references/official_design_rubric_10th.md`
3. `references/subject_stage_patterns/coverage_index.md`
4. The matched subject-stage file under `references/subject_stage_patterns/`
5. `references/discipline_output_contract.md`
6. `references/teaching_process_audit.md`
7. `references/corpus_sample_index.md` when comparing against sample-strength patterns

## How To Run The Review

1. Extract or read the user's lesson-design text.
2. Identify 学段 and 学科 from grade, subject, textbook, objectives, learning content, and activities.
3. Apply the official 30-point teaching-design score.
4. Add a 100-point diagnostic score only as a revision aid.
5. Audit the teaching process activity by activity. For each major activity, name:
   - student task
   - visible output
   - subject-specific thinking
   - evaluation evidence
   - scoring risk and concrete revision
6. Give concrete Chinese replacement text for the core question/problem chain and at least one objective, evaluation criterion, activity wording, technology integration paragraph, or course-ideology paragraph.

## Recommended User Prompt

```text
Please use this GitHub repository as your review rule set:
https://github.com/duelistgernemar-png/teaching-competition-design-judge

Read AGENTS.md and SKILL.md first, then evaluate my lesson-design document. Identify the subject and stage, score only the teaching-design evidence, audit the teaching process activity by activity, and give concrete revision text in Chinese.
```

## Output Language

Use Chinese by default unless the user requests another language.
