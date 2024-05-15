FROM alpine:latest
LABEL org.opencontainers.image.authors="giterinhub@uplimit.com"
LABEL org.opencontainers.image.source=https://github.com/giterinhub/container-fundamentals
LABEL org.opencontainers.image.description="Containter Fundamentals - Static Website Image"
LABEL org.opencontainers.image.licenses=APACHE2
LABEL server_type=edge_server
# RUN apt update
# RUN apt install nginx -y
RUN apk add --no-cache nginx
COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www
EXPOSE 80
# CMD ["ls"]
CMD ["nginx", "-g", "daemon off;"]