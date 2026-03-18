# ---- Build Stage ----
FROM golang:1.25.7-alpine AS builder

WORKDIR /app

COPY go.mod ./
RUN go mod download

COPY . .

RUN go build -o iso-gateway ./cmd/server

# ---- Final Stage ----
FROM gcr.io/distroless/static

WORKDIR /

COPY --from=builder /app/iso-gateway /iso-gateway
COPY configs/config.yaml /configs/config.yaml

EXPOSE 8080

ENTRYPOINT ["/iso-gateway"]