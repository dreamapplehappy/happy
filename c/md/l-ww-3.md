#### 二、安装ant

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