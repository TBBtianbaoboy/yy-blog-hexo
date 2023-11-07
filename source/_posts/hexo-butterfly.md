---
title: Hexo Bufferfly 标签外挂汇总
date: 2023-11-01 19:40:05
tags: hexo_buffergly
categories: Hexo
keywords: Hexo 标签外挂, Hexo Bufferfly 标签外挂
description: 描述了 Hexo Bufferfly 主题以及第三方插件常用的标签外挂使用方法
cover: https://yangyuleng.gitee.io/yyimgs/img/hexo.png # cover image
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

{% note blue 'fas fa-bullhorn' flat %}`[ ]` 中的参数是可选的，`< >` 中的参数是必选的。
{% endnote %}

## Hexo 原生标签外挂

### 代码块

{% folding blue, 展开说明 %}

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

{% endfolding %}

### iframe

{% folding blue, 展开说明 %}
**语法**

```md
{% iframe <url> [width] [height] %}

url : 外链
[width] : 直接使用整数，单位是 pixel。建议使用`100%`，即满屏。
[height] : 直接使用整数，单位是 pixel。建议使用`100%`，即满屏。
```

**举例**

```md
{% iframe //player.bilibili.com/player.html?aid=248141899&bvid=BV12v41157Mb&cid=339791117&page=1 %}
```

**预览**

