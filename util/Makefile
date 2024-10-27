# Dies ist das Makefile um die verschiedenen Publikationsversionen des Verhaltenskodex
# der ZaPF

all: html wiki tex pdf

html: ../verhaltenskodex.md
	pandoc --standalone --metadata-file=./metadata.yml --number-sections --output=../versions/verhaltenskodex.html ../verhaltenskodex.md

tex: ../verhaltenskodex.md
	pandoc --standalone --metadata-file=./metadata.yml --number-sections --to=latex --output=../versions/verhaltenskodex.tex ../verhaltenskodex.md

pdf: ../versions/verhaltenskodex.tex
	pdflatex -output-directory ../versions verhaltenskodex.tex
	pdflatex -output-directory ../versions verhaltenskodex.tex
	rm -f ../versions/verhaltenskodex.{log,aux,out}

wiki: ../verhaltenskodex.md
	pandoc --to=mediawiki --lua-filter=remove-attr.lua --output=../versions/verhaltenskodex.wiki ../verhaltenskodex.md

clean:
	rm ../versions/*
