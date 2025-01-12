FROM ruby:3.2.2
RUN apt-get update -qq && apt-get install -y build-essential vim

WORKDIR /myapp

COPY Gemfile Gemfile.lock /myapp/
RUN bundle install
COPY . /myapp

COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]

CMD ["/bin/sh", "-c", "rm -f tmp/pids/server.pid && bundle exec puma -C config/puma.rb"]
