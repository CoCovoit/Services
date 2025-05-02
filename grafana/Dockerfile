FROM grafana/grafana

EXPOSE 3000

WORKDIR /usr/share/grafana

COPY grafana.ini /usr/share/grafana/conf/grafana.ini

CMD ["grafana-server", "--config=/usr/share/grafana/conf/grafana.ini"]
