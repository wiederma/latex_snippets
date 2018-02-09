title  := 000_titlepage.tex
source := thesis_skeleton.tex

build:
	latexmk -pdf -bibtex -bibtex $(title)
	latexmk -pdf -bibtex -bibtex $(source)

watch:
	latexmk -pdf -bibtex -bibtex $(title)
	latexmk -pvc -pdf -bibtex -interaction=nonstopmode -bibtex $(source)

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
