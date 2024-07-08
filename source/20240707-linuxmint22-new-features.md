---
title: linuxmint 22 新特性
date: 
author:
  - void-mori
cover: https://static.fosscope.com/articles_img/2024.3.26/cover.png
categories:
  - original
tags:
  - original
authorInfo: |
  本文由 [voidmori](https://github.com/void-mori) 编写，[开源观察](https://fosscope.com/) 荣誉推出。
---

Linuxmint22 新特性

<!-- more -->

# Linuxmint22 新特性


## 新特性概要

-   更好的语言支持
    -   非英语语言的预安装软件包和选择的软件包将在安装结束时删除，节省大量磁盘空间
    -   如果在安装过程中已连接到 Internet，则会下载所选语言的语言包
        -   英语、德语、西班牙语、法语、俄语、葡萄牙语、荷兰语和意大利语的语言包在 ISO 镜像上无需联网
-   对新技术的支持
    -   内核版本为 6.8，Linux Mint 22.x 版本将遵循 HWE 系列
        -   21.x 的内核版本为 5.15，版本比较老
        -   相对于 21.x 版本，新版 linuximint 的 cinnamon 桌面环境已支持 wayland 会话
    -   默认声音服务器切换到 Pipewire
    -   软件源获得了对新 Debian DEB822 格式的支持
    -   主题已更新以支持 GTK4
    -   向 Pix 添加了 JXL 支持，并为其实施了新的缩略图器
    -   使用 libsoup2 的所有软件都迁移到了 libsoup3
    -   在 Plymouth 和 Slick-Greeter 的启动序列中改进了 HiDPI 支持
-   支持热门功能
    -   Thunderbird 继续在 Linux Mint 22 中作为原生 .deb 包提供。在 Ubuntu 决定将其移至 Snap 之后，Linux Mint 现在负责打包它
    -   在 GNOME 46 中，libgoa/libgoa-backend 3.50 迁移到了 GTK4，并且无法再被 GTK3 应用程序使用。这意味着在线帐户支持必须从 Cinnamon、Budgie 和 Unity 中消失。XApp 项目实现了一个名为“GNOME Online Accounts GTK”的独立应用程序。这不仅使该功能在这三个桌面环境中回归，而且还使其可以在MATE和Xfce中使用
    -   在 Ubuntu 24.04 中，许多 GNOME 应用程序迁移到 libAdwaita 并停止支持系统主题，由于选择主题是 Linux Mint（Cinnamon、MATE 和 Xfce）提供的桌面的核心部分，因此应用程序需要支持它，因此，GNOME 字体查看器被删除，以下应用程序降级回 GTK3 版本：Celluloid、GNOME Calculator、Simple Scan、Baobab、System Monitor、GNOME Calendar、File Roller、Zenity
-   软件管理器

    -   mintinstall 的加载速度比以前更快，并且主窗口会立即出现
    -   多线程新能提升，新的首选项页面，新的横幅幻灯片
-   更好的安全性

    -   经过验证的 Flatpaks 现在显示其维护者名称
    -   默认情况下，未经验证的 Flatpaks 处于禁用状态
        -   启用后，这些 Flatpak 会被明确标记为未经验证

    -   警告会提醒与之相关的安全风险
    -   未经验证的 Flatpaks 也没有任何评论，没有评分
-   Matrix

    -   Hexchat 停止维护后，Linux Mint 转向 [Matrix](https://matrix.org/) 聊天网络
        -   Linux Mint 22 附带了一个名为 Matrix 的预安装 Web 应用程序，它会显示入门信息
-   Cinnamon 6.2

    -   nemo actions 现在可以由新的布局编辑器统一管理
    -   可以添加分隔符和子菜单
    -   上下文菜单中可以覆盖标签和图标
    -   错误修复、性能改进
        -   减少打印机添加的通知（静音 2 小时）
        -   Wayland 支持：Clutter polkit 代理
        -   Spices：键绑定支持
        -   polkit 代理和用户组件中更好的头像支持
        -   鼠标中键单击可删除悬停的工作区
        -   通过按键绑定进行搜索的能力
        -   角落栏组件：添加了 Shift+单击操作
-   其他改进

    -   笔记应用程序 Sticky 可以从命令行调用，从而可以轻松配置键绑定以在桌面上创建笔记并与之交互
        -   新创建的笔记的默认位置现在是可配置的

    -   Xed 文本编辑器可以通过单击“编辑”菜单中的 Duplicate 或按 Ctrl+Shift+D 来复制所选文本
        -   新的配置设置控制可设置在关闭最后一个选项卡时是否应退出
        -   显示的最近文件数量从 5 个增加到 10 个

    -   在 Timeshift 中，删除快照现在会弹出一个确认对话框
    -   使用 WebApp Manager 创建的 Firefox Web 应用程序具有更智能的菜单栏和工具栏，默认情况下是隐藏的，但在有用时（例如，当打开选项卡时）可见
    -   在 Xfce 中，xfce4-xapp-status-plugin 托盘小程序具有可配置的全彩和符号图标大小
    -   实现了用于 Gimp 文件的新缩略图器。该软件包称为 xapp-thumbnailer-gimp。它在存储库中可用
    -   ISO 映像现在与文件系统转置模式下的 FAT32 兼容
-   艺术作品改进

    -   桌面壁纸更新
-   主要组件

    -   Linux Mint 22 具有 Linux 内核 6.8 和 Ubuntu 24.04 软件包库
-   长期支持策略
    -   Linux Mint 22 将在 2029 年之前收到安全更新
    -   到 2026 年，Linux Mint 的未来版本将使用与 Linux Mint 22 相同的基础软件包，可以轻松升级
    -   在2026年之前，开发团队不会开始开发新的基础版本，并将完全专注于当前基础版本


