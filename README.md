# Repositório de Comandos em Bash

## Instalação PHP 7.2
```
yum install epel-release
yum update
yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
yum-config-manager --enable remi-php72
yum install php php-mbstring php-gd php-mcrypt php-pear php-pspell php-pdo php-xml php-mysqlnd php-pgsql php-process php-pecl-zip php-xml php-intl php-zip php-zlib php-apcu php-redis
``` 
## Configuração Virtual Host
```
/etc/httpd/conf.d/owncloud.conf

<VirtualHost *:80>
    ServerName owncloud.epl.gov.br
    Redirect / https://owncloud.epl.gov.br/
</VirtualHost>
<VirtualHost *:443>
  DocumentRoot /var/www/html/owncloud
  ServerName owncloud.epl.gov.br

  SSLEngine on
  SSLProxyEngine on
  SSLProtocol all -SSLv2 -SSLv3
  SSLCertificateFile /etc/httpd/conf.d/ssl_certs/wildcard.epl.gov.br/cert.pem
  SSLCertificateKeyFile /etc/httpd/conf.d/ssl_certs/wildcard.epl.gov.br/privkey.pem
  SSLCACertificateFile /etc/httpd/conf.d/ssl_certs/wildcard.epl.gov.br/chain.pem
  SSLProxyCheckPeerCN off
  SSLProxyCheckPeerName off

  Loglevel debug
  ErrorLog /var/log/httpd/owncloud/error_log
  CustomLog /var/log/httpd/owncloud/access_log common

  <Directory /var/www/html/owncloud>
     Options Indexes FollowSymLinks
     AllowOverride All
     Order allow,deny
     Allow from all
  </Directory>
</VirtualHost>
```