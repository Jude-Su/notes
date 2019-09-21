

![GcsSloop Blog](http://gcsblog.oss-cn-shanghai.aliyuncs.com/blog/2019-04-29-072758.jpg?gcssloop)

## meta 标签
- 网站描述信息
 `<meta name="description" content="">`

- 网站的关键词 设置
` <meta name="keywords" content="不凡学院,郑州UI培训,河南郑州UI设计培训,河南郑州前端开发培训,郑州H5培训,郑州WEB前端培训,郑州HTML5前端培训,郑州软件培训">`

## 标题 标签
- 一级标题只能有一个

```
 <h1>一级标题</h1>
 <h2>二级标题</h2>
 <h3>三级标题</h3>
 <h4>四级</h4>
 <h5>五级标题</h5>
 <h6>六级标题</h6>
 ```
 ## 布局标签
 - 两个布局标签 没有语义

 ```
    <!-- 会自动换行 -->
    <div>布局标签</div>
    <div>div标签</div>
    <!-- 同行展示 不会自动换行 -->
    <span>文本内容</span>
    <span>span标签</span>
```
## 转义字符

` 空格 &nbsp; &#160;`
` 小于号 &lt; &#60;`
` 大于号 &gt; &#62;`

##  html需要注意的 问题 
- 注释不能嵌套
- 标签必须完整(双标签)
 - 标签可以嵌套，但要注意语义。
 -   标签的属性必须加双引号
  -  标签属性尽量使用小写

## 图片标签 
`<img src="" alt="">`
    引入路径 
   - 绝对路径(网络绝对路径)  (本地绝对路径)
  - 相对路径
    1. 同级目录 直接引入
    2. 下一级目录 img/bf.png
    3. 上一级目录 ../bf.png

## form 标签
`<form action="" method="GET">`
```
  <!-- action  表单提交的地址 -->
  <!-- method  提交方式   -->
  <!-- get 地址栏会显示 不安全 容量有限  用于获取信息 -->
  <!-- post 不会地址栏显示 相对安全
       提交的数据量没有上限
       一般用于提交保存数据 -->
  ```

## 控件属性

- disabled 禁用
- readonly 只读
- placeholder 占位符提供可描述输入字段预期值的提示信息
- autofocus 元素应该自动获得焦点
- multiple 多文件上传 -->
- checked, selected默认选中 
   `
## 下拉 选择框
- select ,option
 ```  
 <select name="city">
     <option value="0">郑州</option>
     <option value="1">北京</option>
     <option value="2">杭州</option>
</select>
```
## 文件上传

`<input type="file" multiple>`
## 按钮

-  提交 `<input type="submit"> `
- 重置 `<input type="reset">`
- 图片提交 `<input type="image" src="bf.png">`
![](https://i.loli.net/2019/07/22/5d3565442e57642802.png)

## 选择器 标签名选择器 id选择器 class选择器
-    复杂选择器
-    后代选择器 .box .inner-box 或者 p span 或者 #p1 .box
-    交集选择器 .text.danger
-    子代选择器 he后代选择器做区分(选中直接子代(儿子辈)) .box>.inner-box
-    并集选择器 .box,p,span{color:red;}
-   通配符 * 选中页面当中所有标签

- 继承性 字体相关属性 文本相关的属性(text-indent ,text-align ,line-height)

```
/* 样式冲突时   选择器权重高的  生效 */
/* 权重大小 */
 /* 行内样式(1000)>id选择器(100)>class 选择器(10)>标签选择器(1) > 通配符/继承属性(0)*/
 /* 复杂选择器权重 累加*/
/* .box .inner-box  权重 20  */
/* .red.text  权重20  */
/* 权重相同时  怎么办? */
/* 后写的生效 */
/* 首行缩进 */
text-indent: 2em;
```

## 颜色
- 预定义颜色：blue、yellow、pink、purple、red 等。
- 十六进制：每两位表示一种颜色的深度，分别表示 red、green、blue，比如：#ff00ff。
     1. rgb: rgb(0,0,255) ==> 绿色。rgb 和十六进制是可以相互转换的。
    rgba: rgba(0,0,255,0.5)。跟 rgb 一样，a 是透明度：0~1，0.5==> .5
    2. 十六进制==> 十进制换算
十进制：  0  1  2  3  4  5  6  7  8  9
十六进制：0  1  2  3  4  5  6  7  8  9   a(10)  b(11)   c(12)  d(13)   e(14)   f(15)
比如： 1e  ==>  1*16 + e ==> 16+ 14 = 30;
    ff ==> f * 16 + f ==> 15*16 + 15 = 255;
比如一个颜色是 aabbcc ==> abc, #00ffaa ==> #0fa

## 标签的表现形式

1. 块状标签：独占一行，宽高有效。比如：div p h1~h6 form table hr br ul>li ol>li dl>dt/dd
2. 行内块标签：可以同一行显示，宽高有效。比如: input select img button
3. 行内标签：可以同一行显示，但是宽高无效。比如：a span  strong del ins em i b
   /* padding  上下 没有作用  ,左右添加padding生效 */
    /* margin  上下 不管用   左右 生效 */
- display: 修改元素的性质。
- block：设置元素为块元素
- inline：设置元素为行内元素
- inline-block：设置元素为行内块元素
    - 转换的必要性：比如可以把a标签转换为块状元素，设置宽高，使用户可点击的区域增大，进而实现一个按钮的样式。
    - 文字水平垂直居中 text-align:center;line-height= 盒子的高度;
    - 块状元素的水平居中 margin:0 auto;

## 显示和隐藏
- 隐藏元素 不再占据位置  消失了
      消失   display: none;  
      出现 display: block
- 隐藏 依然占据位置  好像 透明度 
            /* visibility: hidden; */
			/* visibility: visible; */
- :hover  鼠标悬停时(放在元素上边时) 
        /* 能修改的是他 本身 和他 后代的样式 */
		本身 .box:hover	
		后代 .box:hover span

- overflow  用来处理超出部分 如何展示 */

            /* 超出部分隐藏 */
            /* overflow: hidden; */
            /* 根据超出情况   自动添加滚动条 */
            /* overflow: auto; */
            /* 两个方向都加滚动条 */
            overflow: scroll;
## 超出打点
         /* 宽度有限 */
         /* 不能换行 */
         /* 超出打点 */
        /* 超出部分隐藏 */
         overflow: hidden;
         text-overflow: ellipsis;
         white-space: nowrap;

## border
可以在元素周围创建边框，边框是元素可见框的最外部。
- border:1px solid red; 分别指定了边框的宽度、颜色和样式，是一种缩写：border-width border-style border-color。
- border-style: none (默认) / dashed(虚线) / dotted（点） / solid(实线) / double(双实线)。
- 可以单独设置某一条边框：border-right: 20px solid blue;
改变元素的大小。
-  添加border  也会改变盒子所占空间的大小 
-  分开写 border
    border-width: 10px 20px 30px 40px;
    border-style: solid dashed;
    border-color: #333; */
## 嵌套崩塌
嵌套崩塌：两个盒子发生嵌套的时候，给子类设置 margin 会给父类造成一种崩塌现象，子类元素的 margin-top 没有效果，而是直接作用到父类元素。
解决方案：
1. 父类 overflow: hidden;
2. 父类 设置极小的 padding 或者 border；

## 块状元素重叠

如果垂直两个块状元素同时设置了margin-bottom和margin-top,那么这两个值将会发生重叠,不会累加，哪个值大用哪个
`<div class="box2"></div>`
`<div class="box3"></div>`
## 浮动

- 浮动之后脱离文档流,不再占据位置,下方的元素会上移 
- 浮动之后会变成块元素
- 当一个块级元素浮动以后，宽度会默认被内容撑开，所以当漂浮一个块级元素时我们都会为其指定一个宽度

## 浮动的表现形式
1.当一个元素浮动以后，其下方的元素会上移。元素中的内容将会围2.绕在元素的周围。
3.浮动会使元素完全脱离文本流，也就是不再在文档中在占用位置。
元素设置浮动以后，会一直向上漂浮直到遇到父元素的边界或者其他浮动元素。
4.元素浮动以后即完全脱离文档流，这时不会再影响父元素的高度。也就是浮动元素不会撑开父元素。
5.浮动元素默认会变为块元素，即使设置 display:inline 以后其依然是个块元素。
6.块级元素和行内元素都可以浮动，当一个行内元素浮动以后将会自动变为一个块级元素。
7.当一个块级元素浮动以后，宽度会默认被内容撑开，所以当漂浮一个块级元素时我们都会为其指定一个宽度。

## 文字环绕
```
<style>
        .box {
            width: 400px;
            height: 400px;
            background-color: red;
        }

        .d1 {
            float: left;
            width: 100px;
            height: 100px;
            background-color: blue;
        }

        .d2 {
            /* 当一个元素浮动以后，其下方的元素会上移。元素中的内容将会围绕在元素的周围。 */
            width: 300px;
            height: 300px;
            background-color: orange;
            /* overflow: hidden; */
        }
    </style>
</head>

<body>
    <div class="box">
        <div class="d1">

        </div>
        <div class="d2">
            不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院
            不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院
            不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院不凡学院
        </div>
    </div>
</body>
```

## 右侧自适应
```
   <style>
        .main {
            width: 100%;
            height: 2000px;
            background-color: red;
        }

        .side {
            float: left;
            width: 200px;
            height: 1000px;
            background-color: blue;
        }

        .container {
            height: 1000px;
            background-color: green;
            overflow: hidden;
        }
    </style>
</head>

<body>
    <div class="main">
        <div class="side">

        </div>
        <div class="container">

        </div>

    </div>
</body>
```

## 浮动的影响
高度塌陷: 如果子类元素设置了浮动，而父类元素没有设置高度，或者高度比子类元素小，那么子类元素脱离了文档流，就无法把父类盒子撑开。那么整个文档的结构将受到破坏。 

解决方法(清除浮动的影响)：
    1.通常会给父元素指定一个高度
    2. 给父类盒子 设置 overflow: hidden; 
    3. 在浮动元素 之后 增加 一个 空的  div,给他设置 clear:both  
				.clr {
				clear: both;
			}
注意
- 因为浮动会对文档流造成影响，所以能用流式布局就不要使用浮动。
- 但凡是 遇到浮动,很多情况下  都要都要清除浮动带来的影响 
- 浮动的时候遵循这样一个原则    要浮动都浮动

## 图标如何为字体样式

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<meta http-equiv="X-UA-Compatible" content="ie=edge" />
		<link rel="stylesheet" href="font-awesome-4.7.0/css/font-awesome.min.css" />
		<title>Document</title>
		<style>
			.box {
				font-size: 30px;
				color: red;
			}
		</style>
	</head>

	<body>
		<!-- 把图标做成字体  来使用 ,通过 font-size   color   属性 控制图标颜色和大小 -->
		<!-- 1.下载 font-awesome -->
		<!-- 2.引入css文件 -->
		<!-- fa  和 fa前缀 -->
		<div class="box">
			<i class="fa fa-camera-retro"></i>
			<i class="fa fa-arrow-down"></i>
		</div>
		标记语言
		<h2>标记语言</h2>
	</body>
</html>
```

## 内联框架标签
- ` <iframe src="https://www.baidu.com" frameborder="1" width="400" height="400"></iframe>`
- `<iframe src="01-字体图标.html" frameborder="2" width="400" height="400">`
- `</iframe><iframe src="test.html" frameborder="1"></iframe>`

### 面试题: 什么是web标签语义化

标签语义化的目的在于能够直观的认识标签和属性的用途和作用，好处：

1、使页面的内容结构化：结构更清晰，便于不同的屏幕设备解析；

2、有利于SEO：和搜索引擎建立良好的关系，有助于爬虫更多的有效信息；

3、便于团队开发和维护；

### HTML5 新增 audio 标签 和 video 标签来解决音视频的问题;语法:
```
<audio src="素材/小手拍拍.mp3" controls>不支持</audio>
<!--
	附加属性可以更友好控制音频的播放，如：
	autoplay 自动播放
	controls 是否显不默认播放控件
	loop 循环播放
	preload 预加载 同时设置autoplay时此属性失效
-->

<video src="素材/movie.ogg" width="400" height="300" controls></video>
<!--
	同样，通过附加属性可以更友好的控制视频的播放
	autoplay 自动播放
	controls 是否显示默认播放控件
	loop 循环播放
	preload 预加载，同时设置了autoplay，此属性将失效
	width 设置播放窗口宽度
	height 设置播放窗口的高度
-->
```
```
多浏览器支持方案:

<audio controls>
	<source src="素材/小手拍拍.mp3">
	<source src="素材/小手拍拍.wav">
	<source src="素材/小手拍拍.ogg">
</audio>


<video controls>
	<source src="素材/movie.ogg">
	<source src="素材/movie.mp4">
	<source src="素材/movie.webm">
	您的浏览器不支持
</video>
```
