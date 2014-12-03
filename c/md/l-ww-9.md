(5)添加插件支持
主要为系统硬件访问的插件，常见如照相机、媒体访问、设备访问、加速设备、定位设备等。应按需添加。

    //基本设备资讯 （设备 API）：
    $ cordova plugin add org.apache.cordova.device

    //网路连接和电池事件：
    $ cordova plugin add org.apache.cordova.network-information
    $ cordova plugin add org.apache.cordova.battery-status
    
    //加速度计、 指南针、 和地理定位：
    $ cordova plugin add org.apache.cordova.device-motion
    $ cordova plugin add org.apache.cordova.device-orientation
    $ cordova plugin add org.apache.cordova.geolocation

    //相机、 媒体重播和捕获：
    $ cordova plugin add org.apache.cordova.camera
    $ cordova plugin add org.apache.cordova.media-capture
    $ cordova plugin add org.apache.cordova.media

    //访问设备或网路 （档 API） 上的档：
    $ cordova plugin add org.apache.cordova.file
    $ cordova plugin add org.apache.cordova.file-transfer

    //通过对话方块或振动发出通知：
    $ cordova plugin add org.apache.cordova.dialogs
    $ cordova plugin add org.apache.cordova.vibration

    //连络人：
    $ cordova plugin add org.apache.cordova.contacts

    //全球化：
    $ cordova plugin add org.apache.cordova.globalization

    //闪屏：
    $ cordova plugin add org.apache.cordova.splashscreen

    //打开新的浏览器视窗 (InAppBrowser):
    $ cordova plugin add org.apache.cordova.inappbrowser

    //调试主控台：
    $ cordova plugin add org.apache.cordova.console