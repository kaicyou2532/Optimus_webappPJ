FROM golang:1.10.2

COPY src/api /go/src/api/

WORKDIR /go/src/api/

RUN \
  apt-get update && \
  apt-get install -y \
  git && \
  go get -u github.com/codegangsta/gin && \
  go get -u github.com/golang/dep/cmd/dep && \
  dep ensure

CMD gin -i run