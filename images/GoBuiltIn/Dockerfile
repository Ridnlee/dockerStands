FROM golang:1.10 as builder

WORKDIR /go/src/test

COPY . .

RUN CGO_ENABLED=0 GOOS=linux go build .

FROM scratch

WORKDIR /root/
COPY --from=builder /go/src/test .
CMD ["./test"]
