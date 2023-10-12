# zenn-app/backend/Dockerfile
FROM ruby:3.2.2-alpine3.18

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

RUN mkdir /app
WORKDIR /app

ADD Gemfile /app/Gemfile

RUN sudo apt-get update -qq && \
    sudo apt-get install -y build-essential \
    libpq-dev \
    sudo \
    gem install bundler:2.4.1

RUN bundle install

ADD . /app