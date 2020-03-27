FROM hhvm/hhvm-proxygen:latest

RUN apt-get update -y \
  && apt-get install -y dnsutils iputils-ping net-tools curl

RUN hhvm --version \
  && php --version

# Install composer
RUN cd $(mktemp -d) \
  && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Install the app
RUN rm -rf /var/www
