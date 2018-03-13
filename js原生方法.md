通过html dom可以访问javascript html文档的所有元素。
当网页被加载时，浏览器会创建页面的文档对象模型（Document Object Model）。

通过可编程的对象模型，JavaScript 获得了足够的能力来创建动态的 HTML。
JavaScript 能够改变页面中的所有 HTML 元素
JavaScript 能够改变页面中的所有 HTML 属性
JavaScript 能够改变页面中的所有 CSS 样式
JavaScript 能够对页面中的所有事件做出反应

我们需要通过javascript操作html元素，查找这些html元素有三种方法：
1.通过id查找：
```
var doc=document.getElementById("idName");
```
2.通过标签名查找：
```
var doc=document.getElementsByTagName("tagName");
```
3.通过类名查找：
```
var doc = document.getElementsByClassName("className");
````

html dom允许javascript改变html元素的内容。
1.改变html输出流
在`javascript中，document.write()`可用于直接向html输出流直接写内容。
tip:绝不要使用在文档加载之后使用 document.write()。这会覆盖该文档。
2.改变`html`内容
修改`html`内容的最简单的方法是使用`innerHTML`属性。如：
`document.getElementById(idName).innerHTML="文本内容"`
3.改变`html`属性
`document.getElementById(id).attribute='new value'，如：`
`document.getElementById(idName).src = 'location.png'`

`html dom`允许`javascript`改变`html`元素样式。
```
document.getElementById(id).style.property=new style，如：
document.getElementById(idName).style.color="red";
```
html dom使`javascript`有能力对html事件做出反应。
你可以使用事件属性，比如：
<button onclick="func()">点击</button>
你也可以使用javascript来向html元素分配事件，比如：
document.getElementById("idName").onclick=function(){...};

添加和删除节点（HTML 元素）。（重点温习的内容）
如需向html dom添加新元素，必须先添加元素节点，然后向该元素追加元素节点。
```
var para=document.createElement("p");
var node=document.createTextNode("这是新段落。");
para.appendChild(node);
var element=document.getElementById("div1");
element.appendChild(para);
```
上述操作有三个步骤：
1.创建新的 <p> 元素
2.创建文本节点
3.向已有的元素追加新元素
当然上面也可以不创建新的元素，直接添加到已有的元素中，比如：
var eleNode = document.createTextNode('这是新段落');
document.getElementById('div1').appendChild(eleNode);
常用的dom对象方法：


在html dom（文档对象模型）中，每个部分都是节点：
文档本身是文档节点
所有 HTML 元素是元素节点
所有 HTML 属性是属性节点
HTML 元素内的文本是文本节点
注释是注释节点
在html dom中，element对象表示html元素，下面这些属性和方法可用于所有HTML元素上。


![img1](http://ol1rnobmr.bkt.clouddn.com/1%20%283%29.png)
![img2](http://ol1rnobmr.bkt.clouddn.com/1%20%282%29.png)
![img3](http://ol1rnobmr.bkt.clouddn.com/1%20%281%29.png)