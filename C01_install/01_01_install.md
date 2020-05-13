# mysql安装

## Yum安装mysql

1. 卸载系统自带安装的`MariaDB`

   ```shell
   # 查询是否有MariaDB
   $ sudo rpm -qa|grep mar
   # 卸载软件
   $ sodu yum  -y remove mari*
   # 删除数据库文件
   $ sudo rm -rf /var/lib/mysql/*
   # 查看是否还有残留
   $ sudo rmp -qa|grep mar
   ```

   

2. `MySQL` 基于 `libaio` 库，因此，安装需要提前安装对应依赖

   ```shell
   # 基于YUM系统
   $ sudo yum install -y libaio
   # 基于APT系统
   $ sudo apt-get install -y libaio1
   ```

   

3. 下载需要的mysql版本（此教程使用的是8.0）

   数据库各种版本下载链接](https://downloads.mysql.com/archives/community/) 此处使用的是rpm安装的8.0版本

```shell
$ sudo wget https://downloads.mysql.com/archives/get/p/23/file/mysql-8.0.3-rc-linux-glibc2.12-x86_64.tar.gz
```





