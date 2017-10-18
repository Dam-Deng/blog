title: WEB 浏览器模式 DOCTYPE
date: 2017-08-21 21:49:32
author: dam
tags: DOCTYPE
---

# DTD (document type definition)

获取兼容模式：
```
document.compatMode
// BackCompat：标准兼容模式未开启（Standards-compliant mode）
// CSS1Compat：标准兼容模式已开启。
```

没有写DOCTYPE的都以怪异模式渲染。  
<DOCTYPE html>是严格模式

# 混杂模式/怪异模式/Quirks Mode
1. IE盒子模型：box.width = content.width + padding + border
2. vertical-align 属性默认取值为 bottom，因此，在图片底部会有几像素的空间。
3. table 单元格中字体的 font-size，font-style，font-weight 属性不会继承 body，只有 family 属性会被继承。
4. span和p这些 non-replaced inline 元素可以自定义宽度和高度
5. 元素的百分比高度不能正确应用
6. overflow：visible 子元素溢出的时候，父元素会调整高度，以适应子元素

# 准标准模式/Almost Standards Mode
与标准模式非常类似，表格单元格内垂直方向布局渲染差异。

# 标准模式/严格模式/Standards Mode/Strict Mode
1. W3C 标准盒模型: box.width = content.width
2. vertical-align 属性默认取值为 baseline。
3. table所有font属性都会继承body的。
4. span和p这些 non-replaced inline 元素不可以自定义宽度和高度
5. 元素的百分比高度可以正确应用
6. overflow：visible 子元素溢出的时候，父元素不会调整高度，子元素会溢出


# 冷知识
我们可以发现针对 HTML5 规范而设计的页面（如含有<audio>、<video>、<canvas>等标签）在 IE5Quirks 下是不能正确显示的，但是在 IE10 Quirks 下完全可以正确显示。也就是说，IE10 Quirks 是为了在那些针对 HTML5 设计，但是又没有添加 doctype(可以决定浏览器工作在哪种模式下，后面会详细讨论)的页面而存在的。


```
<meta http-equiv="X-UA-Compatible" content="IE=Edge" >
```
IE 最新版本的 Standards
一般情况下 x-ua-compatible 是优先于 doctype 的设定的，但是当 x-ua-compatible 设定了如“EmulateIExx”的情况时，就会同样考虑到 doctype 的影响。