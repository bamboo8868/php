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
--prefix=/png/php/7.0.0 \
--enable-opcache \
--enable-fpm \
--enable-pdo \
--enable-sockets \
--enable-exif \
--enable-soap \
--enable-ftp \
--enable-wddx \
--enable-pcntl \
--enable-soap \
--enable-bcmath \
--enable-mbstring \
--enable-dba \
--enable-gd-native-ttf \
--enable-gd-jis-conv \
--enable-zip \
--enable-calendar \
--enable-shmop \
--enable-sysvmsg \
--enable-sysvsem \
--enable-sysvshm \
--with-mysqli \
--with-pdo-mysql \
--with-pdo-sqlite \
--with-iconv \
--with-gmp \
--with-pspell \
--with-xmlrpc \
--with-openssl \
--with-mhash \
--with-mcrypt \
--with-xsl \
--with-curl \
--with-pcre-regex \
--with-gd \
--with-jpeg-dir=/usr \
--with-png-dir=/usr \
--with-zlib-dir=/usr \
--with-xpm-dir=/usr \
--with-freetype-dir=/usr \
--with-gettext=/usr \
--with-zlib=/usr \
--with-bz2=/usr \
--with-recode=/usr \
--with-ldap \
--with-pear \
--with-readline \
--with-fpm-user=png \
--with-fpm-group=png \
--with-apxs2=/png/httpd/2.4.17/bin/apxs

#编译安装
make && make install
