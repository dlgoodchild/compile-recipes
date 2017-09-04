# Bison

Required when trying to compile any version of PHP >= 5.4.

```
cd /root/bison
wget http://ftp.gnu.org/gnu/bison/bison-2.6.4.tar.gz && tar --strip-components=1 -xvzf bison-2.6.4.tar.gz
./configure --prefix=/usr/local/bison
make
make install
ln -s /usr/lib/libc-client.a /usr/lib/x86_64-linux-gnu/libc-client.a
cd /root
rm -rf /root/bison
```
