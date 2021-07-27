#! Version 0.2
FROM ubuntu:latest
MAINTAINER leiyu "927049198@qq.com"
RUN mkdir -p /var/www/html /usr/local/nginx/
RUN apt-get update
RUN apt-get install -y build-essential libpcre3 libpcre3-dev zlib1g-dev wget
RUN wget http://nginx.org/download/nginx-1.20.1.tar.gz && \
    tar -zxvf nginx-1.20.1.tar.gz && \
    cd nginx-1.20.1 && \
    ./configure --prefix=/usr/local/nginx/ --with-http_stub_status_module && \
    make && \
    make install && \
    cd / && \
    rm -r nginx-1.20.1 nginx-1.20.1.tar.gz

ENV PATH $PATH:/usr/local/nginx/sbin
WORKDIR /usr/local/nginx
EXPOSE 80
CMD ["nginx","-g","daemon off;"]

