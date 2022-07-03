工作区   	暂存区           本地库                      远程库（git lab  git hub)   
写代码          临时存储        历史版本                  共享开源
可以删           可以删           删不掉，只能删库，删掉某一个版本会使后续版本全消失
                                          局域查看                 所有人都能看
           git add      git commit           push

git按行维护
tab 键可以自动补全代码
隐藏文件.git里面的东西不要动
git 里的命令和Linux通用
添加name email 后在.git 下config文件添加 
[user]
email=eamil@
name=yepao   才可以 commmit   email 开头不能是数字

ll -a 可以查看因隐藏的文件
ctrl+l 清理屏幕

初始化git      git init

查看本地库状态  git status    //（master）这个表示当前分支是master

vim hello.txt  进入某文件 ，没有则创建
esc+:q   退出
esc+:wq  保存并退出
esc 退出insert 模式
yy 复制  p 粘贴 （非insert模式下）
i 进入 insert 模式
dd删除该行

查看文件内容  cat hello.txt
查看文件末尾第一行  tail -n 2  hello.txt   (-n 2代表末尾两行）

添加暂存区  git add 文件
删除暂存区中文件 git rm --cached <file>  工作区还是在的

提交本地库  git commit -m "版本日志信息" 文件名  例如  git commit -m "DNF.0.1.1" DNF.exe
提交后生成版本信息
查看版本信息  git reflog  git log  后者详细
版本穿梭 git  reset --hard 版本号  例如 git  reset --hard 5770506（是reflog最前面的那些） 会刷新工作区对应文件
git切换版本，底层其实是移动的HEAD指针   head 指向分支  分支（master）指向版本

分支 ：意味着程序员可以把自己的工作从开发主线上分离开，开发自己分支时，不会影响主线分支的运行
（分支底层其实也是指针的引用）
并行开发，并且分支开发失败不会影响其他分支

分支操作 
创建分支 git branch 分支名
查看分支 git branch -v 
切换分支 git checkout 分支名 
把指定的分支合并到当前分支上 git merge 分支名
产生冲突：合并分支时，两个分支在同一文件的同一位置有两套完全不同的修改，git无法替我们决定使用哪一个，必须认为决定新代码内容
解决冲突：merge后手动打开该文件 vim 。。。，会显示修改的部分
把 <<<<<HEAD
========
>>>>>>hot-fix删掉，同时留下想要的部分
然后重新add  commit-m 注意，commit不能带文件名了


查看远程库别名 git remote -v
设置远程库别名 git remote add git-demo git@github.com:YePao-active/git-demo.git 
复制 ctrl+ins
粘贴 shift+ins
代码推送远程库 git push 别名（地址）分支

拉取远程库的代码到本地 git pull 别名（地址）分支

克隆远程仓库到本地 git clone 远程地址
clone 会做三件事
1.拉取代码
2.初始化本地库
3.创建别名
