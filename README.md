# Repository for my PhD Thesis

## Contents

- my_theis.tex: The master .tex file.
- valente.sty: Loader for common packages, theorem environments and custom commands.
- valente-ref.bib: Reference library.
- cornell.cls: The LaTeX class for Cornell theses and dissertations.

## Remarks

The cornell class does not like inserting mathmode in \title, since it later calls \@title to print the title in the abstract page . To bypass this, I have split text and mathmode and embedded it directly to the tracked cornell.cls file. **Make sure the titles are correct and matching!**!
