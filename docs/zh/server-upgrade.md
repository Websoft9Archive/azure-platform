# 系统更新

更新操作系统，有两种方案。一种是启动Azure控制台门户的更新管理解决方案，另外一种是手动方案。

## Azure门户更新

Azure提供一套完整的[自动更新管理方案](https://aka.ms/updatemanagement)，

1. 登录Azure门户，点击操作下面的“更新管理”。
2. 为此VM启用更新

![启用更新管理](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-enableupdate-websoft9.png)
3. 耐心等待，系统会创建更新解决方案。点击“安全更新部署”开始设置自动更新策略
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-updateset-websoft9.png)

## 系统中更新

所谓系统中是指通过登录到VM，通过输入更新命令或操作更新功能而实现更新，区别于Azure门户的更新管理功能。

### Linux更新

Linux服务器的更新，只需要运行一条更新命令，即可安装大部分更新

```shell
#CentOS or Redhat
sudo yum update -y

#Ubuntu
apt update && apt upgrade -y
```

实际上，Websoft9提供的镜像已经将以上更新命令通过计划任务定期执行。

### Windows更新

Windows服务器的更新与本地电脑类似，手动找到更新管理程序，设置自动下载自动更新即可。