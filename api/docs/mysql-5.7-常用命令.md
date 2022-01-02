# 创建用户并授权

```shell
create database password_bank;
CREATE USER 'password_bank'@'%' IDENTIFIED BY 'Password_bank_2@220102';
GRANT ALL ON password_bank.* TO 'password_bank'@'%';
flush privileges;
```

# 修改密码
```shell
use mysql;
update user set authentication_string=password('Password_bank_2@220102') where user='password_bank' and Host='%';
flush privileges;
```