FROM ruby:2.6.6

ENV BUNDLER_VERSION=2.1.4

# RUN apt-get update -qq && apt-get install -y nodejs
RUN apt-get update -qq 

RUN gem install bundler -v $BUNDLER_VERSION

WORKDIR /webapp

COPY Gemfile Gemfile.lock ./

ENV BUNDLE_PATH='./vendor/bundle'
RUN bundle check || bundle install --jobs 20 --retry 5

COPY . ./

# Add a script to be executed every time the container starts.
COPY docker-entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/docker-entrypoint.sh
ENTRYPOINT ["docker-entrypoint.sh"]

EXPOSE 3000

# Start the main process.
CMD ["bundle", "exec", "rails", "server", "-b", "0.0.0.0"]
