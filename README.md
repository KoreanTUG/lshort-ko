# lshort-ko


- Korean translation of "The Not So short Introduction to LaTeX2e"
  - Written by Tobias Oetiker, Hubert Partl, Irene Hyna and Elisabeth Schlegl
  - Version 6.4, March 09, 2021
  - Korean translation by Kangsoo Kim, In-Sung Cho.
- LaTeX2e 입문 - 143분동안 익히는 LaTeX2e
  - 김강수, 조인성 옮김.
  - 한국어판 2021, 3월 16일

## How to build

- `pygmentize` (python-pygments) is required.
- `lshort-ko` uses the KoPubWorld font for Hangul characters, which is not redistributable. Install the KoPub World truetype font (downloadable from [kopub website](http://www.kopus.org/biz/electronic/font.aspx)) by yourself and uncomment the font setting lines in `kopubworldfonts.sty`. Otherwise the result PDF file contains Un Fonts shipped in TeX Live.

### macOS/Linux

```bash
cd src
make
```

### Windows

```bash
xelatex --shell-escape lshort-ko.tex
komkindex -k -s kotex lshort-ko.idx
xelatex --shell-escape lshort-ko.tex
xelatex --shell-escape lshort-ko.tex
```

## License

- GNU General Public License.
- 한국어판 저작권: GNU 자유 문서 라이선스(FDL)
- Please refer to page 2 of document.
