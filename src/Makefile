# Makefile
# lshort-ko 2019
LATEX = xelatex
MAKEINDEX = komkindex
FILE = lshort-ko
OUTDIR = build/

default: pdf

all: pdf

batch: once pdf silent distro clean

mkdirbuild:
	if [ -d "./build" ]; then echo "directory build exists"; else mkdir build; fi

pdf: mkdirbuild
	${LATEX} -shell-escape -synctex=1 -output-directory=${OUTDIR} ${FILE}
	${MAKEINDEX} -k -s kotex -o ${OUTDIR}${FILE}.ind -t ${OUTDIR}${FILE}.ilg ${OUTDIR}${FILE}.idx
	${LATEX} -shell-escape -synctex=1 -output-directory=${OUTDIR} ${FILE}

once: mkdirbuild
	${LATEX} -shell-escape -synctex=1 -output-directory=build/ ${FILE}

makeindex: mkdirbuild
	${MAKEINDEX} -k -s kotex -o ${OUTDIR}${FILE}.ind -t ${OUTDIR}${FILE}.ilg ${OUTDIR}${FILE}.idx

silent:	mkdirbuild
	${LATEX} -shell-escape -synctex=1 -interaction=nonstopmode -output-directory=${OUTDIR} ${FILE} | grep -q "Warning|Error" || echo "error or warning detected" ;

clean: 
	if [ -d "${OUTDIR}" ]; then rm -rf ${OUTDIR}; fi
	if [ -d "_minted-${FILE}" ]; then rm -rf _minted-${FILE}; fi

copypdf:
	if [ -f ${OUTDIR}${FILE}.pdf ]; then cp ${OUTDIR}${FILE}.pdf ./ && cp ${OUTDIR}${FILE}.synctex.gz ./ ; fi

distro:
	if [ -d "./distro" ]; then rm -rf distro && mkdir distro ; else mkdir distro ; fi 
	cd distro && mkdir src && cp ../Makefile src/ && cp ../*.tex src/ && cp ../*.sty src/ && tar zcvf ${FILE}-src.tar.gz src/ && cd .. 
	if [ -f "build/lshort-ko.pdf" ]; then cp build/lshort-ko.pdf distro/ ; fi
