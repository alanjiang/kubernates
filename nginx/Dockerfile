FROM ${prefix}/nginx:1.11.6-alpine

LABEL maintainer="jiangpeng@126.com"


COPY 1.tar.gz /var/www/1.tar.gz

COPY 2.tar.gz /var/www/2.tar.gz

RUN cd /var/www/ \

    && tar -zxvf 1.tar.gz \
    && tar -zxvf 2.tar.gz \
    && rm -rf 1.tar.gz \
    && rm -rf 2.tar.gz
   

#CMD ["nginx", "-g", "daemon off;"]
