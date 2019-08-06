# 订阅

下面简单的对Azure云市场镜像类商品的订阅（购买）做一个说明：

## 方式

订阅=购买，具体的表现形式就是 [部署镜像](/zh/stack-deployment.md)

Azure平台中，由于虚拟机采用的是按小时计费，故镜像采用的是也是按小时计费模式，除此之外没有其他模式。

- 镜像部署到虚拟机后，虚拟机用多长时间=镜像订阅了多长时间
- 需要取消镜像订阅，就需要删除对应的虚拟机
- 虚拟机停止运行，镜像停止计费？

## 费用

Azure云市场中，有免费的镜像，也有收费的镜像。

Websoft9公司在Azure平台中提供都是收费镜像，因为我们的盈利模式就是通过收费，为有意愿付费的客户提供企业级开源镜像以及技术支持服务。

> 如果您希望免费使用我们的产品，请部署我们的Ansible自动化脚本（[Github上的主页](https://github.com/websoft9)）

我们的镜像费用会根据虚拟机CPU核数来灵活定价，一般来说核数越大，价格越高。

以我们发布的Gitlab商品为例，通过商品页面的 Plans+Pricing，列出的Software Cost就是镜像定价

![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-fee-websoft9.png)