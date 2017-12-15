# Rp20_1e
The TeX files that make up the Rp20 rulebook, the compiled pdf versions (one-page-per-sheet and two-page-per-sheet), and a makefile to create both pdf's.

In order to rebuild, you actually require a few dependencies. These are mostly just to properly generate the two-page-per-sheet ebook form of the document with all hyperlinks working.
Prerequisites:
-java
-perl
-[pdfbox](https://sourceforge.net/projects/pdfbox/files/)
-pax LaTeX package. The instructions [here](https://bryanwweber.com/writing/personal/2014/04/13/use-pax-to-extract-and-include-links-from-external-pdf-files-in-latex-on-windows/ "Installing pax") will tell you how to set it up properly.

If you are trying to just generate the one-page-per-sheet pdf, you do not need all of these prerequisites, and can simply run
```
pdflatex Rp20_1e.tex
```

To generate all files, simply run
```
make
```

##Todo
-Go through and change all mathematical expressions to actual math.
-Consistently emphasize skills and special terms wherever they are mentioned in text
-Custom hyperref links whenever a section is mentioned for ease of navigation
-Index generation

##Changelog
All changes to this project will be logged in this section.

### [0.7.0] 2017-12-14
####Added
-Files for all sections
-two-page-per-sheet ebook form
-makefile to easily create ebook form
