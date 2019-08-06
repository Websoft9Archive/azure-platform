# 重置

在一些特殊情况下，用户打算将VM恢复到初始状态，但希望保留所有VM的配置选项和关联资源均保留。这个时候，我们就需要用到“重新部署”的操作。

1. 选择想要重新部署的 VM，然后选择“设置”边栏选项卡中的“重新部署”按钮。 可能需要向下滚动，查看包含“重新部署”按钮的“支持和故障排除” 部分，如以下示例所示：
   ![重新部署](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetstart-websoft9.png)
   
2. 若要确认该操作，请选择“重新部署”按钮：

   ![确认重置](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetbutton-websoft9.png)

3. VM 准备好重新部署时，该 VM 的“状态”会更改为“正在更新” ，如以下示例所示：
   ![正在更新](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetupdate-websoft9.png)

4. VM 在新的 Azure 主机上启动时，“状态”将更改为“正在启动”，如以下示例所示：
   ![正在启动](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetstarting-websoft9.png)

5. VM 完成启动过程后，“状态”返回到“正在运行” ，这表示 VM 已成功重新部署：
   ![正在运行](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetruning-websoft9.png)