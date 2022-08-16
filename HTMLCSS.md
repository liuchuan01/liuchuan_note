# HTML/CSS

## HTML：

html主要由标签构成，一般为双标签,

称为开始标签，结束标签。

> <html> </html>



有少数标签为单标签

> <br/>





### 骨架标签：

| 标签名          |     定义 | 说明                |
| --------------- | -------: | ------------------- |
| <html></html>   | html标签 | 根标签              |
| <head></head>   |     头部 | head中必须设置title |
| <title></title> |     标题 | 网页标题            |
| <body></body>   |     主体 | 放置文档的所有内容  |

> 新lang用于指定网页的语言 
>
> en		 英语
>
> zh-CN   中文
>
> 对于浏览器有用，提供翻译等



> charset 用于指定网页编码格式，使用utf-8即可



### 常用标签：

#### 标题标签：

```html
<h1></h1>
~
<h6></h6>
```

html具有六级标题，依据重要性递减

#### 段落标签：

```html
<p>文字段落</p>
```

段落换行依据为浏览器窗口大小

段落之间会有空行



#### 换行标签：

```html
<br/>
```

​	此为单标签，强制换行



### 文本格式化标签：

用于突出文本

#### 加粗：

```html
<strong></strong>
or
<b></b>
```

#### 倾斜：

```html
<em></em>
or
<i></i>
```

#### 删除：

```html
<del></del>
or
<s></s>
```

#### 下划线：

```html
<ins></ins>
or
<u></u>
```



### 盒子标签：

没有语义，仅仅是用于装内容,便于模块化

```html
<div></div>
and
<span></span>
```

可以理解div是大盒子，span是小盒子



### 图像标签：

图像标签用于向html导入图像

```html
<img src="url"/>
```

src是图片标签的路径属性



>相对路径：同级直接写文件名
>
>​				  位于下一级 文件夹名/文件名
>
>​				  位于上一级  ../文件名



> 绝对路径：写死路径，不推荐



| 属性   | 属性值     | 说明                     |
| ------ | ---------- | ------------------------ |
| src    | 图片 路径  | 必须                     |
| alt    | 文本       | 图片无法显示时的替代文本 |
| title  | 文本       | 鼠标悬浮于图片时的文字   |
| width  | 像素（px） | 宽度                     |
| heigh  | 像素（px） | 高度                     |
| border | 像素（px） | 边框                     |



### 超链接标签：

#### 用于网页跳转

```html
<a href = "目标URL" target = “弹出方式”>文本或图像</a>
```

href属性用于指定跳转目标

target属性用于规定打开方式

+ 默认为          _self   ==当前窗口打开==
+ 可更改为       _blank ==新窗口打开==



#### 用于网页内部链接

```html
<a href = "网页内部文件名" target = “弹出方式”>文本或图像</a>
```



#### 用于空链接

```html
<a href = "#" target = “弹出方式”>文本或图像</a>
```

可以将链接设置为"#",当作空链接使用



#### 用于下载链接

```html
<a href = "待下载文件名" target = “弹出方式”>文本或图像</a>
```



#### 用于网页元素链接

```html
<a href = "网页内部文件名" target = “弹出方式”><img src = "url"></a>
```

实现点击图片时跳转



#### 用于锚点链接

```html
<a href = "#one" target = “弹出方式”>第一块内容</a>
并且在需要跳转的链接处加标签 id="one"
```

点击链接时快速跳转到网页的指定位置



### 特殊字符与注释标签:

#### 注释标签:

```html
<!--content-->
```

实际使用时,ctrl+"/"即可



### 特殊字符:

| 字符 | 代码  |
| ---- | ----- |
| 空格 | &nbsp |
| <    | &lt   |
| >    | &gt   |
| ...  | ...   |

需要用到再搜索



### 表格标签:

```html
<table>
	<tr> <th>title</th> <\tr>
	<tr> <td>content</td> <td>content</td> <td>content</td> <\tr>
	<tr> <td>content</td> <td>content</td> <td>content</td> <\tr>
</table>
```

