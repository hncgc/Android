Git教程
-------

[http://www.yiibai.com/git](http://www.yiibai.com/git)  

[Android快速实现上传项目到Github（原来Android Studio的git已经这么好用了）](http://www.jianshu.com/p/aa341d691658)  
游戏头条 https://github.com/MarnoDev/GameNews  

[在Android Studio 中使用Git 教程](http://www.apkbus.com/blog-866962-75821.html)  

[企业级开发：Gitflow Workflow工作流](http://www.jianshu.com/p/104fa8b15d1e)  

[基于git的源代码管理模型——git flow](http://www.ituring.com.cn/article/56870)  
软件开发模型有常见的瀑布模型、迭代开发模型、以及最近出现的敏捷开发模型

[Git版本控制与工作流](http://www.techug.com/post/git-2.html)  

[GitHub 查看地址](https://github.com/HLQ-Struggle/AndroidImmersion)  

[Git Book](https://git-scm.com/book/zh/v1)  

[6. Git 基础 - 打标签](https://git-scm.com/book/zh/v1/Git-%E5%9F%BA%E7%A1%80-%E6%89%93%E6%A0%87%E7%AD%BE#列显已有的标签)  


#### git 操作：

```
强制push：  

    git push -u origin master -f

强制pull  

    git fetch --all  
    git reset --hard origin/master 
    git pull
    
显示最后一次提交:

    git show 
    
查看提交历史（oneline 将 每个提交 放在一行显示）

    git log --pretty=oneline

分享(推送)标签:

    git push origin 标签名

后期加注标签
你甚至可以在后期对早先的某次提交加注标签。比如在下面展示的提交历史中：  
$ git tag -a v1.2 9fceb02  

分享标签
默认情况下，git push 并不会把标签传送到远端服务器上，只有通过显式命令才能分享标签到远端仓库。其命令格式如同推送分支，运行 git push origin [tagname] 即可： 

$ git push origin 标签名  

如果要一次推送所有本地新增的标签上去，可以使用 --tags 选项：  

$ git push origin --tags  

#### 如何使用git获取指定tag的代码

tag是对历史一个提交id的引用，如果理解这句话就明白了
使用git checkout tag即可切换到指定tag，例如：git checkout v0.1.0
切换到tag历史记录会处在分离头指针状态，这个是的修改是很危险的，在切换回主线时如果没有合并，之前的修改提交基本都会丢失，如果需要修改可以尝试git checkout -b branch tag创建一个基于指定tag的分支，例如：git checkout -b tset v0.1.0  这个时候就会在分支上进行开发，之后可以切换到主线合并
```
Git资料汇总
---
[Git资料汇总](https://github.com/ruijun/Android-Dev-Favorites/blob/master/Git/Git.md)  

- [怎么快速开始使用Git](http://sixrevisions.com/web-development/easy-git-tutorial/)  

- [廖雪峰Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)  

- [试试Git – 15分钟的Git交互教程](https://try.github.io/levels/1/challenges/1)  

- [提示和技巧（Ry的Git教学）是常见Git功能的实践教程](http://rypress.com/tutorials/git/tips-and-tricks)  

- [Git简单指南](http://rogerdudler.github.io/git-guide/)  

- [Git Ready是一个收藏有许多简单而简短的Git提示的网站](http://gitready.com/)  

- [git-cheat-sheet](http://www.git-tower.com/blog/git-cheat-sheet/)  

- [Git Tower学习区是一个在我的网站上的Git学习资源列表](http://www.git-tower.com/learn/)  

- [Git官方教程](http://git-scm.com/docs/gittutorial)  

- [Training: Git Basics (视频)是YouTube上的一个视频列表](https://www.youtube.com/playlist?list=PLg7s6cbtAD165JTRsXh8ofwRw0PqUnkVH)  

- [Pro Git一本让你深入了解Git的在线书籍](http://git-scm.com/book/en/v2)  

- [GitHub秘籍](http://snowdream86.gitbooks.io/github-cheat-sheet/content/zh/)  

- [GotGitHub](http://www.worldhello.net/gotgithub/index.html)  

- [写出好的 commit message](https://ruby-china.org/topics/15737)  

- [Git Community Book 中文版](http://gitbook.liuhui998.com/index.html)  

- [git使用笔记](http://jslite.io/2015/04/01/git%E4%BD%BF%E7%94%A8%E7%AC%94%E8%AE%B0/)  

- [使用git和github进行协同开发流程](http://livoras.com/post/28)  

- [Git 速查表](http://itmyhome.com/git-sheet/)  

- [xirong/my-git-个人学习git的资料整理](https://github.com/xirong/my-git/)  

- [Git 常用命令](http://liujin.me/blog/2015/05/25/Git-%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4/)  

- [使用git和github进行协同开发流程](http://livoras.com/post/28)  

- [稀土Git资料](http://gold.xitu.io/tag/Git)  








