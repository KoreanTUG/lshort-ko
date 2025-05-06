# lshort-ko


- Korean translation of "The Not So short Introduction to LaTeX2e"
  - Written by Tobias Oetiker, Hubert Partl, Irene Hyna and Elisabeth Schlegl
  - Version 6.4, March 09, 2021
  - Korean translation by Kangsoo Kim, In-Sung Cho.
- LaTeX2e 입문 - 144분동안 익히는 LaTeX2e
  - 김강수, 조인성 옮김.
  - 한국어판 2025, 2월 8일

## How to build

For Hangul characters, `lshort-ko` uses the KoPubWorld font which is not redistributable. To compile the document from the source code, you need to install the KoPubWorld truetype font (from [kopub website](http://www.kopus.org/biz/electronic/font.aspx)) by yourself. Otherwise comment out the lines for font setting in `kopubworldfont.sty` manually, and the resulting PDF file will contain UnFonts shipped in the TeXLive distribution.

### macOS/Linux

```bash
cd src
make
```

### Windows

```bash
xelatex lshort-ko.tex
komkindex -k -s kotex lshort-ko.idx
xelatex lshort-ko.tex
xelatex lshort-ko.tex
```

## License

- GNU General Public License.
- 한국어판 저작권: GNU 자유 문서 라이선스(FDL)
- Please refer to the page 2 of document.
