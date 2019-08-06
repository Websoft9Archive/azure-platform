# 安全组

安全组是管理VM端口的功能，端口是服务器上应用程序与外部访问出入访问的通道。下面以**开启80端口为例**，为您介绍安全组的使用

1. 打开VM->网络，首先显示的就是安全组配置
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-networkset-websoft9.png)

   

2. 点击“添加入站端口规则”，源端口范围填写*号，目标端口范围填写80，保存后生效
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-safegroup80-websoft9.png)

3. 点击“保存”按钮即可生效