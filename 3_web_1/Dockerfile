FROM ubuntu:latest
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt install -y apache2 \
    vim \
    less \
    php \
    libapache2-mod-php
RUN ln -snf /usr/share/zoneinfo/Europe/Madrid /etc/localtime && echo Europe/Madrid > /etc/timezone
LABEL zona_horaria="Madrid/Europa"

ENV WEB_PORT=80
EXPOSE $WEB_PORT

COPY execute.sh /
ENTRYPOINT bash ./execute.sh