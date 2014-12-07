####2.autojump的基本用法

#####autojump的工作方式很简单：它会在你每次启动命令时记录你当前位置，并把它添加进它自身的数据库中。这样，某些目录比其它一些目录添加的次数多，这些目录一般就代表你最重要的目录，而它们的“权重”也会增大。

#####3.运用
现在不管你在哪个目录，你都可以使用下面的语法来直接跳转到这些目录：


+ autojump [目录的名字或名字的一部分]
注意，你不需要输入完整的名称，因为autojump会检索它的数据库，并返回最可能的结果。

+ $ autojump do
如果你也很讨厌打字，那么我推荐你为autojump起个别名，或者使用默认的别名。

+ $ j [目录的名字或名字的一部分]
另外一个引人注目的功能是，autojump支持zsh和自动补完。如果你不确认哪里是不是你要跳转的地方，敲击TAB键就会列出完整路径。

还是同样的例子，输入：

+ $ autojump d
然后敲击tab键，将会返回/root/home/doc或者/root/home/ddl。

最后，对于高级用户，你可以访问目录数据库，并修改它的内容。可以使用下面的命令来手动添加一个目录：