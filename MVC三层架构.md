# MVC三层架构

三层架构是指：视图层 View、服务层 Service，与持久层Dao。它们分别完成不同的功能。
==View== 层：用于接收用户提交请求的代码在这里编写。
==Service== 层：系统的业务逻辑主要在这里完成。
==Dao 层==：直接操作数据库的代码在这里编写。

![](/home/liuchuan/Downloads/mdpicture/c077fe153fc44d19bcbdeb0fea43c96f.png)



> 为了更好的降低各层间的耦合度,在三层架构程序设计中，采用面向抽象编程。
> 即上层对下层的调用，是通过接口实现的。
> 而下层对上层的真正服务提供者，是下层接口的实现类。
> 服务标准（接口）是相同的，服务提供者（实现类）可以更换。



+ View：视图，为用户提供使用界面，与用户直接进行交互。

+ Model：模型，承载数据，并对用户提交请求进行计算的模块。  

+  Bean：实体类，专门用户承载业务数据的，如 Student、User 等 一类称为业务处理 Bean：指 

+ Service 或 Dao 对象，专门用于处理用户提交请求的。

+ Controller：控制器，用于将用户请求转发给相应的 Model 进行处理，并根据 Model 的计算结果向用户提供相应响应。

  ### 工作流程:

  1. 用户通过 View 页面向服务端提出请求，可以是表单请求、超链接请求、AJAX 请求等

  2. 服务端 Controller 控制器接收到请求后对请求进行解析，找到相应的 Model 对用户请求进行处理
  3. Model 处理后，将处理结果再交给 Controller
  4. Controller 在接到处理结果后，根据处理结果找到要作为向客户端发回的响应 View 页面。页面经渲染（数据填充）后，再发送给客户端。

  ![](/home/liuchuan/Downloads/mdpicture/08aa6caebcc945f5adb65a78300e3d77.png)



















# FreeMarker

### 简介

![](/home/liuchuan/Downloads/Screenshot from 2022-04-17 09-57-27.png)



**定义**:模板引擎,基于模板和要改变的数据,生成文本(html,电子邮件,源代码,配置文件等),是java的类库

![](/home/liuchuan/Downloads/mdpicture/Screenshot from 2022-04-17 10-11-26.png)

将视图从逻辑业务中抽离,java程序准备数据,freemarker渲染输出

```
举例:
<h1>Welcome &{user}<h1>
```

user中的内容来自数据库,动态生成网页

### 环境搭建:

1. 选择maven web app

2. 引入依赖,放置于<dependency>标签中

   ```java
   <dependency>
     <groupId>org.FreeMarker</groupId>
     <artifactId>FreeMarker</artifactId>
     <version>2.3.28</version>
   </dependency>
   ```

   

3. 加入插件,放置于<build>标签中

4. 配置web.xml,模板路径,模板编码,文件后缀...

5. 编写servlet类

6. 新建模板文件(.ftl)

7. 启动访问

> <!-- -->是html注释,网页源代码中可以看见
>
> <#-- -->是freemarker注释,网页源代码中不可见



 ### 组成部分:

1. 文本			直接输出
2. 注释            <#-- -->,内容不输出
3. 插值            即${...}或#{...}格式的部分，类似于占位符
4. FTL指令      FreeMarker指令

```freemarker
<html>
<head>
<title>Welcome to FreeMarker 中文官网</title><br> 
</head> 
<body>
<#-- 注释部分 --> 
<#-- 下面使用插值 --> 
<h1>Welcome ${user} !</h1><br> 
<p>We have these animals:<br> 
<u1>
<#-- 使用FTL指令 --> 
<#list animals as being><br> 
  <li>${being.name} for ${being.price} Euros<br> 
<#list>
<u1>
</body> 
</html> 
```



### 使用过程:

1. 创建一个Configuration对象，直接new一个对象。构造方法的参数就是FreeMarker对于的版本号。

