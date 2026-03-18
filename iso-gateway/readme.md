- Makefile

    build → compiles binary
    test → unit tests
    e2e → integration tests
    lint → code quality
    docker-build → container image

- Dockerfile
    multi stage image
        smaller image and secure

- golangci-lint config
    enforce clean,safe, idiomatic go code.
    golangci.yaml

- add Github Actions CI  -> .github/workflows/ci.yml
    Automates :
        linting
        sesting
        build validation
        docker build