# MongoDB

```
mkdir -p /root/phpext-mongodb-src
cd /root/phpext-mongodb-src
git clone https://github.com/mongodb/mongo-php-driver.git .
git submodule sync && git submodule update --init
/usr/local/php/bin/phpize
./configure --with-php-config="/usr/local/php/bin/php-config"
make all -j 5
make install
cd /root
rm -rf /root/phpext-mongodb-src
```
