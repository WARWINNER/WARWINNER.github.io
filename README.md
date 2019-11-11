# WARWINNER.github.io
无
---
title: CSS
date: 2019-11-9 17:39
tags:
---



#   									                           CSS

##     一、CSS样式

### 1、CSS背景

​	·使用background-color:属性设置背景颜色（ 如果想让背景色从元素中的文本向外少有延伸，只需增加一些内边距：eg.     p {background-color: gray; padding: 20px;}   ） background-color 不能继承，其默认值是 transparent。

​	·使用background-image属性加入图像背景。插入时须定义URL值。 background-image 也不能继承。事实上，所有背景属性都不能继承。 

​	·使用background-repeat属性在页面上对背景图像进行平铺 。 属性值 repeat 导致图像在水平垂直方向上都平铺，就像以往背景图像的通常做法一样。repeat-x 和 repeat-y 分别导致图像只在水平或垂直方向上重复，no-repeat 则不允许图像在任何方向上平铺。 

​	·使用background-position属性改变图像在背景中的位置。提供属性值：首先，可以使用一些关键字：top、bottom、left、right 和 center。通常，这些关键字会成对出现。还可以使用长度值（ 长度值解释的是元素内边距区左上角的偏移。偏移点是图像的左上角 ），如 100px 或 5cm，最后也可以使用百分数值（ 如果图像位于 0% 0%，其左上角将放在元素内边距区的左上角。如果图像位置是 100% 100%，会使图像的右下角放在右边距的右下角）。 

| **单一关键字** | **等价的关键字**               |
| -------------- | ------------------------------ |
| center         | center center                  |
| top            | top center 或 center top       |
| bottom         | bottom center 或 center bottom |
| right          | right center 或 center right   |
| left           | left center 或 center left     |

​	·使用background-attachment属性固定背景图像（fixed,默认时scroll)。

### 2、CSS文本

​	·使用text-indent属性进行文本缩进。可以使用所有长度单位，包括百分比值，也可以是用负数，但在是用负数时，某些文本可能会超出浏览器窗口的左边界。为了避免出现这种显示问题，建议针对负缩进再设置一个外边距或一些内边距： eg.  p {text-indent: -5em; padding-left: 5em;}。 text-indent 属性可以继承 。

 **注意：**一般来说，可以为所有块级元素应用 text-indent，但无法将该属性应用于行内元素，图像之类的替换元素上也无法应用 text-indent 属性。不过，如果一个块级元素（比如段落）的首行中有一个图像，它会随该行的其余文本移动。 

​	·水平对齐：使用text-align属性， 值 left、right 和 center 会导致元素中的文本分别左对齐、右对齐和居中。  最后一个水平对齐属性是 justify。 

**注意**： text-align:center 与 \<CENTER> 作用大不相同。\<CENTER> 不仅影响文本，还会把整个元素居中。text-align 不会控制元素的对齐，而只影响内部内容。元素本身不会从一段移到另一端，只是其中的文本受影响。  

​	·使用word-spacing属性改变字（单词）之间的标准距离。 word-spacing 属性接受一个正长度值或负长度值。如果提供一个正长度值，那么字之间的间隔就会增加。为 word-spacing 设置一个负值，会把它拉近 。

​	·使用letter-spacing属性改变字符或字母之间的间隔。 

​	·字符转换：text-transform属性处理文本的大小写。属性有四个值：none、uppercase、lowercase、capitalize。 uppercase 和 lowercase 将文本转换为全大写和全小写字符。最后，capitalize 只对每个单词的首字母大写。 

​	·文本装饰：text-decoration属性，五个值：none、underline、overline、line-through、blink。 underline 会对元素加下划线，  overline会在文本的顶端画一个上划线 ， 值 line-through 则在文本中间画一个贯穿线，  blink 会让文本闪烁。

​	· white-space属性会影响到用户代理对源文档中的空格、换行和 tab 字符的处理。  如果将 white-space 设置为 pre ，空白符不会被忽略 。如果 white-space 属性的值为 pre，浏览器将会注意额外的空格，甚至回车。在这个方面，而且仅在这个方面，任何元素都可以相当于一个 pre 元素。nowrap会防止元素中的文本换行，除非使用了一个 br 元素。 

| 值       | 空白符 | 换行符 | 自动换行 |
| -------- | ------ | ------ | -------- |
| pre-line | 合并   | 保留   | 允许     |
| normal   | 合并   | 忽略   | 允许     |
| nowrap   | 合并   | 忽略   | 不允许   |
| pre      | 保留   | 保留   | 不允许   |
| pre-wrap | 保留   | 保留   | 允许     |

