创建一个目录：mkdir 含路径的目录名
跳转到上一步创建的目录：cd 含路径的目录名
查看当前的目录路径：pwd
初始化仓库：git init

编写一个readme.txt文件放到上面创建的目录下

将readme.txt添加到git仓库中：git add readme.txt
将readme.txt提交到git仓库中：git commit[ -m "提交说明，可自定义，一般用于对新增文件或此次提交改动的说明"]

查看git仓库当前的状态：git status //可查看有没有修改、有没有提交等。

查看readme.txt最新一次提交与这次提交前做了哪些改动：git diff readme.txt
