# RADIUS-Ubuntu-20.04

- - - history

![](https://github.com/nu11secur1ty/RADIUS-Ubuntu-20.04/blob/master/screen/radius.PNG)

```bash
    1  apt update
    2  apt dist-upgrade
    3  apt update
    4  apt install php-gd php-mail php-mail-mime php-mysql php-pear php-db php-mbstring php-xml php-curl
    5  apt install freeradius freeradius-mysql freeradius-utils
    6  apt autoremove
    7  systemctl stop freeradius
    8  freeradius -X
    9  systemctl enable --now freeradius
   10  ufw allow to any port 1812 proto udp
   11  ufw allow to any port 1813 proto udp
   12  ss -alun4 | grep -E ':1812|:1813'
   13  apt install mariadb
   14  apt install mysql-server
   15  mysql_secure_installation 
   16  mysql -u root -p
   17  mysql -u root -p radiusdb < /etc/freeradius/3.0/mods-config/sql/main/mysql/schema.sql
   18  cp /etc/freeradius/3.0/mods-available/sql /etc/freeradius/3.0/mods-available/sql.back
   19  vim /etc/freeradius/3.0/mods-available/sql
   20  apt install vim
   21  vim /etc/freeradius/3.0/mods-available/sql
   22  ln -s /etc/freeradius/3.0/mods-available/sql /etc/freeradius/3.0/mods-enabled/
   23  chown -h freerad.freerad /etc/freeradius/3.0/mods-enabled/sql
   24  systemctl restart freeradius
   25  mysql -u radiusadmin -p
   26  systemctl stop freeradius
   27  freeradius -X
   28  radtest
   29  radtest demouser demopass localhost 10 testing123
   30  systemctl start freeradius
   31  cd /home/radius-openvpn/Downloads/
   32  ls
   33  unzip daloradius-1.1-2.zip 'daloradius/*' -d /var/www/html/
   34  apt install apache2
   35  unzip daloradius-1.1-2.zip 'daloradius/*' -d /var/www/html/
   36  cd
   37  mysql -u root -p radiusdb < /var/www/html/daloradius/contrib/db/fr2-mysql-daloradius-and-freeradius.sql
   38  mysql -u root -p radiusdb < /var/www/html/daloradius/contrib/db/mysql-daloradius.sql
   39  chown -R www-data.www-data /var/www/html/daloradius/
   40  chmod 664 /var/www/html/daloradius/library/daloradius.conf.php
   41  vim /var/www/html/daloradius/library/daloradius.conf.php
   42  systemctl restart freeradius
   43  ifco
   44  apt install net-tools
   45  ifconfig 
   46  systemctl start mysql
   47  systemctl status mysql
   48  systemctl enable mysql
   49  systemctl enable freeradius
   50  systemctl start freeradius
   51  systemctl restart freeradius
   52  systemctl status freeradius.service 
   53  vim /var/www/html/daloradius/library/daloradius.conf.php
   54  systemctl restart mysql.service 
   55  systemctl restart apache2.service 
   56  systemctl restart freeradius
   57  systemctl restart freeradius.service 
   58  cd /var/www/html/
   59  ls
   60  cd di
   61  cd daloradius/
   62  ls
   63  chmod 664 /var/www/html/daloradius/library/daloradius.conf.php
   64  cd /var/www/html/daloradius/library/
   65  ls
   66  vim daloradius.conf.php
   67  telinit 6
   68  chown -R www-data.www-data /var/www/html/daloradius/
   69  ls /var/www/html/
   70  rm -rm /var/www/html/index.html 
   71  rm -rf /var/www/html/index.html 
   72  ls /var/www/html/
   73  systemctl restart apache2.service 
   74  mysql -u root -p radiusdb < /var/www/html/daloradius/contrib/db/fr2-mysql-daloradius-and-freeradius.sql
   75  mysql -u root -p radiusdb < /var/www/html/daloradius/contrib/db/mysql-daloradius.sql
   76  chown -R www-data.www-data /var/www/html/daloradius/
   77  chmod 664 /var/www/html/daloradius/library/daloradius.conf.php
   78  vim /var/www/html/daloradius/library/daloradius.conf.php
   79  systemctl restart freeradius
   80  php-v
   81  php --v
   82  php -v
   83  a2enmod php7
   84  a2enmod php7.4
   85  a2enmod php
   86  apt install php7
   87  a2enmod php7.0
   88  apt install php libapache2-mod-php
   89  a2enmod php7.0
   90  a2enmod php7.4 
   91  systemctl restart apache2.service

# Mysql 
Yourp@ss

user: radiusadmin
password: myStr0nP@ssW0rd

# Radius
        server = "localhost"
        port = 3306
        login = "radius"
        password = "radpass"
```
