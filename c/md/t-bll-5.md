**CSS Brightness**

Brightness 滤镜是对图片的亮度进行处理，属性值为百分比。该属性的值可以是小数或百分比，其中100 ％或1图像正常，小于1或100%的为降低图像亮度，大于1或100%为增加图像亮度。

    .brightness img{
        filter:brightness(50%);
    }

**CSS Contrast**

Contrast 滤镜是对图片最亮的地方和最暗的地方进行调整，从而改变图片的均衡感。这个值可以是小数或百分比，数值1为对比度，使图像更暗用小于1的值，使之更亮你改变的值大于1 。

    .contrast img{
        filter:contrast(0.3);
    ｝

**CSS Opacity**

Opacity 这个滤镜估计就比较熟悉了，是使图片透明。正常的不透明度设置，将被设置为1 ，如果你想我这个透明的，那么你可以将此值设置为小于1 。

    .opacity img{
        opacity: 0.3;
    }