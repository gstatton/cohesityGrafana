# Build image from nginx alpine image
FROM nginx:1.21.1-alpine

#copy ssl certificate
COPY ./certificate.crt /etc/ssl/certs/

#copy ssl private key
COPY ./nginx-private.key /etc/ssl/private/

# copy nginx conf
COPY ./nginx.conf /etc/nginx/

RUN apk --no-cache add bash=5.1.4-r0 && \
    apk -U upgrade && rm -rf /var/cache/apk/* && \
    addgroup -S cohesity && adduser -S cohesity -G cohesity && \
    chmod -R 777 /usr/share/nginx /etc/nginx/ /etc/ssl /var/cache/nginx /var/run /var/log/nginx &&  \
    sed -i 's/listen\(.*\)443;/listen 8443;/' /etc/nginx/conf.d/default.conf && \
    chown -R cohesity:cohesity /usr/share/nginx

USER cohesity

EXPOSE 443

CMD ["nginx", "-g", "daemon off;"]