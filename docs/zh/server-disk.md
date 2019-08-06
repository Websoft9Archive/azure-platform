# 磁盘

对于Azure平台来说，磁盘可以是单独的一种计算资源（单独创建、单独计费、单独管理等），同时也可以被集成到虚拟机，作为其中的一个组件。

Azure的磁盘管理中有几个特殊的概念，下面提前解释：

* 托管磁盘：托管由Azure公共存储来管理
* 非托管磁盘：指磁盘只能由账号下的存储账号来管理，不作为一个独立资源对外
* 存储账号：Azure的后台中提供了存储账号功能，所谓存储账号，即一个可以管理磁盘的入口。

## 数据盘

我们知道数据盘是区别于系统盘的一种磁盘，主要用于存放数据。

### 增加数据盘

1. 登录Azure云控制台，找到所需操作的虚拟机
2. 打开设置->磁盘，点击“添加数据磁盘”
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-addddisk-websoft9.png)
3. 设置数据磁盘规格
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-addddisk2-websoft9.png)
4. 登录到虚拟机，将已经挂载的数据磁盘进行初始化操作，附加到一个文件目录（简单理解为文件夹）
5. 完成增加数据磁盘工作

### 分离数据盘

1. 在左侧菜单中，选择“虚拟机” 。
2. 选择具有要分离的数据磁盘的虚拟机，并单击“停止” 以解除分配 VM。
3. 在虚拟机窗格中，选择“磁盘” 。
4. 在“磁盘” 窗格的顶部，选择“编辑” 。
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-ddiskds-websoft9.png)
5. 在“磁盘” 窗格中，转到要分离的数据磁盘最右侧，并单击![img](https://cdn.nlark.com/yuque/0/2019/png/152462/1562129007083-89bce572-0db3-4202-be1f-5f6dfdeae000.png)分离按钮。
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-ddiskds2-websoft9.png)
6. 删除磁盘后，单击窗格顶部的“保存”。
7. 在虚拟机窗格中，单击“概述” ，并单击窗格顶部的“开始” 按钮重启 VM。

> 磁盘分离后，会保留在存储中，不会删除

## 容量增加

仅当未附加磁盘或取消分配所有者 VM 时，才可调整磁盘大小或更改帐户类型。

![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-ddiskin-websoft9.png)

> 大多数情况下，磁盘只能增加大小，而不能降低大小