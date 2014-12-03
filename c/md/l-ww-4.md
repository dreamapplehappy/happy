### 三、安装Android SDK

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

关闭“终端”，再开启一个“终端”，让环境变量生效。启动Android SDK Manager

    $ android
根据需要，选择最新版的Android SDK Platform-tools、Samples for SDK等等下载即可。