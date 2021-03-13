FROM golang:latest AS builder

WORKDIR /work
COPY main.go .
COPY go.mod .
COPY go.sum .

RUN go build -o web .

EXPOSE 1323

CMD ["./web"]
