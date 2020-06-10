FROM nginx

RUN useradd jael

COPY fruit /usr/share/nginx/html

ENV file docker

RUN echo "$file" > /usr/share/nginx/html/file.html

WORKDIR /usr/share/nginx/html

EXPOSE 90

LABEL version="1.0.1"

USER jael

RUN echo "i'm $(whoami)" >/tmp/iam.html

USER root 

RUN cp /tmp/iam.html /usr/share/nginx/html/docker.html

VOLUME /tmp/docker

CMD nginx -g 'daemon off;'