FROM golang:1.12.0-alpine3.9 AS builder

RUN mkdir /app

ADD . /app

WORKDIR /app

RUN go build -o main .

FROM scratch

COPY --from=builder app .

CMD ["./main"]

