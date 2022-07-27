# From nginx
# Dockerizing
# Development environnment same as production ennvironment
# 1. to craet a new image for your application
# 2. Customize any publicly available image
# Base image
FROM ubuntu:latest

# APT-GET UPDATE AND INSTALL NGINX
RUN apt-get -y update && apt-get -y install -y nginx

#Add user nginx and group nginx
RUN useradd -ms /bin/bash nginx
# Default path - /var/www/html

# Chown - Chnage Ownership - by def using root user
ADD --chown=nginx:nginx index.html /var/www/html/index.nginx-debian.html
# Ports it will communnicate to external network - no UDP
EXPOSE 80/tcp
EXPOSE 443/tcp

# start nginx web server
CMD ["nginx","-g","daemon off"]



