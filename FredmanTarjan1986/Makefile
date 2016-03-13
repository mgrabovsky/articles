BIB = biber
LTX = xelatex -shell-escape
CHAPTERS = 01-introduction 02-f-heaps 03-variants 04-shortest-paths 05-mst 06-results

main.pdf: references.bib main.ltx $(CHAPTERS:=.tex)
	$(LTX) main.ltx
	$(BIB) main
	$(LTX) main.ltx

FredmanTarjan1986.pdf: main.pdf
	mv -f $^ $@

clean:
	-$(RM) *.{aux,bbl,bcf,blg,log,out,run.xml,toc}

distclean: clean
	-$(RM) FredmanTarjan1986.pdf

.PHONY: clean

