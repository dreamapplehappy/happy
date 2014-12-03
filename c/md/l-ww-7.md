解决办法：
>打开 cordova 目录下的platforms.js文件：

>>可通过以下方法查找：
>>`$ sudo find / -name 'platforms.js'`

>修改其中的url配置地址。这里可以修改为git附件包下载地址，具体到官方github查找https://github.com/apache/ (可用以下内容替换相应内容)
>>`'android' : {
        parser : './metadata/android_parser',
    url : 'https://github.com/apache/cordova-android/archive/master.zip',
    version: '3.7.0'
    },`



>>`'www':{
        hostos : [],
        //url    : 'https://git-wip-us.apache.org/repos/asf?p=cordova-app-hello-world.git',
    url : 'https://github.com/apache/cordova-android/archive/master.zip',
    version: '3.7.0'
        //source : 'git',
        //version: '3.6.3'
    },`