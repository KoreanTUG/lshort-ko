# lshort-ko


- Korean translation of "The Not So short Introduction to LaTeX2e"
  - Written by Tobias Oetiker, Hubert Partl, Irene Hyna and Elisabeth Schlegl
  - Version 6.2, February 28, 2018
  - Korean translation by Kang-su Kim, In-sung Cho.
- LaTeX2e 입문 - 143분동안 익히는 LaTeX2e
  - 김강수, 조인성 옮김.
  - 한국어판 2019, 2019년 2월 9일
  - TeX Live 2020으로 컴파일되도록 스타일 수정, 2020년 4월 2일

## How to build

- `pygmentize` (python-pygments) is required.
- `lshort-ko` uses the [KoPubWorld](http://www.kopus.org/biz/electronic/font.aspx) font, but it's not redistributable. Instead the Nanum or Un font can be used alternatively. Uncomment the font setting lines in `kopubworldfonts.sty` to use either one. Install the TrueType font to use Nanum.

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
