FROM golang:1.18-alpine

WORKDIR /app

RUN apk update && \
apk add --no-cache tzdata

COPY go.mod ./
COPY go.sum ./
RUN go mod download

COPY *.go ./

CMD [ "go","run","main.go" ]