# NEED PATSUBST
# NEED pott.tex dependency

RM = /bin/rm -f
DVIPS = dvips -Ppdf # The -Ppdf option includes fonts but can screw up on
                    # included graphics.  Use with extreme prejudice.
PS2PDF = ps2pdf

.SUFFIXES: .tex .dvi .ps .pdf

ALLFILES = 105_gondola.pdf 125_sailing.pdf 160_barefoot_waterski.pdf 171_sliding_cue.pdf 188_tides.pdf \
	201_discharge.pdf 266_uniform_current.pdf 280_mirror.pdf \
	381_hot_water.pdf \
	402_catastrophe.pdf 410_double_sho.pdf \
	908_elevator.pdf 943_invisible_gw.pdf 971_21cm.pdf
all: $(ALLFILES) clean

.tex.pdf: $*.tex pott.tex
	pdflatex $*
	pdflatex $*
	pdflatex $*

clean:
	$(RM) *.log *.aux *.dvi *.toc *.bbl *.blg

spotless: clean
	$(RM) *.pdf *.ps
