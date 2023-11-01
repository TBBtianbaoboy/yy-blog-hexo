---
title: Hexo 博文撰写方法笔记
date: 2023-11-01 19:40:05
tags: hexo
categories: Hexo
keywords: Hexo博文撰写, Hexo 博文编写方法
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

## 1 Hexo 内置标签

Hexo 内置标签用于在文章中插入相应的内容。

### 1.1 代码块
Hexo 有三种方式在文章中插入代码块, 这三种方式呈现相同的效果。

- codeblock

``` md
{% codeblock [title] [link_url] [link_text] [lang:language] [additional options] %}
code snippet
{% endcodeblock %}
```
- code

``` md
{% code [title] [link_url] [link_text] [lang:language] [additional options] %}
code snippet
{% endcode %}
```

- 反引号

TODO
{% code lang:md %}
``` [language] [title] [link_url] [link_text] 
code snippet
```
{% endcode %}

