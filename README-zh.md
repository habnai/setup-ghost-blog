﻿# Ghost 博客平台一键安装脚本 &nbsp;[![Build Status](https://static.ls20.com/travis-ci/setup-ghost-blog.svg)](https://travis-ci.org/hwdsl2/setup-ghost-blog)

*其他语言版本: [English](README.md), [简体中文](README-zh.md).*

使用 Bash 脚本一键搭建你自己的 <a href="https://github.com/TryGhost/Ghost" target="_blank">Ghost 博客平台</a>。为了最佳化性能与安全性，将同时安装 <a href="http://nginx.org/en/" target="_blank">Nginx</a> (作为反向代理)，以及 Web 应用防火墙 <a href="https://www.modsecurity.org/" target="_blank">ModSecurity</a> 或者 <a href="https://github.com/nbs-system/naxsi" target="_blank">Naxsi</a>。

Ghost 博客是一个简约并且现代的<a href="https://ghost.org/vs/wordpress/" target="_blank"> WordPress 替代品</a>。它设计精美，使用方便，完全开源，并且对所有人都是免费的。

**新：** 在你的服务器上安装 **最多 10 个博客**！只需再次运行脚本，并指定新的完整域名作为参数。

<a href="https://blog.ls20.com/install-ghost-0-3-3-with-nginx-and-modsecurity/" target="_blank">**&raquo; 相关教程： Ghost Blog Auto Setup with Nginx and ModSecurity**</a> <a href="https://blog.ls20.com/install-ghost-0-4-with-nginx-and-naxsi-on-ubuntu/" target="_blank">**(or Naxsi)**</a>

## 系统要求

一个专用服务器或虚拟专用服务器 (VPS)，**全新安装** 以下系统：   
- Ubuntu 16.04 (Xenial), 14.04 (Trusty) or 12.04 (Precise)
- Debian 8 (Jessie)

**注：** 需要至少 **512 MB** 内存。

:warning: **不要** 在你的 PC 或者 Mac 上运行这些脚本！它们只能用在服务器上！

## 安装说明

首先，更新你的系统： 运行 `apt-get update && apt-get dist-upgrade` 并重启。这一步是可选的，但推荐。

#### 选择 ModSecurity 防火墙：

```
wget https://git.io/ghost-nginx-modsecurity -O ghost-nginx-modsecurity.sh
sudo bash ghost-nginx-modsecurity.sh BLOG_FULL_DOMAIN_NAME
```

#### 选择 Naxsi 防火墙：

```
wget https://git.io/ghost-nginx-naxsi -O ghost-nginx-naxsi.sh
sudo bash ghost-nginx-naxsi.sh BLOG_FULL_DOMAIN_NAME
```

**注：** 请将上面的 `BLOG_FULL_DOMAIN_NAME` 替换为你的博客的完整域名。这些脚本将会自动安装 <a href="https://github.com/TryGhost/Ghost/releases" target="_blank">最新版本</a> （除了 beta）的 Ghost 博客平台。

## 作者

**Lin Song** (linsongui@gmail.com)   
- 最后一年的美国在读博士生，专业是电子与计算机工程 (ECE)
- 现在正在积极寻找新的工作机会，比如软件或系统工程师
- 在 LinkedIn 上与我联系： <a href="https://www.linkedin.com/in/linsongui" target="_blank">https://www.linkedin.com/in/linsongui</a>

## 授权协议

版权所有 (C) 2015-2016&nbsp;Lin Song&nbsp;&nbsp;&nbsp;<a href="https://www.linkedin.com/in/linsongui" target="_blank"><img src="https://static.licdn.com/scds/common/u/img/webpromo/btn_viewmy_160x25.png" width="160" height="25" border="0" alt="View my profile on LinkedIn"></a>    
基于 <a href="https://blog.igbuend.com/dude-looks-like-a-ghost/" target="_blank">Herman Stevens 的工作</a> （版权所有 2013）

特别感谢 <a href="https://raymii.org" target="_blank">Remy van Elst</a> 和 <a href="https://philio.me" target="_blank">Phil Bayfield</a> 提供有益的建议。

本程序为自由软件，在自由软件联盟发布的<a href="https://www.gnu.org/licenses/gpl.html" target="_blank"> GNU 通用公共许可协议</a>的约束下，你可以对其进行再发布及修改。协议版本为第三版或（随你）更新的版本。   
我们希望发布的这款程序有用，但不保证，甚至不保证它有经济价值和适合特定用途。详情参见GNU通用公共许可协议。   
你理当已收到一份GNU通用公共许可协议的副本，如果没有，请查阅 <http://www.gnu.org/licenses/>   