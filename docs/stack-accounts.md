# Username and Password

You can get the credentials of Database and OS from this chapter.

## Database

### Database Password

Getting password from Linux and Windows have some difference

#### Linux

For Linux, the database password is stored in the file of your VM: *`/credentials/password.txt`*. Suggest you log in Azure Portal and use the online SSH terminal to run the the `cat` command to get the password：

![run cat Command](https://libs.websoft9.com/Websoft9/DocsPicture/zh/common/catdbpassword-websoft9.png)

#### Windows

For Window, the database password is stored in the file of your VM:*`c:/credentials/password.txt`*

You can also find the shortcut for password file from the Windows Desktop.

### Database Username and GUI

Different databases have certain differences, refer to the following table:

| Database                    | Username     | GUI           |
| ----------------------- | ---------- | ------------------------ |
| MySQL/Mariadb with PHP | root       | http://Internet IP/phpmyadmin |
| MySQL/Mariadb     | root       | http://Internet IP:9090       |
| PostgreSQL              | postgres   | http://Internet IP:9090       |
| Mongodb                 | adminmongo | http://Internet IP:9091       |
| Oracle                  | system     | NO                     |
| SQLServer               | sa         | SQLServer Management Studio,one Desktop client     |



## OS

You should set your username of VM any time you creating a new VM, it means there no default username for VM

![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-vmsetpw-websoft9.png)

The authentication type includes: password and SSH public key (key pair).