FROM suyar/php:7.0-cli

RUN set -eux; \
    apt-get update \
    && apt-get install -y cron \
    && rm -rf /var/lib/apt/lists/*

CMD ["cron","-f"]
