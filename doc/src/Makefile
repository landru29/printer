LATEX=pdflatex
DELETE=rm -f
MAIN=printer.tex

SRC= $(wildcard $(SRCFOLDER)/*.tex)
TARGET= $(MAIN:.tex=.pdf)

TARGET: $(SRC)
	$(LATEX) -output-directory ../. $(MAIN)
	pdftk ../../mecanical/aluminium-sheet/plate.pdf ../../mecanical/aluminium-sheet/y-belt-blocker.pdf ../../mecanical/aluminium-sheet/y-motor-bracket.pdf ../../mecanical/aluminium-sheet/y-stub-bracket.pdf ../../mecanical/aluminium-sheet/y-tensioner.pdf ../../mecanical/aluminium-sheet/z-motor-bracket.pdf ../../mecanical/assembly/body.pdf ../../mecanical/assembly/extruder.pdf ../../mecanical/assembly/head.pdf ../../mecanical/assembly/pulley-assembly.pdf ../../mecanical/bushing-bracket/y-bushing-bracket.pdf ../../mecanical/bushing-bracket/Y-motor-bracket.pdf ../../mecanical/head/cooler.pdf ../../mecanical/head/core.pdf ../../mecanical/head/head-assy.pdf ../../mecanical/head/heater.pdf ../../mecanical/machining/pulley-assembly.pdf cat output ../definition.pdf

clean:
	$(DELETE) ../printer.aux
	$(DELETE) ../printer.log

mrproper: clean
	$(DELETE) ../printer.pdf
