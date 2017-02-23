# ```typographydefaults```

This is a LuaLaTeX and XeLaTeX package that makes selecting quality open-source font family defaults easy and painless. Instead of fiddling with multiple options or doing things by trial and error, an author using this package can just choose a “period”, loosely based around [British standards for type classification](http://luc.devroye.org/britishstandards.html). Currently supported are:

| Period          | Type family                                                        | Parameter            |
|-----------------|--------------------------------------------------------------------|----------------------|
| Medieval        | [Junicode](http://junicode.sourceforge.net/)                       | ```medieval```       |
| Humanist        | [Coelacanth](https://fontlibrary.org/en/font/coelacanth)           | ```humanist```       |
| Garalde         | [EB Garamond](http://www.georgduffner.at/ebgaramond/)              | ```garalde```        |
| Realist         | [PT Serif](http://www.paratype.com/public/)                        | ```realist```        |
| Didone          | [CMU Serif](http://cm-unicode.sourceforge.net/)                    | ```didone```         |
| Mechanistic     | [CMU Concrete](http://cm-unicode.sourceforge.net/)                 | ```mechanistic```    |
| Lineal Humanist | [Source Sans Pro](http://adobe-fonts.github.io/source-sans-pro/)   | ```linealhumanist``` |
| Grotesque       | [HK Grotesk](https://fontlibrary.org/en/font/hk-grotesk)           | ```grotesque```      |
| Geometric       | [Orkney](https://fontlibrary.org/en/font/orkney)                   | ```geometric```      |

The alternative _realist_ term was chosen for what are now commonly called _transitional_ faces. Likewise, despite grotesques and geometrics being lineals, it only makes sense to distinguish humanist from its lineal counterpart due to ambiguity.

There are four styles to choose for monospaced text sections:

| “Period”             | Font                                                      | parameter        |
|----------------------|-----------------------------------------------------------|------------------|
| Typewriter           | [CMU Typewriter Text](http://cm-unicode.sourceforge.net/) | ```typewriter``` |
| Programmer Slender   | [Iosevka](https://be5invis.github.io/Iosevka/)            | ```slender```    |
| Programmer Wide      | [Monoid](http://larsenwork.com/monoid/)                   | ```wide```       |
| Symbolic typesetting | [GNU Unifont](http://www.unifoundry.com/unifont.html)     | ```symbolic```   |

Such monospaced styles have no correspondence in classification that I'm aware of. _Typewriter_ are graphic faces that resemble imprinting ink on paper through a mechanical typewriter. _Programmer_ faces have: a combination of differentiation between similar symbols, such as between ```0``` and ```O```; contrast and shapes suitable for use in “inverted” colours of light text over dark backgrounds; and in some specimens ligatures for common glyph combinations that occur in computer code. Lastly, a _symbolic_ monospaced has high coverage of [Unicode](http://www.unicode.org/standard/standard.html) code points, making it suitable for typesetting scientific material with unusual glyphs.

I recommend _typewriter_ for technical document citations, _programmer_ on either option for source code sections and _symbolic_ for Unicode-heavy typesetting such as [Agda](http://wiki.portal.chalmers.se/agda/pmwiki.php) proofs.

## Requirements

* [LuaTeX](http://luatex.org/) and LuaLaTeX, or [XeTeX](http://xetex.sourceforge.net/) and XeLaTeX
* [CTAN](http://www.ctan.org/) packages:
    * pdftexcmds
    * kvoptions
    * fontspec
    * unicode-math
    * microtype
    
For font downloads use the links provided on the table above.

## Installation instructions

If you have a recent distribution of [TeX Live](https://www.tug.org/texlive/), you most likely have all needed CTAN packages, as well as LuaTeX, LuaLaTeX, XeTeX and XeLaTeX. If you don't, check you operating system package manager, or [install manually those first](https://en.wikibooks.org/wiki/LaTeX/Installing_Extra_Packages).

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
\usepackage[ text = mechanistic
           , mono = typewriter
           ]{typographydefaults}
```

Valid options for ```text``` and ```mono``` are listed on the table above.
Order of parameters is irrelevant.

## Licence

This package uses a 2-clause BSD-like licence. You can check it [here](LICENCE.md).
