# 账号密码

下面分别就数据库和操作系统的账号密码进行说明：

## 数据库

### 数据库密码

分别就Linux系统和Windows系统来说明数据库密码获取方法：

#### Linux系统

对于Linux系统来说，数据库密码存储在您的服务器指定文件中：*`/credentials/password.txt`*。建议通过云控制台直接连接服务器，进入命令终端，运行cat命令获取数据库密码：

![运行cat命令](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpassword-websoft9.png)

#### Windows系统

对于Windows系统来说，数据库密码存储在您的服务器指定文件中：*`c:/credentials/password.txt`*

服务器的桌面上会有打开数据库密码文件的快捷方式

### 数据库账号和管理

不同的数据库有一定的差异，参考下表：

| 名称                    | 用户名     | 可视化管理地址           |
| ----------------------- | ---------- | ------------------------ |
| MySQL/Mariadb PHP环境中 | root       | http://服务器公网IP:9090 或 http://服务器公网IP/phpmyadmin |
| MySQL/Mariadb 其他      | root       | http://服务器公网IP:9090       |
| PostgreSQL              | postgres   | http://服务器公网IP:9090       |
| Mongodb                 | adminmongo | http://服务器公网IP:9091       |
| Oracle                  | system     | 暂无                     |
| SQLServer               | sa         | 使用客户端管理           |



## 操作系统

Azure平台中，操作系统的账号和密码是创建虚拟机的时候自行设置的。图示：

![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-vmsetpw-websoft9.png)

其中，身份验证类型包括：密码和SSH公钥（秘钥对）两种方式。