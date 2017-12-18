# Rp20_1e
The TeX files that make up the Rp20 rulebook, the compiled pdf versions (one-page-per-sheet and two-page-per-sheet), and a makefile to create both pdf's.

The main TeX file is called Rp20_1e.tex, and the file that compiles the pdf this generates into a two-page-per-sheet form is called Rp20_1e_ebookform.pdf.

## Editing the TeX
If you are editing the TeX files, you should know that I've defined a few basic commands in Rp20_1e.tex, which any file included within it can use. A list follows:
- **\\stat{stat name}** - standardizes formatting for stats in formulas, enclosing them in squiggly braces and making the name small caps.
- **\\dice{number of dice}{sides to dice}** - prints out in d notation, e.g. \\dice{X}{Y} prints XdY
- **\\dicedrop{number of dice}{sides to dice}{number to drop}** - prints out in d notation, e.g. \\dice{X}{Y}{Z} prints XdYdZ, indicating you drop the Z lowest rolls.
- **\\dicekeep{number of dice}{sides to dice}{number to keep}** - prints out in d notation, e.g. \\dice{X}{Y}{Z} prints XdYkZ, indicating you keep the Z highest rolls.

Use these formulas within equations for good typesetting.

## Rebuilding pdf's
In order to rebuild, you actually require a few dependencies. These are mostly just to properly generate the two-page-per-sheet ebook form of the document with all hyperlinks working.
Prerequisites:
- java
- perl
- [pdfbox](https://sourceforge.net/projects/pdfbox/files/)
- pax LaTeX package. The instructions [here](https://bryanwweber.com/writing/personal/2014/04/13/use-pax-to-extract-and-include-links-from-external-pdf-files-in-latex-on-windows/ "Installing pax") will tell you how to set it up properly.

If you are trying to just generate the one-page-per-sheet pdf, you do not need all of these prerequisites, and can simply run
```
pdflatex Rp20_1e.tex
```

To generate all files, simply run
```
make
```

## Todo
- Go through and change all mathematical expressions to actual math.
- Consistently emphasize skills and special terms wherever they are mentioned in text
- Custom hyperref links whenever a section is mentioned for ease of navigation
- Index generation
- Crafting examples

## Changelog
All changes to this project will be logged in this section.

### [0.7.3] 2017-12-17
#### Added
- \\stat Command in main file for writing names of stats in equations.
- \\fauxsc command (courtesy of Steven Segletes) for bolded small caps.

#### Modified
- Attribute for the "Hide" skill changed to Int.
- Attacking section in Combat has codified rules for headshots and trying to shoot specific body parts.
- Items Loot and Crafting section has a final section for clarity.
- Buffs in the Items Loot and Crafting has codified giving an item hitpoints.
- Equations have all been made neat and standardized.

### [0.7.2] 2017-12-17
#### Added
- Items Loot and Crafting sections

#### Modified
- Performance skill can now give skill buffs to other characters
- other minor changes.

### [0.7.0] 2017-12-14
#### Added
- Files for all sections
- two-page-per-sheet ebook form
- makefile to easily create ebook form
