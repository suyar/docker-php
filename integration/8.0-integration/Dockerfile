FROM suyar/php:8.0-fpm

RUN set -eux; \
    apt-get update \
    && apt-get install -y supervisor cron \
    && rm -rf /var/lib/apt/lists/*

COPY ./docker-integration.ini /etc/supervisor/conf.d/

RUN chmod -R 644 /etc/supervisor/conf.d/*.ini

CMD ["supervisord","-c","/etc/supervisor/supervisord.conf","-n"]
