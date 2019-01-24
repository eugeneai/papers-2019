.PHONY: clean run

LATEXMK=latexmk -lualatex -latexoption=-shell-escape

Cherkashin-LOD.pdf: Cherkashin-LOD.tex
	$(LATEXMK) $<

run: Cherkashin-LOD.pdf
	$(LATEXMK) $<

clean:
	BIBINPUTS=$(BIBROOT) $(LATEXMK) -C
	rm -f *.{bbl,aux,ps,dvi,log,toc,out,vrb,snm,nav} *~ ~* *.bak *.synctex.* *.thm *-joined.pdf *.wbk *_latexmk *.fls
	# cd pics && make clean
