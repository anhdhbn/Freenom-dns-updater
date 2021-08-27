FROM python:3-alpine

WORKDIR /opt/freenom_dns_updater

COPY . .

RUN python3 -m pip install --no-cache-dir . && /opt/freenom_dns_updater

ENTRYPOINT [ "fdu" ]

CMD [ "process", "-i", "-c", "-r", "-t", "3600", "/etc/freenom.yml" ]
