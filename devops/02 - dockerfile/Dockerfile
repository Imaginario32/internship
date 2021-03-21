#Use a smaller image
FROM node:lts-slim as base
#Create app deirectory
WORKDIR /usr/src/app
#Install npm
RUN npm install
#Install software
RUN apt-get update && apt-get install -y openssh-server apache2 supervisor
#Create a directory
RUN mkdir -p /var/run/sshd /var/log/supervisor
#Copy conf
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
#Open port
EXPOSE 3000
CMD ["/usr/bin/supervisord"]
#Copy files
COPY example/package*.json example/app.js ./