> table代表表格
>
> th用于指定标题
>
> tr用于表示行标签
>
> td用于表示单元格内数据

![](/home/liuchuan/Downloads/Screenshot from 2022-04-10 09-37-24.png)

![](/home/liuchuan/Downloads/Screenshot from 2022-04-10 09-37-54.png)

#### 表格属性:

| 属性        | 属性值            | 描述                     |
| ----------- | ----------------- | ------------------------ |
| align       | left,center,right | 单元格内数据的对齐方式   |
| border      | 1或""             | 是否有边框,默认为"",没有 |
| cellpadding | 像素值            | 数据与单元格间空白,默认1 |
| cellspacing | 像素值            | 单元格间空白,默认2       |
| width       | 像素值或百分比    | 表格宽度                 |

> 在写表格时                 
>
> 在table标签下创建thead标签与tbody标签,
>
> 表头置于thead标签内 
>
> 内容置于tbody内

 

####                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           合并单元格:

合并单元格分为两种:

![](/home/liuchuan/Downloads/Screenshot from 2022-04-10 10-27-24.png)



> 跨行:最上侧为目标单元格,写合并代码 rowspan
>
> 跨列:最左侧为目标单元格,写合并代码 colspan

```html
<table border = 1 cellspacing = 0 align="center">
<tr> <th>rank</th>  <th>book name</th> <th>trend</th> <th>today</th> <th>week</th> <th>link</th></tr>
<tr> <td colspan="2">1</td> <td>book1</td> <td>3</td> <td>310</td>   <td>3000</td> <td> <a href="http://www.baidu.com" >a</a> </td></tr>
<tr> <td>2</td> <td>book2</td> <td>3</td> <td>210</td> <td>2000</td> <td> <a href="http://www.baidu.com" >a</a> </td> </tr>
<tr> <td>3</td> <td>book3</td> <td>3</td> <td>110</td> <td>1500</td> <td> <a href="http://www.baidu.com" >a</a></td></tr>
<tr> <td>4</td> <td>book4</td> <td>3</td> <td>100</td> <td>1000</td> <td> <a href="http://www.baidu.com" >a</a></td></tr>
</table>
```

==<td colspan="2">1</td>==



![](/home/liuchuan/Downloads/Screenshot from 2022-04-11 09-01-57.png)



> 合并单元格后被合并单元格会后移,故因删除

![](/home/liuchuan/Downloads/Screenshot from 2022-04-11 09-05-38.png)



### 列表标签:

#### 无序列表:

```html
<ul></ul>无序列表
<li></li>列表项
```

1. 列表项之间是并列关系

2. *ul* 标签中只能放 *li* 标签,*li*标签内什么都可以放

#### 有序列表:

若各个选项之前有顺序,则可采用有序列表

```html
<ol></ol>有序列表
<li></li>列表项
```

有序列表会自动生成

1. 

2. 

3.  

   标号

#### 自定义列表:

典型特征:

一个标题下带有多个小标题,

小标题用于扩充,解说大标题



```html
<dl></dl>有序列表
<dt></dt>名词
<dd></dd>名词解释1
```



*dl*标签内只能包含*dt*,*dd*.

###  表单标签:

#### 表单:

如网页中注册,用户填写的信息



> 表单主要用于收集用户信息,提交给服务器



![](/home/liuchuan/Downloads/Screenshot from 2022-04-11 09-22-59.png)

```
<form> 表单标签
```

| 属性   | 属性值   | 作用                        |
| ------ | -------- | --------------------------- |
| action | url地址  | 指定服务器的url             |
| method | get/post | 指定提交服务器的方法        |
| name   | 名称     | 表单名称,用以区分不同表单域 |



#### 输入表单:

```html
<input type="" value=""> 输入表单元素
```

==input是一个单标签==

**

通过type指定输入表单元素样式,如

+ *text*: 输入任何文字

+ *password*:输入密码,输入密码不可见

