FROM node:16

WORKDIR /app

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

RUN apt-get update -y && \
  apt-get upgrade -y && \
  npm install npm@6.14.4 && \
  npm install yarn && \
  yarn add ejs@3.0.1 &&\ 
  yarn add nuxt@2.0.0 &&\
  yarn add create-nuxt-app@2.15.0 &&\
  yarn add defu@3.1.0

ADD . /app
