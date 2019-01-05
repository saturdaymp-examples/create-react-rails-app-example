FROM ruby:2.5.3
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir /website
WORKDIR /website
COPY Gemfile /website/Gemfile
COPY Gemfile.lock /website/Gemfile.lock
RUN gem install bundler
RUN bundle install
COPY . /website
