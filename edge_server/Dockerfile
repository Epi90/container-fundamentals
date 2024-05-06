# use a lightweight base image - alpine fits good here (atleast google says that)
FROM alpine:latest

LABEL authors="lars ac"
LABEL server_type="edge_server"

# need apk, otherwise it doesnt work
RUN apk update
RUN apk add nginx

COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
