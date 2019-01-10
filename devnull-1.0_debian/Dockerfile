# installation of DaaS in container
FROM debian 

MAINTAINER boardstretcher version: 1.0

# update container and install apps
RUN apt-get -y update && apt-get -y upgrade && apt-get install -y nginx openbsd-inetd

# service configs
COPY nginx.conf /etc/nginx/nginx.conf
COPY inetd.conf /etc/inetd.conf

# ports
EXPOSE 9 9/udp 80

# start up nginx
CMD /usr/sbin/inetd && nginx
