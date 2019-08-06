# 词汇表

#### Azure Portal

Azure Portal（Azure门户） 就是云控制台，用户创建、管理云资源，查看成本费用的后台门户。

![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-portal-websoft9.png)



#### Azure PowerShell

官方解释：Azure PowerShell 提供一组可以使用 [Azure 资源管理器](https://docs.microsoft.com/zh-cn/azure/azure-resource-manager/resource-group-overview)模型管理 Azure 资源的 cmdlet。 Azure PowerShell 使用了 .NET Standard，这使得它可用于 Windows、macOS 和 Linux。 还可以在 Azure Cloud Shell 中使用 Azure PowerShell。

通俗解释：Azure PowerShell 就是Powershell+Azure模块（Az），就是安装了PowerShell的Windows本地电脑上再安装一个Az模块即可运行Azure PowerShell

#### Azure CLI

官方解释：Azure 命令行接口 (CLI) 是用于管理 Azure 资源的 Microsoft 跨平台命令行体验。 Azure CLI 易于学习，是构建适用于 Azure 资源的自定义自动化功能的完美工具。

通俗解释：Azure CLI是一套客户端命令程序，支持在Windows,Linux,macOS,Azure Cloud Shell上安装，安装完成之后可以使用统一的命令语法操作Azure的云资源，这就是所谓的跨平台。

#### Virtual Machines (VM)

VM=云服务器=实例

#### DNS

DNS (domain name server)，简单的说就是将域名解析成IP地址的服务

#### Azure Marketplace

Azure Marketplace（Azure云市场） 是Azure构建的销售第三方伙伴提供的软件和解决方案的市场平台

#### Port

Port（端口）是计算机网络中的通信端点。 这可以是硬件端口，逻辑端口或两者。 TCP和UDP端口由其端口号（0到65535之间的整数）标识

#### Secure Shell (SSH)

SSH是一种加密网络协议，用于在基于应用层和传输层的不安全网络上安全地操作网络服务。SSH 是目前较可靠，专为远程登录会话和其他网络服务提供安全性的协议

#### Secure Shell key pair (SSH key pair)

SSH key pair（秘钥对）可用于远程登录VM实例的身份验证方法。 SSH密钥对是通过加密算法生成的一对密钥：一个密钥是公共可用的（公钥），另一个密钥是保密的（私钥）。

如果已将公钥放在Linux实例中，则可以使用私钥通过本地计算机或其他没有密码的实例使用SSH命令或相关工具登录实例。

#### Snapshot

Snapshot（快照）是某个时间点磁盘上的数据副本。 有两种类型的快照，自动快照和用户创建的快照。

#### SFTP

SFTP（SSH文件传输协议）是一种安全的文件传输协议。 它运行在SSH协议上。 它支持SSH的完整安全性和身份验证功能。

#### Security Group

Security Gourp (安全组) 是用于管理网络端口访问的一序列协议在组合。

#### VHD

VHD（Azure托管磁盘是虚拟硬盘）。 您可以将其视为本地服务器中的物理磁盘。 Azure托管磁盘存储为页面blob，它是Azure中的随机IO存储对象。 我们称托管磁盘为“托管”，因为它是对页面blob，blob容器和Azure存储帐户的抽象。 使用托管磁盘，您所要做的就是配置磁盘，Azure负责其余部分。

#### Data disk

Data disk（数据盘）区别于系统盘，故名思议是用于存放数据的硬盘

#### OS disk

OS Disk（系统盘）故名思议是用于启动操作系统的磁盘，同时只要容量足够，系统盘也可以存放数据