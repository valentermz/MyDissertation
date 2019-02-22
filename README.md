# Repository for my PhD Thesis

This is the doctoral dissertation I wrote at Cornell University. The final pdf can be found here: [doi: 10.7298/X48913Z1](https://doi.org/10.7298/X48913Z1).

### Contents

- `my_theis.tex`: The master .tex file.
- `valente.sty`: Loader for common packages, theorem environments and custom commands.
- `ref.bib`: Reference library.
- `my_thesis.bbl`: Manually modified bbl file.
- `cornell.cls`: The LaTeX class for Cornell theses and dissertations.

### Remarks

The document class `cornell.cls` has the following bugs:

- The internal links in the Table of Contents do not link to the right page. This can be fixed by adding a `\cleardoublepage\phantomsection` before each "section" (abstract, bio sketch, ...).
- There's a name clash error with the definition of `\ifpdf`. I've added the line `\let\ifpdf\relax` to avoid it after the declaratin of the `\documentclass`.
- The double spacing affects matrix environments. These should be fixed on the class, but it can also be done by hand by adding `\renewcommand*{\arraystretch}{0.65}` or `\singlespacing` before the matrix environment.
- The front cover and the first page of the first chapter are labled as "Page 1". Add `\setcounter{page}{-3}` at the front cover to avoid a warning.
- Several fonts are not available in the required sizes. The package `lmodern` fixes some issues but not all.

I've created an environment `"metadata"` to include Keywords and MSC. The definition is in `valente.sty`. 
