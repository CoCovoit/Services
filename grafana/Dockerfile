FROM grafana/grafana

ENV GF_AUTH_ANONYMOUS_ENABLED "true"

EXPOSE 3000

WORKDIR /usr/share/grafana

# Adding all the files to docker image
ADD provisioning /etc/grafana/provisioning

# Adding config.ini to docker image
ADD config.ini /etc/grafana/grafana.ini
