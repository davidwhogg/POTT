# NEED PATSUBST
# NEED pott.tex dependency

RM = /bin/rm -f
DVIPS = dvips -Ppdf # The -Ppdf option includes fonts but can screw up on
                    # included graphics.  Use with extreme prejudice.
PS2PDF = ps2pdf

.SUFFIXES: .tex .dvi .ps .pdf

ALLFILES = 105_gondola.pdf 125_sailing.pdf 160_barefoot_waterski.pdf 171_sliding_cue.pdf 173_pool_clack.pdf 188_tides.pdf \
	201_discharge.pdf 202_relativity.pdf 266_uniform_current.pdf 280_mirror.pdf 210_high_tension.pdf 265_poynting.pdf\
	324_gravity_specific_heat.pdf 381_hot_water.pdf 390_clouds.pdf \
	402_catastrophe.pdf 403_magnetic_angular.pdf 405_angular_resolution.pdf 410_double_sho.pdf 440_unlikely.pdf 490_solids.pdf \
	901_twins.pdf 908_elevator.pdf 930_equivalence.pdf 943_invisible_gw.pdf 971_21cm.pdf 999_nobel.pdf
all: $(ALLFILES) clean

.tex.pdf: $*.tex pott.tex
	pdflatex $*
	pdflatex $*
	pdflatex $*

clean:
	$(RM) *.log *.aux *.dvi *.toc *.bbl *.blg

spotless: clean
	$(RM) *.pdf *.ps
