FROM centos:7

RUN \
    yum -y install \
    httpd \
    php \
    php-cli \
    php-common \
    mod_ssl \
    openssl

RUN echo "<?php phpinfo();?>" > /var/www/html/hello.php

COPY ssl.conf /etc/httpd/conf.d/default.conf
COPY docker_apacher.cert /docker_apache.crt
COPY docker_apache.key /docker_apache.key

EXPOSE 443
CMD apachectl -DFOREGROUND