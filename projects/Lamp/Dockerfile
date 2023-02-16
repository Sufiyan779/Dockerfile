FROM ubuntu:22.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt install -y tcl
RUN apt update && apt install apache2 -y
RUN apt install php -y
RUN apt install php-dev -y
RUN apt install libapache2-mod-php -y
RUN apt-get install -y php-common
RUN apt-get install -y php-mysql
RUN apt install -y php-curl
RUN apt install -y php-json
RUN apt-get install -y php-common
RUN apt-get install -y php-mbstring
# RUN mkdir /var/www/html
# RUN chown -R $USER:$USER /var/www/html
COPY ./phpinfo /etc/apache2/sites-available/html.conf
COPY ./html /var/www/html/index.html
COPY ./dir /etc/apache2/mods-enabled/dir.conf
COPY ./info /var/www/html/info.php
COPY ./todo_list.php /var/www/html/todo_list.php
#RUN systemctl reload apache2
EXPOSE 80
CMD ["apachectl", "-D", "FOREGROUND"]