2. 设置模板文件所在的路径。

3. 设置模板文件使用的字符集。一般就是utf-8.

4. 加载一个模板，创建一个模板对象。

5. 创建一个模板使用的数据集，可以是pojo也可以是map。一般是Map。

6. 创建一个Writer对象，一般创建一FileWriter对象，指定生成的文件名。

7. 调用模板对象的process方法输出文件。

8. 关闭流。

```
// 第一步：创建一个Configuration对象，直接new一个对象。构造方法的参数就是FreeMarker对于的版本号。
Configuration configuration = new Configuration(Configuration.getVersion());

// 第二步：设置模板文件所在的路径。
configuration.setDirectoryForTemplateLoading(new File("/WEB-INF/ftl"));

// 第三步：设置模板文件使用的字符集。一般就是utf-8.
configuration.setDefaultEncoding("utf-8");

// 第四步：加载一个模板，创建一个模板对象。
Template template = configuration.getTemplate("hello.ftl");

// 第五步：创建一个模板使用的数据集，可以是pojo也可以是map。一般是Map。
Map dataModel = new HashMap<>();
//向数据集中添加数据
dataModel.put("hello", "this is my first FreeMarker test.");

// 第六步：创建一个Writer对象，一般创建一FileWriter对象，指定生成的文件名。
Writer out = new FileWriter(new File("/hello.html"));

// 第七步：调用模板对象的process方法输出文件。
template.process(dataModel, out);

// 第八步：关闭流。
out.close();
```

### 转义:

==超链接转义==

> 传递的参数会在最终的html页面中变为超链接?

1. 在字符串后加?html

2. 使用<#escape>转义,内部内容会作为字符串直接显示于页面

3. 当><作为大于小于使用时,应加上()或使用
   + lt代替<
   + lte代替<=
   + gt代替>
   + gte代替>=

### 插值:

表现格式: *${...}* 

使用数据模型中的部分替代输出



+ *${...}*可直接用于字符串插值

```
println(s"${n} second.")
```
## 常用指令
### assign指令:

assign指令用于为该模板页面创建或替换一个顶层变量

```
<#assign name=value [in namespacehash]>
```

[in namespacehash]子句用于将变量送入命名空间

调用该变量时，应该使用插值*${...}*

==question 1==

```
<#assign names=["1","2","3"]>
${names?join(",")}
//将序列拆分为字符串，与java相同，以参数中的符号分隔数组各项形成字符串
```

### if语句：

```
<#if condition>
...
<#elseif condition2>
...
<#else>
...
<#if>
```

==question 2==


> 判断数据是否存在 
>  变量名？？(属性值或集合是否为空)
>  变量名！（属性值是否为空）
>
>  变量名！数据（若为空则赋值）




### list遍历指令：

用于遍历序列

```
<#list sequence as item>
<#else>
	当没有选项时执行else（数据不存在）
</#list>
```

sequence：想要迭代的项，可以是序列或集合的表达式

item：循环变量名

 

   

### macro宏定义:

自定义指令

```
<#macro greet>     
     <font size="+2">Hello World!</font>     
</#macro>   

```

使用宏（调用指令）: <@greet> < /@greet >

Hello World！会被打印在屏幕上

```
<#macro user uname upwd phone>     
     查询用户 - ${uname}- ${upwd}- ${phone}   
</#macro>   
<@user uname="zhangsan" upwd="123456" phone="12345367"><@user>

```

查询用户 - zhangsan- 123456- 12345367会被打印在屏幕上

用@替换FTL标记中的#

#### nested占位符

在调用的语句中间，写文本，在macro中写nested占位符，

则会在nested位置出现文本。



### import导入指令

import指令，导入库，例如在

a.ftl

```
<#macro cfb>
xxxxx
</#macro>
```

b.ftl

```
<#import "a.ftl " as common>
<#--使用指令-->
<@common.cfb></@common.cfb>
```

b文件即可调用a中指令 