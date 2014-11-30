#Cordova安装
==============================
---
###一、安装nodejs

1、确保你的ubuntu安装了依赖包和 python，gcc，g++组件以及可选的git组件，部分可能会在更新源中已经安装。如果没有则要重新安装，命令如下：

    $ sudo apt-get install g++ curl libssl-dev apache2-utils

    $ sudo apt-get install python 

    $ sudo apt-get install build-essential

    $ sudo apt-get install gcc

    $ sudo apt-get install g++

2、从nodeJS官网 http://nodejs.org/ 下载最新源代码包

    // 下载
    $ wget http://nodejs.org/dist/v0.10.14.tar.gz

    // 解压：
    $ tar -zxf node-v0.10.14.tar.gz 
    $ cd node-v0.10.14 

    // 默认安装： （默认在home目录下）
    $ ./configure 
    $ make 
    $ sudo make install 

    //选择目录安装（将nodejs安装在/usr/local/node目录下）
    $ ./configure –prefix=/usr/local/node 
    $ make 
    $ sudo make install
3、检测是否安装成功

    //通过检测node的版本号查看nodejs有没有安装成功，命令如下所示：
    $ node --version

***

###二、安装ant

#####1、命令直接安装
    $ sudo apt-get install ant

#####2、手动安装

1. 到Apache官网下载最新版本的ant：http://ant.apache.org/bindownload.cgi

2. 解压下载下来的.tar.gz文件：
`$ tar -xf apache-ant-1.8.2-bin.tar.gz `
3. 将解压出来的文件移动到/opt/下：
`$ sudo mv apache-ant-1.8.2 /opt/`
4. 配置环境变量：
`$ sudo gedit /etc/profile`
    
   在原来基础上添加以下内容：
     
>export ANT_HOME=/opt/apache-ant-1.8.2

>export JAVA_HOME=/usr/lib/jvm/java-6-openjdk

>export PATH=$JAVA_HOME/bin:$PATH:$ANT_HOME/bin

>export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar

#####验证是否安装成功： 
    $ ant -version

***

###三、安装Android SDK

#####1、安装32位库文件

Android SDK中的adb程序是32位的，Ubuntu x64系统需要安装32位库文件，用于兼容32位的程序。如果不安装，adb会出错：java.io.IOException: error=2

    $ sudo apt-get install -y libc6-i386 lib32stdc++6 lib32gcc1 lib32ncurses5 lib32z1

#####2、安装Android SDK
(1)安装jdk

     $ sudo apt-get install openjdk-7-jdk

(2)安装SDK
官方下载页面，选择“USE AN EXISTING IDE”，下载不含IDE的纯SDK：http://developer.android.com/sdk/index.html

    $ cd ~/Downloads/

    $ wget http://dl.google.com/android/android-sdk_r23.0.2-linux.tgz

    $ tar -zxvf android-sdk_r23.0.2-linux.tgz

    $ echo 'export ANDROID_HOME="'$HOME'/Downloads/android-sdk-linux"' >> ~/.bashrc

    $ echo 'export PATH="$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools"' >> ~/.bashrc

    $ echo 'export JAVA_CMD="/usr/lib/jvm/java-7-openjdk-amd64/bin/java"' >> ~/.bashrc

关闭“终端”，再开启一个“终端”，让环境变量生效。

启动Android SDK Manager

    $ android

根据需要，选择最新版的Android SDK Platform-tools、Samples for SDK等等下载即可。

(其他详情参考：http://www.cnblogs.com/sink_cup/archive/2011/10/31/ubuntu_x64_android_sdk_java.html)


***

###四、安装cordova

    $ sudo npm install -g cordova

***

###五、更新cordova

    $ sudo npm update cordova -g

***
###六、创建并运行

(1)新建一个目录test,并进入

    $ mkdir test
    $ cd test/

(2)创建一个“myapp”工程

    //第一个myapp是文件夹的名称；com.yourname.myapp是app的id；第二个myapp是工程的名称，也是应用的名称

    $ cordova create myapp com.yourname.myapp MyApp

如果无法无法成功创建：
>可能因为从网址 https://git-wip-us.apache.org/ 下载速度太慢，容易超时。

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

(3)进入工程目录

    $ cd myapp

(4)添加平台支持（这里只提供安卓）

    $ cordova platforms add android

也可有选择的添加其他平台支持，针对每种平台，均应确定已配置好了对应平台的开发环境

    $ cordova platform add ios
    $ cordova platform add amazon-fireos
    $ cordova platform add android
    $ cordova platform add blackberry10
    $ cordova platform add firefoxos
    $ cordova platform add wp7
    $ cordova platform add wp8
    $ cordova platform add windows8

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

(9)常用命令

>（1）create <directory> [<id> [<name>]]
创建一个cordova工程，id为package名。

>（2）platform [ls | list]列出该工程支持哪些平台

>（3）platform add <platform> [<platform> ...]为工程添加一个或多个平台支持

>（4）platform [rm | remove] <platform> [<platform> ...]删除该工程的某个平台支持

>（5）platform [up | update] <platform>更新该工程某个平台的Cordova版本

>（6）plugin [ls | list]列出该工程包含哪些插件

>（7）plugin add <path-to-plugin> [<path-to-plugin> ...]为工程添加一个或多个插件

>（8）plugin [rm | remove] <plugin-name> [<plugin-name> ...]从该工程中删除某个插件

>（9）plugin search [<keyword1> <keyword2> ...]根据关键字从registry中搜索插件

>（10）compile [platform...]编译指定平台的app包

>（11）build [<platform> [<platform> [...]]]先做prepare（拷贝文件）后做compile

>（12）emulate [<platform> [<platform> [...]]]启动模拟器运行应用

>（13）serve [port]启动本地web服务来访问www，默认端口是8000platform和platforms等价plugin和plugins等价详细的内容可以通过cordova help命令查看。