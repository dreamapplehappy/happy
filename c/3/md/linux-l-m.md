###安装JDK
1. 到[官网](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)下载JDK
2. 解压.tar.gz文件
3. 复制解压出来的文件夹到/usr/lib下
          sudo mkdir -p /usr/lib/jvm/
          cp -r jdk1.7.0_71 /usr/lib/jvm/jdk1.7.0_71
  至此JDK安装好了,接下来就是配置
4. 配置环境变量
        sudo gedit /etc/profile
 在文件末尾加上如下内容，保存文件
        # for java
        export JAVA_HOME=/usr/lib/jvm/jdk1.7.0_71
        export JRE_HOME=${JAVA_HOME}/jre
        export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
        export PATH=${JAVA_HOME}/bin:${JRE_HOME}/bin:$PATH
5. 是设置生效:到此JDK配置完成了
        source /etc/profile
6. 设置默认JDK
        sudo update-alternatives --install /usr/bin/java java         /usr/lib/jvm/jdk1.7.0_21/bin/java 1
        sudo update-alternatives --install /usr/bin/javac             javac /usr/lib/jvm/jdk1.7.0_21/bin/javac 1
        sudo update-alternatives --install /usr/bin/javaws            javaws /usr/lib/jvm/jdk1.7.0_21/bin/javaws 1
        sudo update-alternatives --config java
        sudo update-alternatives --config javaws