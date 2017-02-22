# typographydefaults

This is a LaTeX package that makes selecting quality open-source font defaults easy and painless. Instead of fiddling with multiple options or doing things by trial and error, an author using this package can just choose a period in type design and be done with it. Currently supported are:

| Period    | Type family                                                        | Parameter       |
|-----------|--------------------------------------------------------------------|-----------------|
| Medieval  | [Junicode](http://junicode.sourceforge.net/)                       | ```medieval```  |
| Humanist  | [Coelacanth](https://fontlibrary.org/en/font/coelacanth)           | ```humanist```  |
| Garalde   | [EB Garamond](http://www.georgduffner.at/ebgaramond/)              | ```garalde```   |
| Realist   | [PT Serif](http://www.paratype.com/public/)                        | ```realist```   |
| Modern    | [CMU Serif](http://cm-unicode.sourceforge.net/)                    | ```modern```    |
| Mechanist | [CMU Concrete](http://cm-unicode.sourceforge.net/)                 | ```mechanist``` |
| Millenial | [Source Serif Pro](http://adobe-fonts.github.io/source-serif-pro/) | ```millenial``` |
| Grotesque | [HK Grotesk](https://fontlibrary.org/en/font/hk-grotesk)           | ```grotesque``` |
| Geometric | [Orkney](https://fontlibrary.org/en/font/orkney)                   | ```geometric``` |

There are also two fonts to choose for monospaced text sections:

| “Period”             | Font                                                      | parameter        |
|----------------------|-----------------------------------------------------------|------------------|
| Typewriter           | [CMU Typewriter Text](http://cm-unicode.sourceforge.net/) | ```typewriter``` |
| Programmer Slender   | [Iosevka](https://be5invis.github.io/Iosevka/)            | ```slender```    |
| Programmer Wide      | [Monoid](http://larsenwork.com/monoid/)                   | ```wide```       |
| Symbolic typesetting | [GNU Unifont](http://www.unifoundry.com/unifont.html)     | ```symbolic```   |

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
    
For font downloads use the links provided on the table above.

## Installation instructions

If you have a recent distribution of [TeX Live](https://www.tug.org/texlive/), you most likely have all needed CTAN packages, as well as XeTeX and XeLaTeX. If you don't, check you operating system package manager, or [install manually those first](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages).

Installing fonts on every major operating system can be done easily by opening the archives provided by foundry or distributors and simply double-clicking on each font to add it. There are better ways, but this is easy and compatible across most environments.

Once requirements are in place and assuming you're using TeX Live on Linux, you can install by:

```shell
cd ~/texmf/tex/latex
git clone git://github.com/kerscher/typographydefaults ./typographydefaults
texhash
```

If you're using other TeX distribution, check on its documentation how to install packages or [read more about it here](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages).

## How to use it

On your preamble, add this package and declare its options. For example:

```latex
\usepackage[ text = mechanist
           , mono = typewriter
           ]{typographydefaults}
```

Valid options for ```text``` and ```mono``` are listed on the table above.
Order of parameters is irrelevant.

## Licence

This package uses a 2-clause BSD-like licence. You can check it [here](LICENCE.md)
