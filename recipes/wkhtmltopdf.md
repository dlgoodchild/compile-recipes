# WKHTMLToPDF

```
apt-get install -y \
  fontconfig \
  libxrender1 \
  xfonts-base \
  xfonts-75dpi \
mkdir -p /root/wkhtmltopdf
cd /root/wkhtmltopdf
wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.4/wkhtmltox-0.12.4_linux-generic-amd64.tar.xz
tar -xvf wkhtmltox-0.12.4_linux-generic-amd64.tar.xz
cd wkhtmltox
cp -R . /usr
cd /root
rm -rf /root/wkhtmltopdf
```
