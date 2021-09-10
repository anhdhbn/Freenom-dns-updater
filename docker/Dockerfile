FROM python:3.8-alpine

RUN apk add --no-cache zlib openssl-dev binutils

WORKDIR /opt/freenom_dns_updater

COPY . .

RUN python3 -m pip install --no-cache-dir . && rm -rf /opt/freenom_dns_updater

ENTRYPOINT [ "fdu" ]

CMD [ "process", "-i", "-c", "-t", "60", "/etc/freenom.yml" ]
