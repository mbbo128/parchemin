# xDebug with Vagrant

## Configuration xdebug on vagrant

### I assume xdebug is already install on the vagrant machine

cat  /etc/php.d/xdebug.ini 

```
zend_extension=/usr/lib64/php/modules/xdebug.so
xdebug.remote_enable=1
xdebug.remote_handler=dbgp
xdebug.remote_host=11.11.11.11
xdebug.remote_connect_back = on
xdebug.idekey = "XDEBUG"
```

### Restart apache

/etc/init.d/apache2 restart

## 2
