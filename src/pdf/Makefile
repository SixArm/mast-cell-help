top = $(shell git rev-parse --show-toplevel)
key = $(shell basename ${top})

all: tmp/build.md tmp/${key}.pdf

new: clean all

.PHONY: clean
clean:
	rm -f build.md ${key}.pdf

tmp/build.md:
	book-binder start.yml "${top}/src/links.md" "tmp/build.md" "${top}/topics"

tmp/${key}.pdf:
	pandoc-from-markdown-to-pdf "tmp/build.md" -o "tmp/${key}.pdf"
