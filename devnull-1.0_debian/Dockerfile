# installation of DaaS in container
FROM debian 

MAINTAINER boardstretcher version: 1.0

# update container
RUN apt-get -y update && apt-get -y upgrade

# install apps
RUN apt-get install -y nginx openbsd-inetd

# service configs
COPY nginx.conf /etc/nginx/nginx.conf
COPY inetd.conf /etc/inetd.conf

# ports
EXPOSE 9
EXPOSE 9/udp
EXPOSE 80

# start up nginx
CMD /usr/sbin/inetd && nginx
