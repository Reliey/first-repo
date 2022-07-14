---
title: CSS基础
date: 2021-07-27 11:01:16
tags:
---
[TOC]
# 什么是CSS
* Cascading Stylesheets(层叠样式表)
* 不是编程语言
* 告诉浏览器如何指定样式、布局等

#添加CSS
* 外部样式表
    * CSS保存在.CSS文件中
    * 在HTML中使用`<link>`引用
* 内部样式表
    * 不使用外部CSS文件
    * 将CSS放在HTML`<style>`里
* 内联样式(不推荐)
    * 仅影响一个元素
    * 在HTML元素的style属性中添加

# CSS选择器
<p>Lorem ipsum dolor sit amet</p>
<style>h1{color : red;}</style>

 `<style>h1{color : red;}</style>` <br>
h1: selector<br>
color: Property<br>
red: value<br>
**selector**:

1. 直接引用
2. 添加属性class="名称"
3. 添加id="名称"

<div class="container">
<div class="box1">
    <h2>Hello World</h2>
    <p>Lorem ipsum dolor sit amet</p>
</div></div>
<style>.box1{background-color: antiquewhite;
color: royalblue;border: 5px red solid;border-radius: 20px}</style>
<style>.container{width: 80%;
margin: auto;}</style>
<style>.box2{font-family: Dubai,Helvetica,serif;font-style: italic;font-weight: 800;text-decoration: underline;}</style>
<style>body{background-color: #f4f4f4;color: #555555;
font-size:20;font-weight: normal;font: normal 16px Arial,sans-serif;}</style>
#CSS里的颜色及字体
* 颜色
    * 关键词
        * black,silver,while,etc
    * RGB
        * rgb(255,0,0)
    * RGBA
        * rgb(255,0,0,0.5)
    * 十六进制值
        * #ff0000
    * HSL
        * hsl(0,100%,50%)
    * HSLA
        * hsl(0,100%,50%,0.5)
* 字体
    * 用font-family指定字体
    * font-family: Arial,sans-serif(无衬线)；
        * <div class="box2">Lorem ipsum dolor</div>
    * 由两个或两个以上词组成的字体要加引号
        * font-family: "Times New Roman",monospace(等宽);

# CSS属性
* color,background-color
* font-family字体，font-weight字重，font-style字体风格，font-size大小
* text-decoration下划线等，text-transform大小写
* letter-spacing字母间距，word-spacing词间距

#em与px的对应关系
px 绝对尺寸 em 相对尺寸<br>
1 / 父元素的font-size *需要转换的像素值 = em值

#盒子模型

![alt text](https://www.runoob.com/images/box-model.gif)

Margin(外边距): 清除边框外的区域，外边距是透明的<br>
Border(边框)：围绕在内边距和内容外的边框<br>
Padding(内边距)：清除内容周围的区域，内边距是透明的<br>
Content(内容)：盒子的内容，显示文本和图像<br>
div<br>{width: 300px;<br>border: 25px;<br>padding: 25px;<br>margin: 25px;}<br>
总宽度=300px+50px+50px+50px=450px

* border属性
    * border-style
        * dotted: 定义一个点线边框
        * dashed: 定义一个虚线边框
        * solid : 定义实线边框
        * double: 定义两个边框，宽度和border-width相同
        * groove: 定义3D沟槽边框。效果取决于边框的颜色
        * ridge : 定义3D脊边框
        * inset : 定义一个3D的嵌入边框
        * outset: 定义一个3D的突出边框
    * border-width
        * 可以指定长度值，比如2px或0.1em
        * 或使用三个关键字之一：thick,medium,thin
    * border-color
    * border-radius圆角
    * 单独设置各边<br>
      border-top-style:dotted;<br>
      border-right-style:solid;<br>
      border-bottom-style:dottes;<br>
      border-left-style:solid;<br>
      或<br>
        * border-style:dotted(上),solid(右),double(下),dashed(左);
        * border-style:dotted(上),solid(左右),double(下);
        * border-style:dotted(上下)，solid(左右)；
        * border-style:dotted(上下左右)；
    * 简写属性： border:5px solid red;
* outline属性
    * outline是绘制于元素周围的一条线，位于border外缘的外围
* margin和padding属性
![alt text](https://www.runoob.com/wp-content/uploads/2013/08/VlwVi.png)

# CSS列表
* List
<div class="list">
<ul><li><a href="#">List 1</a></li>
<li><a href="http://www.baidu.com">List 2</a></li>
<li><a href="#">List 3</a></li>
<li><a href="#">List 4</a></li>
<li><a href="#">List 5</a></li></ul></div>
<style>.list li{list-style:square;}
a{color:green;}a:hover{color: cyan;}
a:visit{color:red;}.list li:first-child{background:red;}
.list li:nth-child(3){color:grey;}</style>

# CSS按钮
* background-color,color
* button-hover{}按下去样式
* button-active
<div ><button>Button</button></div>
<style>button{background-color: #f4f4f4;color: blue;padding: 10px 15px;}button:hover{background-color:red;}button:active{background:white;}</style>


#CSS超链接样式
* color
* a:hover{}
* a:visit{}

#CSS浮动
* float:left;
* width:33.3%;
* border: 1px solid #ccc;
* box-sizing(防溢出)：border-box;
* 清除浮动 clear:both;

#CSS定位
* static - 静态定位
* relative - 相对定位
* absolute - 绝对定位
* fixed - 固定定位
* sticky

<div class="position-box"><h1>Heading 1</h1>
<h2>heading 2</h2></div>
<style>.position-box{width: 500px;height: 500px;border: 1px solid black;position: relative;}.position-box h1{position: absolute;top: 50px;}.position-box h2{position: absolute;right: 30px;}</style>

* absolute在没有上下文relative时，是参考当前视窗页面做偏移的
* 按钮固定在某处 fixed<br>
<button id="fixed">button</button>
<style>#fixed{position: fixed;right:n200;bottom: 0;}</style>

