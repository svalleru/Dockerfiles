FROM ubuntu:14.04
MAINTAINER Shan Valleru <shanvalleru@gmail.com>
RUN apt-get update
RUN apt-get install -y wget bash-completion vim

#Install python-2.7.10
RUN apt-get -y install build-essential checkinstall libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev
RUN set -ex \
	&& wget https://www.python.org/ftp/python/2.7.10/Python-2.7.10.tgz \
	&& tar xzf Python-2.7.10.tgz \
	&& cd Python-2.7.10 \
	&& ./configure \
	&& make install \
        && cd .. \
	&& rm -rf Python-2.7.10*
