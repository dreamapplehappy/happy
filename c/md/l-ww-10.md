(6)参考 API 文档，开发应用

>API 参考：
>http://docs.phonegap.com/zh/3.4.0/cordova_plugins_pluginapis.md.html

>http://docs.phonegap.com/zh/3.4.0/cordova_events_events.md.html

(7)构建应用

    $ cordova build
    //或者 
    $ cordova build android

(8)测试应用

    // 在模拟器上安装测试应用（如果已经安装模拟器）
    $ cordova emulate android

    //使用真机测试(连接手机，打开调试模式)
    $ cordova run android

    //在浏览器中运行(浏览器访问地址：http://localhost:8000/)
    $ cordova serve android
