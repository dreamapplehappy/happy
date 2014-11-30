### 在$HOME下安装nodejs npm
#### 作者：谢俊杰
------
首先是nodejs在linux下的依赖：

* GCC 4.2 or newer
* Python 2.6 or 2.7
* GNU Make 3.81 or newer
* libexecinfo (FreeBSD and OpenBSD only)

接下来可以去[这里](https://gist.github.com/isaacs/579814)使用第一种方法 把nodejs 编译安装到 ~/local 中. 若脚本无法正常运行，也可以一条条手打.

完成后，使用如下命令检查是否安装成功
```language-bash
$ node -v
v 0.10.29
$ npm -v
1.4.16
```
安装node版本管理工具n
```language-bash
$ npm install -g n
$ echo 'export N_PREFIX=$HOME/local' >> ~/.bashrc
$ . ~/.bashrc
```
使用 n –help查看帮助 