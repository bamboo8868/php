#安装编译PHP依赖的开发工具和库:
sudo apt-get install \
build-essential \
autoconf \
libtool \
re2c \
libxml2-dev \
openssl \
libcurl4-openssl-dev \
libbz2-dev \
libjpeg-dev \
libpng12-dev \
libfreetype6-dev \
libldap2-dev \
libmcrypt-dev \
libmysqlclient-dev \
libxslt1-dev \
libxt-dev \
libpcre3-dev \
libxpm-dev \
libt1-dev \
libgmp-dev \
libpspell-dev \
librecode-dev \
libreadline6-dev 

#配置脚本 configure_php.sh
#!/bin/bash
./configure \
--prefix=/usr/local/php
--disable-debug
--disable-phpdbg
--enable-mysqlnd
--enable-bcmath
--with-bz2=/usr
--enable-calendar
--with-curl
--enable-exif
--enable-fpm
--with-freetype-dir
--enable-ftp
--with-gd
--enable-gd-jis-conv
--enable-gd-native-ttf
--with-gettext=/usr
--with-gmp
--with-iconv
--enable-intl
--with-jpeg-dir
--enable-mbstring
--with-mcrypt
--with-openssl
--enable-pcntl
--with-pdo-mysql=mysqlnd
--with-png-dir
--with-recode=/usr
--enable-shmop
--enable-soap
--enable-sockets
--enable-sysvmsg
--enable-sysvsem
--enable-sysvshm
--enable-wddx
--with-xmlrpc
--with-xsl
--with-zlib=/usr
--enable-zip
--with-mysqli=mysqlnd

#编译安装
make && make install
