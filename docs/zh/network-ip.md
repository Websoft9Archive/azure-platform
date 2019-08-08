# 公网IP地址

## 查看

1. 登录Azure控制台
2. 打开要查看公网IP的虚拟机，我们会看到公网IP地址项
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-publicip-websoft9.png)
3. 如果虚拟机没有公网IP地址项（或为空），就需要参考下一个小节挂载一个公网IP

## 挂载

当创建的虚拟机没有公网IP地址，只要有空闲（或新购）的公网IP地址，Azure控制台是可以给虚拟机挂载上公网IP地址的。具体操作步骤如下：

1. 登录到Azure控制台
2. 打开所需的虚拟机，查看：网络->网络接口
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-networkinterface-websoft9.png)

2. 在网络接口详情操作中，打开设置->IP配置，点击ipconfig1项
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-ipconfig-websoft9.png)

3. 对ipconfig1进行已有公网IP挂载操作
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-ipconfig1-websoft9.png)
4. 如果没有公网IP可选，可以新建一个
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-createip-websoft9.png)

## 静态IP
创建虚拟机默认选项是创建动态IP，你也可以选择创建静态IP
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-createstaticip-websoft9.png)