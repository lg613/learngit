﻿创建一个目录：mkdir 含路径的目录名 //测试目录为：learngit。
跳转到上一步创建的目录：cd 含路径的目录名
查看当前的目录路径：pwd
初始化仓库：git init

编写一个readme.txt文件放到上面创建的目录下

将readme.txt添加到git仓库中：git add readme.txt
将readme.txt提交到git仓库中：git commit[ -m "提交说明，可自定义，一般用于对新增文件或此次提交改动的说明"]

查看git仓库当前的状态：git status //可查看有没有修改、有没有提交等。

查看readme.txt最新改动与上次提交有什么不同：git diff readme.txt 

查看提交的历史记录：git log[ --pretty=oneline]

注：readme.txt每提交一次就是一个版本。

把readme.txt退回上一个版本：git reset --hard HEAD^ //HEAD表示当前版本，HEAD^表示上一个版本，HEAD~*（*是>0的正整数）表示上*个版本。
把readme.txt回到前面新的版本：git reset --hard * //*是版本号，只需前7位即可，当然也可以超过7位甚至写全，前提是得知道版本号，怎么获取？
查看提交或跳转版本命令的使用记录：git reflog

工作区
即电脑里能看见的目录，比如上面开始时创建的目录（learngit）。

版本库
工作区里面的一个隐藏目录".git"，它不算是工作区的内容，是Git的版本库，版本库里面存了很多东西，最重要的就是称为stage或index的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。

我们把文件往Git版本库里添加的时候，是分两步执行的：
第一步是用git add把文件添加到暂存区。
第二步是用git commit把暂存区的内容提交到当前分支。

查看指定文件内容：cat "含路径的文件名"

查看工作区指定文件与它在版本库中最新版的区别：git diff HEAD -- "含路径的文件名"

撤销工作区指定文件的修改：git checkout -- "含路径的文件名"
两种撤销情况：
①readme.txt自修改后还没有被放到暂存区，撤销修改就回到版本库最新版一样的状态。
②readme.txt已经添加到暂存区，又作了修改，撤销修改就回到添加到暂存区后的状态。

把暂存区的内容撤销，退回到工作区：git reset HEAD "含路径的文件名"

远程仓库：
注册github账号
Git Bash设置：ssh-keygen -t rsa -C  "youemail@example.com"，把邮箱换成自己的然后一路回车即可，无需设置密码。
添加远程仓库：git remote add origin git@github.com:lg613/learngit.git //origin可自定义
将本地仓库的内容推送到github：git push -u origin master // 注：如果是第一次推送，要加“-u”参数，之后无需添加。






