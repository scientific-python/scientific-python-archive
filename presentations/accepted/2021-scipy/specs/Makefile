BUILDDIR  = _build

all: clean specs.pdf

clean:
	-rm -rf $(BUILDDIR)/*

$(BUILDDIR):
	mkdir -p $@

$(BUILDDIR)/%.tex: %.md $(BUILDDIR)
	cp macros.tex $(BUILDDIR)/.
	cp -r _static $(BUILDDIR)/.
	pandoc -t beamer -V aspectratio=169 --highlight=pygments --slide-level=2 -o $@ $< -s

%.pdf: $(BUILDDIR)/%.tex
	cd $(BUILDDIR) && latexmk -pdfxe $(<F)
	cp $(BUILDDIR)/$(@) .
