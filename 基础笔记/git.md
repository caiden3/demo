#  git

**配置自己的账号和邮箱(适用于全局)**

~~~
configuration--global user.name '你的名字'
git config --global user.email '你的邮箱'
配置完存放在  .gitconfig 文件内

git config   配置
~~~

**设置要忽略的文件**

**生成密钥**

~~~
ssh-keygen   生成一对密钥   id_rsa 私钥   id_rsa.pub 公钥
放在 ~/.ssh 文件夹内   
~~~

**常用git命令**

~~~
1、 git init          初始化一个仓库   生成一个 .git 文件

2、 git status        查看当前状态

3、 git add ./文件名   将文件添加到‘暂存区’，添加一个追踪状态

4、 git reset 文件名     将‘暂存区’的文件取消暂存状态  

5、 git commit -m '注释'  将文件提交到本地仓库

6、 git push origin master  将代码推送到远端  

7、 git pull origin master   将代码从远端拉取到本地

~~~

**克隆**

~~~
1.克隆仓库
     git clone 网址 
     eg ： git clone  git@github.com:caiden3/demo.git
2.克隆分支
	 git clone 网址 "指定目录"        clone到指定目录
	 git clone -b branchname 网址    clone时创建新的分支替代默认的 origin  master 分支
~~~

**查看远程库**

~~~
1、 git remote add 仓库名 网址      添加远程仓库
2、 git remote remove 远端名       删除本地指定的远程地址(远程库)

3、 git remote          查看远程库的信息
4、 git remote –v       查看本地添加了哪些远程地址          
~~~

**撤销修改(慎用)**

~~~
1、 git checkout 文件名      恢复某个已修改的文件（撤销未提交的修改）
2、 git revert HEAD         还原最近一次提交的修改(撤销前一次的commit)
3、 git revert HEAD^        撤销前前一次的commit
4、 git revert commit-id    还原指定版本的修改
~~~

**版本回退(慎用)**

~~~
1、 git reset –hard HEAD^        回退到上一个版本(把你工作目录中所有未提交的内容清空)
2、 git reset --hard HEAD~第几个  如果想回退到第3个版本，使用git reset –hard HEAD~3
3、 git reset --hard 057d        回退到某一个具体的版本号

4、 git reset 文件名     将‘暂存区’的文件取消暂存状态  
HEAD 代表版本库
~~~

**查看命令**

~~~
1 git status        	查看仓库状态

2 git diff  文件名       查看文件修改了那些内容  

3 git diff              查看所有文件修改了那些内容

4 git log           	查看历史记录

5 git reflog        	查看历史记录的版本号id（记录你的每一次命令,不论是否提交）

6 git log --pretty=oneline  如果信息量太多可以进行比较好的列表显示 

7 git log --graph       查看树状结构
~~~

**分支**

~~~
1 git branch         查看本地分支
2 git branch -a      查看远程分支

3 git branch  分支名                创建本地分支
4 git branch –d 分支名              删除本地分支
5 git push origin --delete 分支名   删除远程的分支
6 git branch -m 分支名  develop     重命名分支

7 git checkout 分支名 				切换分支
8 git checkout -b 分支名           创建分支并切换到新分支

9 	git merge 分支名                 合并分支
10  git push origin 分支名         把当前的分支推送到远程库(远程仓库没有给分支则会新建立该分支)
11	
~~~

**隐藏文件**

~~~
1 git stash       把当前的工作隐藏起来 等以后恢复现场后继续工作
2 git stash list  查看所有被隐藏的文件列表
3 git stash apply 恢复被隐藏的文件，但是内容不删除
4 git stash drop  删除文件
5 git stash pop   恢复文件的同时 也删除文件
~~~

**git 设置大小写敏感**

~~~
Windows上的Git默认是大小写不敏感的，这样多平台写作就可能会出现问题。Win上的Git设置为大小写敏感的命令如下
		 git config core.ignorecase false 
~~~

**git 设置忽略文件或文件夹权限修改**

~~~
 git config core.filemode false
~~~

**切换git 命令提示中文到英文**

~~~
ubuntu装的git会出现全中文的提示,切换到英文了,切换方法如下:
1:写入
echo "alias git='LANG=en_GB git'" >> ~/.bashrc

2:生效
source ~/.bashrc
~~~



~~~
which django-admin
source .venv/bin/activate
~~~

