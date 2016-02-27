FROM ubuntu:14.04
MAINTAINER Shan Valleru <shanvalleru@gmail.com>
RUN apt-get update
RUN apt-get -y install redis-server wget
RUN set -ex \
	&& wget https://www.dropbox.com/s/pr52n8d965rpv88/findsimi.tar.gz \
	&& tar zxvf findsimi.tar.gz \
	&& rm -rf findsimi.tar.gz

#Redis & Revel
ADD ./redis.sh /redis.sh
EXPOSE 800
CMD /redis.sh && /run.sh
