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

## Hexo 内置标签

### codeblock

{% codeblock struct_test https://www.hao123.com hao123 lang:cpp mark:1,4-7,10 %}
typedef struct {
uint8_t edge_padding_flag; ///< 0: disable, 1: enable
uint8_t padding_value_r; ///< r or y
uint8_t padding_value_g; ///< g or u
uint8_t padding_value_b; ///< b or v
uint32_t edge_top; ///< top edge in pixel
uint32_t edge_bottom; ///< bottom edge in pixel
uint32_t edge_left; ///< left edge in pixel
uint32_t edge_right; ///< right edge in pixel
EdgePaddingTypeUint32_t edge_padding_type; ///< only EDGE_PADDING_TYPE_CONSTANT valid
} image_edge_padding_t; // corresponding to copyMakeBorder in openCV.
{% endcodeblock %}
