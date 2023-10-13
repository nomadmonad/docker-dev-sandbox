# zenn-app/backend/Dockerfile
FROM ruby:3.2.2-alpine3.18

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

RUN mkdir /app
WORKDIR /app

ADD Gemfile /app/Gemfile

# RUN apk --update add build-base \
#     git \
#     libpq-dev \
#     sudo

RUN apk update && \
    apk upgrade && \
    apk add --no-cache \
    gcompat \
    linux-headers \
    libxml2-dev \
    make \
    gcc \
    libc-dev \
    bash \
    vim \
    git \
    nodejs \
    mysql-dev \
    tzdata \
    yarn && \
    apk add --virtual build-packs --no-cache \
    alpine-sdk \
    build-base \
    curl-dev \
    mysql-client


RUN gem install bundler:2.4.1 && \
    bundle install

ADD . /app