title  := 000_titlepage
source := thesis_skeleton

build:
	latexmk -pdf -bibtex -bibtex $(title).tex
	latexmk -pdf -bibtex -bibtex $(source).tex

watch:
	latexmk -pdf -bibtex -bibtex $(title).tex
	latexmk -pvc -pdf -bibtex -interaction=nonstopmode -bibtex $(source).tex

clean:
	latexmk -c

gitclean:
	git clean -fx

mrproper:
	git clean -fx

spell-check:
	hunspell -d de_DE -t **/*.tex

.PHONY: build watch clean gitclean mrproper spell-check
