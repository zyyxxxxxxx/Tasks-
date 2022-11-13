阶段三     Web相关领域的学习笔记 

一、HTML

1.常用的HTML标签

| 标签       | 功能                     |
| ---------- | ------------------------ |
| <div>      | 分隔                     |
| <p>        | 段落标签                 |
| <a>        | 锚或超链接               |
| <button>   | 定义点击一个按钮         |
| <!--...--> | 定义注释。               |
| <!DOCTYPE> | 定义文档类型。           |
| <html>     | 定义 HTML 文档。         |
| <frame>    | 定义框架集的窗口或框架。 |
| <head>     | 定义关于文档的信息。     |

❤Remark：（1）标签一般都是成对出现的，例如：<div>和</div>。也有单独呈现的标签，如:<img src="百度百科.jpg" />等。一般成对出现的标				          签，其内容在两个标签中间。单独呈现的标签，则在标签属性中赋值。

​						  (2)  始终需要为 <button> 元素规定 type 属性。不同的浏览器对 <button> 元素的 type 属性使用不同的默认值。

​                       （3）<input>和<button>的区别：在 <button> 元素内部，可以放置内容，比如文本或图像。<input> 标签用于搜集用户信息。根据不同  						  的 type 属性值，输入字段拥有很多种形式，可以是文本字段、复选框、掩码后的文本控件、单选按钮、按钮等等。

​					   （4）标签对中的第一个标签是开始标签，第二个标签是结束标签。开始和结束标签也被称为开放标签和闭合标签。

 					  （5）<a> 元素最重要的属性是 href 属性，它指定链接的目标。如果没有使用 href 属性，则不能使用 hreflang、media、rel、target 以及 						 type 属性。

​      				 （6)<div>标签定义 HTML 文档中的一个分隔区块或者一个区域部分,常用于组合块级元素，以便通过 CSS 来对这些元素进行格式化。

2、各类标签中的块级元素与内联元素

（1)块级元素（block）：

| <address> – 地址         | <**blockquote> – 块引用** | <dir> – 目录列表            |
| ------------------------ | ------------------------- | --------------------------- |
| **<div> – 常用块级容易** | **<dl> – 定义列表**       | **<fieldset> – form控制组** |
| **<form>– 交互表单**     | **h1 – h6 标题**          | **<hr> – 水平分隔线**       |
| **<menu>– 菜单列表**     | **<ol >– 有序表单**       | **<p> – 段落**              |
| **<pre> – 格式化文本**   | **<table> – 表格**        | **<ul> – 无序列表**         |

(2)内联元素（inline）:

| **<a>– 锚点**                                 | <abbr> – 缩写           | <b> – 粗体                                |
| --------------------------------------------- | ----------------------- | ----------------------------------------- |
| **<big> – 大字体**                            | **br – 换行**           | **<cite> – 引用**                         |
| **<code> – 计算机代码(在引用源码的时候需要)** | **<em> – 强调**         | **<i> – 斜体**                            |
| **<img> – 图片**                              | **<input> – 输入框**    | **<kbd> – 定义键盘文本**                  |
| **<label> – 表格标签**                        | **<q> – 短引用**        | **<span> – 常用内联容器，定义文本内区块** |
| **<font> – 字体设定**                         | **<strong> – 粗体强调** | **<textarea> – 多行文本输入框**           |

(3)块级元素与内联元素之间的区别

(1)块级元素会独占一行，而内联元素和内联[块元素](https://so.csdn.net/so/search?q=块元素&spm=1001.2101.3001.7020)则会在一行内显示。

(2)块级元素和内联块元素可以设置 width、height 属性，而内联元素设置无效。

(3)块级元素的 width 默认为 100%，而内联元素则是根据其自身的内容或子元素来决定其宽度。

3、HTML标签的样式

1）块级样式：html{ display: block }

2）列表样式：li{ display:list-item }

​					 	ol{list-style-type: decimal }

​						 ol ul, ul ol,ul ul, ol ol  { margin-top: 0; margin-bottom: 0 }

3)标题样式：h1{ font-size:2em; margin: .67em 0 }

​					   h2{ font-size:1.5em; margin: .75em 0 }

4）伪类样式：br:before{ content: ”\A” }

​					     :before, :after{ white-space: pre-line }

​						 :link, :visited { text-decoration: underline }

​     					:focus{ outline: thin dotted invert }

5）表格样式：table{ display: table }

​						 tr{ display:table-row }

​						 thead{ display:table-header-group }



二、CSS

1、这是什么：CSS就是一种叫做样式表（stylesheet）的技术。也有的人称之为“层叠样式表”（Cascading Stylesheet）。

在主页制作时采用CSS技术，可以有效地对页面的布局、字体、颜色、背景和其它效果实现更加精确的控制。

只要对相应的代码做一些简单的修改，就可以改变同一页面的不同部分，或者页数不同的网页的外观和格式。

2、它有什么作用：

1）在几乎所有的浏览器上都可以使用。

（2）以前一些非得通过图片转换实现的功能，现在只要用CSS就可以轻松实现，从而更快地下载页面。

（3）使页面的字体变得更漂亮，更容易编排，使页面真正赏心悦目。

（4）你可以轻松地控制页面的布局 。

（5）你可以将许多网页的风格格式同时更新，不用再一页一页地更新了。你可以将站点上所有的网页风格都使用一个CSS文件进行控制，只要修改这个CSS文件中相应的行，那么整个站点的所有页面都会随之发生变动。