{% iframe //player.bilibili.com/player.html?aid=248141899&bvid=BV12v41157Mb&cid=339791117&page=1 %}

{% endfolding %}

## Hexo Bufferfly 主题标签外挂

### label

{% folding blue, 展开说明 %}
**语法**

```md
{% label [text] [color=default] %}

color: blue / pink / red / purple / orange / green
```

**举例**

```md
我仿佛{% label 从来没有 blue %} 来过这里。
```

**预览**

我仿佛{% label 从来没有 blue %} 来过这里。

{% endfolding %}

## 第三方插件标签外挂

### link

{% folding blue, 展开说明 %}
**语法**

```md
{% link <标题>, <链接>, [图片链接] %}
```

**举例**

```md
{% link 糖果屋教程贴, https://akilar.top/posts/615e2dec/, https://cdn.jsdelivr.net/gh/Akilarlxh/akilarlxh.github.io/img/siteicon/favicon.ico %}
```

**预览**

{% link 糖果屋教程贴, https://akilar.top/posts/615e2dec/, https://cdn.jsdelivr.net/gh/Akilarlxh/akilarlxh.github.io/img/siteicon/favicon.ico %}

{% endfolding %}

### notation

{% folding blue, 展开说明 %}
**语法**

```md
{% nota <label>,<text> %}

label: 文章中的标签
text: 注解内容
```

**举例**

```md
{% nota 把鼠标移动到我上面试试 ,可以看到注解内容出现在顶栏 %}
```

**预览**

{% nota 把鼠标移动到我上面试试 ,可以看到注解内容出现在顶栏 %}
{% endfolding %}

### poem

{% folding blue, 展开说明 %}

**语法**

```md
{% poem [title],[author] %}
诗词内容
{% endpoem %}

title: 诗词标题
author: 诗词作者
```

**举例**

```md
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
```

**预览**

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
{% endfolding %}

### progress

{% folding blue, 展开说明 %}
**语法**

```md
{% progress <width> <color> <text> %}

width: 进度条进度，取值范围 0-100
color: 进度条颜色，取值范围 red,yellow,green,cyan,blue,gray
text: 进度条右侧的文本
```

**举例**

```md
{% progress 10 red 进度条样式预览 %}
{% progress 30 yellow 进度条样式预览 %}
{% progress 50 green 进度条样式预览 %}
{% progress 70 cyan 进度条样式预览 %}
{% progress 90 blue 进度条样式预览 %}
{% progress 100 gray 进度条样式预览 %}
```

**预览**

{% progress 10 red 进度条样式预览 %}
{% progress 30 yellow 进度条样式预览 %}
{% progress 50 green 进度条样式预览 %}
{% progress 70 cyan 进度条样式预览 %}
{% progress 90 blue 进度条样式预览 %}
{% progress 100 gray 进度条样式预览 %}
{% endfolding %}

### sitegroup

{% folding blue, 展开说明 %}
**语法**

```md
{% sitegroup %}
{% site 标题, url=链接, screenshot=截图链接, avatar=头像链接（可选）, description=描述（可选） %}
{% site 标题, url=链接, screenshot=截图链接, avatar=头像链接（可选）, description=描述（可选） %}
{% endsitegroup %}
```

**举例**

```md
{% sitegroup %}
{% site xaoxuu, url=https://xaoxuu.com, screenshot=https://i.loli.net/2020/08/21/VuSwWZ1xAeUHEBC.jpg, avatar=https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png, description=简约风格 %}
{% site inkss, url=https://inkss.cn, screenshot=https://i.loli.net/2020/08/21/Vzbu3i8fXs6Nh5Y.jpg, avatar=https://cdn.jsdelivr.net/gh/inkss/common@master/static/web/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site MHuiG, url=https://blog.mhuig.top, screenshot=https://i.loli.net/2020/08/22/d24zpPlhLYWX6D1.png, avatar=https://cdn.jsdelivr.net/gh/MHuiG/imgbed@master/data/p.png, description=这是一段关于这个网站的描述文字 %}
{% site Colsrch, url=https://colsrch.top, screenshot=https://i.loli.net/2020/08/22/dFRWXm52OVu8qfK.png, avatar=https://cdn.jsdelivr.net/gh/Colsrch/images/Colsrch/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site Linhk1606, url=https://linhk1606.github.io, screenshot=https://i.loli.net/2020/08/21/3PmGLCKicnfow1x.png, avatar=https://i.loli.net/2020/02/09/PN7I5RJfFtA93r2.png, description=这是一段关于这个网站的描述文字 %}
{% endsitegroup %}
```

**预览**
{% sitegroup %}
{% site xaoxuu, url=https://xaoxuu.com, screenshot=https://i.loli.net/2020/08/21/VuSwWZ1xAeUHEBC.jpg, avatar=https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/avatar/avatar.png, description=简约风格 %}
{% site inkss, url=https://inkss.cn, screenshot=https://i.loli.net/2020/08/21/Vzbu3i8fXs6Nh5Y.jpg, avatar=https://cdn.jsdelivr.net/gh/inkss/common@master/static/web/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site MHuiG, url=https://blog.mhuig.top, screenshot=https://i.loli.net/2020/08/22/d24zpPlhLYWX6D1.png, avatar=https://cdn.jsdelivr.net/gh/MHuiG/imgbed@master/data/p.png, description=这是一段关于这个网站的描述文字 %}
{% site Colsrch, url=https://colsrch.top, screenshot=https://i.loli.net/2020/08/22/dFRWXm52OVu8qfK.png, avatar=https://cdn.jsdelivr.net/gh/Colsrch/images/Colsrch/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site Linhk1606, url=https://linhk1606.github.io, screenshot=https://i.loli.net/2020/08/21/3PmGLCKicnfow1x.png, avatar=https://i.loli.net/2020/02/09/PN7I5RJfFtA93r2.png, description=这是一段关于这个网站的描述文字 %}
{% endsitegroup %}
{% endfolding %}

### button

{% folding blue, 展开说明 %}
**语法**

```md
{% btns 样式参数 %}
{% cell 标题, 链接, 图片或者图标 %}
{% cell 标题, 链接, 图片或者图标 %}
{% endbtns %}

样式参数:
圆角样式：rounded, circle

其他参数:
wide 宽一点的按钮
fill 填充布局，自动铺满至少一行，多了会换行
center 居中，按钮之间是固定间距
around 居中分散
grid2 等宽最多 2 列，屏幕变窄会适当减少列数
grid3 等宽最多 3 列，屏幕变窄会适当减少列数
grid4 等宽最多 4 列，屏幕变窄会适当减少列数
grid5 等宽最多 5 列，屏幕变窄会适当减少列数
```

1. 如果需要显示类似「团队成员」之类的一组含有头像的链接：

   **举例**

   ```md
   {% btns circle grid5 %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% endbtns %}
   ```

   **预览**

   {% btns circle grid5 %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% cell MaraPython, https://marapython.com, https://cdn.jsdelivr.net/gh/sviptzk/HexoStaticFile@latest/avatar.jpg %}
   {% endbtns %}

2. 或者含有图标的按钮：

   **举例**

   ```md
   {% btns rounded grid5 %}
   {% cell 下载源码, /, fa fa-download %}
   {% cell 查看文档, /, fa fa-book %}
   {% endbtns %}
   ```

   **预览**

   {% btns rounded grid5 %}
   {% cell 下载源码, /, fa fa-download %}
   {% cell 查看文档, /, fa fa-book %}
   {% endbtns %}

{% endfolding %}

### 行内文本样式 text

{% folding blue, 展开说明 %}

```md
1. 带 {% u 下划线 %} 的文本
2. 带 {% emp 着重号 %} 的文本
3. 带 {% wavy 波浪线 %} 的文本
4. 带 {% del 删除线 %} 的文本
5. 键盘样式的文本 {% kbd command %} + {% kbd D %}
6. 密码样式的文本：{% psw 这里没有验证码 %}
```

1. 带 {% u 下划线 %} 的文本
2. 带 {% emp 着重号 %} 的文本
3. 带 {% wavy 波浪线 %} 的文本
4. 带 {% del 删除线 %} 的文本
5. 键盘样式的文本 {% kbd command %} + {% kbd D %}
6. 密码样式的文本：{% psw 这里没有验证码 %}
   {% endfolding %}

### 行内文本 span

{% folding blue, 展开说明 %}
**语法**

```md
{% span 样式参数(参数以空格划分), 文本内容 %}

样式参数:
字体: logo, code
颜色: red,yellow,green,cyan,blue,gray
大小: small, h4, h3, h2, h1, large, huge, ultra
对齐方向: left, center, right
```

**举例**

```md
- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% span red, 红色 %}、{% span yellow, 黄色 %}、{% span green, 绿色 %}、{% span cyan, 青色 %}、{% span blue, 蓝色 %}、{% span gray, 灰色 %}。
- 超大号文字
  文档「开始」页面中的标题部分就是超大号文字。
  {% span center logo large, Volantis %}
  {% span center small, A Wonderful Theme for Hexo %}
```

**预览**

- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% span red, 红色 %}、{% span yellow, 黄色 %}、{% span green, 绿色 %}、{% span cyan, 青色 %}、{% span blue, 蓝色 %}、{% span gray, 灰色 %}。
- 超大号文字
  文档「开始」页面中的标题部分就是超大号文字。
  {% span center logo large, Volantis %}
  {% span center small, A Wonderful Theme for Hexo %}
  {% endfolding %}

### note

{% folding blue, 展开说明 %}
**语法**

```md
{% note [color] [icon] [style] %}
Any content (support inline tags too.io).
{% endnote %}

样式参数:
color: default / blue / pink / red / purple / orange / green
icon: 参考 font awesome 图标
style: simple/modern/flat/disabled
```

{% btns circle grid5 %}
{% cell font awesome 图标, https://fontawesome.com/icons, fa-solid fa-font-awesome %}
{% endbtns %}

**举例**

```md
{% note 'fab fa-cc-visa' flat %}你是刷 Visa 还是 UnionPay{% endnote %}

{% note blue 'fas fa-bullhorn' flat %}2021 年快到了....{% endnote %}

{% note pink 'fas fa-car-crash' flat %}小心开车 安全至上{% endnote %}

{% note red 'fas fa-fan' flat%}这是三片呢？还是四片？{% endnote %}

{% note orange 'fas fa-battery-half' flat %}你是刷 Visa 还是 UnionPay{% endnote %}

{% note purple 'far fa-hand-scissors' flat %}剪刀石头布{% endnote %}

{% note green 'fab fa-internet-explorer' flat %}前端最讨厌的浏览器{% endnote %}
```

**预览**

{% note 'fab fa-cc-visa' flat %}你是刷 Visa 还是 UnionPay{% endnote %}

{% note blue 'fas fa-bullhorn' flat %}2021 年快到了....{% endnote %}

{% note pink 'fas fa-car-crash' flat %}小心开车 安全至上{% endnote %}

{% note red 'fas fa-fan' flat%}这是三片呢？还是四片？{% endnote %}

{% note orange 'fas fa-battery-half' flat %}你是刷 Visa 还是 UnionPay{% endnote %}

{% note purple 'far fa-hand-scissors' flat %}剪刀石头布{% endnote %}

{% note green 'fab fa-internet-explorer' flat %}前端最讨厌的浏览器{% endnote %}
{% endfolding %}

### tip

{% folding blue, 展开说明 %}
**语法**

```md
{% tip [样式] %}文本内容{% endtip %}

样式: info, success, error, warning, bolt, ban, home, sync, cogs, key, bell
样式也可以是 font awesome 图标
```

**举例**

```md
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
```

**预览**

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

{% endfolding %}

### checkbox

{% folding blue, 展开说明 %}
**语法**

```md
{% checkbox [参数], 文本（支持简单md） %}

样式: plus, minus, times
颜色: red,yellow,green,cyan,blue,gray
选中状态: checked
```

**举例**

```md
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
```

**预览**

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

{% endfolding %}

### 单选列表 radio

{% folding blue, 展开说明 %}
**语法**

```md
{% radio [参数], 文本（支持简单md） %}

颜色: red,yellow,green,cyan,blue,gray
选中状态: checked
```

**举例**

```md
{% radio 纯文本测试 %}
{% radio checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% radio red, 支持自定义颜色 %}
{% radio green, 绿色 %}
{% radio yellow, 黄色 %}
{% radio cyan, 青色 %}
{% radio blue, 蓝色 %}
```

**预览**

{% radio 纯文本测试 %}
{% radio checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% radio red, 支持自定义颜色 %}
{% radio green, 绿色 %}
{% radio yellow, 黄色 %}
{% radio cyan, 青色 %}
{% radio blue, 蓝色 %}

{% endfolding %}

### timeline

{% folding blue, 展开说明 %}
**语法**

```md
{% timeline [标题],[color] %}

<!-- timeline 时间节点 [标题] -->

正文内容

<!-- endtimeline -->

{% endtimeline %}

color: blue / pink / red / purple / orange / green
```

**举例**

```md
{% timeline 时间轴样式,blue %}

<!-- timeline 2020-04-20 [github](https://github.com) -->

正文内容

<!-- endtimeline -->

{% endtimeline %}
```

**预览**

{% timeline 时间轴样式,blue %}

<!-- timeline 2020-04-20 [github](https://github.com) -->

正文内容

<!-- endtimeline -->

{% endtimeline %}

{% endfolding %}

### inlineimage

{% folding blue, 展开说明 %}
**语法**

```md
{% inlineimage 图片链接, height=高度（可选） %}

高度默认为 20px
```

**举例**

```md
这是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/0000.gif %} 一段话。

这又是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/5150.gif, height=40px %} 一段话。
```

**预览**

这是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/0000.gif %} 一段话。

这又是 {% inlineimage https://cdn.jsdelivr.net/gh/volantis-x/cdn-emoji/aru-l/5150.gif, height=40px %} 一段话。

{% endfolding %}

### audio

{% folding blue, 展开说明 %}
**语法**

```md
{% audio 音频链接 %}
```

**举例**

```md
{% audio https://github.com/volantis-x/volantis-docs/releases/download/assets/Lumia1020.mp3 %}
```

**预览**

{% audio https://github.com/volantis-x/volantis-docs/releases/download/assets/Lumia1020.mp3 %}

{% endfolding %}

### video

{% folding blue, 展开说明 %}
**语法**

```md
{% videos, <列数>, [对齐方式] %}
{% video <链接> %}
{% endvideos %}

或

{% video <链接> %}

对齐方式: left, center, right
列数: 1-4 列
```

**举例**

```md
{% videos, 2 %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% endvideos %}
```

**预览**

{% videos, 2 %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% video https://github.com/volantis-x/volantis-docs/releases/download/assets/IMG_0341.mov %}
{% endvideos %}

{% endfolding %}

### folding

{% folding blue, 展开说明 %}
{% tip info %}支持嵌套使用{% endtip %}
**语法**

```md
{% folding [color] [statu], <标题> %}
折叠内容
{% endfolding %}

color: blue, cyan, green, yellow, red
statu: open 代表打开。
```

**举例**

```md
{% folding cyan, 查看图片测试 %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}
```

**预览**

{% folding cyan, 查看图片测试 %}

![](https://cdn.jsdelivr.net/gh/volantis-x/cdn-wallpaper/abstract/41F215B9-261F-48B4-80B5-4E86E165259E.jpeg)

{% endfolding %}

{% endfolding %}

### tabs

{% folding blue, 展开说明 %}
**语法**

```md
{% tabs <name>, [index] %}

<!-- tab [tab_name] [@icon] -->

tab 内容

<!-- endtab -->

{% endtabs %}

name: 唯一标识符
index: 默认打开哪个 tab, 下标从 1 开始
tab_name: tab 名称
icon: font awesome 图标
```

**举例**

```md
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
```

**预览**

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

{% endfolding %}

### 旋转相册 carousel

{% folding blue, 展开说明 %}
**语法**

```md
{% carousel [Id] , [name] %}
![](/img/1.jpg)
![](/img/2.jpg)
![](/img/3,jpg)
{% endcarousel %}

Id: 相册唯一 ID，用于监测相册鼠标动作。禁止使用中文。同一页内不得出现相同 ID 的 carousel 相册。
name: 相册中间显示的内容，建议用英文单引号包裹。
```

**举例**

```md
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
```

**预览**

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

{% endfolding %}
