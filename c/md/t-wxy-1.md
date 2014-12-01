### 使用js+flash实现copy效果
#####   作者 ：王雪莹
------
我们在很多网站上都能看到复制代码段的效果，例如个人博客，bootstrap等网站，现在小编就分析一下他的实现原理，方便大家更简单的使用。
+ 效果演示地址：
    http://demo.jb51.net/js/ZeroClipboard/index.html
+ 实现原理分析：
首先介绍一个跨浏览器的库类 Zero Clipboard 。它利用 Flash 进行复制，所以只要浏览器装有 Flash 就可以运行，而且比 IE 的 document.execCommand("Copy") 更加灵活。他会自动创建一个的flash，让其漂浮在按钮之上，这样其实点击的不是按钮而是 Flash ，也就可以使用 Flash 的复制功能了
+ 注意事项：
一定要在PHP环境下运行，即使你打开的是html文件。。
+ 需要的引入两个js jquery库和zclip库
------
######(上)