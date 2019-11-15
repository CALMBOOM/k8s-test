FROM golang:1.12-alpine as builder
WORKDIR /home/go
COPY hello.go /home/go
RUN go mod init hello \
    && go build .


FROM alpine:latest
WORKDIR /home/go
COPY --from=builder /home/go/hello .

