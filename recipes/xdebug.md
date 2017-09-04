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

Create a file named /etc/php.d/xdebug.ini with the following content, pay attention to the extensions path:
```
[xdebug]
zend_extension = "/usr/local/php/lib/php/extensions/no-debug-non-zts-20160303/xdebug.so"
xdebug.profiler_output_dir = "/tmp/xdebug/profiling"
xdebug.profiler_enable = 0
xdebug.profiler_enable_trigger = 1
xdebug.profiler_output_name = "cachegrind.out.%t_%R"
xdebug.remote_enable = 1
xdebug.remote_host = "localhost"
xdebug.remote_port = 9000
xdebug.remote_handler = "dbgp"
xdebug.remote_connect_back = 1
xdebug.var_display_max_data = 1024
xdebug.var_display_max_depth = 32
```
