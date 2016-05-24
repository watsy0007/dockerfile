FROM watsy0007/rails:4.2.6

RUN apt-get update && \
    apt-get install git build-essential -y && \
    rm -rf /var/lib/atp/lists/*

WORKDIR /tmp
ADD Gemfile /tmp
RUN bundle install

CMD ["/bin/bash"]
