This is a basic template for a dissertation at the [TU Bergakademie Freiberg](https://tu-freiberg.de). It is based on the packages provided by [Thomas Benkert](https://tu-freiberg.de/presse/latex/tubaf-latex). No changes on the styles files (`*.sty`) or classes (`*.cls`) were made.


# What is provided?

 - Bibliography via `biblatex` and `biber`
 - Units via `siunitx`
 - Nomenclature via `nomencl`
 - Adding units to the nomenclature 
 - Appendix, incl. proper citing in the table of contents
 - Creating of to do notes and a to do list at the end
 - Upright mu symbol in combination with `siunitx`


# What should be noted?


__Include__

Using of `\include` commands, makes it easier to structure large text files. But it made it more difficult to add an appendix to the table of content. Therefor the `\addtocontents{toc}` is placed in a separate file.


__draft and syntaxonly__

In order to speed up the writing process you may use `draft`, which creates a drafted pdf (without images,...) or you just check if `pdflatex` compiles (no pdf is created) using `\syntaxonly`.


# Compiling latex in a bash

 #. `pdflatex <file>.tex`
 #. `makeindex <file>.nlo -s nomencl.ist -o <file>.nls`
 #. `pdflatex <file>.tex`


