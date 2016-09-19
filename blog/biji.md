# 基础知识  HTML && CSS
## 一.   HTML标签
### 1. HTML文档结构
```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
  //Html文档头部，重点是针对搜索引擎，浏览器看不到此处的内容
</head>
<body>
  //Html文档的主体部分，浏览器中能看到的内容都在此处
</body>
</html>
```
### 2. 块元素（block）
特点：有大小，未指定宽度则宽度自适应，能产生布局，独立成行
- div： 典型的块元素特征
- p：除了具有块元素的特征外，具有上下边距(margin-top/margin-bottom)
- h1、h2、h3、h4、h5、h6：除了具有P标签的所有特性之外，还有具有特定的字	号，并给文字加粗
- ul/ol：除了具有p 标签的特性外，还多了个左填充(padding-left)
- dl：特性同p标签
- dt：特性同div
- dd：比div多了左边距(margin-left)
- Li：同div

### 3. 行级元素（inline）
特点：无大小，不独立成行
- span：典型的行级元素
- a：除了具有行级元素特性外，会使其内部的文字默认颜色变蓝色，同时添加了下划线，在IE浏览器中，a标签内部的图片会有四个边框
- b/strong：除了具有行级元素特性外，使其内部的文字加粗
- i/em：除了具有行级元素特性外，使其内部的文字倾斜

### 4. 行级块元素/内联块（inline-block）
特点：不独立成行，但有大小；
主要有img、input
### 5. 行.块转换
- 行转块  ： display: block;
- 块转行  ： display:inline;
- 块转行块： display:inline-block;

### 6. 列表
有序列表
```js
<ol>
    <li>音乐ol</li> //    1.音乐
    <li>视频ol</li> //    2.视频
    <li>图片ol</li> //    3.图片
</ol>
```
<ol>
    <li>音乐ol</li>
    <li>视频ol</li>
    <li>图片ol</li>
</ol>
无序列表
```js
<ul>
    <li>音乐ul</li> //    .音乐
    <li>视频ul</li> //    .视频
    <li>图片ul</li> //    .图片
</ul>
```
<ul>
    <li>音乐ul</li>
    <li>视频ul</li>
    <li>图片ul</li>
</ul>
定义列表
```js
<dl>
    <dt>标签</dt>
    <dd>解释说明</dd>
</dl>
```
<dl>
    <dt>标签</dt>
    <dd>解释说明</dd>
</dl>
### 7. H5新增标签
- header：页面或者某一区块的头部
- footer：页面或者某一区块的底部
- section：页面中的某一区块
- nav：导航或者是链接组
- article：文章
- aside：定义内容以外的内容（一般用在侧边栏）
- figure：图文解释说明，常与figcapition联合使用，figcapition是图片的标题
- time/mark/
- video、audio、canvas

## 二. CSS样式：selector {css样式}
### 1. 选择器
- 	标签选择器：通过标签的名称来选择，例如：p{ }
- 	类选择器 / class选择器：.class值 {  }，一个文档中可以有多个同名的class, 例如：.wrap{ }
- 	Id选择器：#id值 {  }，在一个html文档中id值不能重复,例如：#nav { }
- 	后代选择器：E F {  }，E与F分别是一个有效的单一类型的选择器，E是F的祖先级元素，也就是说F是嵌套在E的内部的元素
- 	选择器群组：E,F {   }，E和F共用样式，E和F可以有嵌套关系也可以没有嵌套关系
- 	通配符 ※* {  }，※ *表示html文档中的所有标签*

### 2. CSS样式
#### (1).	文字相关的样式
-	font-family：字体（web安全字体）
-	font-size：字号（默认字号为16px，字号一般不要小于12px）
- color：#ff0000/red   颜色
-	font-weight: bold/bolder,6 00~900加粗，100~500正常,normal	 文字加粗
-	font-style：italic/normal 文字倾斜/正常
-	text-align：left/center/right/justify 文本对齐
-	line-height：行高（1~2倍的字高,em，单行文本垂直居中：line-height=	父级容器的高度）
-	text-indent：首行缩进（值可正可负）
-	text-decoration：underline/overline/line-through/none;
文本装饰   underline = 下划线； overline = 上划线； line-through = 删除； none = 没有文本装饰
-	word-spacing：单词间距 例如：word-spacing:10px;
-	letter-spacing：字母间距，汉字的字间距
-	text-transform：capitalize首字母大写 / uppercase全部大写 / lowercase全部小写 / none对文本不做任何改动
-	white-space：nowrap强制不换行 / normal正常

#### (2).背景相关样式
- background-color：背景色
-	background-image：url( );背景图
-	background-repeat：no-repeat/repeat-x/repeat-y/repeat默认repeat重复
-	background-position：水平 垂直；背景定位   
    水平：left/center/right/数值（值可以正负），
    垂直：top/center/bottom/数值（可正负）
-	background-attachment：fixed固定 / scroll滚动
-	background：#ccc url() no-repeat left center; 缩写
      若同时出现背景色与背景图，图永远在上

#### (3). 列表样式
- list-style-type:none / disc列表符号的类型
- list-style-image:url( )自定义列表符号
- list-style:square 方块 / inside缩写
- list-style-position:inside/outside（默认） 控制列表符号位置

#### (4). 链接伪类
```js
<a href="url">内容</a>
```
url：相对的url，从html文档的位置出发，寻找要链接的目标文件;
	   绝对的url，网址比如，https://www.baidu.com
```js
<img src="url" alt=" ">
```
url：相对url参照的也是html文档的位置

###### 注意：背景样式background-image:url();参照的是css所在的位置
与 a 相关的效果
- a：link  { 默认的链接样式 }
- a：visited { 访问后的样式 }
- a：hover { 鼠标滑过时的样式 }
- a：active { 鼠标按下时的样式 }
一定要注意先后顺序:link  visited  hover  active

