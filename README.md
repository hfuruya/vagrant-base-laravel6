# README

## Commands

### Start Up
```
vagrant up
```

### Composer
```
cd /vagrant
curl -sS https://getcomposer.org/installer | php
./composer.phar self-update
php ./composer.phar 
```

### Laravel Installer
```
./composer.phar require "laravel/installer=~1.1"
./composer.phar update "laravel/installer" --prefer-dist
```

### Laravel
```
sudo mkdir laravel
./composer.phar create-project "laravel/laravel=6.*" laravel/ --prefer-dist
```

### Settings
```
{
sudo chmod -R 777 laravel/storage
sudo chmod -R 777 laravel/bootstrap/cache
}

cd /var/www
sudo rm -rf html
sudo ln -s /vagrant/laravel /var/www/html
```

### httpd.conf
```
sudo cp /vagrant/httpd.conf /etc/httpd/conf.d/main.conf
sudo systemctl restart httpd
```



