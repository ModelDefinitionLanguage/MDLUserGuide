# MDLUserGuide
MDL User Guide and Reference Manual

This online version of the MDL User Guide and Reference Manual is created using 
[RStudio's bookdown package](https://github.com/rstudio/bookdown).

Content is created within markdown .Rmd files where are then built into the book
using bookdown::render_book(input="Index.Rmd").

Each .Rmd is a chapter, with ONE top level markdown header (# Chapter title).
Subsections are labelled using second level markdown headers and so on... (## subsection, ### sub-sub-section).
MDL Block names are cross-referenced using the subsection name e.g. [`RANDOM_VARIABLE_DEFINITION`]. This allows
the user to jump to sections within the document.

The Index.Rmd controls settings for the book as a whole, including settings for HTML, PDF / LateX and ePub. It also
points to the bibliography file "references.bib".

Include graphics using the knitr::include_graphics(...) function rather than using markdown ![](<image file.png>).
This ensures that graphics are rendered equivalently across different book formats. Graphics properties can be 
managed via knitr R chunk options e.g. out.width="70%" etc.

HTML and LaTeX formatting can be used directly within the .Rmd files. These may result in different outcomes when
rendering for different outputs i.e. HTML or PDF so should be used sparingly. Please see 
[Yihui Xie's book on bookdown](https://bookdown.org/yihui/bookdown/markdown-extensions-by-bookdown.html)
for more details.
