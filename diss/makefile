# The M/MP/MF options here create phony Makefile rules in $*.deps, which are
# picked up the the -include *.deps below. The end result is that latexmk
# dynamically generates the list of *all* dependencies for each document it
# builds, so that 'make' will attempt to rebuild the document whenever any of
# those dependencies change.
#
%.pdf: %.tex
	latexmk -lualatex -M -MP -MF $*.deps $<

clean:
	latexmk -C

count:
	detex diss.tex | tr -cd '0-9A-Za-z \n' | wc -w

-include *.depsb
