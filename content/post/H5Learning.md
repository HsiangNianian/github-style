---
title: "H5Learning"
date: 2023-09-26T00:11:56+08:00
draft: false
summary: '初步学习H5'
tags:
    - HTML
katex: math
mathJax: true
---

## 为何开始学习前端?

我一直在注意着 go-cqhttp 与 Mirai 这两个"无头 QQ 客户端"的发展, 同时也时刻留意着 QQ 官方的更新动态, 半年前我得知除了 Watch 手表协议外的协议 bot 基本都下线了, 而这样做的目的我想可能是 Tencent 官方想要把大家驱赶到 Watch 手表协议后再一网打尽吧。

2022 年 12 月 30 日, 腾讯推出基于 NT 架构的全新 Linux QQ 并正式上线官网, 版本号 3.0.0。

之后每次发送消息都需要握手通信, 因此大批 bot 又因为发送消息没有认证挂了, 好在之后出现了 qsign 服务器，暂时缓解了这样的签名认证带来的极大危害。~~(只是现在 qsign 也停更了)~~

我开始寻找其它可以平替 QQ 的平台, 这样我就可以把 HydroRoll 部署在上面, 权衡了 Discord, Telegram, DoDo, KOOK(原 kaiheila), Fanbook 等一系列聊天平台的利与弊之后, 我最终妥协于 KOOK, 并开始为 iamai 编写 KOOK 的适配器。

... ...

这很遭罪, 我忍受不了 KOOK 的各种失败设计, 所以我才开始着手规划一个网页聊天 bot 框架——事实上这是去年冬天就有的想法, 因为我原本便是打算让 HydroRoll 也能够在网页上工作。

> HTML5 是如何起步的？
HTML5 是 W3C 与 WHATWG 合作的结果,WHATWG 指 Web Hypertext Application Technology Working Group。

WHATWG 致力于 web 表单和应用程序，而 W3C 专注于 XHTML 2.0。在 2006 年，双方决定进行合作，来创建一个新版本的 HTML。

HTML5 中的一些有趣的新特性：

 - 用于绘画的 canvas 元素
 - 用于媒介回放的 video 和 audio 元素
 - 对本地离线存储的更好的支持
 - 新的特殊内容元素，比如 article、footer、header、nav、section
 - 新的表单控件，比如 calendar、date、time、email、url、search

## 最小的HTML文档

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>文档标题</title>
</head>
 
<body>
文档内容......
</body>
 
</html>
```