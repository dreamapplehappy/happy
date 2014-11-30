(下)**解决方法:**

方法一:万能float闭合:
```css
.clearfix{clear:both;overflow:hidden;}
```
上诉办法是在需要清除浮动的地方加个div.clear或者br.clear，我们知道这样能解决基本清浮1动问题。
但是这种方法的最大缺陷就是改变了html结构，虽然只是加个div。

方法二:
最优浮动闭合方案（**推荐**）：
```css
.clearfix:after{content:".";display:block;height:0;clear:both;visibility:hidden}
.clearfix{*+height:1%;}
```
用法很简单，在浮动元素的父云素上添加class=”demo clearfix”。
你会发现这个办法也有个弊端，但的确是小问题。改变css写法就ok了：
```css
.demo:after,.demo2:after{content:".";display:block;height:0;clear:both;visibility:hidden}
.demo,.demo2{*+height:1%;}
```
以上写法就避免了改变html结构，直接用css解决了。

方法三:
很拉轰的浮动闭合办法：
```css
.clearfix{overflow:auto;_height:1%}
```

方法四:
.clearfix{overflow:hidden;_zoom:1;}

参考资料:
[解决方法参考1](http://fireflywithcat.iteye.com/blog/1615606)
[解决方法参考2](http://www.daqianduan.com/3606.html)
[为什么清除浮动](http://hi.baidu.com/doushatuzi/item/8c6f085d7117e7434fff20d8)
[那些年我们一起清除的浮动](http://www.iyunlu.com/view/css-xhtml/55.html)