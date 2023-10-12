# zenn-app/backend/Dockerfile
FROM ruby:3.2.2-alpine3.18

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

RUN mkdir /app
WORKDIR /app

ADD Gemfile /app/Gemfile

RUN apk --update install build-base \
    libpq-dev \
    sudo

RUN gem install bundler:2.4.1 && \
    bundle install

ADD . /app