FROM alpine:3.10

RUN apk update \
		&& apk --update --no-cache add \
                grafana --repository http://dl-3.alpinelinux.org/alpine/edge/community/

EXPOSE 3000

COPY dashboards/ /usr/share/grafana/public/dashboards/

ENTRYPOINT ["/usr/sbin/grafana-server", "--homepath=/usr/share/grafana"]
