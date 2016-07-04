#Tennant.Family LEMPServer Dockerfile
FROM debian:latest
Maintainer Ben Tennant "ben@tennant.family"

RUN apt-get update
RUN apt-get -y install php5-fpm php5-mysql php-apc php5-imap php5-mcrypt php5-curl php5-gd php5-json
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server
RUN apt-get -y install nginx

ADD nginx_default.conf /etc/nginx/sites-available/default
RUN echo "cgi.fix_pathinfo = 0;" >> /etc/php5/fpm/php.ini
RUN mkdir -p /var/www && chown -R www-data:www-data /var/www

EXPOSE 80


