# MySQL 使用

## 1. 命令行操作

```bash
mysql -u root -p
```

```sql
show databases;
```

```sql
use db;
```

```sql
show tables;
```

```sql
show columns from mysql.user\G;
```

```sql
describe mysql.user\G;
```

## 2. 用户操作

### 2.1. 查询所有用户

```sql
select host, user, authentication_string from mysql.user;
```

### 2.2. 创建用户

```sql
create user 'username'@'localhost' identified by 'password';
create user 'username'@'%' identified by 'password';
flush privileges;
```

### 2.3. 删除用户

```sql
drop user 'username'@'localhost';
flush privileges;
```

### 2.4. 取消 root 远程登录

```sql
delete from mysql.user where user = 'root' and host = '%';
flush privileges;
```

### 2.5. 修改密码

```sql
set password for 'username'@'%' = 'new_password';
flush privileges;
```

## 3. 权限操作

### 3.1. 查看用户权限

```sql
show grants for 'username'@'localhost';
```

### 3.2. 全部授权

```sql
grant all on db.* to 'username'@'%';
flush privileges;
```

### 3.3. 部分授权

```sql
grant select, delete, update, create, drop on db.* to 'username'@'%';
flush privileges;
```

### 3.4. 取消授权

```sql
revoke all on db.* from 'username'@'%';
flush privileges;
```
