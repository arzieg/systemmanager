# Define variables
APP_NAME := registeruser
SRC := $(shell find . -type f -name '*.go')

# Default target
all: release

# create release
release: $(SRC)
	CGO_ENABLED=0 go build -ldflags "-s -w" -o ../cmd/$(APP_NAME)

# Build the Go program
build: $(SRC)
	go build -o ../cmd/$(APP_NAME)

# Run tests
test:
	go test ./...

# Clean up build files
clean:
	rm -f ../cmd/$(APP_NAME)

# Run the application
run: build
	./$(APP_NAME)

# Specify phony targets
.PHONY: all build test clean run
