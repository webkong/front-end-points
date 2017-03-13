### CSS

#### 1.介绍CSS的盒子模型？

* 有两种， IE 盒子模型、标准 W3C 盒子模型，IE的content部分包含了 border 和 pading;

* 盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border).

#### 2.CSS 选择符有哪些？哪些属性可以继承？优先级算法如何计算？ CSS3新增伪类有那些？

*   1.id选择器（ # myid）    
    2.类选择器（.myclassname）    
    3.标签选择器（div, h1, p）    
    4.相邻选择器（h1 + p）    
    5.子选择器（ul > li）    
    6.后代选择器（li a）    
    7.通配符选择器（ * ）    
    8.属性选择器（a[rel = "external"]）    
    9.伪类选择器（a: hover, li: nth - child）
*   可继承的样式： font-size font-family color, UL LI DL DD DT;
*   不可继承的样式：border padding margin width height ;
*   优先级就近原则，同权重情况下样式定义最近者为准;
*   载入样式以最后载入的定位为准;优先级为:  
    !important >  id > class > tag    
    important 比 内联优先级高

#### 3.居中一个浮动元素?

```css
.div {
    width:500px;
    height:300px;//高度可以不设
    margin: -150px 0 0 -250px;
    position:relative;相对定位
    background-color:pink;//方便看效果
    left:50%;
    top:50%;
} 
```

#### 4.列出display的值，说明他们的作用。position的值,relative和absolute定位原点是？

1. block 象块类型元素一样显示
none 缺省值。象行内元素类型一样显示
inline-block 象行内元素一样显示，但其内容象块类型元素一样显示
list-item 象块类型元素一样显示，并添加样式列表标记

2. 
    * absolute 生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。 
    * fixed （老IE不支持）生成绝对定位的元素，相对于浏览器窗口进行定位。
    * relative生成相对定位的元素，相对于其正常位置进行定位。
    * static  默认值。没有定位，元素出现在正常的流中*（忽略 top,bottom,left, right z-index 声明）
    * inherit 规定从父元素继承 position 属性的值



