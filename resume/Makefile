TEX = xelatex
FLAGS = -interaction=nonstopmode -halt-on-error
SRC = resume.tex
PDF = resume.pdf

.PHONY: all clean view publish

all: $(PDF)

$(PDF): $(SRC)
	$(TEX) $(FLAGS) $(SRC)
	$(TEX) $(FLAGS) $(SRC)

clean:
	rm -f *.aux *.log *.out *.synctex.gz *.xdv

view: $(PDF)
	xdg-open $(PDF) >/dev/null 2>&1 &

# Copy the built PDF up to the site root so the homepage can link to it.
publish: $(PDF)
	cp $(PDF) ../assets/resume.pdf
