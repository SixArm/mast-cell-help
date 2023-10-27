top = $(shell git rev-parse --show-toplevel)
key = $(shell basename ${top})

all: build.md ${key}.epub ${key}.pdf

new: clean all

.PHONY: clean
clean:
	rm -f build.md ${key}.epub ${key}.pdf

build.md:
	book-binder start.yml links.md build.md ${top}/topics

${key}.epub:
	pandoc-from-markdown-to-epub build.md -o ${key}.epub

${key}.pdf:
	pandoc-from-markdown-to-pdf build.md -o ${key}.pdf
