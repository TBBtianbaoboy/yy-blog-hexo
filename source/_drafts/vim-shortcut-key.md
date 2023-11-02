---
title: Hexo Bufferfly 标签外挂汇总
date: 2023-11-01 19:40:05
tags: hexo_tag
categories: Hexo
keywords: Hexo 标签外挂, Hexo Bufferfly 标签外挂
description:
cover: /img/background.jpg # cover image
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
abcjs:
---

{% note primary %}
`[ ]` 中的参数是可选的，`< >` 中的参数是必选的。
{% endnote %}

## 1 Hexo 原生标签外挂

### 1.1 代码块

Hexo 有两种方式在文章中插入代码块, 这两种方式呈现相同的效果。

1. codeblock

> 别名: code

**语法**

```md
{% codeblock [title] [link_url] [link_text] [lang:language] [mark:line_number] %}
code snippet
{% endcodeblock %}

title: 代码块的标题
link_url: 代码块标题的链接
link_text: 代码块标题的链接文本
lang: 代码块的语言
mark: 高亮代码块的行号或行号范围
```

**举例**

```md
{% codeblock 标题 https://github.com Github lang:cpp mark:1,3-4 %}
#include <iostream>
int main(){
std::cout << "demo" << std::endl;
return 0;
}
{% endcodeblock %}
```

**预览**

{% codeblock 标题 https://github.com Github lang:cpp mark:1,3-4 %}
#include <iostream>
int main(){
std::cout << "demo" << std::endl;
return 0;
}
{% endcodeblock %}

2. 反引号

**语法**

````md
```[language] [title] [link_url] [link_text]
code snippet
```

title: 代码块的标题
link_url: 代码块标题的链接
link_text: 代码块标题的链接文本
language: 代码块的语言
````

**举例**

````md
```cpp 标题 https://github.com Github
#include <iostream>
int main(){
std::cout << "demo" << std::endl;
return 0;
}
```
````

**预览**

```cpp 标题 https://github.com Github
#include <iostream>
int main(){
std::cout << "demo" << std::endl;
return 0;
}
```

> 个人推荐使用 `反引号` 的方式。

### 1.2 link

### 1.3 iframe

## 2 Hexo Bufferfly 主题标签外挂

### 2.1 button

```md
{% btn <url>,<text>,[icon],[color] [style] [layout] [position] [size] %}

[url] : 链接
[text] : 按钮文字
[icon] : [可選] 圖標
[color] : [可選] 按鈕背景顔色(默認 style 時） 按鈕字體和邊框顔色(outline 時)
default/blue/pink/red/purple/orange/green
[style] : [可選] 按鈕樣式 默認實心
outline/留空
[layout] : [可選] 按鈕佈局 默認為 line
block/留空
[position] : [可選] 按鈕位置 前提是設置了 layout 為 block 默認為左邊
center/right/留空
[size] : [可選] 按鈕大小 larger/留空
```

{% btn https://github.com, Github, fa fa-github, outline block center larger green %}

## 3 第三方插件标签外挂

### 3.1 link

{% link 糖果屋教程贴, https://akilar.top/posts/615e2dec/, https://cdn.jsdelivr.net/gh/Akilarlxh/akilarlxh.github.io/img/siteicon/favicon.ico %}

### 3.2 notation

{% nota 把鼠标移动到我上面试试 ,可以看到注解内容出现在顶栏 %}

### 3.3 poem

{% poem 水调歌头,苏轼 %}
丙辰中秋，欢饮达旦，大醉，作此篇，兼怀子由。
明月几时有？把酒问青天。
不知天上宫阙，今夕是何年？
我欲乘风归去，又恐琼楼玉宇，高处不胜寒。
起舞弄清影，何似在人间？

转朱阁，低绮户，照无眠。
不应有恨，何事长向别时圆？
人有悲欢离合，月有阴晴圆缺，此事古难全。
但愿人长久，千里共婵娟。
{% endpoem %}

### 3.4 progress

{% progress 10 red 进度条样式预览 %}
{% progress 30 yellow 进度条样式预览 %}
{% progress 50 green 进度条样式预览 %}
{% progress 70 cyan 进度条样式预览 %}
{% progress 90 blue 进度条样式预览 %}
{% progress 100 gray 进度条样式预览 %}

### 3.5 sitegroup

{% sitegroup %}
{% site xaoxuu, url=https://xaoxuu.com, screenshot=https://i.loli.net/2020/08/21/VuSwWZ1xAeUHEBC.jpg, avatar=https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png, description=简约风格 %}
{% site inkss, url=https://inkss.cn, screenshot=https://i.loli.net/2020/08/21/Vzbu3i8fXs6Nh5Y.jpg, avatar=https://cdn.jsdelivr.net/gh/inkss/common@master/static/web/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site MHuiG, url=https://blog.mhuig.top, screenshot=https://i.loli.net/2020/08/22/d24zpPlhLYWX6D1.png, avatar=https://cdn.jsdelivr.net/gh/MHuiG/imgbed@master/data/p.png, description=这是一段关于这个网站的描述文字 %}
{% site Colsrch, url=https://colsrch.top, screenshot=https://i.loli.net/2020/08/22/dFRWXm52OVu8qfK.png, avatar=https://cdn.jsdelivr.net/gh/Colsrch/images/Colsrch/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site Linhk1606, url=https://linhk1606.github.io, screenshot=https://i.loli.net/2020/08/21/3PmGLCKicnfow1x.png, avatar=https://i.loli.net/2020/02/09/PN7I5RJfFtA93r2.png, description=这是一段关于这个网站的描述文字 %}
{% endsitegroup %}

### 3.6 button

1. 如果需要显示类似「团队成员」之类的一组含有头像的链接：

   {% btns circle grid5 %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% endbtns %}

2. 或者含有图标的按钮：

   {% btns rounded grid5 %}
   {% cell 下载源码, /, fa fa-download %}
   {% cell 查看文档, /, fa fa-book %}
   {% endbtns %}

3. 圆形图标 + 标题 + 描述 + 图片 + 网格 5 列 + 居中

   {% btns circle center grid5 %}
   <a href='https://apps.apple.com/cn/app/heart-mate-pro-hrm-utility/id1463348922?ls=1'>
   <i class='fab fa-apple'></i>
   <b>心率管家</b>
   {% p red, 专业版 %}
   <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_pro.png'>
   </a>
   <a href='https://apps.apple.com/cn/app/heart-mate-lite-hrm-utility/id1475747930?ls=1'>
   <i class='fab fa-apple'></i>
   <b>心率管家</b>
   {% p green, 免费版 %}
   <img src='https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/qrcode/heartmate_lite.png'>
   </a>
   {% endbtns %}