### 3、CSS字体

​	·使用font-family 定义文本的字体系列 ，也可以设置更具体的字。

​	·字体风格：font-style 属性最常用于规定斜体文本。该属性有三个值：

 	normal - 文本正常显示

​	 italic - 文本斜体显示

​	 oblique - 文本倾斜显示

​	· font-variant 属性可以设定小型大写字母。 eg.  p {font-variant:small-caps;}

​	·font-weight属性可以设置文本的粗细。 使用 bold 关键字可以将文本设置为粗体。 关键字 100 ~ 900 为字体指定了 9 级加粗度。如果一个字体内置了这些加粗级别，那么这些数字就直接映射到预定义的级别，100 对应最细的字体变形，900 对应最粗的字体变形。数字 400 等价于 normal，而 700 等价于 bold。如果将元素的加粗设置为 bolder，浏览器会设置比所继承值更粗的一个字体加粗。与此相反，关键词 lighter 会导致浏览器将加粗度下移而不是上移。

​	·font-size属性设置文本的大小（1em=16px）

### 4、CSS链接

​	· text-decoration 属性大多用于去掉链接中的下划线。

​	·background-color属性规定链接的背景色。

### 5、CSS列表

​	·使用list-style-type属性改变列表项的标志类型eg. ul {list-style-type : square} 。

​	·使用list-style-image属性使用图像做标志eg. ul li {list-style-image : url(xxx.gif)}

**注**： 为简单起见，可以将以上 2 个列表样式属性合并为一个方便的属性：list-style

### 6、CSS表格

​	·使用border属性设置表格边框（如果原表格有一边框使用border-collapse定义单线条边框)

eg.

```css
table, th, td
  {
  border: 1px solid blue;
  }
```

​	·通过width和height属性定义表格的宽和高度

​	· text-align 和 vertical-align 属性设置表格中文本的对齐方式 。

text-align 属性设置水平对齐方式，比如左对齐、右对齐或者居中：eg.

```css
td
  {
  text-align:right;
  }
```

 vertical-align 属性设置垂直对齐方式，比如顶部对齐、底部对齐或居中对齐：eg.

```CSS
td
  {
  height:50px;
  vertical-align:bottom;
  }
```

​	·使用padding 控制表格中内容与边框的距离 。

### 7、CSS轮廓

| 属性          | 描述                             | CSS  |
| :------------ | :------------------------------- | :--- |
| outline       | 在一个声明中设置所有的轮廓属性。 | 2    |
| outline-color | 设置轮廓的颜色。                 | 2    |
| outline-style | 设置轮廓的样式。                 | 2    |
| outline-width | 设置轮廓的宽度。                 | 2    |

```css
p.one
{
border:red solid thin;
outline-style:solid;
outline-width:thin;
}
p.two
{
border:red solid thin;
outline-style:dotted;
outline-width:3px;
}
```

## 二、CSS框模型

### 1、CSS内边距

​	· padding 属性定义元素的内边距。padding 属性接受长度值或百分比值，但不允许使用负值。  按照上、右、下、左的顺序分别设置各边的内边距，各边均可以使用不同的单位或百分比值：eg.           h1 {padding: 10px 0.25em 2ex 20%;}

​	·通过使用下面四个单独的属性，分别设置上、右、下、左内边距：

padding-top

padding-right

padding-bottom

padding-left

### 2、CSS边框

​	·  border-style 属性定义了 10 个不同的非 inherit 样式，包括 none。 

​	·定义单边样式：

- border-top-style

- border-right-style

- border-bottom-style

- border-left-style

  ·使用border-width指定边框宽度，为边框指定宽度有两种方法：可以指定长度值，比如 2px 或 0.1em；或者使用 3 个关键字之一，它们分别是 thin 、medium（默认值） 和 thick。可以按照 top-right-bottom-left 的顺序设置元素的各边边框 。

  也可以通过下列属性分别设置边框各边的宽度：

  - border-top-width
  - border-right-width
  - border-bottom-width
  - border-left-width

  ·使用border-color属性设置边框颜色， 它一次可以接受最多 4 个颜色值。

  ·定义单边颜色：

- border-top-color

- border-right-color

- border-bottom-color

- border-left-color

  ·透明边框：transparent(颜色值)

  ### 3、CSS外边距

  ​	·使用margin属性（可以设置为auto）设置外边距（顺寻top right bottom left）可以设置百分数。

  ​	·规则：

  - 如果缺少左外边距的值，则使用右外边距的值。
  - 如果缺少下外边距的值，则使用上外边距的值。
  - 如果缺少右外边距的值，则使用上外边距的值。

  ·单边外边距属性：

