FROM nginx:latest

# Update "./certificate.crt" with path of certificate
COPY /Users/gregstatton/Desktop/Grafana/certificate.crt /etc/ssl/certs/

# Update "./nginx-private.key" with path of certificate key
COPY /Users/gregstatton/Desktop/Grafana/key.key /etc/ssl/private/

COPY /Users/gregstatton/Desktop/Grafana/nginx.conf /etc/nginx/

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]
