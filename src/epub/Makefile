top = $(shell git rev-parse --show-toplevel)
key = $(shell basename ${top})

all: build.md ${key}.epub

new: clean all

.PHONY: clean
clean:
	rm -f build.md ${key}.epub

build.md:
	book-binder start.yml "${top}/src/links.md" "build.md" "${top}/topics"

${key}.epub:
	pandoc-from-markdown-to-pdf "build.md" -o "${key}.epub"