- margin-top
- margin-right
- margin-bottom
- margin-left

## 三、CSS选择器

## 1、CSS元素选择器

​	· 如果设置 HTML 的样式，选择器通常将是某个 HTML 元素，比如 p、h1、em、a，甚至可以是 html 本身： eg. 

```css
html {color:black;}
h1 {color:blue;}
h2 {color:silver;}
```

### 2、CSS选择器分组

​	· 通配选择器（universal selector），显示为一个星号（*）。该选择器可以与任何元素匹配，就像是一个通配符。 

 	·声名分组：eg.   h1 {font: 28px Verdana; color: white; background: black;}  

**注**： 一定要在各个声明的最后使用分号。

### 3、CSS类选择器

**提示**： **提示：**只有适当地标记文档后，才能使用这些选择器。

​	·修改HTML码： 需要修改具体的文档标记，以便类选择器正常工作。  为了将类选择器的样式与元素关联，必须将 class 指定为一个适当的值。 

eg.

```CSS
<h1 class="important">
This heading is very important.
</h1>
cs
<p class="important">
This paragraph is very important.
</p>
```

​	· 类名前有一个点号（.），然后结合通配选择器： eg.  *.important {color:red;}  (\*为类名如p)

### 4、CSS ID选择器详解

​	· ID 选择器前面有一个 # 号 - 也称为棋盘号或井号。eg.    *#intro {font-weight:bold;}

​	·  #intro {font-weight:bold;}  ID 选择器不引用 class 属性的值它要引用 id 属性中的值。 

​	· 区别：只能在文档中使用一次； ID 选择器不能结合使用，因为 ID 属性不允许有以空格分隔的词列表；ID 能包含更多含义（区分大小写）

### 5、CSS属性选择器详解

​	·简单属性选择器：eg.   

​             *[title] {color:red;}

​             a[href] {color:red;}

​             a\[href][title] {color:red;}

​			 img[alt] {border: 5px solid red;}

​	· 可以进一步缩小选择范围，只选择有特定属性值的元素。 eg.

​			 假设希望将指向 Web 服务器上某个指定文档的超链接变成红色，可以这样写： a[href="http://www.w3school.com.cn/about_us.asp"] {color: red;}

   		   可以把多个属性-值选择器链接在一起来选择一个文档。 a[href="http://www.w3school.com.cn/"][title="W3School"] {color: red;}

​	·根据部分属性值选择: 需要根据属性值中的词列表的某个词进行选择，则需要使用波浪号（~）。 

eg.想选择 class 属性中包含 important 的元素，可以用下面这个选择器做到这一点：

```css
p[class~="important"] {color: red;}
```

​	·子串匹配属性选择器:

| 类型         | 描述                                       |
| ------------ | ------------------------------------------ |
| [abc^="def"] | 选择 abc 属性值以 "def" 开头的所有元素     |
| [abc$="def"] | 选择 abc 属性值以 "def" 结尾的所有元素     |
| [abc*="def"] | 选择 abc 属性值中包含子串 "def" 的所有元素 |

​	·特定属性选择类型：如：  *[lang|="en"] {color: red;}  选择 lang 属性等于 en 或以 en- 开头的所有元素 

### 6、CSS后代选择器

​	·如   h1 em {color:red;} 这个规则会把作为 h1 元素后代的 em 元素的文本变为 红色。其他 em 文本（如段落或块引用中的 em）则不会被这个规则选中 。选择器之间的空格是一种结合符 。

​	· 两个元素之间的层次间隔可以是无限的 。例如，如果写作 ul em，这个语法就会选择从 ul 元素继承的所有 em 元素，而不论 em 的嵌套层次多深。

因此，ul em 将会选择以下标记中的所有 em 元素。

### 7、CSS子元素选择器

​	· 缩小范围，只选择某个元素的子元素

 eg.如果您希望选择只作为 h1 元素子元素的 strong 元素，可以这样写：

```css
h1 > strong {color:red;}
```

 这个规则会把第一个 h1 下面的两个 strong 元素变为红色 , 但是第二个 h1 中的 strong 不受影响 . 子结合符两边可以有空白符，这是可选的。 

### 8、CSS相邻兄弟选择器

​	· 选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器 

eg.  要增加紧接在 h1 元素后出现的段落的上边距，可以这样写：

```css
h1 + p {margin-top:50px;}
```

 选择紧接在 h1 元素后出现的段落，h1 和 p 元素拥有共同的父元素 

