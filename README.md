# typographydefaults

This is a LaTeX package that makes selecting quality font defaults easy and painless. Instead of fiddling with multiple options or doing things by trial and error, an author using this package can just choose a period in type design and be done with it. Currently supported are:

| Period    | Type family        |
|-----------|--------------------|
| Medieval  | Junicode           |
| Humanist  | Centaur MT Std     |
| Garalde   | Adobe Garamond Pro |
| Realist   | Fairfield LT Std   |
| Modern    | Didot LT Std       |
| Mechanist | Caecilia LT Std    |
| Millenial | Warnock Pro        |
| Grotesque | Grotesque MT Std   |
| Geometric | Futura Std         |

There are also two fonts to choose for monospaced text sections:

| “Period”   | Font               |
|------------|--------------------|
| Typewriter | Prestige Elite Std |
| Programmer | PragmataPro        |

## Requirements

* [XeTeX](http://xetex.sourceforge.net/) and XeLaTeX
* [CTAN](http://www.ctan.org/) packages:
    * pdftexcmds
    * kvoptions
    * xunicode
    * xunicode-addon
    * fontspec
    * unicode-math
    * microtype
* [Adobe Font Folio](http://www.adobe.com/products/fontfolio.html)
* [Junicode](http://junicode.sourceforge.net/)
* [Essential PragmataPro](http://www.fsd.it/fonts/pragmatapro.htm)

## Installation instructions

If you have a recent distribution of [TeX Live](https://www.tug.org/texlive/), you most likely have all the needed CTAN packages, as well as XeTeX and XeLaTeX. If you don't, check you operating system package manager, or [install manually those first](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages).

For Adobe Font Folio, you or (most likely) your employer only need to have bought and installed the font families listed above. Install all variants of the given family. A [font manager](http://fontmanager.github.io/) might be a good option to help you on this.

Once the requirements are in place and assuming you're using TeX Live on Linux, you can install by:

```shell
cd ~/texmf/tex/latex
git clone git://github.com/kerscher/typographydefaults ./typographydefaults
texhash
```

If you're using other TeX distribution, check on its documentation how to install a package or [read more about it here](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages).

## How to use it

In the preamble, add the package and declare its options:

```latex
\usepackage[ text = medieval
           , mono = programmer
           ]{typographydefaults}
```

Valid options for ```text``` are listed on the table above. To use them change the one you want to lowercase as in the example. For monospaced fonts, use the ```mono``` parameter. The order of parameters is irrelevant.

## Licence

This package uses a 2-clause BSD-like licence. You can check it [here](LICENCE.md)