# WordPress htaccess boilerplate for Apache 2.4

See also:  
- [Creare/WP-htaccess](https://github.com/Creare/WP-htaccess/blob/master/.htaccess)
- [roots/wp-h5bp-htaccess](https://github.com/roots/wp-h5bp-htaccess/blob/master/h5bp-htaccess.conf)


## Disabling access log for specific file types
```
# in your .htaccess
SetEnvIf Request_URI "\.(css|js|png|jpe?g|gif|svg|map|woff2|ico)(\?.*)?$" dontlog

# in httpd.conf or httpd-vhosts.conf
CustomLog ${APACHE_LOG_DIR}/access.log combined env=!dontlog
``` 