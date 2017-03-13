### CSS选择器

#### 1.id选择器

```
#note{}
```

#### 2.类选择器class

```
.note{}
```

#### 3.类型选择器Element

```
td{}
a{}
```

#### 4.属性选择器

1. E1\[attr\]  选择具有attr属性的E1 
2. E1\[attr=value\] 选择具有attr属性且属性值等于value的E1 
3. E1\[attr~=value\] 选择具有attr属性且属性值为一用空格分隔的字词列表，其中一个等于value的E1。这里的value不能包含空格 
4. E1\[attr\|=value\] 选择具有attr属性且属性值为一用连字符分隔的字词列表，由value开始的E1

```
span[class=demo] { color: red; } 

div[speed="fast"][dorun="no"] { color: red; } 

a[rel~="copyright"] { color:black; } 
```

> CSS3

1. E\[att^="val"\] 匹配具有att属性、且值以val开头的E元素
2. E\[att$="val"\] 匹配具有att属性、且值以val结尾的E元素
3. E\[att\*="val"\] 匹配具有att属性、且值中含有val的E元素

#### 5.子对象选择器

```
body > p { font-size:14px; } 
/* 所有作为body的子对象的p对象字体尺寸为14px */ 

div ul>li p { font-size:14px; } 
```

#### 6.包含选择器

```
table td { font-size:14px; } 

div.sub a { font-size:14px; } 
```

#### 7.分组选择器

```
.td1,div a,body { font-size:14px; } 
```

#### 8.通配符选择器

```
* 
*[lang=fr] { font-size:14px; width:120px; } 
*.div { text-decoration:none; } 
```

#### 9.伪类选择器

:link  
:visited  
:hover  
:active  
:first-letter 此伪对象仅作用于块对象。内联对象要使用该伪对象，必须先设定对象的height或width属性，或者设定position属性为absolute，或者设定display属性为block。  
在此伪类中配合使用font-size属性和float属性可以制作首字下沉效果。   
:first-line  
:first-child  
:first  
:left  
:right  
:lang

> CSS3


| 结构性伪类 | [E:root](itss://chm/attribute_selector_04.html) | 匹配文档的根元素。在HTML中，根元素永远是HTML |
| :--- | :--- | :--- |
| 结构性伪类 | [E:nth-child\(n\)](itss://chm/attribute_selector_05.html) | 匹配父元素中的第n个子元素E |
| 结构性伪类 | [E:nth-last-child\(n\)](itss://chm/attribute_selector_06.html) | 匹配父元素中的倒数第n个结构子元素E |
| 结构性伪类 | [E:nth-of-type\(n\)](itss://chm/attribute_selector_07.html) | 匹配同类型中的第n个同级兄弟元素E |
| 结构性伪类 | [E:nth-last-of-type\(n\)](itss://chm/attribute_selector_08.html) | 匹配同类型中的倒数第n个同级兄弟元素E |
| 结构性伪类 | [E:last-child](itss://chm/attribute_selector_09.html) | 匹配父元素中最后一个E元素 |
| 结构性伪类 | [E:first-of-type](itss://chm/attribute_selector_10.html) | 匹配同级兄弟元素中的第一个E元素 |
| 结构性伪类 | [E:only-child](itss://chm/attribute_selector_11.html) | 匹配属于父元素中唯一子元素的E |
| 结构性伪类 | [E:only-of-type](itss://chm/attribute_selector_12.html) | 匹配属于同类型中唯一兄弟元素的E |
| 结构性伪类 | [E:empty](itss://chm/attribute_selector_13.html) | 匹配没有任何子元素（包括text节点）的元素E |
| 目标伪类 | [:target](itss://chm/attribute_selector_20.html) | 匹配相关URL指向的E元素 |
| UI元素状态伪类 | [E:enabled](itss://chm/attribute_selector_14.html) | 匹配所有用户界面（form表单）中处于可用状态的E元素 |
| UI元素状态伪类 | [E:disabled](itss://chm/attribute_selector_15.html) | 匹配所有用户界面（form表单）中处于不可用状态的E元素 |
| UI元素状态伪类 | [E:checked](itss://chm/attribute_selector_16.html) | 匹配所有用户界面（form表单）中处于选中状态的元素E |
| UI元素状态伪类 | [E::selection](itss://chm/attribute_selector_17.html) | 匹配E元素中被用户选中或处于高亮状态的部分 |
| 否定伪类 | [E:not\(s\)](itss://chm/attribute_selector_18.html) | 匹配所有不匹配简单选择符s的元素E |
| 通用兄弟元素选择器 | [E ~ F](itss://chm/attribute_selector_19.html) | 匹配E元素之后的F元素 |

#### 10.伪对象选择器

:before  
:after

