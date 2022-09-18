TITLE := Funktechnik

# pandoc-include muss installiert sein damit dies funktioniert
FILTER := --filter pandoc-include

PANDOC := pandoc

OPTS_ALL := --toc \
            --top-level-division=chapter
PDF_OPTS := $(OPTS_ALL) \
            --default-image-extension=pdf
EPUB_OPTS := $(OPTS_ALL) \
            --default-image-extension=png \
            -t epub3 --toc-depth=1 \
            --epub-cover-image=cover.png

all: $(TITLE).pdf $(TITLE).epub $(TITLE).docx

Funktechnik.pdf:
	$(PANDOC) $(TITLE).md $(FILTER) $(PDF_OPTS) -o $@

Funktechnik.epub: 
	$(PANDOC) $(TITLE).md $(FILTER) $(EPUB_OPTS) -o $@

Funktechnik.docx:
	$(PANDOC) $(TITLE).md $(FILTER) $(PDF_OPTS) -o $@

Funktechnik.pptx:
	$(PANDOC) $(TITLE).md $(FILTER) $(PDF_OPTS) -o $@

clean:
	rm -f Funktechnik.pdf Funktechnik.docx Funktechnik.docx

