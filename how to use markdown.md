# how to use markdown



## code block:

```java
public class FastAppSetupServiceImpl implements FastAppSetupService {

    protected final FastAppConst appConst;
    protected final AppBlockService blockService;
    protected final AppFileService fileService;
    protected final AppNavigationService navigationService;
    protected final AppSettingService settingService;
    protected final AppUserService userService;

```

use ``` then add the code name

```java
example:```java
```

## title：

markdown have six title level

should begin with:

#

##

###

...

end with single space.

title perform like this:

![](/home/liuchuan/Downloads/Screenshot from 2022-04-09 14-27-40.png)

## fonts:

#### bold: 

use ** content ** to bold words

example: **bold word**



#### highlight:

use == content == to highlight words

example: ==highlight words==



#### strikeout:

use ~~ content ~~to strikeout words

example: ~~strikeout words~~



#### italic: 

use * content * to italic words

example:  *italic word*

#### commit:

use [ ^  content]  to make commit

example: [^this is a commit]

## block:

use > content 

can use more > 

example:

> content
>
> > content
> >
> > > content



## cut-off line:

use --- or ***  

example:---

---

example:***

***



## picture:

use ! [ picture name ] ( src )



![my picture](1.png)



## list:

supports * + - to make list

should end with a single space



example:

+ first

 + second
 + third  

ordered list : number + '' . "

1. first

2. second
3. third

> if you want to end list,press enter double;

​    

## link:

put link like this :  

```
[link name](URL)
or
<URL>
```

[baidu](http://www.baidu.com)

<http://www.baidu.com>



## form:

add a from like this:

```
| head  | head | head |
|  ---- | ---- |----  |
| cell  | cell | cell |
| cell  | cell | cell |
```

| head | head | head |
| ---- | ---- | ---- |
| cell | cell | cell |
| cell | cell | cell |

you can make elements right or left by use " : " 

| head | head |  head |
| :--- | :--: | ----: |
| left | cell | right |
| left | cell | right |
