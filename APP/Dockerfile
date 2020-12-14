FROM centos:8
RUN dnf update -y
RUN dnf install -y nginx php php-fpm php-mysqli
RUN dnf clean all
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
RUN mkdir /run/php-fpm
COPY root/html/APP/APP/ /usr/share/nginx/html/
CMD php-fpm -D ; nginx
EXPOSE 80
