WHAT = lab_notes

best: $(WHAT).tex
	pdflatex $(WHAT).tex
	bibtex $(WHAT)
	pdflatex $(WHAT).tex
	pdflatex $(WHAT).tex
	evince $(WHAT).pdf

fast: $(WHAT).tex
	pdflatex $(WHAT).tex
	open -a Skim.app $(WHAT).pdf

$(WHAT): $(WHAT).tex $(WHAT).bib
	pdflatex $(WHAT).tex

#	dvips -t letter $(WHAT).dvi
#	ps2pdf $(WHAT).ps

xbest:
	taskkill /f /im acrobat.exe ; echo OK
	pdflatex $(WHAT).tex
	bibtex $(WHAT)
	pdflatex $(WHAT).tex
	pdflatex $(WHAT).tex
	explorer $(WHAT).pdf ; echo OK

xfast:
	taskkill /f /im acrobat.exe ; echo OK
	pdflatex $(WHAT).tex
	explorer $(WHAT).pdf ; echo OK

clean:
	rm *.log *.aux *.bbl *.blg $(WHAT).dvi $(WHAT).ps $(WHAT).pdf
