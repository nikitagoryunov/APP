FROM centos:8
RUN dnf update -y
RUN dnf install -y nginx php php-fpm php-mysqli
RUN dnf clean all
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
RUN mkdir /run/php-fpm
COPY ./html/APP/APP/index.html /usr/share/nginx/html/index.html
CMD php-fpm -D ; nginx
EXPOSE 80
