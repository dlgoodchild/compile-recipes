# Yaml PHP Extension (PECL)

Requires compilation of libyaml.

```
mkdir -p /root/pecl-yaml-ext
cd /root/pecl-yaml-ext
wget http://pecl.php.net/get/yaml-2.0.0.tgz
tar -zxvf yaml-2.0.0.tgz
cd yaml-2.0.0
/usr/local/php/bin/phpize
./configure --with-php-config="/usr/local/php/bin/php-config"
make
make install
cd /root
rm -rf /root/pecl-yaml-ext
```

Create a file named /etc/php.d/yaml.ini with the following content, pay attention to the extensions path:
```
extension = "/usr/local/php/lib/php/extensions/no-debug-non-zts-20160303/yaml.so"
```
