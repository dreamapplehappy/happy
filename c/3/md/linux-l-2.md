5.是设置生效:到此JDK配置完成了

        source /etc/profile
6.设置默认JDK

        sudo update-alternatives --install /usr/bin/java java         /usr/lib/jvm/jdk1.7.0_21/bin/java 1
        sudo update-alternatives --install /usr/bin/javac             javac /usr/lib/jvm/jdk1.7.0_21/bin/javac 1
        sudo update-alternatives --install /usr/bin/javaws            javaws /usr/lib/jvm/jdk1.7.0_21/bin/javaws 1
        sudo update-alternatives --config java
        sudo update-alternatives --config javaws
7.为保证正确，进项测试

        java -version