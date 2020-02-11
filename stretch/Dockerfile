FROM python:3.7-stretch

RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get -y install \
    postgresql-client \
    && rm -rf /var/lib/apt/lists/* \
    && mkdir /app

WORKDIR /app

COPY entrypoint.sh /

ENTRYPOINT /entrypoint.sh

CMD ["sh", "-c", "python", "$APP_NAME"]