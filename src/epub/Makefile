top = $(shell git rev-parse --show-toplevel)
key = $(shell basename ${top})

all: tmp/build.md tmp/${key}.epub

new: clean all

.PHONY: clean
clean:
	rm -f build.md ${key}.epub

tmp/build.md:
	book-binder start.yml "${top}/src/links.md" "tmp/build.md" "${top}/topics"

tmp/${key}.epub:
	pandoc-from-markdown-to-epub "tmp/build.md" -o "tmp/${key}.epub"
