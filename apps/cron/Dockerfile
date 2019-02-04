FROM alpine

LABEL maintainer="Richard"

COPY script /bin/script

COPY root /var/spool/cron/crontabs/root

RUN chmod +x /bin/script

CMD crond -l 2 -f