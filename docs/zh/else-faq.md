# FAQ

#### 虚拟机的登录账号是什么？

虚拟机账号和密码是用户在创建虚拟机的时候，自行设置的。参考[连接Linux](/zh/server-login.md)和[连接Windows](/zh/server-loginwin.md)

#### 数据库账号密码是什么？

数据库账号密码默认存放在服务器中，参考本文档的[账号密码-数据库](/zh/stack-accounts.md)章节

#### 如何给存储配置CDN？

创建CDN，然后再CDN中绑定存储账号即可

#### 如何启用Linux系统的root账号？

Azure默认情况下，root账号是没有启用的，实际上我们可以想办法启用它。

参考：[连接Linux-示例2 启用root账号](/zh/server-login.md)

#### 如何上传文件到服务器？

对于Windows来说，远程桌面登录到服务器后，通过复制/粘贴就可以上传文件

对于Linux来说，通过SFTP连接服务器即可管理文件

#### 镜像可以退款吗？

镜像是按时间计费，用半小时就付费半小时费用，用一个小时就付费一个小时...

因此不可以退款，如果不使用镜像，请删除镜像或停止服务器

#### 服务器的IP地址重启后发生变化怎么办？

建议更改为静态IP或为服务器设置一个由Azure提供的DNS

#### Websoft9有免费镜像吗？

我们在Azure的云市场上不提供免费镜像。如果您想免费使用我们的部署包，请通过 [Github](https://github.com/websoft9) 下载我们的自动化脚本，通过Ansible部署。

#### 对于Websoft9的部署包来说，通过Github脚本部署与Azure云市场的镜像部署有区别吗？

部署结果是一样的，只是部署方式不同

#### 如何列出Websoft9在Azure云市场上的所有产品？

通过 [Websoft9镜像库](https://azuremarketplace.microsoft.com/en-us/marketplace/apps?page=1&search=websoft9) 查看我们在Azure上的所有镜像，也可以通过搜索关键字“websoft9”列出

#### 虚拟机上的镜像是否可以更换？

不可以

#### 是否可以使用临时磁盘 (/dev/sdb1) 存储数据？

不要使用临时磁盘 (/dev/sdb1) 存储数据。 它只是用于临时存储。 有丢失无法恢复的数据的风险。

#### 托管磁盘与非托管磁盘有什么区别？

托管磁盘即用户的磁盘属于Azure磁盘集群中的一部分，非托管磁盘是用户存储账号下的磁盘。

#### 创建VM，对用户名和密码有什么格式要求？

Azure有较为明确的要求，具体参考[Azure用户名和密码要求](https://docs.microsoft.com/zh-cn/azure/virtual-machines/linux/faq#what-are-the-username-requirements-when-creating-a-vm)
