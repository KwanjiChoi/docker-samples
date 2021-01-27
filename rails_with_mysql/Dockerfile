FROM ruby:latest

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
  apt-get update -qq && apt-get install -y \
  nodejs \
  yarn

WORKDIR /test_app/

COPY Gemfile Gemfile.lock /test_app/

RUN bundle install