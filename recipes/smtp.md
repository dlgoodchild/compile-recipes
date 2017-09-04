# SMTP

Not so much of a compilation, more configuration of a pre-existing service.

```
sed -i -e 's/mibs\s*:\s*/#mibs :/' /etc/snmp/snmp.conf
apt-get install -y snmp-mibs-downloader
download-mibs
```
