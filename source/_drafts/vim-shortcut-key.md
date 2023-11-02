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

### 3.7 行内文本样式 text

1. 带 {% u 下划线 %} 的文本
2. 带 {% emp 着重号 %} 的文本
3. 带 {% wavy 波浪线 %} 的文本
4. 带 {% del 删除线 %} 的文本
5. 键盘样式的文本 {% kbd command %} + {% kbd D %}
6. 密码样式的文本：{% psw 这里没有验证码 %}

### 3.8 行内文本 span

- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% span red, 红色 %}、{% span yellow, 黄色 %}、{% span green, 绿色 %}、{% span cyan, 青色 %}、{% span blue, 蓝色 %}、{% span gray, 灰色 %}。
- 超大号文字
  文档「开始」页面中的标题部分就是超大号文字。
  {% span center logo large, Volantis %}
  {% span center small, A Wonderful Theme for Hexo %}

### 3.9 note

{% note 'fab fa-cc-visa' flat %}你是刷 Visa 还是 UnionPay{% endnote %}

{% note blue 'fas fa-bullhorn' flat %}2021 年快到了....{% endnote %}

{% note pink 'fas fa-car-crash' flat %}小心开车 安全至上{% endnote %}

{% note red 'fas fa-fan' flat%}这是三片呢？还是四片？{% endnote %}

{% note orange 'fas fa-battery-half' flat %}你是刷 Visa 还是 UnionPay{% endnote %}

{% note purple 'far fa-hand-scissors' flat %}剪刀石头布{% endnote %}

{% note green 'fab fa-internet-explorer' flat %}前端最讨厌的浏览器{% endnote %}

### 3.10 tip

{% tip %}default{% endtip %}
{% tip info %}info{% endtip %}
{% tip success %}success{% endtip %}
{% tip error %}error{% endtip %}
{% tip warning %}warning{% endtip %}
{% tip bolt %}bolt{% endtip %}
{% tip ban %}ban{% endtip %}
{% tip home %}home{% endtip %}
{% tip sync %}sync{% endtip %}
{% tip cogs %}cogs{% endtip %}
{% tip key %}key{% endtip %}
{% tip bell %}bell{% endtip %}
{% tip fa-atom %}自定义 font awesome 图标{% endtip %}

### 3.11 动态标签

{% tip warning faa-horizontal animated-hover %}warning{% endtip %}
{% tip ban faa-flash animated-hover %}ban{% endtip %}

### 3.12 checkbox

{% checkbox 纯文本测试 %}
{% checkbox checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% checkbox red, 支持自定义颜色 %}
{% checkbox green checked, 绿色 + 默认选中 %}
{% checkbox yellow checked, 黄色 + 默认选中 %}
{% checkbox cyan checked, 青色 + 默认选中 %}
{% checkbox blue checked, 蓝色 + 默认选中 %}
{% checkbox plus green checked, 增加 %}
{% checkbox minus yellow checked, 减少 %}
{% checkbox times red checked, 叉 %}

### 3.13 单选列表 radio

{% radio 纯文本测试 %}
{% radio checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% radio red, 支持自定义颜色 %}
{% radio green, 绿色 %}
{% radio yellow, 黄色 %}
{% radio cyan, 青色 %}
{% radio blue, 蓝色 %}

### 3.14 timeline

{% timeline 时间轴样式,blue %}

<!-- timeline 2020-07-24 [2.6.6 -> 3.0](https://github.com/volantis-x/hexo-theme-volantis/releases) -->

1. 如果有 `hexo-lazyload-image` 插件，需要删除并重新安装最新版本，设置 `lazyload.isSPA: true`。
2. 2.x 版本的 css 和 js 不适用于 3.x 版本，如果使用了 `use_cdn: true` 则需要删除。
3. 2.x 版本的 fancybox 标签在 3.x 版本中被重命名为 gallery 。
4. 2.x 版本的置顶 `top: true` 改为了 `pin: true`，并且同样适用于 `layout: page` 的页面。
5. 如果使用了 `hexo-offline` 插件，建议卸载，3.0 版本默认开启了 pjax 服务。

<!-- endtimeline -->

<!-- timeline 2020-05-15 [2.6.3 -> 2.6.6](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.6) -->

不需要额外处理。

<!-- endtimeline -->

<!-- timeline 2020-04-20 [2.6.2 -> 2.6.3](https://github.com/volantis-x/hexo-theme-volantis/releases/tag/2.6.3) -->

1. 全局搜索 `seotitle` 并替换为 `seo_title`。
2. group 组件的索引规则有变，使用 group 组件的文章内，`group: group_name` 对应的组件名必须是 `group_name`。
3. group 组件的列表名优先显示文章的 `short_title` 其次是 `title`。

<!-- endtimeline -->

{% endtimeline %}

### 3.15 inlineimage

这是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/0000.gif %} 一段话。

这又是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/5150.gif, height=40px %} 一段话。

### 3.16 audio

