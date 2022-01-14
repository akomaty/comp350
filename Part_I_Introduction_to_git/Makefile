# Created by Andre Anjos <andre.anjos@idiap.ch>
# Mon 11 May 2015 12:22:13 CEST

B := main.tex

%.pdf: %.tex
	pdflatex --shell-escape $<
	pdflatex --shell-escape $<

all: large

b: $(B:%.tex=%.pdf)

once:
	pdflatex --shell-escape $(b)

.PHONY: abstract clean mrproper

abstract:
	$(MAKE) -C abstract

clean:
	@rm -f *~ */*~ *.log *.pdf *.aux *.nav *.out *.snm *.toc

mrproper: clean
	$(MAKE) -C abstract mrproper
	@rm -vf $(LARGE:%.tex=%.pdf)
	@rm -vf $(MEDIUM:%.tex=%.pdf)
	@rm -vf $(KEYNOTE:%.tex=%.pdf)
