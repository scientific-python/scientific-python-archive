build_dir := build
excluded := README.md invitees.md
sources := $(filter-out $(excluded),$(wildcard *.md))
reports = $(addprefix $(build_dir)/,$(sources:.md=.pdf))
vector_images = $(wildcard *.svg)
images := $(addprefix $(build_dir)/,$(vector_images:.svg=.png))

# Look up your bibliography style at https://www.zotero.org/styles
# Download the CSL file to the current directory and modify `bibstyle`
# below
bibstyle := ieee-with-url.csl

.PHONY: default
default: $(reports)

$(build_dir)/:
	mkdir -p $@

$(reports): $(build_dir)/%.pdf : %.md | $(images)
	# See https://pandoc.org/MANUAL.html#extensions for a list of extensions
	pandoc --from markdown+implicit_figures \
	       --include-in-header header.tex \
	       --toc --template tufte-template.tex \
	       --filter pandocCommentFilter.py \
	       -s -o $@ $<

$(images): $(build_dir)/%.png : %.svg
	-inkscape --export-png=$@ --export-dpi=300 $<

# Add the build directory as an order only prerequisite
$(foreach report,$(reports),$(eval $(report): | $(dir $(report))))
$(foreach image,$(images),$(eval $(image): | $(dir $(image))))

clean: $(build_dir)
	rm -rf $(build_dir)
