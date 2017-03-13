### 关于HTML的Doctype和严格模式与混杂模式

DOCTYPE标签是一种标准通用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义（[DTD](http://baike.baidu.com/item/dtd)）来解析文档。

Doctype可声明三种DTD类型，分别表示严格版本、过渡版本以及基于框架的 HTML 文档。

以下主要介绍超文本标记语言以及可扩展超文本标记语言两种集合

（一）超文本标记语言

超文本**严格文档**类型定义：
　　如果需要干净的标记，免于表现层的混乱，则使用此类型。请与层叠样式表配合使用：
　　（公共标识符称为：“-//W3C//DTD HTML 4.01//en”。）

```javascript
<!DOCTYPE HTML
　　PUBLIC "-//W3C//DTD HTML 4.01//en"
　　"http://www.w3. org/TR/html4/strict.dtd">
```
超文本**过渡文档**类型定义：
　　可包含万维网联盟所期望移入样式表的呈现属性和元素。如果读者使用了不支持层叠样式表的浏览器以至于不得不使用超文本标记语言的呈现特性时，则使用此类型：
（公共标识符称为：“-//W3C//DTD HTML 4.01 Transitional//en”。）

```javascript
<!DOCTYPE HTML
PUBLIC "-//W3C//DTD HTML 4.01 Transitional//en"
"http://www.w3. org/TR/html4/loose.dtd">
```

超文本框架集文档类型定义：
　　框架集文档类型定义应当被用于带有框架的文档。除 frameset 元素取代了 body 元素之外，等同于过渡文档类型定义：
　　（公共标识符称为：“-//W3C//DTD HTML 4.01 Frameset//en”。）

```javascript
<!DOCTYPE HTML
PUBLIC "-//W3C//DTD HTML 4.01 Frameset//en"
"http://www.w3. org/TR/html4/frameset.dtd">
```

（二）可扩展超文本标记语言

可扩展超文本标记语言严格文档类型定义:
（公共标识符称为：“-//W3C//DTD XHTML 1.0 Strict//en”。）

```
<!DOCTYPE html
PUBLIC "-//W3C//DTD XHTML 1.0 Strict//en"
"http://www.w3. org/TR/xhtml1/DTD/xhtml1-strict.dtd">

```


