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