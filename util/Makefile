# Dies ist das Makefile um die verschiedenen Publikationsversionen des Verhaltenskodex
# der ZaPF zu erzeugen

all: html tex pdf wiki

html: ../verhaltenskodex.rst
	rst2html ../verhaltenskodex.rst > ../versions/verhaltenskodex.html

tex: ../verhaltenskodex.rst
	rst2latex --documentclass=scrartcl --documentoptions=12pt,oneside --stylesheet=./preamble.tex --embed-stylesheet --latex-preamble= ../verhaltenskodex.rst > ../versions/verhaltenskodex.tex

pdf: ../versions/verhaltenskodex.tex
	pdflatex -output-directory ../versions verhaltenskodex.tex
	pdflatex -output-directory ../versions verhaltenskodex.tex
	rm ../versions/verhaltenskodex.{log,aux,out}

wiki: ../verhaltenskodex.rst
	./rst2wiki/rst2wiki.py ../verhaltenskodex.rst > ../versions/verhaltenskodex.wiki

clean:
	rm ../versions/*
