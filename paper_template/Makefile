source	:= 000_paper_template.tex

build:
	latexmk -pdf -bibtex -bibtex $(source)

watch:
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

mrpropper:
	git clean -fx

.PHONY: build watch clean cleaner gitclean mrpropper
