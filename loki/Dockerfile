FROM grafana/loki

EXPOSE 3100

WORKDIR /etc/loki

COPY loki-config.yaml /etc/loki/loki-config.yaml

CMD ["loki", "--config.file=/etc/loki/loki-config.yaml"]
