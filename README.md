## WordPress starting php and extensions
```sh
sudo apt install -y php8.0 php8.0-curl php8.0-xml php8.0-mysql php8.0-imagick php8.0-xml php8.0-zip php8.0-mcrypt
```

## Per passare da 7.2 a 8.0
```sh
sudo a2dismod php7.2
sudo a2enmod php8.0
sudo update-alternatives --set php /usr/bin/php8.0
```

### su singola linea
```sh
sudo a2dismod php7.2 && sudo a2enmod php8.0 && sudo update-alternatives --set php /usr/bin/php8.0 && sudo service apache2 restart
```

## Per passare da 8.0 a 7.2
```sh
sudo a2dismod php8.0
sudo a2enmod php7.2
sudo update-alternatives --set php /usr/bin/php7.2
```

### su singola linea
```sh
sudo a2dismod php8.0 && sudo a2enmod php7.2 && sudo update-alternatives --set php /usr/bin/php7.2 && sudo service apache2 restart
```

## Per verficare la versione
```sh
php -v
```

## Al termine riavviare apache2
```sh
sudo service apache2 restart
```
