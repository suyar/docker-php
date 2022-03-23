FROM suyar/php:8.1-cli

RUN set -eux; \
    apt-get update \
    && apt-get install -y cron \
    && rm -rf /var/lib/apt/lists/*

CMD ["cron","-f"]
