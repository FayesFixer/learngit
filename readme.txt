Git is a distributed version control system.
Git is free software.
git diff 比较被修改的内容(本地当前状态与上次add的内容)
git status 查看本地当前状态，文件是否完成上传之类的
    Changes not staged for commit:
    Changes to be committed: （add之后

版本回退：
git reset --hard (HEAD^)  版本回退 ，HEAD表示当前，HEAD^为上一个， 类似有HEAD~100
git reflog 用于查看历史命令和输出，可用于找回最新版本号
（感觉不如直接使用git checkout 版本号

stage 即为git的暂存区，add之后的文件就在这里 直接编辑的是工作区，上传到的是正式分支区
修改
git checkout -- readme.txt  撤销回到上次add （用.可以代替所有文件吗
git reset HEAD readme.txt   回到当前上传的分支

删除
直接删掉就可以，再使用git rm或者git add

远程同步
上传
git push -u origin master 第一次上传，关联本地和远程库
git push origin master

git push <远程主机名> <本地分支名>:<远程分支名>
如果本地分支名与远程分支名相同，则可以省略冒号

拉取
git pull <远程主机名> <远程分支名>:<本地分支名>
git pull origin next:master   若与本地当前分支合并，则可以省略冒号与后面的部分

要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
git remote add origin git@github.com:FayesFixer/learngit.git

关联一个远程库时必须给远程库指定一个名字，origin是默认习惯命名；

解除同步关系
 git remote rm origin
