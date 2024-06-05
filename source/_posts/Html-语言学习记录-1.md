---
title: Html 语言学习记录 day 1
date: 
tags: Html
categories: 学习记录
---
# Html 语言学习记录 day 1
## Html 简介
HTML 全称为 HyperText Markup Language，译为超文本标记语言。
超文本的含义:
&emsp;（1）图片，视频，音频等超出文本限制的内容
&emsp;（2）超级链接文本，可以跳转文件
HTML 不是一种编程语言，是一种描述性的标记语言。
&emsp;（1）标记语言是一套标记标签。比如：标签`<a>`表示超链接、标签`<img>`表示图片、标签`<h1>`表示一级标题等等，它们都是属于 HTML 标签。
&emsp;（2）编程语言是有编译过程的，而标记语言没有编译过程，HTML标签是直接由浏览器解析执行。
## Html结构解析
Html标签通常成对出现，比如`<div>`和`/div`，成为双边标记;也有部分单标签，如`<br/>`,`<hr/>`，称为单边标记
html骨架结构:
|标签名|定义|说明|
|---|---|---|
|`<html></html>`|Html标签|最大的标签，即根标签|
|`<head></head>`|文档头部|包含title标签|
|`<title></title>`|文档标题|网页标题|
|`<body></body>`|文档主体|文档的所有页面内容|

vscode快速生成网页骨架：`html:5`

    网页骨架示例
    <!DOCTYPE html>
    #文档声明头，告知浏览器文档使用哪种 HTML 或 XHTML 规范。
    <html lang="en">
    #指定页面语言类型，zh-CN中文，en英文
    <head>
        <meta charset="UTF-8">
        #网页编码方式
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        #viewport表示表示视口宽度等于屏幕宽度。
        <meta name="Keywords" content="娱乐,女性,亚运,论坛,短信" />
        #定义网站关键词，对接搜索引擎，提高搜索命中率
        <meta http-equiv="refresh" content="3;http://www.baidu.com">
        #3秒后自动跳转网页
        <title>Document</title>
        #网站标题
        <base href="https://www.baidu.com/" target="_blank">
        #为页面上所有来链接指定默认url和默认目标
    </head>
    <body>
        
    </body>
    </html>
**`<body>`标签**
- `bgcolor`: 设置整个网页的背景颜色
- `background`: 设置整个网页的背景图片
- `text`: 设置网页中文本颜色
- `leftmargin`: 网页左边距，ie默认8个像素
- `topmargin`: 网页上边距
- `rightmargin`: 网页右边距
- `bottommargin`: 网页下边距

**html**基本语法特性
（1）html对换行和tab不敏感，只在乎标签的嵌套结构.
（2）空白折叠，所有文字之间的空格，换行，tab都会被折叠成一个空格
（3）标签要严格封闭,即双边标记需要完整
## 排版标签
### 标题标签
标题使用`<h1>`-`<h6>`进行定义，`<h1>`最大标题，`<h6>`最小标题，具有属性align(对齐方式)，属性值可以为left，center，right。
代码示例

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <h1>H1：却因浊酒恋风尘</h1>
        <h2>H3：却因浊酒恋风尘</h2>
        <h3>H3：却因浊酒恋风尘</h3>
        <h4>H4：却因浊酒恋风尘</h4>
        <h5>H5：却因浊酒恋风尘</h5>
        <h6>H6：却因浊酒恋风尘</h6>
    </body>
    </html>
### 注释
格式如下
`<!-- 此处是注释 -->`
### 段落

`<p>`,paragraph,为双边标记，同样具有属性align(对齐方式)，属性值可以为left，center，right。

代码示例

    <p>paragraph one </p>
    <p>paragraph two </p>

html标签分等级
（1）文本级标签：p，span，a，b，i，e，u，em，文本级标签中只能放文字，图片，表单元素（a标签中不能放a和input）
（2）容器级标签：div，h，li，dt，dd，容器级标签中可以放任何东西
例如：p标签中不能放入h标题标签
### 分隔线
`<hr>`，horizontal，为单边标记，具有属性aligin，size，width，color，noshade
### 换行
`<br/>`为单边标记
### 分割
`<div>`，为双边标记，可以把标签中的内容分割为独立的区块，必须单独占一行
`<soan>`，和`<div>`的作用一致，但是不换行

    <body>
        <div>
            div标签1
        </div>
        <div>
            div标签2
        </div>
        <span>
            span标签1
        </span>
        <span>
            span标签2
        </span>
    </body>

### 内容居中标签
`<center>`，为双边标记，所有放在标签中的内容都会居中
### 预定义标签
`<center>`，保留标签中所有空白字符，原封不动输出结果
### 字体标签
特殊字符，参照https://tool.chinaz.com/tools/htmlchar.aspx
- `<u>`：下划线
- `<s>`或`<del>`：删除线
- `<i>`或`<em>`：斜体
- `<sup>`：上标
- `<sub>`：下标
### 超链接
（1）外部链接
`<a href='example.html'>点击进入example文件</a>`
`<a href="http://www.baidu/com" target="_black">点击进入百度</a>`
（2）锚链接
创立一个锚点，用`name`或`id`属性为特定的位置起一个名字，然后在底部的超链接进行跳转，即`#name`

    <body>
        <a name="name1">顶部</a>
        <pre>


        </pre>
        <a href="#name1">回到顶部</a>
    </body>
如果改为
`<a href="a.html#name">回到顶部<\a>`
就意味着点击之后跳转到`a.html`页面中的`name1`锚点
（3）邮件链接
`<a href="mailto:xxx@qq.com">邮箱</a>`
超链接的属性如下
- `href`：目标url
- `title`：悬停文本
- `name`：设置一个锚点的名称
- `target`：告诉浏览器用什么方式打开目标界面
    - `_self`:在同一个网页显示（默认值）
    - `_blank`:在新窗口打开
    - `_parent`:在父窗口中显示
    - `_top`:在顶级窗口中显示
### 图片标签

