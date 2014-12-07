###linux使用笔记
######作者：李金祥

#####添加软件源(只需三步)
    sudo add-apt-repository ppd:docky-core/ppa

    sudo apt-get update

    sudo apt-get install docky

#####文件操作
1. 文件复制
        cp [选项] 源文件或目录 目标文件或目录
        $cp exam.txt /usr/wang/
2. 文件移动(把laravel文件夹移动到/var/www/larvel文件夹下)
-r表示如果有那个文件会提示是否覆盖,-f不会提示
***mv不同于cp,是复制到新的目录并且取得新的名字***
        mv [选项] 源文件或目录 目标文件或目录(新名字)  
        mv -r laravel /var/www/laravel

