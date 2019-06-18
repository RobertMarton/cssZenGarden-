# cssZenGarden案例研究报告
# <center>cssZenGarden案例研究报告</center>



## **案例一：**FOUNTAIN KISS 

Pls refer this link for detail informations：[http://www.csszengarden.com/216/](http://www.csszengarden.com/216/)

code link：[view-source:http://www.csszengarden.com/216/](view-source:http://www.csszengarden.com/216/)



​		首先该页面的布局总体来看是两个左右设计的分区div大布局，然后在每个div分区内部采用嵌套的方式继续布局div，设计采用的原型图坐侧是固定的侧边栏显示界面，整体是可下拉的活动模块，长度根据文字内容填充有所不同，右侧首先分为左右两部分，左侧作为独立的一个分区，然后右侧上下再分为两个矩形分区。设计风格很巧妙。

### 布局分区图



![image-20190618195620762](/Users/Leo/Library/Application Support/typora-user-images/image-20190618195620762.png)		

## 每个布局／分区的分析

​		首先查看网页的尺寸大小：

![image-20190618183606052](/Users/Leo/Library/Application Support/typora-user-images/image-20190618183606052.png)

​		可以看到<meta> viewport元素为浏览器提供有关如何控制页面尺寸和缩放的说明。width = device-width部分将页面宽度设置为遵循设备的屏幕宽度（具体取决于设备）。initial-scale = 1.0部分设置浏览器首次加载页面时的初始缩放级别。

​		当然也可以直接查看：

![image-20190618185525217](/Users/Leo/Library/Application Support/typora-user-images/image-20190618185525217.png)

​		对于每个网页元素来说，均有clientHeight和clientWidth属性，它们代表该属性所指向的元素内容加上padding所占据的视觉面积，不含border以及滚动条所占据的面积。

​		整体的页面在div page-wrapper 里面，他的尺寸是1353*297

![image-20190618190850150](/Users/Leo/Library/Application Support/typora-user-images/image-20190618190850150.png)



​		左侧栏中有显示"CSSZENGARDEN"的字样，字体是48px Ultra，尺寸是48*456，Color是#FFFFFF也即是白色，margin是39.84px 0px，详见下图：

![image-20190618190913731](/Users/Leo/Library/Application Support/typora-user-images/image-20190618190913731.png)



​		对整个右侧body来说其布局如下

![image-20190618192154147](/Users/Leo/Library/Application Support/typora-user-images/image-20190618192154147.png)



​		在body中有分别嵌入了div：page-wrapper,尺寸是660*3323.25

![image-20190618192535494](/Users/Leo/Library/Application Support/typora-user-images/image-20190618192535494.png)

​		其字体大小是：16px，字体是Georgia，颜色是＃772244，背景色是＃FCEEC6，Margin是0px 0px 0px 160px，Padding填充值是：30px 0px 0px，其详细参数如下：

![image-20190618192803081](/Users/Leo/Library/Application Support/typora-user-images/image-20190618192803081.png)

​		该div内部左侧布局section：zen_intro，这里我们用元素id来作为唯一指定值，其尺寸为560*536.25

![image-20190618193232356](/Users/Leo/Library/Application Support/typora-user-images/image-20190618193232356.png)

​		右侧上方布局为：

![image-20190618193403527](/Users/Leo/Library/Application Support/typora-user-images/image-20190618193403527.png)

​		颜色是＃772244，字体大小是30px，字体是Georgia，Margin是0px －672px 0px 0px，详细布局参数为：

![image-20190618193524997](/Users/Leo/Library/Application Support/typora-user-images/image-20190618193524997.png)

​		右侧下方布局为：

![image-20190618193434088](/Users/Leo/Library/Application Support/typora-user-images/image-20190618193434088.png)

​		颜色是＃FFFFF也即白色，字体大小是16px，字体是Georgia，Margin是0px －672px 0px 0px，padding填充是0px 19.2px 10px,详细布局参数为：
![image-20190618193640128](/Users/Leo/Library/Application Support/typora-user-images/image-20190618193640128.png)



​		对左侧的分区来说，第一个方块，我们用'检查'点击相应模块查看源代码，可以看到这个模块内部镶嵌了一个圆，园内部镶嵌了一个356*401.63的div, 其类型是"preamble",id是"zen-preamble"

![image-20190618182206540](/Users/Leo/Library/Application Support/typora-user-images/image-20190618182206540.png)

​		点击这个div模块，可以看到里面的元素模块

![image-20190618194154293](/Users/Leo/Library/Application Support/typora-user-images/image-20190618194154293.png)

​		这个div中首先用"h3"标签为"The Road to Englishtenment"作为文本标题，字体尺寸为284.69*22，然后用三个"p"标签来书写段落文本，每个段落中用"abbr"对DOM，CSS作标题化处理。

![image-20190618194322429](/Users/Leo/Library/Application Support/typora-user-images/image-20190618194322429.png)

​		通过对这个网页案例的学习分析，可以根据左右布局的特点制作一个简易版的网页设计，在右侧设计中可以采用上下的分区设计嵌套div模块，然后可以继续嵌套布局div，最后形成一个丰富的网页设计界面。





## 案例二：CSS ZEN GARMENTS

Pls refer this link for detail informations：[http://www.csszengarden.com/220/](http://www.csszengarden.com/220/)

Code link：[view-source:http://www.csszengarden.com/220/](view-source:http://www.csszengarden.com/220/)

​		首先该页面的布局总体来看是两个侧边栏固定的上下式的分布界面设计，主界面是一个大的body，主要分为上中下三个大的div模块，在每个div中继续布局嵌套子div，最后形成结果设计，设计采用的原型图的两侧都是固定的，整体是下滑形式的显示界面，重点突出，给人一种很清晰的感觉。

### 布局分区图

![image-20190618205730689](/Users/Leo/Library/Application Support/typora-user-images/image-20190618205730689.png)

### 每个布局／分区分析

​		先从源代码中head查看网页尺寸：

![image-20190618201031538](/Users/Leo/Library/Application Support/typora-user-images/image-20190618201031538.png)

​		看到<meta name="viewport" content="width=device-width, initial-scale=1.0"> ，<meta> viewport元素为浏览器提供有关如何控制页面尺寸和缩放的说明。width = device-width部分将页面宽度设置为遵循设备的屏幕宽度（具体取决于设备）。initial-scale = 1.0部分设置浏览器首次加载页面时的初始缩放级别。

![image-20190618201440006](/Users/Leo/Library/Application Support/typora-user-images/image-20190618201440006.png)

​		点击切换键即可切换：

![image-20190618201410853](/Users/Leo/Library/Application Support/typora-user-images/image-20190618201410853.png)



​		或者直接查看：



![image-20190618200730803](/Users/Leo/Library/Application%20Support/typora-user-images/image-20190618200730803.png)



​		整体body的尺寸是1387*3839，Color是＃333333，字体大小是12px，字体是effra，背景色是＃E8ECF0

![image-20190618200824170](/Users/Leo/Library/Application Support/typora-user-images/image-20190618200824170.png)





​		整个div左侧部分布局如下：

![image-20190618201815697](/Users/Leo/Library/Application Support/typora-user-images/image-20190618201815697.png)

​		这是一个page-wrapper div,尺寸是1248.3*3839。



![image-20190618202117276](/Users/Leo/Library/Application Support/typora-user-images/image-20190618202117276.png)

​		这是在上一div里嵌套的section：zen-intro.intro,它的尺寸是1248.3*1268，

![image-20190618201634927](/Users/Leo/Library/Application Support/typora-user-images/image-20190618201634927.png)

​		对于右侧布局，右上方是一个header模块：

![image-20190618202604637](/Users/Leo/Library/Application Support/typora-user-images/image-20190618202604637.png)

​		该header模块的尺寸是1248.3*383，颜色是＃333333，字体大小是12px，字体是effra，用padding填充：200px 374.484px 36px 312.062px, 其详细参数如下：

![image-20190618202715404](/Users/Leo/Library/Application Support/typora-user-images/image-20190618202715404.png)

​		对于header模块：

![image-20190618203035680](/Users/Leo/Library/Application Support/typora-user-images/image-20190618203035680.png)





​		这一模块上面是"h1"一级标题，其尺寸是561.75*124:

![image-20190618203208301](/Users/Leo/Library/Application Support/typora-user-images/image-20190618203208301.png)

​		下面是"h2"二级标题，其尺寸是57*133:

![image-20190618203724049](/Users/Leo/Library/Application Support/typora-user-images/image-20190618203724049.png)



​		对于右侧布局，右下方分为一个div分区：zen-summary.summary,它的尺寸是1248.3*274，颜色是＃333333，字体大小是12px，字体是effra，用padding填充：0px 374.484px 120px 312.062px

![image-20190618202340560](/Users/Leo/Library/Application Support/typora-user-images/image-20190618202340560.png)

​		对于div：zen-summary.summary，这一模块左侧敲套为一个div：design-selection，其尺寸是202.42*606.88，颜色是＃333333，字体大小是12px，字体是effort，Margin是36px 0px 0px

![image-20190618204059508](/Users/Leo/Library/Application Support/typora-user-images/image-20190618204059508.png)



​		中间由两个文本段落组成，

![image-20190618203902830](/Users/Leo/Library/Application Support/typora-user-images/image-20190618203902830.png)

​		该文本字体大小是18px，字体是effra，颜色是＃333333，Margin是0px 0px 27px：

![image-20190618204257159](/Users/Leo/Library/Application Support/typora-user-images/image-20190618204257159.png)

​		下面的分区是div：zen-preamble.preamble,这个div的尺寸是1248.3＊610，颜色是＃333333，字体大小是12px，字体是effra，用Padding填充： 120px 374.484px 120px 312.062px:

![image-20190618204541383](/Users/Leo/Library/Application Support/typora-user-images/image-20190618204541383.png)

​		该div:zen-preamble 由一个三级标签和两个段落构成：

![image-20190618204924336](/Users/Leo/Library/Application Support/typora-user-images/image-20190618204924336.png)

​		"h3"标题尺寸是124.33*37，段落"p"中用了"abbr"来标题化缩写title “DOM”，“CSS”。

  	通过对这个网页案例的学习分析，可以根据上下布局的特点制作一个网易设计的详细demo，在主界面的设计中可以通过分析流式布局和固定布局的优劣选取设计，在每个设计分区中通过敲套div模块来丰富界面设计，最终形成一个较为客观的设计界面。
