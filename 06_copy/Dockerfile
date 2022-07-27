# Example 6 - copy

FROM ubuntu:latest

# web server - nginx

RUN apt-get -y update && apt-get -y install nginx python3
#RUN yum -y update && yum -y install nginix python3

# path when using nginx image from docker hub /usr/share/nginx/html
# copy --chown <group1> SRC DEST
COPY index.html /var/www/html/index.nginx-debian.html

# Expose the port - http (80)
EXPOSE 80

# Expose the port - https (443)
EXPOSE 443/tcp

# start the nginx server
CMD ["nginx", "-g", "daemon off;"]


