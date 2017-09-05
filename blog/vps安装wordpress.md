
1.安装LAMP环境
	1.1 安装Apache2
	1.2 安装MySQL5
	1.3 安装PHP5
2.初始化数据库
3.下载并配置WordPress
4.安装WordPress
6.设置主题（themes）

### 1. 安装LAMP环境
LAMP是Linux，Apache，MySQL，php的缩写，是指在Linux上安装Apache2，MySQL, PHP等软件包所建立的网站运行平台。
#### 1..1安装Apache2
`sudo apt-get install apache2`
#### 1.2安装MySQL5
`sudo apt-get install mysql-server mysql-client`
在安装MySQL过程中会要求你设置root用户的密码
#### 1.3 安装PHP5
`sudo apt-get install php5 libapache2-mod-php5 php5-mysql php5-curl php5-gd php5-intl php-pear php5-imagick php5-imap php5-mcrypt php5-memcache php5-ming php5-ps php5-pspell php5-recode php5-snmp php5-sqlite php5-tidy php5-xmlrpc php5-xsl php5-xcache libssh2-php`
### 2.初始化数据库
 `sudo mysql -u root -p`
```
Enter Password:
...
mysql>  CREATE DATABASE wordpress;（此处是设置wordpress数据库的名字，我这里设置的名字就为“wordpress”）;

mysql> exit（退出数据库操作）
```

重启Apache2和MySQL
`sudo service apache2 restart`
`sudo service mysql restart`

### 3.下载和配置wordpress
```
cd tmp
wget http://wordpress.org/wordpress-4.x.tar.gz
tar zxf wordpress-4.x.tar.gz
然后把wordpress文件夹里面的全部东西提取到/var/www/html/里面，命令忘了怎么写了（GG）
mkdir -p /var/www/html/wordpress/wp-content/uploads
```
[image:225ECB5A-039F-4A69-9487-D47999090C2E-6632-00000CFAAA199C09/Snip20170902_1.png]
修改关键目录权限
```
sudo chown -R www-data.www-data /var/www/html
sudo chmod -R 755 /var/www/html
sudo chown -R :www-data /var/www/html/wp-content/uploads
```

