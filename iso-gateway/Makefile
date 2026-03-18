APP_NAME=iso-gateway

.PHONY: build

build:
	go build -o bin/$(APP_NAME) ./cmd/server

test:
	go test ./...

e2e:
	go test ./test/e2e/...

lint:
	golangci-lint run

docker-build:
	docker build -t $(APP_NAME):latest .