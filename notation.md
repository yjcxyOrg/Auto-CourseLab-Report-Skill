# Logic notation

Use the handout's symbols, in math mode.

| Handout | LaTeX |
|---|---|
| ∧ | `\land` |
| ∨ | `\lor` |
| ¬ | `\neg` |
| → | `\rightarrow` |
| ⇔ | `\Leftrightarrow` |
| ∀ | `\forall` |
| ∃ | `\exists` |

Typed quantifiers, as printed on the sheet:

```latex
\(\forall x : U \cdot P(x)\)
\(\exists x : U \cdot P(x)\)
```

`U` is the universe. Keep the colon and the centred dot. Implication is `\rightarrow`, matching the sheet's single arrow. Equivalence is `\Leftrightarrow`.

## Predicates

`\pname` is defined in [template.tex](template.tex). It keeps a hyphen as a hyphen:

```latex
\(\pname{is-tall}(x)\)
```

Give the English reading once, then use `\pname`. Prefer the names the sheet lists. Where the sheet has already chosen letters (`A`, `B`, `P`, `W`, `t`), keep those letters.

## Truth values

Use \(T\) and \(F\). Keep the sheet's row order and column order. On a two-atom table that order is FF, FT, TF, TT. On the three-atom table, use the eight rows the sheet prints.

A blank cell on the sheet is a cell to calculate. Do not add rows the sheet does not print.

## Tables

Typeset a truth table with `truthtable`. It takes a caption and a column spec. The first row is the header. Handwriting is only for a sheet that asks for it. See [handwriting.md](handwriting.md).

```latex
\begin{truthtable}{Caption naming the exercise.}{ccc}
\(A\) & \(B\) & \(A \land B\) \\
\midrule
\(F\) & \(F\) & \(F\) \\
\(F\) & \(T\) & \(F\) \\
\(T\) & \(F\) & \(F\) \\
\(T\) & \(T\) & \(T\) \\
\end{truthtable}
```

This sample shows the shape only. It is not an answer to paste into an exercise.

For a header row of many formulas, scale that table down. Do not use this form for a table that already fits.

```latex
\begin{table}[H]
  \centering
  \caption{Caption naming the exercise.}
  \renewcommand{\arraystretch}{1.22}
  \resizebox{\textwidth}{!}{%
  \begin{tabular}{cccccc}
    \toprule
    \rowcolor{rowalt}
    \(A\) & \(B\) & \(A \land B\) & \(\neg A\) & \(A \lor B\) & \(\neg B\) \\
    \midrule
    \(F\) & \(F\) & \(F\) & \(T\) & \(F\) & \(T\) \\
    \bottomrule
  \end{tabular}}
\end{table}
```

One sentence after the table is enough. For equivalence, name the columns that match on every row. For consistency, say whether any row makes the relevant formulas true together.
