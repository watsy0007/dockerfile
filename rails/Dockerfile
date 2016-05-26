FROM zhulux/ruby:2.3.0
MAINTAINER watsy0007@mail.com

ENV BUNDLER_VERSION 1.12.4
ENV RAILS_VERSION 4.2.6

RUN apt-get update && \
    apt-get install postgresql-client libpq-dev graphicsmagick imagemagick ghostscript libgs-dev nodejs -y && \
    rm -rf /var/lib/atp/lists/*

RUN ln -s /usr/bin/ruby2.3 /usr/bin/ruby && \
    ln -s /usr/bin/gem2.3 /usr/bin/gem
    
RUN gem install bundler --version "$BUNDLER_VERSION" --no-rdoc --no-ri  && \
    gem install rails --version "$RAILS_VERSION"  --no-rdoc --no-ri && \
    gem install pry --no-rdoc --no-ri

CMD [ "pry" ]