3、CSS的选择器

😊id 选择器：id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 "#" 来定义。

以下的样式规则应用于元素属性 id="para1":

\#para1 {    text-align:center;  

​					  color:red; }

❤Remark：ID属性不要以数字开头，数字开头的ID在 Mozilla/Firefox 浏览器中不起作用。且id值必须为一。

😊通用选择器：用 \* 匹配，样式辐射到全部范围

😊元素选择器：通过元素匹配样式

😊类选择器：采用全局属性 class 进行匹配

4、 CSS的盒模型

<img src="C:\Users\lenovo\Desktop\box-model.gif" style="zoom:80%;" />

🎁盒模型各部分解释：

- **Margin(外边距)** - 清除边框外的区域，外边距是透明的。
- **Border(边框)** - 围绕在内边距和内容外的边框。
- **Padding(内边距)** - 清除内容周围的区域，内边距是透明的。
- **Content(内容)** - 盒子的内容，显示文本和图像。

✨重点： （1）当指定一个 CSS 元素的宽度和高度属性时，不能只是设置内容区域的宽度和高度。因为完整大小的元素，还必须添加内边距，边框和外边距。

  				（2）最终元素的总宽度计算公式是这样的：总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距

​						    元素的总高度最终计算公式是这样的：总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

5、CSS Position(属性指定了元素的定位类型)

1）static：HTML 元素的默认值，即没有定位，遵循正常的文档流对象。同时，静态定位的元素不会受到 top, bottom, left, right影响。

2）fixed：元素的位置相对于浏览器窗口是固定位置，即使窗口是滚动的它也不会移动。

3）relative:相对定位元素的定位是相对其正常位置;移动相对定位元素，但它原本所占的空间不会改变;相对定位元素经常被用来作为绝对定位元素的容器块。

4）absolute:绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于<html>；absolute 定位使元素的位置与文档流无关，因此不占据空间；absolute 定位的元素和其他元素重叠。

5）sticky：粘性定位的元素是依赖于用户的滚动，在 **position:relative** 与 **position:fixed** 定位之间切换。它的行为就像 **position:relative;** 而当页面滚动超出目标区域时，它的表现就像 **position:fixed;**，它会固定在目标位置。

6、CSS的伪类

（1）语法：selector:pseudo-class {property:value;}

​					 selector.class:pseudo-class {property:value;}

（2）类型：anchor伪类：a:link {color:#FF0000;} /* 未访问的链接 */*

​											 a:visited {color:#00FF00;} /* 已访问的链接 */

​						  				   *a:hover {color:#FF00FF;} /* 鼠标划过链接 */*

​									         a:active {color:#0000FF;} /* 已选中的链接 */

​					伪类和CSS类：伪类可以与 CSS 类配合使用：a.red:visited {color:#FF0000;}

 																							    <a class="red" href="css-syntax.html"></a>

​					first-child伪类：在IE8的之前版本必须声明 ，这样 :first-child 才能生效。

​					lang伪类：q:lang(no) {quotes: "~" "~";}

三、Java Script

1、语法--字面量

| Java script                                                  | C语言                            |
| ------------------------------------------------------------ | -------------------------------- |
| **数字（Number）字面量** 可以是整数或者是小数，或者是科学计数(e)。 | 数字的数据类型分为：实型、浮点型 |
| **字符串（String）字面量** 可以使用单引号或双引号            | 字符串最好使用单引号             |
| **表达式字面量** 用于计算：如：5+6                           | 计算只能通过表达式               |
| **数组（Array）字面量** 定义一个数组：[40, 100, 1, 5, 25, 10] | 数组a[6]={40,100,1,5,25,10}      |
| **函数（Function）字面量**：function myFunction(a, b) { return a * b;} | 大致相同                         |

2、JS中的各种数据类型

- 字符串（String）：字符串是存储字符（比如 "Bill Gates"）的变量。字符串可以是引号中的任意文本,可以使用单引号或双引号
- 数字（Number）:JavaScript 只有一种数字类型。数字可以带小数点，也可以不带。极大或极小的数字可以通过科学（指数）计数法来书写。
- 布尔（Boolean）:布尔（逻辑）只能有两个值：true 或 false。
- Null:可以通过将变量的值设置为 null 来清空变量。
- Undefined:Undefined 这个值表示变量不含有值。
- 对象（Object）:例如：{firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}
- 数组（Array）:例如：[40, 100, 1, 5, 25, 10]

❤提醒：当声明新变量时，可以使用关键词 "new" 来声明其类型

三、HTML、CSS、Java Script三者之间的关系

一个基本的网站包含很多个网页，一个网页由html, css和javascript组成。

html是主体，装载各种dom元素；css用来装饰dom元素；javascript控制dom元素。

用一扇门比喻三者间的关系是：html是门的门板，css是门上的油漆或花纹，javascript是门的开关。

四、参考文献

【1】https://www.runoob.com/js/js-syntax.html  菜鸟教程

【2】https://www.bilibili.com/video/BV14S4y1K774/?spm_id_from=333.788   html基础

【3】https://blog.csdn.net/hemiaolin8393/article/details/80557781   HTML、 CSS、 JavaScript三者的关系

【4】https://baike.so.com/doc/5869876-6082735.html     360百科