#### (5). 定位
position:relative/absolute/fixed/static(默认，正常不变)
  1. 找到绝对定位元素 position:absolute;
  2. 指定参照物，相对定位 position:relative;
  3. left / top / bottom / right
  4. z-index : 10 ;
  5. 固定定位    position : fixed ;  

```js
body{
    position : relative;
}
p{
    position : absolute;
    left : 0;
    top : 0;
    z-index : 10 ;
}
```

###### 注意：使用绝对定位时参照物的指定，只有绝对定位元素的祖先级元素才有资格（通常用其父级元素），并指定该元素的position : relative;
#### (6). 布局
- float:left/right/none;  浮动
- clear:left/right/both;  清浮动
- display:block/inline/inline-block/none  行块转换
- overflow:hidden（盒子以外的内容隐藏） / scroll(滚动) / auto(自动) / visible(默认，可见的)

###### 注意：子元素使用 float ,父级元素高度不能自适应，给父级元素添加上 overflow:hidden;   clear:both;  清浮动

#### (7). 表格
border-spacing:数值(左右，上下); 设置单元格间距
border-collapse:collapse;  合并单元格的边
```js
<table>
    <tr>
        <td>第一行第一列</td>
        <td>第一行第二列</td>
    </tr>
    <tr>
        <td>第二行第一列</td>
        <td>第二行第二列</td>
    </tr>
</table>
```

| 第一行第一列     | 第一行第二列    |
| :------------- | :------------- |
| 第二行第一列    | 第二行第二列    |

## 三. csss3
### 1. CSS3选择器
#### (1).  位置：
- first-child/last-child
- :nth-child(n)，n可以是数字，也可以是odd(奇数) / even(偶数)，也可以是	表达式	2n+1

#### (2).  属性选择器：
- a[ href ] , p[ title ];
- a[ href = ”#” ]
- a[ href^ = ”http://” ]{ }; 选择其src属性值以 "http://" 开头的每个a标签
- a[ href$ = ”.pdf” ]{ };  选择其src属性值以 ".pdf" 为结尾的所有a标签
- a[ href* = ”adobe” ]{ }

#### (3). 其他
:first-letter/:first-line
:before/:after
- p : first-letter	选择每个 < p > 元素的首字母。
- p : first-line	选择每个 < p > 元素的首行。
- p : before	在每个 < p > 元素的内容之前插入内容。
- p : after	在每个 < p > 元素的内容之后插入内容。
- p	选择所有 < p > 元素。
- div ， p	选择所有 < div > 元素和所有 < p > 元素。
- div p	选择 < div > 元素内部的所有 < p > 元素。
- div > p	选择父元素为 < div > 元素的所有 < p > 元素。
- div + p	选择紧接在 < div > 元素之后的所有 < p > 元素。

### 2. css3样式
#### (1). 边框
-	border-radius : left-top / right-top / right-bottom / left-bottom;(顺时针顺序)
- border-radius:num;四个圆角一样
- box-shadow:水平距离  垂直距离  模糊度  投影尺寸  颜色  类型；
- 投影描边：box-shadow:0 0 0 2px;在原有的border之外添加了2px的描边效果；

###### 备注：水平与垂直距离可以使用负数，给一个元素指定多个投影，多个投影之间使用逗号隔开，box-shadow : 1px 2px,-2px -2px;
#### (2). 背景
- background-size: 200px 300px ;给固定大小
- background-size: 100% 80% ;(如果只给一个值，则第二个值会为auto)
- background-size: Cover ; 覆盖所有背景区域，图片等比缩放，背景图像的某些部分也许无法显示在背景定位区域中。
- background-size: Contain ; 等比缩放把图像扩展至最大尺寸，以使其宽度或高度完全适应内容区域(不一定完全覆盖背景区域)。
- background-origin：规定背景图片的起始位置 / 设置背景图原点					  
- background-origin：border-box ； 边框盒子
- background-origin：content-box ;  内容盒子
- background-origin：padding-box ;  (默认)
- background-clip:规定背景图的绘制区域，值同上

#### (3). 文本效果
- text-shadow ： 给文字添加一个或多个阴影<br>
- text-shadow: 水平距离 垂直距离 模糊 颜色

###### 备注：如果有多个阴影，俩个阴影之间用逗号隔开；
例如：text-shadow:1px 2px 3px #999,-2px -1px 3px #000;

CSS换行的问题：
- 强制换行：word-wrap : break-word ;
- 强制不换行：white-space : nowrap ;
- 自动换行：word-wrap : normal ;

#### (4). 自定义字体
@font-face  <br>
在线字体格式转换：https://www.fontsquirrel.com/tools/webfont-generator
例如：
```js
<style>
/*定义字体*/
@font-face{
    font-family: myFirstFont;
    src:  url('Sansation_Light.ttf'),
          url('Sansation_Light.eot'), /* IE9+ */
    	  url(“Sansation_Light.svg”),
    	  url(“Sansation_Light.woff”);
}
div{
    font-family:myFirstFont;/*设置字体*/
}
</style>
```
#### (5). 线性渐变：
- background-image : linear-gradient(#f00,#00f) ; (默认颜色从上到下)
- background-image : linear-gradient(left,#f00,#00f) ;从左往右渐变
- left = 90deg  从左往右渐变
- top = 180deg 从上往下渐变
- 60deg 从左上角开始以 60deg 开始渐变

#### (6). 厂商前缀：
-webkit-    谷歌 · 苹果 · 360 · 猎豹<br>
-moz-    火狐<br>
-o-      欧朋<br>
-ms-     IE浏览器