{% audio https://github.com/volantis-x/volantis-docs/releases/download/assets/Lumia1020.mp3 %}

### 3.17 video

{% videos, 2 %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% endvideos %}

### 3.18 folding

{% folding 查看图片测试 %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% folding cyan open, 查看默认打开的折叠框 %}

这是一个默认打开的折叠框。

{% endfolding %}

{% folding green, 查看代码测试 %}
假装这里有代码块（代码块没法嵌套代码块）
{% endfolding %}

{% folding yellow, 查看列表测试 %}

- haha
- hehe

{% endfolding %}

{% folding red, 查看嵌套测试 %}

{% folding blue, 查看嵌套测试2 %}

{% folding 查看嵌套测试3 %}

hahaha <span><img src='https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/tieba/%E6%BB%91%E7%A8%BD.png' style='height:24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}

### 3.19 tabs

{% tabs test4,2 %}

<!-- tab 第一个Tab -->

**tab 名字为第一个 Tab**

<!-- endtab -->

<!-- tab @fab fa-apple-pay -->

**只有图标 没有 Tab 名字**

<!-- endtab -->

<!-- tab 炸弹@fas fa-bomb -->

**名字+icon**

<!-- endtab -->

{% endtabs %}

### 3.20 alibaba icon

{% icon icon-rat_zi %}{% icon icon-rat,2 %}

{% icon icon-ox_chou,3 %}{% icon icon-ox,4 %}

{% icon icon-tiger_yin,5 %}{% icon icon-tiger,6 %}

{% icon icon-rabbit_mao,1 %}{% icon icon-rabbit,2 %}

{% icon icon-dragon_chen,3 %}{% icon icon-dragon,4 %}

{% icon icon-snake_si,5 %}{% icon icon-snake,6 %}

{% icon icon-horse_wu %}{% icon icon-horse,2 %}

{% icon icon-goat_wei,3 %}{% icon icon-goat,4 %}

{% icon icon-monkey_shen,5 %}{% icon icon-monkey,6 %}

{% icon icon-rooster_you %}{% icon icon-rooster,2 %}

{% icon icon-dog_xu,3 %}{% icon icon-dog,4 %}

{% icon icon-boar_hai,5 %}{% icon icon-boar,6 %}

### 3.21 气泡注释 bubble

最近我学到了不少新玩意儿（虽然对很多大佬来说这些已经是旧技术了），比如 CSS 的{% bubble 兄弟相邻选择器,"例如 h1 + p {margin-top:50px;}" %}，{% bubble flex布局,"Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性","#ec5830" %}，{% bubble transform变换,"transform 属性向元素应用 2D 或 3D 转换。该属性允许我们对元素进行旋转、缩放、移动或倾斜。","#1db675" %}，animation 的{% bubble 贝塞尔速度曲线,"贝塞尔曲线(Bézier curve)，又称贝兹曲线或贝济埃曲线，是应用于二维图形应用程序的数学曲线。一般的矢量图形软件通过它来精确画出曲线，贝兹曲线由线段与节点组成，节点是可拖动的支点，线段像可伸缩的皮筋","#de4489" %}写法，还有今天刚看到的{% bubble clip-path,"clip-path属性使用裁剪方式创建元素的可显示区域。区域内的部分显示，区域外的隐藏。","#868fd7" %}属性。这些对我来说很新颖的概念狠狠的冲击着我以前积累起来的设计思路。

### 3.22 reference

Akilar の糖果屋(akilar.top)是一个私人性质的博客{% referto '[1]','Akilarの糖果屋群聊简介' %}，从各类教程至生活点滴，无话不谈。建群的目的是提供一个闲聊的场所。博客采用 Hexo 框架{% referto '[2]','Hexo中文文档' %}，Butterfly 主题{% referto '[3]','Butterfly 安装文档(一) 快速开始' %}

本项目参考了 Volantis{% referto '[4]','hexo-theme-volantis 标签插件' %}的标签样式。引入`[tag].js`，并针对`butterfly`主题修改了相应的`[tag].styl`。在此鸣谢`Volantis`主题众开发者。
主要参考内容包括各个 volantis 的内置标签插件文档{% referto '[5]','Volantis文档:内置标签插件' %}
Butterfly 主题的各个衍生魔改{% referto '[6]','Butterfly 安装文档:标签外挂（Tag Plugins' %}{% referto '[7]','小弋の生活馆全样式预览' %}{% referto '[8]','l-lin-font-awesome-animation' %}{% referto '[9]','小康的butterfly主题使用文档' %}

{% referfrom '[1]','Akilarの糖果屋群聊简介','https://jq.qq.com/?_wv=1027&k=pGLB2C0N' %}
{% referfrom '[2]','Hexo中文文档','https://hexo.io/zh-cn/docs/' %}
{% referfrom '[3]','Butterfly 安装文档(一) 快速开始','https://butterfly.js.org/posts/21cfbf15/' %}
{% referfrom '[4]','hexo-theme-volantis 标签插件','https://volantis.js.org/v5/tag-plugins/' %}
{% referfrom '[5]','Volantis文档:内置标签插件','https://volantis.js.org/tag-plugins/' %}
{% referfrom '[6]','Butterfly 安装文档:标签外挂（Tag Plugins','https://butterfly.js.org/posts/4aa8abbe/#%E6%A8%99%E7%B1%A4%E5%A4%96%E6%8E%9B%EF%BC%88Tag-Plugins%EF%BC%89' %}
{% referfrom '[7]','小弋の生活馆全样式预览','https://lovelijunyi.gitee.io/posts/c898.html' %}
{% referfrom '[8]','l-lin-font-awesome-animation','https://github.com/l-lin/font-awesome-animation' %}
{% referfrom '[9]','小康的butterfly主题使用文档','https://www.antmoe.com/posts/3b43914f/' %}

### 3.23 旋转相册 carousel

{% carousel 'SF','strike freedom' %}
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110444226.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110508327.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110525753.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110600751.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110621554.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110637459.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110654150.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110707916.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110719787.png)
![](https://npm.elemecdn.com/akilar-candyassets/image/20200907110731118.png)
{% endcarousel %}
