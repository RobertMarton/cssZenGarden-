# cssZenGarden案例研究报告
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
