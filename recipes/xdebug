# Xdebug

Requires that PHP be compiled/installed.

Be sure to update the location of your php-config and the specific xdebug version you require (i.e. replace `master` with an actual release version.

```
mkdir -p /root/xdebug-src
cd /root/xdebug-src
git clone --branch master https://github.com/xdebug/xdebug.git .
/usr/local/php/bin/phpize
./configure --enable-xdebug --with-php-config="/usr/local/php/bin/php-config"
make
make install
cd /root
rm -rf /root/xdebug-src
```
