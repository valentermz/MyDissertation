# Repository for my PhD Thesis

## Contents

- `my_theis.tex`: The master .tex file.
- `valente.sty`: Loader for common packages, theorem environments and custom commands.
- `valente-ref.bib`: Reference library.
- `cornell.cls`: The LaTeX class for Cornell theses and dissertations.

## Remarks

The class `cornell.cls` does not like inserting mathmode in `\title{}`, since it later calls ` \@title` to print the title in the abstract page (and the abstract title command is defined in a weird way). To bypass this, I have split text and mathmode and embedded it directly to the `cornell.cls` file tracked in this repo. **Make sure the titles are correct and matching!**!

The document class `cornell.cls` has the following bugs:

- The internal links in the Table of Contents do not link to the right page. This can be fixed by adding a `\cleardoublepage\phantomsection` before each "section" (abstract, bio sketch, ...).
- There's a name clash error with the definition of `\ifpdf`. I've added the line `\let\ifpdf\relax` to avoid it after the declaratin of the `\documentclass`.
- The double spacing affects matrix environments. These should be fixed on the class, but it can also be done by hand by adding `\renewcommand*{\arraystretch}{0.65}` or `\singlespacing` before the matrix environment.

I've created an environment `"metadata"` to include Keywords and MSC. The definition is in `valente.sty`. 