相邻兄弟选择器使用了加号（+），即相邻兄弟结合符（Adjacent sibling combinator）。

**注释：**与子结合符一样，相邻兄弟结合符旁边可以有空白符。

​	· 相邻兄弟结合符还可以结合其他结合符。  eg.   html > body table + ul {margin-top:20px;}

### 9、CSS伪类

​	·语法：

```css
selector : pseudo-class {property: value}
```

或与CSS类搭配使用

```CSS
selector.class : pseudo-class {property: value}
```

​	·锚伪类 链接的不同状态都可以不同的方式显示，这些状态包括：活动状态，已被访问状态，未被访问状态，和鼠标悬停状态。 如：

```CSS
a:link {color: #FF0000}		/* 未访问的链接 */
a:visited {color: #00FF00}	/* 已访问的链接 */
a:hover {color: #FF00FF}	/* 鼠标移动到链接上 */
a:active {color: #0000FF}	/* 选定的链接 */
```

**提示：**在 CSS 定义中，a:hover 必须被置于 a:link 和 a:visited 之后，才是有效的。

**提示：**在 CSS 定义中，a:active 必须被置于 a:hover 之后，才是有效的。

**提示：**伪类名称对大小写不敏感。

​	·伪类与CSS类配合使用，eg.

```CSS
a.red : visited {color: #FF0000}

<a class="red" href="css_syntax.asp">CSS Syntax</a>
```

 假如上面的例子中的链接被访问过，那么它将显示为红色。 

​	·使用 first-child伪类来选择元素的第一个子元素 。

eg one.匹配第一个 \<p> 元素

```html
<html>
<head>
<style type="text/css">
p:first-child {
  color: red;
  } 
</style>
</head>

<body>
<p>some text</p>
<p>some text</p>
</body>
</html>
```

eg two.匹配所有 \<p> 元素中的第一个\<i> 元素

```html
<html>
<head>
<style type="text/css">
p > i:first-child {
  font-weight:bold;
  } 
</style>
</head>

<body>
<p>some <i>text</i>. some <i>text</i>.</p>
<p>some <i>text</i>. some <i>text</i>.</p>
</body>
</html>
```

eg three. 匹配所有作为第一个子元素的 \<p> 元素中的所有 \<i> 元素

```html
<html>
<head>
<style type="text/css">
p:first-child i {
  color:blue;
  } 
</style>
</head>

<body>
<p>some <i>text</i>. some <i>text</i>.</p>
<p>some <i>text</i>. some <i>text</i>.</p>
</body>
</html>
```

​	· ：lang类使你有能力为不同的语言定义特殊的规则。 

eg. 

```html
<html>
<head>

<style type="text/css">
q:lang(no)
   {
   quotes: "~" "~"
   }
</style>

</head>

<body>
<p>文字<q lang="no">段落中的引用的文字</q>文字</p>
</body></html>
```

效果： 文字~段落中的引用的文字~文字 

### 10、CSS伪元素

​	· first-line 伪元素用于向文本的首行设置特殊样式。 

**注释：**"first-line" 伪元素只能用于块级元素。

**注释：**下面的属性可应用于 "first-line" 伪元素：

- font

- color

- background

- word-spacing

- letter-spacing

- text-decoration

- vertical-align

- text-transform

- line-height

- clear

  · first-letter"伪元素用于向文本的首字母设置特殊样式： 

**注释：**"first-letter" 伪元素只能用于块级元素。

**注释：**下面的属性可应用于 "first-letter" 伪元素：

- font

- color

- background

- margin

- padding

- border

- text-decoration

- vertical-align (仅当 float 为 none 时)

- text-transform

- line-height

- float

- clear

  ·伪元素和CSS类搭配: eg.

  ```css
  p.article:first-letter
    {
    color: #FF0000;
    }
  
  <p class="article">This is a paragraph in an article。</p>
  ```

 上面的例子会使所有 class 为 article 的段落的首字母变为红色。 

​	·可以结合多个伪元素来使用。eg.

```CSS
p:first-letter
  {
  color:#ff0000;
  font-size:xx-large;
  }

p:first-line
  {
  color:#0000ff;
  font-variant:small-caps;
  }
```

 段落的第一个字母将显示为红色，其字体大小为 xx-large。第一行中的其余文本将为蓝色，并以小型大写字母显示。段落中的其余文本将以默认字体大小和颜色来显示。

​	· ":before" 伪元素可以在元素的内容前面插入新内容。 eg.

```CSS
h1:before
  {
  content:url(logo.gif);
  }
```

​	·":after" 伪元素可以在元素的内容之后插入新内容。 

