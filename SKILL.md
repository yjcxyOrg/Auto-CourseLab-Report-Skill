---
name: auto-courselab-report-skill
description: >-
  Writes an individual assignment report in English XeLaTeX: cover page,
  handout-ordered exercises, typed first-order logic, and truth tables.
  Use when the user asks to write, revise, compile, or format a lab report,
  Assignment N, a submission PDF, or this LaTeX template. If a handout asks
  for handwriting, send a copy sheet and wait for the photo. Individual
  submission only.
---

# Assignment Report

English individual laboratory report. Copy [template.tex](template.tex), fill it from the handout, and compile with XeLaTeX.

The author's name and ID live in [student.md](student.md). Connectives and quantifiers live in [notation.md](notation.md). Handwritten grids live in [handwriting.md](handwriting.md).

## Workflow

Copy and track:

```
- [ ] Read the lab handout end to end
- [ ] Map one report section to each exercise that asks for an answer
- [ ] Confirm the plan with the user unless they already said to write
- [ ] Scaffold report/assignmentN_report.tex from template.tex
- [ ] Fill the cover from student.md
- [ ] If the handout asks for handwriting, send a copy sheet and wait for the photo
- [ ] Write the English body; read notation.md before typesetting formulas
- [ ] xelatex twice; fix overfull boxes and unreadable figures
```

Do not start the PDF until the section plan matches the handout. If the report later drifts, cut invented sections first. A report that still has an empty `\shot` slot is not finished.

## Hard rules

- The PDF body is **English only**. The cover name defaults to `name`.
- One author. The cover has one row. The report stops after the last required exercise.
- Do not add a group roster, contribution scores, or a peer-review matrix. This template has no group assessment.
- Follow the handout. No extra exercises, no historical essay, and no code listings unless that handout asks for a tool run.
- Typeset truth tables. Handwriting applies only when the handout or the user asks for a handwritten page. Then follow [handwriting.md](handwriting.md). Do not invent a handwritten figure.
- Every truth-table cell is calculated. Keep the sheet's row order and column order.
- Use XeLaTeX. The template loads `fontspec` and `xeCJK`.
- Do not invent the student's name or ID. If [student.md](student.md) still says to ask, ask before compiling the final PDF.
- Do not commit or upload unless asked.

## Assignment map

This copy has no fixed handout, course offering, or due date. Read the handout the user provides and rebuild the section list.

Sections follow the handout, in that order. One section per exercise that asks for an answer.

- Translations into formulas keep the letters the sheet already chose.
- A truth-table exercise gets a typeset table and one sentence after it, unless the handout asks for handwriting.
- Quantified formulas are typed. Define each predicate in words once. Use the predicate names the sheet suggests, including parameterised predicates when the sheet asks for them.
- Where a sentence on the sheet is ambiguous, state the reading in one sentence, then give the formula.
- Pages with no further questions are omitted.

## Repo layout

```
labN/
  report/assignmentN_report.tex
  report/assignmentN_report.pdf
  figures/hand_<exercise>.png
```

Leave the handout PDF where it already is. Do not create `src/` or `artifacts/` for a written sheet. `figures/` holds only the photos the user sent back.

When asked to upload: the PDF only. Leave out `.log`, `.aux`, `.toc`, and `.cursor/`.

## Compile

From `report/`:

```bash
xelatex -interaction=nonstopmode -halt-on-error assignmentN_report.tex
xelatex -interaction=nonstopmode -halt-on-error assignmentN_report.tex
```

The second pass fills the table of contents. If MiKTeX is missing a package, install that package and recompile. The CJK font is `Microsoft YaHei` with `AutoFakeBold`.

After compile, check:

- cover name, student ID, and date
- the cover has no lab title, lecturer line, or submission line
- the section list matches the handout
- formulas use the sheet's connectives and typed quantifiers
- truth tables are complete and still readable
- there is no group section
- headings and tables have no serious overfull boxes

## Layout

Reuse the colours, fonts, title-page geometry, and `truthtable` environment from [template.tex](template.tex).

- A4, margin 2.4 cm, `parskip`, section colour `heading` `#1B365D`
- Title page: `\hypersetup{pageanchor=false}`, then turn page anchors back on after `\end{titlepage}`
- Header: course code, then `Assignment N`, on the left. The right side stays empty.
- Cover, top to bottom: course code, “Laboratory Report”, “Assignment N”, the name table, the date. No lab title under the assignment number. No course subtitle, lecturer line, or submission line.
- Tables use `[H]` so a truth table stays with the sentence that reads it
- A wide table uses `\resizebox{\textwidth}{!}{...}`. A narrow table stays at its natural width
- Formulas and truth tables follow [notation.md](notation.md)

Fill these macros before `\begin{document}`:

- `\coursenum` `\labnum` `\reportdate`
- `\studentname` `\studentid`

A submission page may call the uploaded file a draft until the student clicks submit. That status stays on the submission page. Do not print “draft” on the cover, and do not add a draft watermark.

## Prose

Academic, in the voice of a student who did the sheet:

- Complete sentences and short paragraphs. Answer the question, then stop.
- Put the formula in the same sentence as the English. Do not start every item with “The formula is”.
- The truth table is the argument. One sentence after it states what the columns show.
- Name a predicate in English once, then use the symbol.
- Few parentheses. A second sentence is better than a bracketed aside.
- Few dash characters. No em dashes, and no hyphenated line-breaks in headings.
- British spelling when the handout uses it.
- Mathematics in math mode, as `\(A \land B\)`, including formulas that sit inside a sentence.

## Answer shape

- **Translation.** The English sentence, then the formula.
- **Equivalence.** The formula, the truth table, then one sentence naming the columns that agree on every row.
- **Consistency.** The completed table, then the answer in the sheet's words. Consistent means the formulas can be true together. The same means the columns match on every row.
- **Quantifiers.** The predicate definitions, then one typed formula: `\forall x : U \cdot P(x)` or `\exists x : U \cdot P(x)`.
