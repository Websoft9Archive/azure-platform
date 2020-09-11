# 故障处理

下面列出最常见的故障或设置错误导致的问题。

如果您已经明确问题原因是云服务器产生的，那么请直接阅读[Azure虚拟机故障排查](https://docs.microsoft.com/zh-cn/azure/virtual-machines/troubleshooting/)。

#### SFTP无法登录？

检查账号和密码是正确，请保证[服务器安全组](/zh/network-safegroup.md)的22端口是开启的

#### Windows远程桌面连接失败？

检查账号和密码是正确，请保证[服务器安全组](/zh/network-safegroup.md)的3389端口是开启的

#### 服务器无法重启？

请联系Azure官方修复

#### http://公网IP 无法打开软件的初始化界面？

检查是否安装了所需的软件，请保证[服务器安全组](/zh/network-safegroup.md)的80端口是开启的

#### 基于VHD磁盘创建VM失败？

如果VHD中包含云市场镜像，那么创建VM会报错，报错信息大意是没有包含云市场的plan。需要模板的虚拟机属性中加入云市场镜像的计划，例如：

```
"plan": {
                "name": "wordpress52-lemp72-centos76",
                "publisher": "websoft9inc",
                "product": "w9wordpress2"}
```

设置 Plan 之前，需通过 PowerShell 命令获取 plan

```
PS Azure:\> az vm image list --offer w9wordpress2 --all --output table
Offer         Publisher    Sku                          Urn                                                             Version
------------  -----------  ---------------------------  --------------------------------------------------------------  ---------
w9wordpress2  websoft9inc  wordpress52-lemp72-centos76  websoft9inc:w9wordpress2:wordpress52-lemp72-centos76:5.2.20000  5.2.20000
```