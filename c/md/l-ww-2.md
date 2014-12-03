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