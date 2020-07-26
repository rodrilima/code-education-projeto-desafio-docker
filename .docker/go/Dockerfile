FROM golang:1.15rc1-alpine3.12 as builder

COPY . /go/src/main

WORKDIR /go/src/main

RUN go build main.go

FROM scratch

WORKDIR /app

COPY --from=builder /go/src/main .

ENTRYPOINT ["./main"]
