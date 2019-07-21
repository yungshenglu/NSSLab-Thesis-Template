.PHONY: all clean dist print

P = main
O = outline

default : $P.ps  

nobibtex : $(wildcard *.tex Chapters/*.tex Bib/*.bib Figures/*.eps)
	latex  $P < /dev/null || $(RM) $@
	latex  $P < /dev/null || $(RM) $@	

$P.dvi	: $(wildcard *.tex Chapters/*.tex Bib/*.bib Figures/*.eps)
	latex  $P < /dev/null || $(RM) $@
	bibtex $P < /dev/null || $(RM) $@
	latex  $P < /dev/null || $(RM) $@
	latex  $P < /dev/null || $(RM) $@

pdf  : $P.ps
	ps2pdf -sPAPERSIZE=letter -dEmbedAllFonts=true -dSubsetFonts=true -dEPSCrop=true ./$P.ps ./$P.pdf
#	dvipdf  ./$P
#	dvipdfm -p letter -o ./$P.pdf ./$P.dvi

outline	: $(wildcard *.tex Chapters/*.tex Bib/*.bib Figures/*.eps)
	latex  $O < /dev/null || $(RM) $@
	bibtex $O < /dev/null || $(RM) $@
	latex  $O < /dev/null || $(RM) $@
	latex  $O < /dev/null || $(RM) $@
	dvips -tletter -Ppdf $O.dvi -o $O.ps
	ps2pdf -sPAPERSIZE=letter $O.ps $O.pdf

$P.ps	: $P.dvi
	dvips -tletter -Ppdf $P.dvi -o $P.ps

$P.ps.gz: $P.ps
	$(RM) $P.ps.gz
	gzip -9 < $P.ps > $P.ps.gz


print:	$P.ps 

dist:	$P.ps.gz

clean:
	$(RM) $P.log $P.aux $P.bbl $P.blg $P.dvi $P.ps $P.ps.gz texput.log $P.out .*.un~ $O.log $O.aux $O.bbl $O.blg $O.dvi $O.ps $O.ps.gz $O.out 
