XELATEXARGS = -file-line-error -halt-on-error
IMAGES = remotecontrol-top.jpeg auto-shutdown-timeout-hack.jpeg

.PHONY: clean all

all: cockshock2.pdf

cockshock2.pdf: cockshock2.tex $(IMAGES) cockshock2.bbl
	xelatex $(XELATEXARGS) cockshock2.tex; xelatex $(XELATEXARGS) cockshock2.tex

cockshock.bbl: cockshock2.tex $(IMAGES) cockshock2.bib
	xelatex $(XELATEXARGS) cockshock2.tex; bibtex lospre; rm cockshock2.pdf

