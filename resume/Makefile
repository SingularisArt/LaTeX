DOCNAME=master
PDF_VIEWER=zathura

.PHONY:
	clean

all:
	make compile
	make clean

doall:
	make clean compile clean view

compile:
	pdflatex -synctex=1 $(DOCNAME).tex
	pdflatex -synctex=1 $(DOCNAME).tex
	pdflatex -synctex=1 $(DOCNAME).tex
	make clean

clean:
	rm -rf *.aux *.bcf *.fdb* *.fls *.log *.out *.toc *.synctex* *.tdo *.loe *.snm *.nav *.auxlock *.maf *.mtc* *.ptc *.bbl *.blg *blx.bib *.run.xml

view:
	make compile
	make clean
	$(PDF_VIEWER) $(DOCNAME).pdf
