# 创建

下面介绍Azure上虚拟机的创建方式。

创建虚拟机最基本的条件是需要给虚拟机准备一个系统盘的启动模板文件。这个模板文件有两种：一个是我们非常熟悉的镜像，另外一个是VHD（虚拟磁盘）文件。

因此，创建VM也有两种方式：基于镜像创建和基于系统盘创建

## 镜像创建

1. 登录Azure控制台，打开：虚拟机->添加，开始创建虚拟机

2. 创建虚拟机的时候选择合适的镜像（这是最重要的步骤）
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-createvmbyimage-websoft9.png)

   > 镜像来源有：官方镜像、云市场镜像和自定义镜像三种镜像来源。如果自定义镜像来源，磁盘就只能选择托管模式

3. 依次设置账号密码、网络、安全组等配置

4. 查看 + 创建 通过之后，点击“创建”即可

## 系统盘创建

1. 登录Azure控制台，打开“所有资源”，找到一个已经被解除绑定的磁盘
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-createvmbydisk-websoft9.png)
2. 点击这个磁盘，对这个磁盘进行“创建VM”操作
3. 依次设置账号密码、网络、安全组等配置
4. 查看 + 创建 通过之后，点击“创建”即可

## 秘钥对
在创建VM的时候，有些用户喜欢采用秘钥对方式作为登录凭证

![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-createvmsshkey-websoft9.png)

由于Azure需要自行提供SSH public key, 因此需要用户提前准备。

下面以PUTTYGEN(KEY GENERATOR FOR PUTTY ON WINDOWS)为例，说明如何创建SSH public key

1. Download and Install [PUTTYGEN](https://www.ssh.com/ssh/putty/windows/puttygen).

2. Click "Generate"  
![image.png](https://libs.websoft9.com/Websoft9/DocsPicture/en/putty/puttygen-generate-websoft9.png)

3. Public key and Private key is OK, you can copy public to Azure(format starting with "ssh-rsa") ,and Save the public key and private key on your local computer for backups
   ![image.png](https://libs.websoft9.com/Websoft9/DocsPicture/en/putty/puttygen-generatesave-websoft9.png)

4. When connect Linux on your local computer, you can use private key for authentication 