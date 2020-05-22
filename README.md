# php-crud-pdo-extension

# PHP web application on a LAMP Stack
This solution walks you through the creation of an Ubuntu **L**inux virtual server, with **A**pache web server, **M**ySQL, and **P**HP (the LAMP stack). To see the LAMP server in action

## Objectives
* Provision a LAMP server
* Install Apache, MySQL, and PHP
* Verify installation and configuration
* Creating crud operations using PDO operations

## Verify installation and configuration
Verify Apache, MySQL, and PHP running on Ubuntu image.

1. Installing Apache and Updating the Firewall
```
sudo apt update
sudo apt install apache2
sudo ufw app list
sudo ufw allow in "Apache Full"
```
2. Installing MySQL
   ```
   sudo apt install mysql-server
   ```
   check online for tuts
3. Installing PHP
   ```
   sudo apt install php libapache2-mod-php php-mysql
   ```

4.  restart the Apache web server
   ```sh
   sudo systemctl restart apache2
sudo systemctl status apache2
   ```
5. Copy the following lines to the file, substituting *yourPassword* with your MySQL database password (leave other values unchanged). Then save using Ctrl+X to exit and save the file.   
   ```php
   <?php
   define('DB_NAME', 'wordpress');
   define('DB_USER', 'wordpress');
   define('DB_PASSWORD', 'yourPassword');
   define('DB_HOST', 'localhost');
   ?>
   ```

## Happy Coding!
