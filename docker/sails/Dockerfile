FROM node:5.1.1-slim

RUN apt-get update && apt-get install -q -y supervisor
RUN npm install -g sails@0.11.3 grunt bower
RUN mkdir /server

# Define mountable directories.
VOLUME ["/server"]

# Define working directory.
WORKDIR /server

# Expose ports.
EXPOSE 1337

ADD etc /etc
CMD ["/usr/bin/supervisord", "-n"]
