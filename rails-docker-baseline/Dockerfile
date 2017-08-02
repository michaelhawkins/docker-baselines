FROM ruby:2.4.1
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs libxml2-dev libxslt1-dev
#RUN mkdir /app
WORKDIR /app

ADD . /app
ADD Gemfile /app/Gemfile
ADD Gemfile.lock /app/Gemfile.lock
RUN bundle install

# Add default unicorn config
ADD config/unicorn.rb /app/config/unicorn.rb
