FROM ruby:2.5.3

# To install a later version of Node JS and Yarn.
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

# Install the needed software.
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs yarn

# Create the website folder and map the Gemfiles.
RUN mkdir /website
WORKDIR /website
COPY Gemfile /website/Gemfile
COPY Gemfile.lock /website/Gemfile.lock

# Update the bundler then install the gems.
RUN gem install bundler
RUN bundle install

# Copy our files to the website.
COPY . /website

