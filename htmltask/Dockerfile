FROM ubuntu:latest
WORKDIR /var/www/html/
COPY index.html .
RUN apt-get update
RUN apt-get install -y sudo
RUN apt-get update && apt-get install -y tzdata
RUN apt-get update && apt-get install -y apache2
RUN apt-get update
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf
EXPOSE 80
RUN service apache2 restart
CMD apachectl -D FOREGROUND

