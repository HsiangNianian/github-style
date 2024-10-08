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

# 为何开始学习前端?

我一直在注意着 go-cqhttp 与 Mirai 这两个"无头 QQ 客户端"的发展, 同时也时刻留意着 QQ 官方的更新动态, 半年前我得知除了 Watch 手表协议外的协议 bot 基本都下线了, 而这样做的目的我想可能是 Tencent 官方想要把大家驱赶到 Watch 手表协议后再一网打尽吧。

2022 年 12 月 30 日, 腾讯推出基于 NT 架构的全新 Linux QQ 并正式上线官网, 版本号 3.0.0。

之后每次发送消息都需要握手通信, 因此大批 bot 又因为发送消息没有认证挂了, 好在之后出现了 qsign 服务器，暂时缓解了这样的签名认证带来的极大危害。~~(只是现在 qsign 也停更了)~~

我开始寻找其它可以平替 QQ 的平台, 这样我就可以把 HydroRoll 部署在上面, 权衡了 Discord, Telegram, DoDo, KOOK(原 kaiheila), Fanbook 等一系列聊天平台的利与弊之后, 我最终妥协于 KOOK, 并开始为 iamai 编写 KOOK 的适配器。

... ...

这很遭罪, 我忍受不了 KOOK 的各种失败设计, 所以我才开始着手规划一个网页聊天 bot 框架——事实上这是去年冬天就有的想法, 因为我原本便是打算让 HydroRoll 也能够在网页上工作。

# 我如何开始

其实在此之前我已经写过很多网站了, 但基本都是根据其模板或者现有的源码去魔改。我并没有系统的学习过 HTML 代码以及 TypeScript(我有一些网站是基于 nextjs 这个框架的), 但是我还是凭借之前的编程经验以及自己无可救药的英语改了很多东西, 在此之前我一直把网页制作当做后端来写(我知道这很滑稽, 但是这就是我的所作所为)。

直到我发现没有我想要的现成的网页时, 我知道自己终究是局限了点, 我找了很多 repo, 但是没有一个是我喜欢的。

我一直以来都知道我不懂的是什么——不熟悉 HTML 控件都有哪些, 不懂得何为 CSS, 是的, 我很不懂网页布局。

因此接下来的学习中我也会特别小心以上两点, 这里就先从平易近人的菜鸟教程入手吧。希望我确实能学到点什么。

---

# Day 1

## H5 的基本介绍

> HTML5 是如何起步的？
> HTML5 是 W3C 与 WHATWG 合作的结果,WHATWG 指 Web Hypertext Application Technology Working Group。

WHATWG 致力于 web 表单和应用程序，而 W3C 专注于 XHTML 2.0。在 2006 年，双方决定进行合作，来创建一个新版本的 HTML。

HTML5 中的一些有趣的新特性：

- 用于绘画的 canvas 元素
- 用于媒介回放的 video 和 audio 元素
- 对本地离线存储的更好的支持
- 新的特殊内容元素，比如 article、footer、header、nav、section
- 新的表单控件，比如 calendar、date、time、email、url、search

![web 页面结构](https://www.jyunko.cn/images/Day0101.png)

完整的 HTML 页面应该是包含一个 `声明`, `头部元素`, `可见的页面内容` 三部分组成。

> 啊, `<!DOCTYPE html>` 原来是向浏览器声明要使用哪种 HTML 或 XHTML 规范的意思。大小写不区分, 所以我打算全部大写。

对于中文编码, 需要在 `<head>` 内加上 `<meta charset="UTF-8">` 标签。

有趣的是, 所有换行都被当做了空格。

## 附录

[**最小的HTML文档**](https://www.jyunko.cn/assets/H5Learning/Day01/01.html)

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

---

# Day 2

## 基本属性

`class` 是可以多个的, 但是 `id` 只能有一个，这点有点类似 `Python`。

| 属性  | 描述                                                          |
| ----- | ------------------------------------------------------------- |
| class | 为html元素定义一个或多个类名（classname）(类名从样式文件引入) |
| id    | 定义元素的唯一id                                              |
| style | 规定元素的行内样式（inline style）                            |
| title | 描述了元素的额外信息 (作为工具条使用)                         |


`<hr>` 可以用于创建水平线。
`<h1>-<h6>` 标题有六级。
`<br>` 用于折行。
`<p>` 段落的行数依赖于浏览器窗口的大小。如果调节浏览器窗口的大小，将改变段落中的行数。
`<b>` 是加粗。
`<big>` 放大。
`<i>` 斜体。
`<small>` 缩小。
`<sub>` 下标。
`<sup>` 上标。

## 附录

[**标题与字体测试**](https://www.jyunko.cn/assets/H5Learning/Day02/01.html)
[**字符串格式化**](https://www.jyunko.cn/assets/H5Learning/Day02/02.html)

### H5 全局属性

> HTML 全局属性
> `New` : HTML5 新属性。

| 属性                 | 描述                                                       |
| -------------------- | ---------------------------------------------------------- |
| accesskey            | 设置访问元素的键盘快捷键。                                 |
| class                | 规定元素的类名（classname）                                |
| contenteditable`New` | 规定是否可编辑元素的内容。                                 |
| contextmenu`New`     | 指定一个元素的上下文菜单。当用户右击该元素，出现上下文菜单 |
| data`New`            | 用于存储页面的自定义数据                                   |
| dir                  | 设置元素中内容的文本方向。                                 |
| draggable`New`       | 指定某个元素是否可以拖动                                   |
| dropzone`New`        | 指定是否将数据复制，移动，或链接，或删除                   |
| hidden`New`          | hidden 属性规定对元素进行隐藏。                            |
| id                   | 规定元素的唯一 id                                          |
| lang                 | 设置元素中内容的语言代码。                                 |
| spellcheck`New`      | 检测元素是否拼写错误                                       |
| style                | 规定元素的行内样式（inline style）                         |
| tabindex             | 设置元素的 Tab 键控制次序。                                |
| title                | 规定元素的额外信息（可在工具提示中显示）                   |
| translate`New`       | 指定是否一个元素的值在页面载入时是否需要翻译               |