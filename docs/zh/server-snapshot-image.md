# 快照与镜像

之所以我们把快照和镜像放在一起描述，是因为这两者有一定的关联，甚至说有互生关系。

## 关系

此处不对快照和镜像进行抽像概念描述，只列出如下几个关键信息点：

* 基于磁盘可以创建一个快照。

  快照是对磁盘进行“拍照”，顾名思义就是备份某个时间点磁盘的数据，是一种备份手段

* 基于快照可以创建一个镜像，而镜像无法直接转换成快照。

* 基于镜像可以直接创建一个虚拟机，基于虚拟机也可以直接创建一个镜像

总结：（磁盘-->快照） --> （镜像<-->虚拟机）

## 创建快照

1. 登录到 [Azure 门户](https://portal.azure.com/)。
2. 首先在左上角单击“所有服务” ，找到：计算->快照
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-snapshot-websoft9.png)
3. 在“快照”边栏选项卡中，单击“添加” 或点击“创建快照”
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-createsnapshot-websoft9.png)
4. 根据提示，完成从**源磁盘**到快照的创建过程

## 创建镜像

前面讲过，基于快照可以创建镜像，基于虚拟机也可以创建镜像

### 虚拟机创建镜像

1. 登录到 [Azure 门户](https://portal.azure.com/)。
2. 打开需要创建镜像的虚拟机，点击“捕获”
![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-vmtoimage-websoft9.png)
3. 根据提示完成后续步骤
4. 值得注意的是，捕获操作在创建镜像的同时也会删除虚拟机

### 快照创建镜像

1. 登录到 [Azure 门户](https://portal.azure.com/)。
2. 首先在左上角单击“所有服务” ，找到：计算->快照
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-snapshot-websoft9.png)
3. 系统会列出所有快照
4. 选择所需的快照，对它进行创建镜像操作
