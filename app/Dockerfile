FROM ubuntu:23.04

LABEL author="GSM"

WORKDIR /var/www/html

RUN apt update \
    && apt install git -y \
    && apt install apache2 -y

RUN git clone https://github.com/josejuansanchez/2048.git /app \
    && mv /app/* /var/www/html \
    && rm -rf /app

EXPOSE 80

CMD [ "/usr/sbin/apache2ctl", "-D", "FOREGROUNG" ]