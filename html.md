### HTML

#### 1.Doctype作用? 严格模式与混杂模式如何区分？它们有何意义?

* `<!DOCTYPE>`声明位于文档中的最前面，处于 `<html>` 标签之前。告知浏览器的解析器，用什么文档类型规范来解析这个文档
* 严格模式的排版和JS运作模式是以该浏览器支持的最高标准运行
* 在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作
* DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现

[Html的严格模式和混杂模式](detail/html.md)

#### 2.行内元素有哪些？块级元素有哪些？ 空\(void\)元素有那些？

* CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，比如div默认display属性值为“block”，成为“块级”元素；span默认display属性值为“inline”，是“行内”元素

* 行内元素有：a b span img input select strong

* 块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p

* 知名的空元素： `<br> <hr> <img> <input> <link> <meta>`

* 鲜为人知的空元素：`<area> <base> <col> <command> <embed> <keygen> <param> <source> <track> <wbr>`

#### 3.link 和@import 的区别是？

\(不常用\)

* link属于XHTML标签，而@import是CSS提供的;
* 页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;
* import只在IE5以上才能识别，而link是XHTML标签，无兼容问题;
* link方式的样式的权重 高于@import的权重. 

#### 4.浏览器的内核分别是什么?

| 浏览器 | 内核 |
| :--- | :--- |
| IE | Trident |
| Mozilla | Gecko |
| Opera | Presto-&gt;Blink |
| Chrome | Blink（WebKit的分支） |

#### 5.常见兼容性问题？

* png24位的图片在iE6浏览器上出现背景，解决方案是做成PNG8.

* 浏览器默认的margin和padding不同。一般不会加一个全局的`{margin:0;padding:0;}`来统一，而是使用自己的或者第三方的reset

* IE6双边距bug:块属性标签float后，又有横行的margin情况下，在ie6显示margin比设置的大。   
  浮动ie产生的双倍距离 `#box{ float:left; width:10px; margin:0 0 0 100px;}`这种情况之下IE会产生20px的距离，解决方案是在float的标签样式控制中加入`_display:inline;`将其转化为行内属性。\(\_这个符号只有ie6会识别,这是hack相关内容\)。

  渐进识别的方式，从总体中逐渐排除局部。   
  首先，巧妙的使用“\9”这一标记，将IE游览器从所有情况中分离出来。   
  接着，再次使用“+”将IE8和IE7、IE6分离开来，这样IE8已经独立识别。

```css
.bb{
    background-color:#f1ee18;/*所有识别*/
    .background-color:#00deff\9; /*IE6、7、8识别*/
    +background-color:#a200ff;/*IE6、7识别*/
    _background-color:#1e0bd1;/*IE6识别*/
} 
```

* IE下,可以使用获取常规属性的方法来获取自定义属性,也可以使用getAttribute\(\)获取自定义属性;Firefox下,只能使用getAttribute\(\)获取自定义属性. 解决方法:统一通过getAttribute\(\)获取自定义属性.

* IE下,even对象有x,y属性,但是没有pageX,pageY属性;   
  Firefox下,event对象有pageX,pageY属性,但是没有x,y属性.

* Chrome 中文界面下默认会将小于 12px 的文本强制按照 12px 显示, 可通过加入 CSS 属性 `-webkit-text-size-adjust: none;`解决.

* 超链接访问过后hover样式就不出现了 被点击访问过的超链接样式不在具有hover和active了解决方法是改变CSS属性的排列顺序: L-V-H-A :  
  `a:link {} a:visited {} a:hover {} a:active {}`

#### 5.html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 HTML5？

* HTML5 现在已经不是[SGML](http://baike.baidu.com/item/%E6%A0%87%E5%87%86%E9%80%9A%E7%94%A8%E7%BD%AE%E6%A0%87%E8%AF%AD%E8%A8%80/10471466?fromtitle=SGML&fromid=2901416)的子集，主要是关于图像，位置，存储，多任务等功能的增加

| tag | description |
| :--- | :--- |
| canvas | 绘图 |
| video/audio | 媒体播放 |
| localStorage | 本地离线存储，长期存储数据，浏览器关闭后不丢失 |
| sessionStorage | 临时存储，关闭浏览器后自动删除 |
| article/footer/header/nav/section | 语义化更好的标签 |
| calendar/date/time/email/url/search | 新增表单空间的type |
| webworker/websocket/Geolocation | 新的技术 |
| ~~basefont/big/center/font/s/strike/tt/u~~ | 删除的纯表现的元素 |
| ~~frame/frameset/noframes~~ | 对可用性产生影响的元素 |


#### 6.让浏览器支持html5

* IE8/IE7/IE6支持通过document.createElement方法产生的标签，可以利用这一特性让这些浏览器支持HTML5新标签，浏览器支持新标签后，还需要添加标签默认的样式：

* 当然最好的方式是直接使用成熟的框架、使用最多的是html5shim框架   
```
<!--[if lt IE 9]>
<script src="http://html5shim.googlecode.com/svn/trunk/html5.js></script> 
<![endif]--> 
```

#### 7.语义化的理解？

* 用正确的标签做正确的事情！

* html语义化就是让页面的内容结构化，便于对浏览器、搜索引擎解析；

* 在没有样式CCS情况下也以一种文档格式显示，并且是容易阅读的。

* 搜索引擎的爬虫依赖于标记来确定上下文和各个关键字的权重，利于SEO。

* 使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。

#### 8.Html5离线存储？

sessionStorage 持久化本地存储
localStorage   临时本地存储

#### 9.iframe的缺点？

* iframe会阻塞主页面的Onload事件；
* iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。
使用iframe之前需要考虑这两个缺点。如果需要使用iframe，最好是通过javascript动态给iframe添加src属性值，这样可以可以绕开以上两个问题。

#### 10.如何实现浏览器内多个标签页之间的通信? 

调用localstorge、cookies等本地存储方式

#### 11.webSocket如何兼容低浏览器？

Adobe Flash Socket 、 ActiveX HTMLFile (IE) 、 基于 multipart 编码发送 XHR 、 基于长轮询的 XHR


