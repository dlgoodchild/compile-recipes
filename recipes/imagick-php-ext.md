# IMagick PHP Extension

Careful of the extensions path, this will vary depending on the architecture and version of your PHP installation.  
The path in the following works with PHP v7.1.x

```
mkdir -p /root/imagick-src
cd /root/imagick-src
git clone https://${github_auth}:x-oauth-basic@github.com/mkoppanen/imagick.git .
/usr/local/php/bin/phpize
./configure --with-php-config="/usr/local/php/bin/php-config"
make
make install
cp /root/imagick-src/modules/imagick.so /usr/local/php/lib/php/extensions/no-debug-non-zts-20160303/
cd /root
rm -rf /root/imagick-src
```

Create a file named `/etc/php.d/imagick.ini` with the following content, again remembering to pay attention to the extensions path:
```
extension = "/usr/local/php/lib/php/extensions/no-debug-non-zts-20160303/imagick.so"
```
