FROM ubuntu:14.04
MAINTAINER Shan Valleru <shanvalleru@gmail.com>
RUN apt-get update

#install git & golang
RUN apt-get install -y git golang
RUN mkdir /golang
ENV GOPATH /golang
ENV PATH $GOPATH/bin:$PATH

#Install revel
RUN go get github.com/revel/revel
RUN go get github.com/revel/cmd/revel
