# minecraftctl

[![GitHub](https://img.shields.io/github/license/MemoryShadow/minecraftctl)](LICENSE)
[![language support](https://img.shields.io/badge/language%20support-i18n-success)](https://github.com/MemoryShadow/minecraftctl/tree/i18n)
[![Build/release](https://github.com/MemoryShadow/minecraftctl/actions/workflows/main.yml/badge.svg?branch=master)](https://github.com/MemoryShadow/minecraftctl/actions/workflows/main.yml)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg)](https://github.com/RichardLitt/standard-readme)
[![GitHub release (latest by date)](https://img.shields.io/github/downloads/MemoryShadow/minecraftctl/latest/total)](https://github.com/MemoryShadow/minecraftctl/releases/latest)

这是一个Minecraft服务端管理工具, 此工具用于帮助运维人员减少重复的操作，帮助他们更加轻松的工作，在保证几乎为0的占用前提下无需修改服务端文件即可支持:  
  后台运行，快速下载部署，启动，停止，重启，备份，恢复备份，向玩家发送消息，监控玩家消息并响应(beta)

在支持这些功能的前提下, 本工具本身带来的占用极小, 经测试, 常驻后台部分仅占用约1M内存(实际上用不到这么多), 其他部分更少, 能有效的为您节约服务器资源.

除去极低的占用外, 本工具能与CI或是其他的程序紧密的贴合, 例如:

1. 本项目的CI就是使用本工具进行的测试  
  通过本工具, 我们能够在CI中实现自动化测试与部署, 从而实现自动化运维. 我们还能为其他程序提供基础的CI支持, 例如在本项目的CI中, 我们就为项目[pyCraft](https://github.com/MemoryShadow/pyCraft/ "点击查看")设计了[基础功能的测试](https://github.com/MemoryShadow/minecraftctl/blob/e1c6e89241e255d9e867083c62a5aa924b6bd447/.github/workflows/main.yml#L256 "点击查看"). 通过这些测试, 我们能够保证项目的稳定性, 从而为用户提供更好的体验.

当然, 语言也是必不可少的, 本项目编写了I18n支持, 欢迎各位参照[如何贡献](#如何贡献)章节参与到我们的翻译工作中来, 您也可以直接前往[I18n仓库](https://github.com/minecraftctl/I18N "点击前往")来查看或参与我们的翻译进度

项目中还附带了一些实用的功能, 如:

- download模块: 能够帮助您快速下载文件(不限于Minecraft相关).
- install模块: 能帮助您实现高效自动部署, 无需手动下载, 解压, 配置
- start/stop/restart模块: 负责启动服务端, 仅需一条命令即可完成.
- backup模块: 能够高效的备份与差分回档备份

## 用法示例

```bash
[hostname@username ~]$ minecraftctl help
此脚本用于以尽可能简洁的方式对Minecraft服务端进行控制
minecraftctl <功能名称> [可能的参数]

  backup	备份或恢复服务器存档
  download
		分析传入的 URL 并尝试使用找到的最合适的下载方法
  edit  	编辑 minecraftctl 和 minecraft 相关文件
  help  	获取这个帮助菜单
  install  	在 Linux 上自动安装Minecraft服务端
  join  	连接服务器后台控制台
  listen  	听取传入的信息并采取适当的行动
  QQMsg  	获取QQ群消息
  restart  	重启 Minecraft 服务端
  say  		向游戏内发送消息
  start  	启动 Minecraft 服务端
  stop  	停止 Minecraft 服务端
  view  	[测试中]打开一个视图，可以查看服务器的状态的同时操作终端
[hostname@username ~]$
```

## 相关仓库

- [screen](https://git.savannah.gnu.org/cgit/screen.git) — 一个优秀的会话管理工具
- [aric2](https://github.com/aria2/aria2.git) — 一个支持多线程和多协议的下载程序
- [whiptail](https://salsa.debian.org/mckinstry/newt/-/tree/debian/master) - 用于支持whiptail窗口，来实现部分区域的窗口化交互 [文档](https://linux.die.net/man/1/whiptail)

## 项目状态

![ProjectStatus](https://repobeats.axiom.co/api/embed/8af05dfe07fe74bce4691e9cc3bb15e81747bfab.svg)

## 贡献者

[![Contributors](https://contrib.rocks/image?repo=MemoryShadow/minecraftctl)](https://github.com/MemoryShadow/minecraftctl/graphs/contributors)

### 如何贡献

非常欢迎你的加入！[提一个 Issue](https://github.com/MemoryShadow/minecraftctl/issues/new) 或者提交一个 Pull Request。

标准 Readme 遵循 [Contributor Covenant](http://contributor-covenant.org/version/1/3/0/) 行为规范。

### 特别鸣谢

本项目高速下载由[BMCL](https://github.com/bangbang93/BMCL "点击查看详情")项目提供部分加速支持

感谢[bangbang93](https://github.com/bangbang93 "点击前往")与[MCBBS](https://www.mcbbs.net/ "点击前往")为我们的Minecraft之旅提供极高的下载速度

## 展望未来

详见[Issues · 鸽子画饼](https://github.com/MemoryShadow/minecraftctl/issues/3 "点击前往")

## 使用许可

[GPL-3.0](LICENSE) © MemoryShadow
