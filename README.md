# lshort-ko


- Korean translation of "The Not So short Introduction to LaTeX2e"
  - Written by Tobias Oetiker, Hubert Partl, Irene Hyna and Elisabeth Schlegl
  - Version 6.2, February 28, 2018
  - Korean translation by Kang-su Kim, In-sung Cho.
- LaTeX2e 입문 - 143분동안 익히는 LaTeX2e
  - 김강수, 조인성 옮김.
  - 한국어판 2019, 2019년 2월 9일

## How to build

- `pygmentize` (python-pygments) is required.
- `lshort-ko` uses [KoPubWorld](http://www.kopus.org/biz/electronic/font.aspx) font. Since the font is not redistributable, the source given here will use Nanum font.

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