title  := 000_titlepage
source := thesis_skeleton

build:
	latexmk -pdf -bibtex -bibtex $(title).tex
	latexmk -pdf -bibtex -bibtex $(source).tex

watch:
	latexmk -pdf -bibtex -bibtex $(title).tex
	latexmk -pvc -pdf -bibtex -interaction=nonstopmode -bibtex $(source).tex

# remove all temp files
clean:
	latexmk -c

# remove also result files (PDF etc)
cleaner:
	latexmk -C

# removes all unversioned files!
gitclean:
	git clean -fx

mrproper:
	git clean -fx

spell-check:
	hunspell -d de_DE -t **/*.tex

.PHONY: build watch clean cleaner gitclean mrproper spell-check
