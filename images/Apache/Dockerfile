FROM centos:7

LABEL version="1.0.0"
LABEL description="my first image"

RUN yum -y install httpd -y

#that indicates where we are working docker 
WORKDIR /var/www/html

COPY index.php html

#create environment variables
ENV content="html"

RUN echo "$content"  > content.html
#use add to download resources from internet
#ADD index /var/www/html
RUN echo "$(whoami)" > user1.html

RUN useradd jael
USER jael

RUN echo "$(whoami)" > /tmp/user2.html
USER root
RUN cp /tmp/user2.html /var/www/html/.

VOLUME /var/www/htmlset

#expose another port
#EXPOSE 81

COPY run.sh  /run.sh
CMD sh /run.sh