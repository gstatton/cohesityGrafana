FROM grafana/grafana:8.0.6

USER root

# refresh apk repos and get latest
RUN apk -U upgrade && rm -rf /var/cache/apk/*

RUN addgroup -S cohesity && adduser -S cohesity -G cohesity

USER cohesity

EXPOSE 3000