+ *radio*: 单选按钮 圆形

+ *checkbox*: 多选按钮 方形
+ *submit*:将表单域中数值提交
+ *reset*:清空表单域数据
+ *button*: 普通按钮,用于js使用
+ *file*: 上传文件



通过name==表单元素名称==指定多个输入标签的归属,如radio默认可以多选,当多个选项name属性一致时,变为单选





通过value==表单元素值==指定值,如网页中密码框中默认提醒 "密码六位以上",或是用于指定当用户选定某一选项时,传给后段的值



通过checked,控制选择按钮默认被打勾



通过maxlength,规定用户输入字符最长长度

#### 绑定元素:

如普通的单选按钮特别小,难以点中,则可使用label绑定此按钮,点击label也可达到相同效果

```html
<label for="sex">male</label>
<input type="radio" name="sex" id="sex"/>
```

> label标签中的for属性与相关元素的id属性相同 即可

#### 下拉表单:

页面中有多个表单需要选择,且需要节约页面空间

```html
<select>
	<option>one</option>
	<option>two</option>
	<option select="selected">three</option> //默认选项
</select>
```

#### 文本域:

特大号文本框,支持多行输入 

```html
<textarea>
aaaaaaaaaaaaaa   //默认文本
</textarea>
```





## CSS:

层叠样式表,css也是层叠样式表



> css代码置于head标签中的<style></style>中

```css
p{
	color: red;
	font-size: 12px
}

<p>this is a example</p>
```

即可实现将段落标签中的文字颜色变为红色,字体大小变为12像素



> 一个完整的css包含选择器与样式



![](/home/liuchuan/Downloads/Screenshot from 2022-04-11 10-59-33.png)



+ 属性与属性值以键对值的形式出现
+ 语句必须以" ; "结尾

###  css书写风格:

1. 使用展开式,每条属性之间换行
2. 除特殊情况均使用小写
3. 选择器后加空格
4. " : "的前后加空格

### css引入方式:

#### 内部样式表:

```css
<style>
    <div>{
        color : red;
    }
</style>
```

#### 行内样式表:

用于小更改,结构样式未分离,少用

```css
<div style="color:red;">aaa</div>
```

#### 外部样式表:

实际开发使用

在外部单独建立css文件,引入html

> 1.在外部建立a.css
>
> 2.在html页面中用link引入:

```css
<link rel= "stylesheet" href="src">
```



### css基础选择器:

选择器就是选择标签使用的

#### 标签选择器:

标签选择器(元素选择器),是以==html标签名==称作为选择器,

按标签名称分类,为某一类标签指定==统一==的css样式

> 选出所有的标签!!! 不能差异化设置,所有该类型标签都被指定为该样式

```css
p {
	color : blue;
}
div {
	color : red;
}
```

所有的段落标签内容都变为蓝色,div内容变为红色

#### 类选择器:

类选择器可以差异化选择一个或几个标签

```css
.red {
	color : red;
}

 <p class="red">example</p>
 <p>example</p>
```

第一个example就会变成红色,

第二个example不会变成红色

> 实际开发中,类选择器最常用

 

##### 多类名:

```css
<div class = "a b">example</div>
```

运行一个元素拥有多个类,以空格分割

提高代码可维护性与复用性

#### ID选择器:

```css
定义
#red {
	....
}

调用方法:
<div id="red">example</div>
```

> ID只能被调用一次,不可以被多个元素使用

#### 通配符选择器:

```css
定义
* {
	....
}
```

> 无需调用,页面内全部元素,会自动使用该样式

### 字体属性:

+ font-family

  字体

  ```css
  font-family:"Microsoft YaHei","font two"...
  ```

  > 可以写多个字体,以逗号分割,浏览器会从第一个开始查找可用的字体.

+ font-size

  字号大小

  ```css
  font-size: 20px
  ```

  > 标题标签比较大,需要单独指定

+ font-weight

  字体粗细

  ```css
  font-weight: normal|bolder|lighter|number
  实际开发中更倾向 数字,700(加粗),400(正常)
  ```

