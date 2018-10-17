##### Install pecl
- https://jason.pureconcepts.net/2012/10/install-pear-pecl-mac-os-x/

##### Install Xdebug On Mac
```pecl install xdebug```

##### Configure your php.ini

vim /usr/local/etc/php/7.1/php.ini
```
[Xdebug]
zend_extension="/usr/local/lib/php/pecl/20160303/xdebug.so"
xdebug.remote_enable=1
xdebug.remote_host=127.0.0.1
xdebug.remote_port=9002
xdebug.remote_handler="dbgp"
xdebug.remote_log="/Users/m.boissa/Log/xdebug.log"
```
