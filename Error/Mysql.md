## [ERR] 1153 - Got a packet bigger than 'max_allowed_packet' bytes

用 Navicat 导入 SQL 文件时报错：

```
[ERR] 1153 - Got a packet bigger than 'max_allowed_packet' bytes
```

MySQL 默认读取执行的 SQL 文件最大为16M，sql脚本实际 260M

> 解决方法

修改配置文件 my.cnf ，将默认值调大

```
vi /etc/my.cnf
[mysqld]
max_allowed_packet=400M
```

重启 MySQL

```
service restart mysqld
```

## You must reset your password using ALTER USER statement before executing this statement.

MySQL 安装完成后，首次登陆报以下错误

```
ERROR 1820 (HY000): You must reset your password using ALTER USER statement before executing this statement.
```

因为我们首次登陆使用的 MySQL 初始化始生成的临时密码，所以需要我们修改 root 用户密码。

```
alter user user() identified by 'root';
```

或者

```
 alter user 'root'@'localhost' identified by 'root';
```

如果密码设置了过期时间且密码已经到了过期时间也会报这个错误，解决方法同样是修改密码。