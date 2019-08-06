# 备份

我们知道任何人（组织）都无法保证VM永远正常运行状态。假如VM出现无法启动或无法连接的故障，若没有备份会是什么样的后果？这样的教训是否值得尝试？

如果有备份，就能够恢复到备份之时的状态，大大降低损失。

Azure中，控制台门户->存储->保管库服务就是用于备份VM的专项服务：

![保管库](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-backuprs-websoft9.png)



下面我们针对已有VM和创建VM中如何设置备份，分别作出说明

## 已有VM设置

对于已经创建的VM，设置自动备份策略请参考下图

![设置备份](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-backupstart-websoft9.png)

## 创建VM设置

在创建VM之时，我们便可以设置自动备份方式

1. 创建VM，在管理选项卡下备份项，启用备份![启用备份](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-backupmanage-websoft9.png)
2. 选择已经建立的保管库名称 或 新建一个保管库名称，然后设置备份策略
   ![备份策略](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-backuppolicy-websoft9.png)
3. 在预算允许的情况下，提高备份的频次是不错的选择