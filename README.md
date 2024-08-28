# NextcloudRedOS
*Oблако Nextcloud на системе RedOS*
1. На время установки отключаем SELinux в файле */etc/selinux/config*
Меняем ```SELINUX=enforcing на SELINUX=permissive```
2. устанавливаем необходимые пакеты 
```
dnf install httpd php php-dom php-mbstring php-gd php-pdo php-json php-xml php-zip php-curl php-mcrypt php-pear setroubleshoot-server bzip2 php-ldap php-mysqlnd mariadb mariadb-server mod_auth_kerb php-fpm
```
*Настройка MySQL*

3.Запускаем службу mariadb
```
sudo systemctl start mariadb && systemctl enable mariadb

```
```
sudo mysql_secure_installation
```
Задаем пароль root удаляем анонимных пользователей запрешаем удаленый вход для root, удаляем тестовую базу.
4. Создаем базу и пользователя   
```
mysql -u root –p
```
![alt text](./Pictures/Screenshot_1.jpg)

*Установка Nextcloud*
5.Устанавливаем nectcloud
 ```
dnf install nextcloud nextcloud-httpd nextcloud-mysql
```
6. Создаём виртуальный хост в файле *etc/httpd/conf.d/nextcloud.conf.*
7. Редактируем */usr/share/nextcloud/config/config.php*
 ![alt text](./Pictures/Screenshot_2.jpg)

