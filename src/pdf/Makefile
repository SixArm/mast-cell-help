top = $(shell git rev-parse --show-toplevel)
key = $(shell basename ${top})

midput="tmp/midput.md"
output="tmp/${key}.pdf"
pandoc="pandoc-from-markdown-to-pdf"

all: ${midput} ${output}

new: clean all

.PHONY: clean
clean:
	rm -f ${midput} ${output}

${midput}:
	book-binder start.yml "../links.md" ${midput} "${top}/topics"

${output}:
	${pandoc} ${midput} -o ${output}
