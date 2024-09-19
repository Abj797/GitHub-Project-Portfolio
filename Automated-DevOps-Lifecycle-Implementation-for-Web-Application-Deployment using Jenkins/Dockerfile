FROM ubuntu 
RUN apt-get update
RUN apt-get install apache2 -y
COPY . /var/www/html
EXPOSE 80
CMD "/usr/sbin/apache2ctl", "-D", "FOREGROUND"
