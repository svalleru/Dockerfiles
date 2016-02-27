FROM ubuntu:14.04
MAINTAINER Shan Valleru <shanvalleru@gmail.com>
RUN apt-get update
RUN apt-get -y install redis-server wget
RUN set -ex \
	&& wget https://www.dropbox.com/s/pr52n8d965rpv88/findsimi.tar.gz \
	&& tar zxvf findsimi.tar.gz \
	&& rm -rf findsimi.tar.gz

#Redis
#CMD ["redis-server", "/src/findsimi/redis/tindex/redis6360.conf"]
#CMD ["redis-server", "/src/findsimi/redis/gindex/redis6361.conf"]
#CMD ["redis-server", "/src/findsimi/redis/sindex/redis6362.conf"]
ADD ./redis.sh /redis.sh
CMD ["/redis.sh"]

#Revel
EXPOSE 800
CMD ["/run.sh"]
