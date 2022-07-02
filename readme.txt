工作区   	暂存区           本地库                      远程库（git lab  git hub)   
写代码          临时存储        历史版本                  共享开源
可以删           可以删           删不掉，只能删库，删掉某一个版本会使后续版本全消失
                                          局域查看                 所有人都能看
           git add      git commit           push

tab 键可以自动补全代码
隐藏文件.git里面的东西不要动
git 里的命令和Linux通用
添加name email 后在.git 下config文件添加 
[user]
email=your email
name=your name   才可以 commmit

ll -a 可以查看因隐藏的文件

初始化git      git init

查看本地库状态  git status    //（master）这个表示当前分支是master

vim hello.txt  进入某文件 ，没有则创建
esc+:q   退出
esc+:wq  保存并退出
esc 退出insert 模式
yy 复制  p 粘贴 （非insert模式下）

查看文件内容  cat hello.txt
查看文件末尾第一行  tail -n 2  hello.txt   (-n 2代表末尾两行）

添加暂存区  git add 文件
删除暂存区中文件 git rm --cached <file>  工作区还是在的

提交本地库  git commit -m "版本日志信息" 文件名  例如  git commit -m "DNF.0.1.1" DNF.exe
提交后生成版本信息
查看版本信息  git reflog