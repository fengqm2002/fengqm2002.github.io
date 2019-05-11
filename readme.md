1.先在github上面创建一个项目地址

2.命令行选好自己目标文件夹的位置后，将远程仓库内容克隆到本地仓库
  
  git clone https://github.com/fenqm2002/fengqm2002.github.io
  
3.其次进入到本地项目的目录文件下面

执行

a、  git init：初始化本地仓库

b、git add . 添加全部已经修改的文件，准备commit 提交 

该命令效果等同于 git add -A

C、git commit -m ‘提交说明’  将修改后的文件提交到本地仓库，如：git commit -m ‘项目创建’

D、连接到远程仓库，并将代码同步到远程仓库

git remote add origin 远程仓库地址

E、git pull origin master  // 把本地仓库的变化连接到远程仓库主分支

F、 git push -u origin master  创建一个 upStream （上传流），并将本地代码通过这个 upStream 推送到 别名为 origin 的仓库中的 master 分支上，

-u ，就是创建 upStream 上传流，如果没有这个上传流就无法将代码推送到 github；同时，这个 upStream 只需要在初次推送代码的时候创建，以后就不用创建了

到此执行完毕，查看分支提交状态确认是否提交完整

G、git status

如果遇到：Updates were rejected because the remote contains work that you do的问题

执行git push -u origin master  前

执行git pull origin master 

如果遇到Updates were rejected because the tip of your current branch is behind即:自己当前版本低于远程仓库版本

执行 git push -u origin master -f
