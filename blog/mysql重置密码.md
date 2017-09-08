1.  Stop the mysqld server.  
	1. Typically this can be done by from 'System Prefrences' > MySQL > 'Stop MySQL Server'
2. Start the server in safe mode with privilege bypass     
	1. From a terminal:     sudo /usr/local/mysql/bin/mysqld_safe --skip-grant-tables
3. In a new terminal window:     
	1. sudo /usr/local/mysql/bin/mysql -u root     
	2. UPDATE mysql.user SET Password=PASSWORD('NewPassword') WHERE user='root'     
	3. FLUSH PRIVILEGES     
	4. \q
4. Stop the mysqld server again and restart it in normal mode.
5. 使用mysql -u root -p 连接数据库。
	1. 操作提示：You must reset your password using ALTER USER statement before executing this statement. 
	2. 按照提示ALTER USER 修改密码无效，后来发现执行如下命令即可： 
		1. SET PASSWORD = PASSWORD(‘123456’);
