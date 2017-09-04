# PHP

## Prerequisits
Bison

This is tried and tested on Ubuntu 14.x and 16.x
```
apt-get update && apt-get install -y --no-install-recommends \
  curl \
  git \
  memcached \
  snmp \
  xz-utils \
  unzip cmake libqt4-dev \
  build-essential \
  libfcgi-dev \
  libfcgi0ldbl \
  libjpeg62-dbg \
  libmcrypt-dev \
  libssl-dev \
  libc-client2007e \
  libc-client2007e-dev \
  libldb-dev \
  libldap2-dev
apt-get build-dep -y php5

cd /root/php
git clone --verbose --branch php-7.1.9 https://github.com/php/php-src.git .
./buildconf --force
./configure --prefix=/usr/local/php --with-config-file-scan-dir=/etc/php.d
  --disable-rpath \
  --enable-bcmath \
  --enable-calendar \
  --enable-exif \
  --enable-fpm \
  --enable-ftp \
  --enable-gd-native-ttf \
  --enable-inline-optimization \
  --enable-mbregex \
  --enable-mbstring \
  --enable-opcache \
  --enable-pcntl \
  --enable-phpdbg \
  --enable-soap \
  --enable-sockets \
  --enable-sysvsem \
  --enable-sysvshm \
  --enable-zip \
  --with-bz2 \
  --with-curl \
  --with-fpm-user=www-data \
  --with-fpm-group=www-data \
  --with-freetype-dir \
  --with-gd \
  --with-gettext \
  --with-iconv \
  --with-imap \
  --with-imap-ssl \
  --with-jpeg-dir=/usr \
  --with-kerberos \
  --with-libdir=/lib/x86_64-linux-gnu \
  --with-libxml-dir=/usr \
  --with-ldap=/usr \
  --with-mcrypt \
  --with-mhash \
  --with-mysql \
  --with-mysqli \
  --with-openssl \
  --with-pcre-regex \
  --with-pdo-mysql \
  --with-pdo-pgsql \
  --with-pear \
  --with-pgsql \
  --with-png-dir=/usr \
  --with-snmp \
  --with-xmlrpc \
  --with-xsl \
  --with-zlib \
  --with-zlib-dir 
make
make install
```
