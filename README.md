# Auto Course Lab Report

English | [中文](README.zh-CN.md)

A Cursor skill for one author's course lab report, set in XeLaTeX.

It is built for three things.

- **No AI trace.** The voice is a student who did the sheet. Complete sentences, the formula in the same sentence as the English, one sentence after a truth table. No overview, no extra exercise, no closing essay.
- **Concise.** Answer the question, then stop.
- **Complete.** One section for each exercise that asks for an answer, in the handout's order. Letters, connectives, predicate names, and truth-table row order stay as the sheet printed them.

The report body is English. This page is the English copy of the documentation.

## Files

| File | Role |
|---|---|
| `SKILL.md` | Workflow and rules |
| `template.tex` | Cover, header, truth tables |
| `template.pdf` | Example of the empty template |
| `student.md` | Name and student ID |
| `notation.md` | Connectives, quantifiers, table shape |
| `handwriting.md` | Photo step, only when a page must be handwritten |

## Use

Place this folder where Cursor loads project skills, then ask for the lab report and provide the handout.

The cover name stays `name` until you replace it. The student ID is unset. It is requested before the final PDF, and it is not invented. Compile twice with XeLaTeX from the `report/` directory. The example cover in `template.pdf` uses course code `COURSE`, assignment `N`, and the date `1 January 2026`.
