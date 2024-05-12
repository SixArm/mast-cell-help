top = $(shell git rev-parse --show-toplevel)
key = $(shell basename ${top})
bin="bin"

all: build

clear: clean all

.PHONY: clean
clean:
	"${bin}/clean"

.PHONY: build
build:
	"${bin}/build"
	npm run build
