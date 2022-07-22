# ----------------------------------
# Pterodactyl Custom
# Environment: Linux
# Minimum Panel Version: 0.6.0
# ----------------------------------
FROM alpine:3.16

MAINTAINER Michael Johnson-Moore, <mtjohnson47@gmail.com>

RUN apk add --no-cache --update libssl1.0 libunwind icu \
    && adduser --disabled-password --home /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY ./entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
