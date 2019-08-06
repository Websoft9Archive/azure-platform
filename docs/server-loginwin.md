# 连接Windows

可以通过本地电脑的远程桌面工具 (MSTSC) 连接 Window 服务器，也可是使用Powershell连接。后者是命令操作，这里不展开说明。

下面介绍连接Window服务器的操作步骤：

1. 登录Azure Portal，找到需要登录的服务器的**公网IP地址**
   ![image.png](https://cdn.nlark.com/yuque/0/2019/png/152462/1557627419242-b57de49d-8e87-4c6c-ac60-cf11dd07852f.png)

   

2. 选择一种打开本地电脑远程桌面的方式（三选一）:

- - 打开 **开始菜单** -> **远程桌面连接**
  - 打开 **开始菜单**，输入”mstsc“ ，系统会搜索远程桌面连接工具
  - 通过 **Windows Logo** + **R** 打开系统的命令窗口，输入”mstsc“来启动远程桌面连接工具

3. 打开远程桌面连接，输入公网IP地址

![img](https://cdn.nlark.com/yuque/0/2019/png/152462/1553156688326-e4ccce23-97c5-4c37-861b-864b6b6f3637.png)



4. 通过更多选项，设置默认用户名，例如”Administrator“，并勾选”允许我保存凭据“

![img](https://cdn.nlark.com/yuque/0/2019/png/152462/1553156688333-18a41d09-32d7-4372-9b16-ec3d2fa1f924.png)

5. 点击连接，成功后会看到Windows界面
   ![image.png](https://cdn.nlark.com/yuque/0/2019/png/152462/1556246801720-3aa464d9-b885-4c73-829c-833c818456b6.png)

6. 远程登录后，就可以直接从本地**拷贝**文件，然后**粘贴**文件到服务器上。
7. 如果需要使用FTP，需要自行安装FTP软件（推荐使用FileZilla Server）