FROM ubuntu:latest

RUN apt-get update && apt-get install -y nginx

RUN apt-get clean \
    && rm -rf /etc/nginx/sites-enabled/default \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ADD ./sites/default.conf /etc/nginx/sites-enabled/default.conf
ADD ./nginx.conf /etc/nginx/nginx.conf

EXPOSE 80 443

CMD ["nginx"]