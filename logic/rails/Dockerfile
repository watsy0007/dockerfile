FROM zhulux/rails:4.2.6

RUN apt-get update && \
    apt-get install git npm build-essential nodejs-legacy pdftk poppler-utils libpoppler-dev --no-install-recommends -y && \
    apt-get autoremove && apt-get clean && \
    rm -rf /var/lib/atp/lists/* && \
    npm install bower -g  --allow-root

WORKDIR /tmp
ADD Gemfile /tmp
RUN bundle install

CMD ["/bin/bash"]
