### 关于HTML的Doctype和严格模式与混杂模式

DOCTYPE标签是一种标准通用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义（[DTD](http://baike.baidu.com/item/dtd)）来解析文档。

Doctype可声明三种DTD类型，分别表示严格版本、过渡版本以及基于框架的 HTML 文档。

以下主要介绍超文本标记语言以及可扩展超文本标记语言两种集合

（一）超文本标记语言

超文本**严格文档**类型定义：
　　如果需要干净的标记，免于表现层的混乱，则使用此类型。请与层叠样式表配合使用：
　　（公共标识符称为：“-//W3C//DTD HTML 4.01//en”。）

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//en" "http://www.w3. org/TR/html4/strict.dtd">
```
超文本**过渡文档**类型定义：
　　可包含万维网联盟所期望移入样式表的呈现属性和元素。如果读者使用了不支持层叠样式表的浏览器以至于不得不使用超文本标记语言的呈现特性时，则使用此类型：
（公共标识符称为：“-//W3C//DTD HTML 4.01 Transitional//en”。）

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//en" "http://www.w3. org/TR/html4/loose.dtd">
```

超文本框架集文档类型定义：
　　框架集文档类型定义应当被用于带有框架的文档。除 frameset 元素取代了 body 元素之外，等同于过渡文档类型定义：
　　（公共标识符称为：“-//W3C//DTD HTML 4.01 Frameset//en”。）

```javascript
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//en" "http://www.w3. org/TR/html4/frameset.dtd">
```

（二）可扩展超文本标记语言

可扩展超文本标记语言严格文档类型定义:
（公共标识符称为：“-//W3C//DTD XHTML 1.0 Strict//en”。）

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//en" "http://www.w3. org/TR/xhtml1/DTD/xhtml1-strict.dtd">

```

可扩展超文本标记语言过渡文档类型定义：
　　可包含 W3C 所期望移入样式表的呈现属性和元素。如果您的读者使用了不支持层叠样式表（CSS）的浏览器以至于您不得不使用 XHTML 的呈现　　特性时，请使用此类型：
　　（公共标识符称为：“-//W3C//DTD XHTML 1.0 Transitional//en”。）

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//en" "http://www.w3. org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

可扩展超文本标记语言框架集文档类型定义：
　　当您希望使用框架时，请使用此文档类型定义！
　　（公共标识符称为：“-//W3C//DTD XHTML 1.0 Frameset//en”。）

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//en" "http://www.w3. org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

当浏览器厂商开始创建与标准兼容的浏览器时，他们希望确保向后兼容性。为了实现这一点，他们创建了两种呈现模式：标准模式和混杂模式


>在标准模式中，浏览器以其支持的最高标准呈现页面。

>在混杂模式中，页面以一种比较宽松的向后兼容的方式显示。混杂模式通常模拟老式浏览器的行为以防止老站点无法工作。

关于模式触发

浏览器根据DOCTYPE是否存在以及使用的哪种DTD来选择要使用的呈现方法。

如果XHTML、HTML 4.01文档包含形式完整的DOCTYPE，那么它一般以标准模式呈现。

包含过渡DTD和URI的DOCTYPE也导致页面以标准模式呈现，但是有过渡DTD而没有URI会导致页面以混杂模式呈现。

DOCTYPE不存在或形式不正确会导致HTML和XHTML文档以混杂模式呈现。

html5既然没有DTD，也就没有严格模式与宽松模式的区别，html5有相对宽松的语法，实现时，已经尽可能大的实现了向后兼容。