+ font-style

  ```css
  font-style:italic|normal
  可将正体变斜,斜体变正
  ```

### 文本:

#### 文本颜色:

```css
div {
	color:pink;      // 1.使用预设的颜色
	color:#ffffffff; // 2.使用十六进制颜色代码
}
```

#### 文本对齐:

```css
div {
	text-align: center|right|left;//水平文本对齐
}
```

> 本质是盒子内的文字水平居中对齐



#### 文本装饰:

```css
div {
	text-decoration:underline|overline|line-through;// 下划线...
}
```

> 可用于取消网页链接的下划线

#### 文本缩进:

```css
div {
	text-indent: 10px|2em
}//em根据文本大小计算,2em即空两格
```

通过设置该属性,所有文字第一行都可以有一个缩进

```css
p {
	text-indent: 10px
}//所有的段落标签缩进
```

#### 行间距:

```css
div {
	line-height:26px
}
```

![](/home/liuchuan/Downloads/Screenshot from 2022-04-11 19-55-39.png)



### Emmet:

可快速生成html/css结构语法

+ 快速生成标签,输入标签名,按tab

+ 快速生成多个标签 div*10 按tab,生成10个div
+ 父子标签,div>span,自动生成包含span的div

+ 兄弟标签,div+span,生成的标签并列存在

+ 生成多个div类,id有序 .demo$*5,id为demo1到demo5

+ css属性输入第一个词,直接生成属性

### 复合选择器:

由基础选择器集合而来

#### 后代选择器:

包含选择器

```
ol li {
	color=pink
}

```

只有ol的子代中的li标签才使用

> + 可以一层一层嵌套ol li a....
> + 可以以标签的类名替代标签名,用以指定某个标签

#### 子元素选择器:

```css
div>p {
	color:red
}
```

将div标签的子元素选中,孙子元素不会被选中



#### 并集选择器:

```css
div,
p {
	color:red
}
```

同时选择多个元素



#### 伪类选择器:

##### 链接伪类选择器:

为选择的元素增加特殊的效果

```
:xxx #伪类选择器以冒号开头
```

1.链接伪类选择器

```css
a：link //未被访问的链接
a:visited //已被访问的链接
a:hover //鼠标悬浮其上时的链接
a:active //鼠标按下未松开的链接
```

> 四个需要按顺序写
>
> 实际开发一般写link与hover即可

2.focus伪类选择器

用于选取获得焦点（鼠标点击）的表单元素

```css
input:focus {
  background-color:red;
}
```

### 元素选择模式

#### 块元素：

​	常见的如<h> <p> <div> <ul> 

>  特点：独占一行
>
> ​            宽高，内外元素可指5定
>
> ​			宽度默认为父元素的100%
>
> ​			是一个盒子/容器，内可放行内或块级元素
>
> 注意：文字属性的块元素内不可嵌套元素<p><h>等

#### 行内元素：

   常见的 如<a><b><strong><i><s><span>

 >特点：一行多个
 >
 >​		宽高设置无效
 >
 >​		默认宽度即为内容宽度
 >
 >​		行内元素只能容纳文本及其他行内元素
 >
 >注意：链接里不能再放链接
 >
 >​			<a>在转换为块级元素后里面可以放块级元素

#### 行内块元素

常见的如<img/><input/><td>。同时具有行内元素与块元素的特点

> 特点：行内块元素在同一行上，行内块元素之间有缝隙
>
> ​			默认宽度为内容宽度
>
> ​			高度，行距，内外边距可以控制

#### 元素显示模式转换

行内元素转换块级元素的方法

1.

```css 
a {
  display:block; //转换为块元素
  display:inline; //转换为行内元素
  display:inline-block;  s//转换为行内块元素
}
```



### CSS背景：

#### 背景颜色background-color:red;

默认为transparent，透明的；

#### 背景图片

比起插入图片，更易控制位置

```css
background-image:url（image src）
```

默认值为none。

