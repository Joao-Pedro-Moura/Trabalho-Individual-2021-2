FROM ruby:3.0.0
RUN apt-get update -qq &&\ 
    apt-get install -y\ 
    nodejs \
    postgresql-client
WORKDIR /aplicacao
COPY Gemfile Gemfile
COPY Gemfile.lock Gemfile.lock
RUN bundle install

COPY . .

CMD ["rails", "server", "-b", "0.0.0.0"]