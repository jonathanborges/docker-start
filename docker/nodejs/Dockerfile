FROM ubuntu:latest

RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_7.x | bash /dev/stdin
RUN apt-get install -y nodejs \
    build-essential \
    git

RUN npm install -g nodemon

WORKDIR /var/www/backend

EXPOSE 3000

CMD ["nodemon", "-L", "server.js"]