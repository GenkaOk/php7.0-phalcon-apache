php7.0-phalcon-apache
=====================

A Docker image based on php7.0-apache

Extra library: 
- PHP Framework Phalcon `php7.0-phalcon`
- composer library `hirak/prestissimo`

Tags
-----

* latest: Debian Jessie 8.0 (LTS), Apache 2.4, PHP 7.0.x with support for setting `error_reporting`, PhalconPHP

Usage
------

```
$ docker run -d -P genkaok/php7.0-phalcon-apache
```

With all the options:

```bash
$ docker run -d -p 8080:80 \
    -v /home/user/webroot:/var/www \
    -e PHP_ERROR_REPORTING='E_ALL & ~E_STRICT' \
    genkaok/php7.0-phalcon-apache
```

* `-v [local path]:/var/www` maps the container's webroot to a local path
* `-p [local port]:80` maps a local port to the container's HTTP port 80
* `-e PHP_ERROR_REPORTING=[php error_reporting settings]` sets the value of `error_reporting` in the php.ini files.
