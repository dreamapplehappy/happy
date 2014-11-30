**表达式**

    img {
     filter: type(value);
    }

css3中的使用方法，一般都需要加浏览器前缀。

    img
    {
       filter: type(value);
      -webkit-filter: type(value);
      -moz-filter: type(value);
      -ms-filter: type(value);
      -o-filter: type(value);
    }

#### 浏览器支持
+ 目前支持这一目标的唯一浏览器是wekbit浏览器， Chrome和Safari浏览器。
+ CSS过滤器已经在Chrome自版本21支持，已经在Safari浏览器版本6中支持。
+ 目前还不知道，IE版本10或Firefox版本17是否会支持这些属性。但现在支持滤镜最好的浏览器是WebKit的，如Chrome和Safari浏览器。