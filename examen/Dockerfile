FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

ENV TZ=America/New_York

RUN apt-get update && \
    apt-get install -y apache2 php libapache2-mod-php tzdata

RUN apt-get install -y git

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

RUN rm -rf /var/www/html

RUN git clone https://gist.github.com/4371331.git /var/www/html/

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
