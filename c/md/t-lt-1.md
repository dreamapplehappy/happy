### CSS清除浮动
###### 作者：刘铁
------
在设计网页布局时，有一个很蛋疼的问题，那就是使用浮动（float）时的**父容器塌陷**问题。
先说一下什么是塌陷：
塌陷：父元素只包含浮动元素，那么它的高度就会塌缩为零（前提就是你们没有设置高度（height）属性，或者设置了为auto。就会出现这种情况，当然不是所用的浏览器都是这样的，在IE8下面没有这种情况。）如果父元素不包含任何的可见背景，这个问题会很难被注意到，但是这是一个很重要的问题。

先看看代码
**CSS代码:**
```css
#clearfix{width:900px; background-color:#556677; margin:0 auto;   height:auto; }
.test{border: 5px solid #126121; float: left; height: 200px;  margin-left: 18px;
            margin-top: 40px;  width: 150px; }
```
```html
<div class="clearfix" id="clearfix">
        <div class="test">111</div>
        <div class="test ">222</div>
        <div class=" test ">333</div>
        <div class=" test ">444</div>
        <div class=" test ">555</div>
</div>
```
这样的话，在fireFox、chrome下是没有body的#556677颜色。并不是没有上色。你查看body元素的盒型图会发现，他的高度为0。这就是塌陷。
######(上)
------