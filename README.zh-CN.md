<p align="center">
  <a href="README.md">English</a>
  &nbsp;·&nbsp;
  <a href="README.zh-CN.md"><b>中文</b></a>
</p>

<h1 align="center">课程实验报告</h1>

<p align="center">
  面向单人课程实验报告的 Cursor 技能，用 XeLaTeX 排版。<br>
  无 AI 痕迹。答完即止。讲义要求的每一题，按原顺序写完。
</p>

<p align="center">
  <img alt="XeLaTeX" src="https://img.shields.io/badge/XeLaTeX-report-1B365D">
  <img alt="单人" src="https://img.shields.io/badge/author-one-2B6CB0">
  <img alt="正文语言" src="https://img.shields.io/badge/body-English-1F2933">
</p>

<p align="center">
  <a href="#preview">预览</a>
  &nbsp;·&nbsp;
  <a href="#quick-start">开始使用</a>
  &nbsp;·&nbsp;
  <a href="#layout">文件</a>
</p>

<br>

## 为什么是这个样子

<table>
<tr>
<td width="33%" valign="top">

### 无 AI 痕迹

正文是做完题目的学生口吻。公式写在同一句英文里。真值表或语法树后面只留一句说明。不加综述，不加讲义没要求的题，不加收尾议论。

</td>
<td width="33%" valign="top">

### 简洁

每题答完即止。谓词用英文说明一次，之后只用符号。

</td>
<td width="33%" valign="top">

### 要求齐全

讲义里要求作答的每一题都有一节，顺序与讲义一致。字母、联结词、谓词名和真值表行序都沿用讲义。

</td>
</tr>
</table>

## 预览

左边是空白模板封面，右边以及下面是成稿。只涂黑了作者姓名和两个学号。页眉里的课程号仍然可见。

<table>
<tr>
<td width="50%">

**空白模板**
占位为 `COURSE`、`name`、`000000000`。

<img src="docs/template-cover.png" alt="空白模板封面">

</td>
<td width="50%">

**成稿封面**
姓名和两个学号为黑块。

<img src="docs/finished-cover.png" alt="成稿封面">

</td>
</tr>
<tr>
<td width="50%">

**目录**
每道要求作答的题一行。

<img src="docs/finished-contents.png" alt="成稿目录">

</td>
<td width="50%">

**第 1 至 6 题**
谓词说明一次，随后写入公式。

<img src="docs/finished-exercises.png" alt="第 1 至 6 题">

</td>
</tr>
</table>

**第 12 与 13 题。** 先画语法树，再用一句话指出根和左右子树。

<img src="docs/finished-trees.png" alt="第 12 与 13 题的语法树" width="49%">

## 开始使用

1. 把本目录放到 Cursor 会加载的项目技能路径下。
2. 给出讲义，并要求写报告。
3. 替换封面姓名。学号在定稿前询问，不会编造。
4. 在 `report/` 目录用 XeLaTeX 编译两遍。第二遍填上目录。

只有讲义要求交照片时才用手写，其余表格都排版。

## 文件

| 文件 | 作用 |
|---|---|
| `SKILL.md` | 流程与规则 |
| `template.tex` | 封面、页眉、真值表 |
| `template.pdf` | 编译好的空白模板 |
| `student.md` | 姓名与学号 |
| `notation.md` | 联结词、量词、表格形式 |
| `handwriting.md` | 仅在要求手写时使用的拍照步骤 |
| `docs/` | 上面这些图 |

<p align="center">
  <a href="README.md">Read this page in English</a>
</p>
