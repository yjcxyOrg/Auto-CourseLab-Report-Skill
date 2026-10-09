# Handwritten working

Use this only when the handout asks for handwriting, a scan, or a photo, or when the user asks for a handwritten page. Otherwise typeset the truth tables. See [notation.md](notation.md).

Do not draw a fake handwritten table in TikZ. Do not invent a handwritten figure the handout did not ask for.

## Copy sheet

Before the final PDF, send the user one copy sheet in the chat. One block per grid. Then stop and wait for the photos.

Each block has:

- the exercise number
- the column headers, in the handout's order
- every row, already filled with `T` and `F`

Use a plain monospaced grid, not LaTeX. Example shape:

```text
Exercise 5

A  B | A∧B | ¬A ∨ (A∧B) | A∧¬B | ¬(A∧¬B)
F  F |  F  |      T      |  F   |    T
F  T |  F  |      T      |  F   |    T
T  F |  F  |      F      |  T   |    F
T  T |  T  |      T      |  F   |    T
```

That sample is the shape only. Fill it from the real calculation. Tell the user to copy it by hand, photograph the page, and send the photo back. The surrounding English can be drafted while waiting. Leave a `\shot` slot for each missing photo, and do not treat the PDF as finished until those photos are in.

## After the photo comes back

Save it under `figures/hand_<exercise>.png`. Crop the margins and keep a small pad. The writing must stay readable at `\linewidth`.

Embed it next to the sentence that reads it:

```latex
\shot{../figures/hand_ex5.png}{Completed truth table for Exercise 5.}
```

`\shot` is defined in [template.tex](template.tex).

Check the photo against the copy sheet: same headers, same row order, same cells. If a cell disagrees, say which cell and wait for a new photo. Do not quietly typeset a replacement.
