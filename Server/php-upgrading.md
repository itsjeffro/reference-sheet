# PHP Upgrading

## 1. Anylise code base
Check for imcompatibility issues by using a static code anylizer.

Analyizers:
* Phan

## 2. List PHP modules
Get a list of PHP modules installed.

### Ubuntu
Command:
```
dpkg --get-selections | grep -i php
```

Example output:
```
php-common
php7.*
php7.*-cli
php7.*-common
php7.*-curl
php7.*-fpm
php7.*-json
php7.*-mbstring
php7.*-mysql
php7.*-opcache
php7.*-readline
php7.*-xml
```

## 3. Install PHP/modules
TBA