##### 背景平铺：

当图片小于盒子时，图片会默认复制，平铺。

```css
background-repeat:no-repeat;//取消平铺
background-repeat:repeat-x;//延x轴平铺
background-repeat:repeat-y;//延y轴平铺
```

> 背景颜色与背景图片可以同时存在，背景图片压住背景颜色

##### 背景图片位置

```css
background-position:x y;//x即水平位置，y垂直位置
```

| 参数值   | 说明                                            |
| -------- | ----------------------------------------------- |
| length   | 百分数，长度值（精确单位）                      |
| position | top/center/bottom/left/center/right（方位名词） |

省略值默认居中对齐

> 例如带图标的文字，即可使用背景图片精准控制位置
>
> 作为大背景图片时，可能由于图片过大显示不全，使用背景图片位置将其位于中间即可。

使用方位名词时，x，y可以混写。

使用精确单位与混合方式时，x，y要确定（如10px，10px）。

#### 背景固定：

图片是否随内容滚动而变化。

==可用于实现视差滚动==

#### 背景色半透明：

实现盒子背景色为半透明

background：rgba（x，x，x，0.5）

a即为alpha的简写，取值0～1，1为完全不透明

### CSS三大特性：

#### 层叠性：

解决样式冲突问题，如一个元素拥有两个相同属性的不同样式，则**执行就近样式**，（即后面的样式覆盖前面的样式 ）

只会覆盖冲突的样式。

#### 继承性：

元素会继承父元素的样式，使用此特性，可简化代码。

特殊情况：

```
font:14px/1.5 "字体"
```

1.5意为行高为当前文字大小的1.5倍

此用法下行高不是绝对值继承。

#### 优先级：

当多个选择器选中一个元素时。

选择器相同时，按重叠性处理。

选择器不同时，按选择器权重处理

！important>行内>ID选择器>类&伪类选择器>元素选择器>继承&*全局选择器

> 在属性后加！important，其优先级最高。

##### 权重叠加：

如有一个li标签

```css
使用li{
}
与
ul li{
}
时，后者的权重会更高，因为后者的权重为ul+li
```

### 盒子模型

盒子的父元素可使用

```css
text-align:center
```

使子元素水平居中

1. border边框

   + 边框宽度border-width

   + 边框样式border-style（实线虚线等等）

   + 边框颜色borrder-color

     > 边框可以指定单条，使用复合写法，如：
     >
     > border-top：1px solid red；
     >
     > 即上边框为1像素高的红色直线
     >
     > 先指定整个边框样式，再指定单条

     盒子边框向外扩展，边框会导致盒子会==变大==

2. content内容

   在盒子内装其他盒子，文字等等

3. padding内边距

   盒子与内容的距离

   ```css
   padding-top=30px
   padding-left=10px
   //距上边30px，左边10px
   ```

   复合写法

   ```css
   padding:5px;//上下左右都为5
   padding:5px,10px;//上下为5，左右为10
   padding:5px,10px,20px;//上5，左右10，下20
   padding:5px,10px,20px,30px;//上5，右10，下20，左30，顺时针
   ```

   padding向外扩展，内边距会导致盒子==变大==

   也可用于多个相同盒子内文字数量不一致的情况，用padding撑开  盒子。 

4. margin外边距

   盒子之间的距离

   ```css
   margin-top=30px
   margin-left=10px
   //距上30px，左10px
   ```

    特殊情况：

   1. 垂直相邻块元素外边距合并，如上方盒子下外边距20px，下方盒子上外边距10px，最终只会剩下20px

      解决：

      ​    只设一个外边距

   2. 外边距塌陷，父盒子内嵌套子盒子，此时想要子盒子离父盒子上边一定距离，设置子盒子的margin-top，导致父盒子整体下移

      解决：

      + 为父元素增加边框
      + 添加父元素的上内边距
      + 为父元素添加overflow：hidden

   ![image-20220609232235631](/Users/liuchuan/Documents/image-20220609232235631.png)

