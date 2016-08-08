#git学习笔记

Git是一种版本控制系统，Github是一个网站，给用户提供git服务。

###1. Git安装设定
下载：windows.gitHub.com
设定：
	git --version  #确定是否成功安装Git
	git config --global user.name "<Your Name>"  #设定名字
	git config --global user.email "<Youremail@example.com>"  #设定邮箱
	git config --global user.username <Your github Name>  #你的GitHub账号名

###2. 在自己的电脑上建立一个程序库（repository）
一个repository就是一个项目，可以想象成是包含所有相关文档的文件夹.

	mkdir test  #新建文件夹，为了方便，建议命名为项目名称
	cd test  #进入文件夹
	git init  #把这个文件夹设定成一个git项目
	git status  #确定项目是否已经是个git repository

###3. 在项目中创建一个新文件
假设已创建好一个test.txt文件，终端进入test项目里。

	git status  #查看是否有所改变
	git add test.txt  #新增想提交的文件
	git commit -m "<Your commit message>"  #提交到repository，并附加一个简短的说明

###4. 将项目传到GitHub，将存储在GitHub的主机上，这个项目就成了远端程序库（remote repository）
首先到github.com新建一个repository（名称最好和电脑上的程序名一样）.
开源项目中经常遇到的文档：

	readme  #通常用来解释程序的功能、使用方法以及如何贡献（有时会用CONTRIBUTING.md来说明）
	.gitignore  #要忽略的档案清单，告诉Git在做版本控制记录时不要理会这些档案
	License  #著作声明
	git remote add <remote name>  #新增remote连接
	git remote set-url <remote name>  #给一个remote设定位址（Window）
	git remote add origin <URL from GitHub>  #把电脑上的repository 和remote  repository连接在一起，在远端的那份就称为origin
	git remote -v  #查看有哪些remote
	git push origin master  #把master分支的程序传到origin远端

网址：http://jlord.us/git-it/index.html

###5. Forks And Clones
Forks（副本），项目合作。
到项目所在github.com位置，点击"fork"按钮，然后你的账号中就出现了一份项目副本，复制项目链接终端切换到工作区间。

	git clone <URL from GitHib>  #下载（Clone）项目。不需要事先建立项目名称
	git remote add upstream <Origin URL>  #给原始的repository命名为upstream，在原始项目变更时pull

###6. branch
branch用来隔离进度.

	git branch <branch name>  #新建一个分支。Git会把目前branch上所有的文件拷贝到新branch上
	git checkout <branch name>  #进入branch

###7. Collaborators 新增项目编辑权限试用装
到repository的GitHub页面，点击右边的"Settings"，选择"Collaborators"分页，输入账号添加。

###8. Pull requests
将你所修改的fork文档发给原本的作者，希望作者收取。在repository的GitHub页面，点击右边的"Pull request"，按步骤进行即可。
当pull request 成功后，可以吧fork和原始的repository同步。

git checkout gh-pages  #把自己的分支merge进主要的branch（gh-pages）。
注意首先要进入想要merge的分支.

	git merge <branch name>  #merge你的分支进来
	git branch -d <branch name>  #把已经merged的branch删除
	git push <remote name> --delete <branch name>  #把branch从GitHub上的fork repository中删除
	git pull upstream gh-pages  #从原项目收取回来

###常见问题
当本地仓库没有与远程仓库同步时，也就是远程仓库中有的文件，在本地没有。比如刚新建的一个仓库默认生成README文件，而在本地没有，这是无法push的。需要先pull从远程获取最新版本并merge到本地，然后才执行push。


