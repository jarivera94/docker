FROM centos:7

RUN yum -y install httpd -y


COPY index.php /var/www/html
#use add to download resources from internet
#ADD index /var/www/html

CMD apachectl -DFOREGROUND