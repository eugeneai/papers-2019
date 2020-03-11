.PHONY: clean run present

LATEXMK=latexmk -lualatex -latexoption=-shell-escape
BODY=talk-mda-ngs-2019-10-ru

present: $(BODY).pdf

$(BODY).pdf: $(BODY).tex
	$(LATEXMK) $<

mda-paper.pdf: mda-paper.tex
	$(LATEXMK) $<

run: mda-paper.tex
	$(LATEXMK) $<

clean:
	BIBINPUTS=$(BIBROOT) $(LATEXMK) -C
	rm -f *.{bbl,aux,ps,dvi,log,toc,out,vrb,snm,nav} *~ ~* *.bak *.synctex.* *.thm *-joined.pdf *.wbk *_latexmk *.fls
	# cd pics && make clean
