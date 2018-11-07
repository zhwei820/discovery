
.PHONY: all test clean build install gen_api

GOFLAGS ?= $(GOFLAGS:)

all: install test

build_docker: build docker_image

build:
	go build $(GOFLAGS) ./.

docker_image:
	docker build . -t discovery:latest

bench: install
	go test -run=NONE -bench=. $(GOFLAGS) ./...

clean:
	go clean $(GOFLAGS) -i ./...
