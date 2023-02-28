DOCNAME=master
PDF_VIEWER=zathura

.PHONY:
	clean

all:
	make compile
	make clean

compile:
	lualatex -synctex=1 $(DOCNAME).tex
	lualatex -synctex=1 $(DOCNAME).tex
	lualatex -synctex=1 $(DOCNAME).tex

clean:
	rm -rf *.aux *.bcf *.fdb_latexmk *.fls *.log *.out *.toc

view:
	make compile
	make clean
	$(PDF_VIEWER) $(DOCNAME).pdf
