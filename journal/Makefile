DOCNAME=master
PDF_VIEWER=zathura

.PHONY:
	clean

all:
	make compile
	make clean

compile:
	pdflatex --extra-mem-top=100000000 -enable-write18 $(DOCNAME).tex
	pdflatex --extra-mem-top=100000000 -enable-write18 $(DOCNAME).tex
	pdflatex --extra-mem-top=100000000 -enable-write18 $(DOCNAME).tex

clean:
	rm -rf *.aux *.bcf *.fdb_latexmk *.fls *.log *.out *.toc *.synctex*

view:
	make compile
	make clean
	$(PDF_VIEWER) $(DOCNAME).pdf
