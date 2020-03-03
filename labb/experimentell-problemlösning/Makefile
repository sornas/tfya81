FILE_NAME = rapport
DIFF_STYLE = CCHANGEBAR

FLAGS = -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make

.PHONY: pdf open diff clean

pdf: $(FILE_NAME).pdf
diff: $(FILE_NAME)-diff.pdf

# CUSTOM BUILD RULES

# '$@' is a variable holding the name of the target and '$<' is a variable
# holding the (first) dependency of a rule. "raw2tex" and "dat2tex" are
# placeholders for whatever custom steps you might have.

%.tex: %.raw
	./raw2tex $< > $@

%.tex: %.dat
	./dat2tex $< > $@

# -pdf tells latexmk to generate PDF directly (instead of DVI).
# -pdflatex="" tells latexmk to call a specific backend with specific options.
# -use-make tells latexmk to call make for generating missing files.

# -interaction=nonstopmode keeps the pdflatex backend from stopping at a
# missing file reference and interactively asking for an alternative.

# [ -f $(FILE_NAME)-old.tex ] && $(error $(FILE_NAME)-old.tex does not exist)
# if -f $(FILE_NAME)-old.tex; then $(error $(FILE_NAME)-old.tex does not exist); fi;

$(FILE_NAME).pdf: $(FILE_NAME).tex data/
	latexmk $(FLAGS) $<

open: $(FILE_NAME).pdf
	open $<

$(FILE_NAME)-diff.pdf: data/
	latexdiff -t $(DIFF_STYLE) $(FILE_NAME)-old.tex $(FILE_NAME).tex > $(FILE_NAME)-diff.tex
	latexmk $(FLAGS) $(FILE_NAME)-diff.tex

clean:
	latexmk -CA
	rm -f *.cb
	rm -f *.cb2

