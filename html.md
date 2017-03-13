### HTML

#### 1.Doctype作用? 严格模式与混杂模式如何区分？它们有何意义?

* `<!DOCTYPE> `声明位于文档中的最前面，处于 `<html>` 标签之前。告知浏览器的解析器，用什么文档类型规范来解析这个文档
* 严格模式的排版和JS运作模式是以该浏览器支持的最高标准运行
* 在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作
* DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现

[Html的严格模式和混杂模式](detail/html.md)

#### 2.行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

* CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，比如div默认display属性值为“block”，成为“块级”元素；span默认display属性值为“inline”，是“行内”元素

* 行内元素有：a b span img input select strong

* 块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p

* 知名的空元素： <br> <hr> <img> <input> <link> <meta> 

* 鲜为人知的空元素： <area> <base> <col> <command> <embed> <keygen> <param> <source> <track> <wbr>

