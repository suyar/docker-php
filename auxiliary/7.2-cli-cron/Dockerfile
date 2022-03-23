FROM suyar/php:7.2-cli

RUN set -eux; \
    apt-get update \
    && apt-get install -y cron \
    && rm -rf /var/lib/apt/lists/*

CMD ["cron","-f"]
