# Ubuntu20.4 Command For Apache2 and PHP problem mainly for APACHE2

========================================================

## 1st Try:

---

```
sudo apt-get remove apache2
sudo apt-get purge apache2
sudo apt-get update
sudo apt-get autoremove
sudo apt-upgrade
```

# Then Check version of apache2 if not available try with command which was recommended by your OS and reinstall apache2 or if not solved try below command.

## 2nd try part-1: Remove Some packages and dependencies

---

```
sudo apt remove php7.4-cli libapache2-mod-php7.4 php-pear php7.4-fpm php7.4-cgi php7.4 apache2 apache2-bin apache2-data apache2-utils php7.4-json php7.4-opcache php7.4-readline libapr1 libaprutil1 libaprutil1-dbd-sqlite3 libaprutil1-ldap liblua5.2-0 dbconfig-common dbconfig-mysql icc-profiles-free libjs-jquery libjs-openlayers libjs-sphinxdoc libjs-underscore libmcrypt4 libzip4 php-bz2 php-common php-curl php-gd php-google-recaptcha php-mbstring php-mysql php-phpmyadmin-motranslator php-phpmyadmin-shapefile php-phpseclib php-psr-cache php-psr-container php-psr-log php-symfony-cache php-symfony-cache-contracts php-symfony-expression-language php-symfony-service-contracts php-symfony-var-exporter php-tcpdf php-twig php-twig-extensions php-xml php-zip php7.1-common php7.1-mcrypt php7.4-bz2 php7.4-common php7.4-curl php7.4-gd php7.4-mbstring php7.4-mysql php7.4-xml php7.4-zip php-json phpmyadmin
```

## 2nd try part-2: Installing again which was removed by before command

---

```
sudo apt install php7.4-cli libapache2-mod-php7.4 php-pear php7.4-fpm php7.4-cgi php7.4 apache2 apache2-bin apache2-data apache2-utils php7.4-json php7.4-opcache php7.4-readline libapr1 libaprutil1 libaprutil1-dbd-sqlite3 libaprutil1-ldap liblua5.2-0 dbconfig-common dbconfig-mysql icc-profiles-free libjs-jquery libjs-openlayers libjs-sphinxdoc libjs-underscore libmcrypt4 libzip4 php-bz2 php-common php-curl php-gd php-google-recaptcha php-mbstring php-mysql php-phpmyadmin-motranslator php-phpmyadmin-shapefile php-phpseclib php-psr-cache php-psr-container php-psr-log php-symfony-cache php-symfony-cache-contracts php-symfony-expression-language php-symfony-service-contracts php-symfony-var-exporter php-tcpdf php-twig php-twig-extensions php-xml php-zip php7.1-common php7.1-mcrypt php7.4-bz2 php7.4-common php7.4-curl php7.4-gd php7.4-mbstring php7.4-mysql php7.4-xml php7.4-zip php-json phpmyadmin
```

## 3rd if problem after 2nd tried: If face this problem again

---

```
dpkg -S /usr/share/apache2/default-site/index.html
```

```
sudo apt-get remove --purge apache2 apache2-data apache2-utils
```

```
sudo apt-get install apache2
```

---

[BACK Ubuntu Main](ubuntu-main.md)
<br/>
[BACK Main](../README.md)
