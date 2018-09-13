# WordPress server configurations

Some Apache/Nginx settings and boilerplate files for WordPress

## Disabling access log for specific file types
```
# in your .htaccess
SetEnvIf Request_URI "\.(css|js|png|jpe?g|gif|svg|map|woff2|ico)(\?.*)?$" dontlog

# in httpd.conf or httpd-vhosts.conf
CustomLog ${APACHE_LOG_DIR}/access.log combined env=!dontlog
``` 