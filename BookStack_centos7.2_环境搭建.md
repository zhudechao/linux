# BookStack centos7.2 环境搭建

安装谷歌浏览器

```
yum -y install chromium
```

校验能不能打开百度网页代码

```
chromium-browser --headless --disable-gpu --dump-dom --no-sandbox https://www.baidu.com
```

安装puppeteer

```
npm install -g n
n stable
npm install -g cnpm
cnpm install puppeteer
```

安装calibre

```
yum install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gcc make xdg-utils wget qt4 qt4-devel qt4-x11 libpcap-devel xz-devel -y
```

```
sudo -v && wget -nv -O- https://download.calibre-ebook.com/linux-installer.py | sudo python -c "import sys; main=lambda:sys.stderr.write('Download failed\n'); exec(sys.stdin.read()); main()"
```

检查哪个包含有libstdc++.so.6

```
yum provides libstdc++.so.6
```

