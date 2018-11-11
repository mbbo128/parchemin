# Install xDebug on Mac OS

## Install pecl
- https://jason.pureconcepts.net/2012/10/install-pear-pecl-mac-os-x/

## Install Xdebug On Mac
```pecl install xdebug```

## Configure your php.ini

vim /usr/local/etc/php/X.X/php.ini
```
[Xdebug]
zend_extension="/usr/local/lib/php/pecl/20160303/xdebug.so"
xdebug.remote_enable=1
xdebug.remote_host=127.0.0.1
xdebug.remote_port=9002
xdebug.remote_handler="dbgp"
xdebug.remote_log="/Users/m.boissa/Log/xdebug.log"
```

## Configure your PHPStorm

### Preferences -> Languages and Frameworks -> PHP -> Debug

Set Xdebug port to 9002

### Preferences -> Languages and Frameworks -> PHP -> Servers

Add a server :

name : 127.0.0.1
host : 127.0.0.1
port : 8000

### Run -> Edit Configurations -> PHP Built-in Web Server

Host : http://localhost
Port: 8000
Document root : /Users/m.boissa/Documents/fac/web
