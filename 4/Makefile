SHELL := bash

all: front.png back.png

front.pdf: front.tex front.jpg
	latexmk --pdf $<

back.pdf: back.tex back.jpg
	latexmk --pdf $<

%.png: %.pdf
	convert -verbose -density 150 -trim $< -quality 100 -flatten -sharpen 0x1.0 $@
