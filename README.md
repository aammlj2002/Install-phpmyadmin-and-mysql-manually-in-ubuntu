
# Install phpmyadmin and mysql manually in ubuntu


we are going to install phpmyadmin and mysql manually. We don't need xammp and you can use globally in you PC.


## Installation

First we are going to install apache web server

```bash
  sudo apt-get update
```
    
```bash
  sudo apt-get upgrade
```
```bash
  sudo apt-get install tasksel
```
```bash
  sudo tasksel install lamp-server
```
```bash
  sudo apt-get update
```
```bash
  sudo systemctl restart apache2
```

And check php version

```bash
  php -v
```

Go to browser and enter "localhost"

![App Screenshot](img/localhost.jpg)

And check mysql version
```bash
  mysql -V
```

And we are going to install mysql account

```bash
  sudo mysql
```

![App Screenshot](img/sudo_mysql.jpg)

```bash
create user 'admin'@'localhost' identified by '123456';
```

```bash
grant all privileges on * . * to 'admin'@'localhost';
```

```bash
flush privileges;
```

```bash
exit;
```

And install phpmyadmin


```bash
sudo apt install phpmyadmin
```

![App Screenshot](img/phpmyadmin1.jpg)

Choose 'apache2' by using arrow and space

![App Screenshot](img/phpmyadmin2.jpg)

And use tap to go to ok and Enter

![App Screenshot](img/phpmyadmin3.jpg)

And choose yes and Enter

![App Screenshot](img/phpmyadmin4.jpg)

Enter Password "123456"

![App Screenshot](img/phpmyadmin5.jpg)

And comfirm password

Go to Browser and enter "localhost/phpmyadmin"

Enter user-admin and password-123456

![App Screenshot](img/phpmyadminuser.jpg)

Create a folder and Create a file "index.php"

In "index.php" write "<?php echo 'hello'; ?>"

Save this file and open terminal and run

```bash
php -S localhost:8000
```

![App Screenshot](img/localhostrun.jpg)

Go to browser and enter "localhost:8000"
