FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y cron && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY scripts/ /scripts/
RUN chmod +x /scripts/*.sh

RUN crontab /scripts/crontab.txt

RUN touch /var/log/cron.log

CMD ["cron", "-f"]