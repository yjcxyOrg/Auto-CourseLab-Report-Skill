<p align="center">
  <a href="README.md"><b>English</b></a>
  &nbsp;·&nbsp;
  <a href="README.zh-CN.md">中文</a>
</p>

<h1 align="center">Auto Course Lab Report</h1>

<p align="center">
  A Cursor skill for one author's course laboratory report, set in XeLaTeX.<br>
  No AI trace. Concise answers. Every required exercise, in handout order.
</p>

<p align="center">
  <img alt="XeLaTeX" src="https://img.shields.io/badge/XeLaTeX-report-1B365D">
  <img alt="One author" src="https://img.shields.io/badge/author-one-2B6CB0">
  <img alt="Report language" src="https://img.shields.io/badge/body-English-1F2933">
</p>

<p align="center">
  <a href="#preview">Preview</a>
  &nbsp;·&nbsp;
  <a href="#quick-start">Quick start</a>
  &nbsp;·&nbsp;
  <a href="#layout">Layout</a>
</p>

<br>

## Why this shape

<table>
<tr>
<td width="33%" valign="top">

### No AI trace

The voice is a student who did the sheet. The formula sits in the same sentence as the English. A truth table or a parse tree is followed by one sentence. No overview, no extra exercise, no closing essay.

</td>
<td width="33%" valign="top">

### Concise

Each exercise answers the question and then stops. A predicate is named in English once, then used as a symbol.

</td>
<td width="33%" valign="top">

### Complete

Every exercise that asks for an answer gets its own section, in the handout's order. Letters, connectives, predicate names, and truth-table rows stay as the sheet printed them.

</td>
</tr>
</table>

## Preview

The empty template is the left cover. The finished assignment is everything to its right. Only the author's name and the two ID numbers are covered. The course code in the header stays visible.

<table>
<tr>
<td width="50%">

**Empty template**
Placeholders: `COURSE`, `name`, `000000000`.

<img src="docs/template-cover.png" alt="Empty template cover">

</td>
<td width="50%">

**Finished cover**
Name and both ID numbers are black.

<img src="docs/finished-cover.png" alt="Finished cover">

</td>
</tr>
<tr>
<td width="50%">

**Contents**
One line for each required exercise.

<img src="docs/finished-contents.png" alt="Finished contents">

</td>
<td width="50%">

**Exercises 1 to 6**
A predicate, named once, then a typed formula.

<img src="docs/finished-exercises.png" alt="Exercises 1 to 6">

</td>
</tr>
</table>

**Exercises 12 and 13.** The parse tree is drawn, then one sentence names the root and the two subtrees.

<img src="docs/finished-trees.png" alt="Parse trees for exercises 12 and 13" width="49%">

## Quick start

1. Place this folder where Cursor loads project skills.
2. Give it the handout and ask for the report.
3. Replace the cover name. The student ID is requested before the final PDF, and it is not invented.
4. From `report/`, compile twice with XeLaTeX. The second pass fills the contents.

Handwriting is used only when the handout asks for a photo. Otherwise the table is typeset.

## Layout

| File | Role |
|---|---|
| `SKILL.md` | Workflow and rules |
| `template.tex` | Cover, header, truth tables |
| `template.pdf` | The empty template, compiled |
| `student.md` | Name and student ID |
| `notation.md` | Connectives, quantifiers, table shape |
| `handwriting.md` | Photo step, only when a page must be handwritten |
| `docs/` | The figures above |

<p align="center">
  <a href="README.zh-CN.md">阅读中文说明</a>
</p>
