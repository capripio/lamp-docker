FROM ubuntu:17.10

RUN apt-get update
RUN apt-get -y dist-upgrade
RUN apt-get autoremove
RUN apt-get install -y apache2
RUN service apache2 start
RUN apt-get install -y php libapache2-mod-php php-mysql
COPY apache2.conf /etc/apache2/
COPY init.sh /init.sh

ENTRYPOINT [ "/init.sh" ]