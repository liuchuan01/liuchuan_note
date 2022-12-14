# DaVinCi

## 一 面板简介



![截屏2022-07-14 上午9.28.33](https://tva1.sinaimg.cn/large/e6c9d24ely1h4677diizzj21z401w0st.jpg)

达芬奇不同面板负责不同功能，从左向右依次：

+ 媒体面板 用于导入素材并分类管理
+ 快编面板 用于快速编辑
+ 剪辑面板 剪辑视频
+ fusion面板 制作效果
+ 调色面板
+ Fairlight面板 音频制作
+ 交付面板 导出视频

## 二 调色

### 界面介绍



<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h46hgl3wnmj21jf0u0q7o.jpg" alt="截屏2022-07-14 下午3.22.07" style="zoom:33%;" />

在中间一栏中，会显示素材，左上角的编号若为灰色则未调色，若为彩色，则已调色。

在素材的下方会显示编码格式，双击可切换为素材名称/隐藏

若不够直观，右上角的时间线可帮助定位素材在时间线的位置

> 抓取静帧
>
> 在预览窗口右键，抓取静帧。
>
> 抓取的静帧在左上角画廊中可点击查看

最右侧为核心逻辑区域：节点逻辑

<img src="/Users/liuchuan/Library/Application Support/typora-user-images/截屏2022-07-14 下午3.37.16.png" alt="截屏2022-07-14 下午3.37.16" style="zoom:50%;" />

用于规划整体的前后顺序与逻辑



色轮与曲线，与FCPX相似

在预览窗口上方的这个图标，点击后可对比调色前后影片色彩

==shift D==

![截屏2022-07-14 下午3.48.29](https://tva1.sinaimg.cn/large/e6c9d24ely1h46i6nldr7j201s01qa9t.jpg)

> 一级调色：对画面整体的调色
>
> 二级调色：对画面局部的调色，经常用到蒙版，扣像，跟踪等等



### 示波器

眼睛与显示器无法百分百精准，需要使用示波器

*工作区->视频示波器->开启*

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h46jdqowfmj21hu0loq7y.jpg" alt="截屏2022-07-14 下午4.29.49" style="zoom:33%;" />

波形图展示的就是我们的画面，展示的是像素的亮度

左侧的数字代表颜色，底部为纯黑，顶部为纯白

调色时，使用色轮，将暗部调低，直到波形图下方触底，亮部调高，直到波形图上方触顶

### 节点的使用

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h46jyheunxj20ka0bk74g.jpg" alt="截屏2022-07-14 下午4.49.48" style="zoom:50%;" />

如图节点的下方显示你所做的调整，同时也可右键为节点添加标签

每一个节点都会继承上一个节点的更改

双击小绿点即可断开连接，重新连接节点

1. 串行节点

   线性连接，前后相继

2. 并行节点

   允许一个节点后连多个节点，多个节点都只继承前方节点，不被其他节点干扰

3. 图层节点

   图层节点类似PS，当画面重叠时，显示位于上方的节点。（达芬奇相反，优先显示下方）

   若是并行节点，就会混合重叠的颜色

### 扣像

![截屏2022-07-14 下午4.56.45](https://tva1.sinaimg.cn/large/e6c9d24ely1h46k62fnt6j21es03gjrr.jpg)

点击此处的小吸管，在画面中选取想要的颜色

而后按下==shift H==即可单独显示此颜色



### LUT颜色查找表

类似于调色师的通用预设

可在项目设置中导入LUT

LUT一般分为以下两种

1. 矫正LUT

2. 风格LUT

> ![截屏2022-07-17 下午4.21.15](https://tva1.sinaimg.cn/large/e6c9d24ely1h49zzpeqqvj203w0203y9.jpg)
>
> 当你的LUT过浓时，点击键，更改输出增益即可
>
> 当你的LUT使用后，画面模糊，可能是LUT精度不够，点击项目设置，将三线性更改为四面体