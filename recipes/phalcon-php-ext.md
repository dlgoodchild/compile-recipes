# Phalcon PHP Extension

```
mkdir -p /root/phalcon-src
cd /root/phalcon-src
git clone https://github.com/phalcon/cphalcon.git .
cd build/php7/64bits
/usr/local/php/bin/phpize
./configure --with-php-config="/usr/local/php/bin/php-config"
make
make install
cd /root
rm -rf /root/phalcon-src
```
