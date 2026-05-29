FROM ubuntu:22.04
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y \
    apache2 \
    php \
    libapache2-mod-php \
    curl \
    && rm -rf /var/lib/apt/lists/*

RUN rm -f /var/www/html/index.html && \
    curl -sSL https://raw.github.com/antonechete/pps_devsecops/main/ejercicio1/index.php -o /var/www/html/index.php

EXPOSE 80
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
