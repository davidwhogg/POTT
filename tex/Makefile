# NEED PATSUBST
# NEED pott.tex dependency

RM = /bin/rm -f
DVIPS = dvips -Ppdf # The -Ppdf option includes fonts but can screw up on
                    # included graphics.  Use with extreme prejudice.
PS2PDF = ps2pdf

.SUFFIXES: .tex .dvi .ps .pdf

ALLFILES = 171_sliding_cue.pdf 266_uniform_current.pdf 410_double_sho.pdf 943_invisible_gw.pdf
all: $(ALLFILES) clean

.tex.pdf:
	pdflatex $*
	pdflatex $*
	pdflatex $*

clean:
	$(RM) *.log *.aux *.dvi *.toc *.bbl *.blg

spotless: clean
	$(RM) *.pdf *.ps
