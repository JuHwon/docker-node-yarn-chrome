FROM node:latest

MAINTAINER juhwon

RUN npm install -g --progress=false yarn

# install chrome
RUN set -xe
RUN wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -
RUN echo "deb http://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google.list
RUN apt-get update -yqqq
RUN apt-get install -y google-chrome-stable
RUN apt-get install -y xvfb

WORKDIR /workspace
