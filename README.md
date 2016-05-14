﻿# Ghost Blog Auto Setup Scripts <a href="https://travis-ci.org/hwdsl2/setup-ghost-blog"><img align="right" src="https://travis-ci.org/hwdsl2/setup-ghost-blog.svg?branch=master" alt="Build status" /></a>

*Read this in other languages: [English](README.md), [简体中文](README-zh.md).*

Scripts to install your own <a href="https://github.com/TryGhost/Ghost" target="_blank">Ghost blog</a>, with <a href="http://nginx.org/en/" target="_blank">Nginx</a> (as a reverse proxy) and <a href="https://www.modsecurity.org/" target="_blank">ModSecurity</a> or <a href="https://github.com/nbs-system/naxsi" target="_blank">Naxsi</a> web application firewall for better performance and security.

Ghost is a simple, modern <a href="https://ghost.org/vs/wordpress/" target="_blank">WordPress alternative</a> which puts the excitement back into blogging. It's beautifully designed, easy to use, completely open source, and free for everyone.

**NEW:** You can now install **up to 10** blogs on the same server. Just run the script again with a new full domain name.

#### <a href="https://blog.ls20.com/install-ghost-0-3-3-with-nginx-and-modsecurity/" target="_blank">Link to my blog article with detailed information</a>   

## Requirements

A dedicated server or Virtual Private Server (VPS), with **freshly installed**:   
- Ubuntu 16.04 (Xenial), 14.04 (Trusty) or 12.04 (Precise)
- Debian 8 (Jessie)

Note: A minimum of 512 MB RAM is required.

:warning: **DO NOT** run these scripts on your PC or Mac! They should only be used on a server!

## How To Use

First, update your system with `apt-get update && apt-get dist-upgrade` and reboot. This is optional, but recommended.

### Install with ModSecurity:

```
wget https://github.com/hwdsl2/setup-ghost-blog/raw/master/ghost-nginx-modsecurity.sh -O ghost-nginx-modsecurity.sh
sudo bash ghost-nginx-modsecurity.sh BLOG_FULL_DOMAIN_NAME
```

### Install with Naxsi:

```
wget https://github.com/hwdsl2/setup-ghost-blog/raw/master/ghost-nginx-naxsi.sh -O ghost-nginx-naxsi.sh
sudo bash ghost-nginx-naxsi.sh BLOG_FULL_DOMAIN_NAME
```

Note: Replace `BLOG_FULL_DOMAIN_NAME` above with your actual domain name.

## License

Copyright (C) 2015-2016&nbsp;Lin Song&nbsp;&nbsp;&nbsp;<a href="https://www.linkedin.com/in/linsongui" target="_blank"><img src="https://static.licdn.com/scds/common/u/img/webpromo/btn_viewmy_160x25.png" width="160" height="25" border="0" alt="View my profile on LinkedIn"></a>    
Based on <a href="https://blog.igbuend.com/dude-looks-like-a-ghost/" target="_blank">the work of Herman Stevens</a> (Copyright 2013)

Special thanks to <a href="https://raymii.org" target="_blank">Remy van Elst</a> and <a href="https://philio.me" target="_blank">Phil Bayfield</a> for their helpful suggestions.

This program is free software: you can redistribute it and/or modify it under the terms of the <a href="https://www.gnu.org/licenses/gpl.html" target="_blank">GNU General Public License</a> as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
