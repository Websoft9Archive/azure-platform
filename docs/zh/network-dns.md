# 域名

申请域名，解析域名等通用技术，本文档不会讨论。

这里我们介绍一个Azure比较实用的域名功能：Azure针对于每个虚拟机提供了DNS服务。

当VM配置的是动态IP时，每次重启VM，IP地址都可能会发生变化，导致需要重新解析域名，给运维带来不必要的麻烦。Azure的DNS功能，就是帮我们避免这个问题的。

1. 在Azure门户打卡虚拟机->概述，找到DNS名称，点击“配置”
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-opendns-websoft9.png)
2. 输入DNS标签，例如：mysite，点击保存
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-setdns-websoft9.png)
3. 设置完成之后，通过域名：mysite.centralus.cloudapp.azure.com 就可以访问这台VM