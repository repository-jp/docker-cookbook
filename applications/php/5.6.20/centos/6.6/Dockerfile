FROM repositoryjp/virtphp
MAINTAINER Shinya Kinoshita <skinoshita@repositories.jp>

LABEL name="PHP 5.6.20 Image" \
      description="The image for creating docker container of PHP 5.6.20 Environment." \
      distribution="centos" \
      centos-version="6.6" \
      php-version="5.6.20" \
      vendor="REPOSIORY <http://www.repositories.jp>" \
      license="MIT"

ENV PHP_VERSION 5.6.20

USER root

# Install PHP 5.6.20
RUN phpbrew install ${PHP_VERSION} +default +everything -- --with-icu-dir=/usr --with-gd --with-jpeg-dir=/usr/lib64 --with-png-dir=/usr/png --enable-gd-jis-conv
RUN phpbrew switch ${PHP_VERSION}

RUN virtphp create --php-bin-dir=$HOME/.phpbrew/php/php-${PHP_VERSION}/bin phpenv

RUN sed -e 's/;date.timezone =/date.timezone = UTC/g' $HOME/.virtphp/envs/phpenv/etc/php.ini > /tmp/php.ini
RUN mv -f /tmp/php.ini .virtphp/envs/phpenv/etc/php.ini
RUN echo "[[ -e ~/.virtphp/envs/phpenv/ ]] && source ~/.virtphp/envs/phpenv/bin/activate" >> ~/.bashrc

# Configure container.
USER root
WORKDIR /root

CMD ["/usr/sbin/sshd", "-D"]
