# nextcloudRedOS
*Oблако Nextcloud на системе RedOS*
1. На время установки отключаем SELinux в файле ```/etc/selinux/config```
Меняем ```SELINUX=enforcing на SELINUX=permissive```
2. устанавливаем необходимые пакеты 
```
dnf install httpd php php-dom php-mbstring php-gd php-pdo php-json php-xml php-zip php-curl php-mcrypt php-pear setroubleshoot-server bzip2 php-ldap php-mysqlnd mariadb mariadb-server mod_auth_kerb php-fpm
```

![alt text](./Pictures/Screenshot_1.jpg)
