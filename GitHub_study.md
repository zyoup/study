```
这是我的GitHub管理工具的学习笔记
```
---------------------------------------
# Git简介
---------------------------------------
## Git与SVN对比
>	SVN是集中式版本控制系统，版本库是集中放在中央服务器的，
> 而工作的时候我们所使用的都是自己的电脑，所以首先要从中央服务器
> 那里得到最新的版本，然后才能开始工作，工作完成后，还需要把自己
> 工作的内容及时推送到中央服务器。集中式版本控制系统必须联网才可
> 以正常工作，在局域网或互联网下都可以。
> 	集中管理方式在一定程度上可以相互看到其他开发人员开发的哪些内容，
> 而且管理员也可以轻松的掌握每一个攻城狮的开发权限。
> 	但是相较于其优点而言，集中式版本控制工具缺点很明显：
>	* 服务器单点故障（一旦服务器宕机或损坏，历史数据就会全部丢失）
>	* 容错性差

> 	Git是分布式版本控制系统，它是没有中央服务器的，每一个人的电脑
> 都是一个完整的版本库，这样，攻城狮在工作的时候就可以无需联网，因为项目
> 的版本都在攻城狮的电脑上。
> 	>如何多人协作：假如自己在电脑上修改了文件A，其他人也在电脑上修改
> 	>了文件A，此时，我们两人之间只需要把我们各自修改的推送给对方就可以
> 	>相互看到对方的修改了。
---------------------------------------
## 版本控制工具应该具备的功能
1.协同修改<br/>
&nbsp;&nbsp;&nbsp;&nbsp;多人并行不相悖的修改服务器的同一个文件。<br/>
2.数据备份<br/>
&nbsp;&nbsp;&nbsp;&nbsp;不仅保存目录和文件的当前状态，还能够保存每一个提交过的历史状态。<br/>
3.版本管理<br/>
&nbsp;&nbsp;&nbsp;&nbsp;在保存每一个版本的文件信息的时候要做到不保存重复数据，以节约存储空间，
提高运行效率。在这方面SVN采用的是增量式管理的方法，而Git采取的则是文件系统快照
的方式。<br/>
4.权限控制<br/>
&nbsp;&nbsp;&nbsp;&nbsp;1）对团队中参与开发的人员进行权限的控制。<br/>
&nbsp;&nbsp;&nbsp;&nbsp;2）对团队外的开发者贡献的代码进行审核——Git独有的。<br/>
5.历史记录<br/>
&nbsp;&nbsp;&nbsp;&nbsp;1）查看修改人、修改时间、修改内容、日志信息。<br/>
&nbsp;&nbsp;&nbsp;&nbsp;2）可将本地文件恢复到某一个历史状态。<br/>
6.分支管理<br/>
&nbsp;&nbsp;&nbsp;&nbsp;允许开发团队在工作过程中多条生产线同时推进任务，经一部提高效率。<br/>
---------------------------------------
## 版本控制简介
1.版本控制<br/>
&ensp;工程设计领域中使用版本控制管理工程蓝图的设计过程。在IT开发过程中也可以使用版本<br/>
&ensp;控制思想管理代码的版本迭代。<br/>
2.版本控制工具<br/>
&ensp;集中式版本控制工具：<br/>
&emsp;CVS、SVN、VSS……<br/>
&ensp;分布式版本控制工具：<br/>
&emsp;Git、Mercurial、Bazzar、Darcs……<br/>
---------------------------------------
## Git的优势
* 大部分操作可在本地完成，不需要联网
* 完整性保证（Hash）
* 尽可能的去添加数据而不是删除或者修改数据
* 分支操作非常快捷流畅
* 与Linux命令全面兼容
---------------------------------------
## Git结构
```
工作区（写代码）=>git add=>暂存区（临时存储）=>git commit=>本地库（历史版本）
```
---------------------------------------
## Git和代码托管中心
***代码托管中心的任务：维护远程库***
* 局域网环境下
> GitLab服务器
*外网环境下
> GitHub
> 码云
---------------------------------------
## 本地库和远程库
* 团队内部协作
![团队内部协作](https://github.com/zyoup/image/blob/master/git_all/git简介/本地库和远程库/团队内部协作.jpg "团队内部协作")
* 跨团队协作
![跨团队协作](https://github.com/zyoup/image/blob/master/git_all/git简介/本地库和远程库/跨团队协作.jpg "跨团队协作")
---------------------------------------
## git安装
1.![步骤1](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/1.jpg "步骤1")
2.![步骤2](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/2.jpg "步骤2")
3.![步骤3](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/3.jpg "步骤3")
4.![步骤4 安装目录的名字](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/4安装目录的名字.jpg "步骤4 安装目录的名字")
5.![步骤5](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/5.jpg "步骤5")
6.![步骤6](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/6.jpg "步骤6")
7.![步骤7](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/7.jpg "步骤7")
8.![步骤8](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/8.jpg "步骤8")
9.![步骤9](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/9.jpg "步骤9")
10.![步骤10](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/10.jpg "步骤10")
11.![步骤11](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/11.jpg "步骤11")
12.![步骤12](https://github.com/zyoup/image/blob/master/git_all/git简介/安装/12.jpg "步骤12")
---------------------------------------
# git命令
---------------------------------------
## 本地库初始化
```
* 命令：git init
* 注意：.git目录中存放的是本地库相关的子母录和相关的文件，不要删除，也不要胡乱修改。
```
---------------------------------------
## 设置签名
```
* 形式：
	用户名：zyp
	Email 地址：zyoup2@163.com
* 作用：区分不同开发人员的身份 
* 辨析：这里设置的签名和登录远程库（代码托管中心）的账号、密码没有任何关系。
* 命令：
	❈项目级别/仓库级别：仅在当前本地库范围内有效
		git config user.name zyp
		git config user.email zyoup1@163.com
		◆信息保存位置：./.git/config （隐藏文件）
	❈系统用户级别：登录当前操作系统的用户范围
		git config --global user.name zyp
		git config --global user.email zyoup1@163.com
		◆信息保存位置：~/.gitconfig （隐藏文件）
	❈优先级：
		◆就近原则：项目级别优先于系统用户级别，二者都有时采用项目级别
			的签名
		◆如果只有系统用户级别的签名，则以系统用户级别的签名为准
		◆二者都没有不允许 
```
---------------------------------------
## 基本操作
> 1.状态查看操作
```
git status
◆ 查看工作区、暂存区状态
```
> 2.添加操作 
```
git add [file name]
◆ 将工作区的“新建/修改”添加到暂存区
```
> 3.提交操作
```
git commit -m “commit message”[file name]
◆ 将暂存区的内容提交到本地库
```
> 4.查看历史记录
```
git log
◆ 显示详细信息
◆ 多屏显示控制方式：
	空格 向下翻页
	b 向上翻页
	q 退出
```
![git log](https://github.com/zyoup/image/blob/master/git_all/git命令/git_log.jpg "git log")
```
git log --pretty=oneline
```
![git log --pretty=oneline](https://github.com/zyoup/image/blob/master/git_all/git命令/git_long_pretty_oneline.jpg "git log --pretty=oneline")
```
git log --oneline
◆ 精简版
```
![git log --oneline](https://github.com/zyoup/image/blob/master/git_all/git命令/git_log_oneline.jpg "git log --oneline")
```
git reflog
◆ HEAD@{移动到当前版本需要多少步}
```
![git reflog](https://github.com/zyoup/image/blob/master/git_all/git命令/git_reflog.jpg "git reflog")
> 5.前进后退
```
❈ 本质
```
![本质](https://github.com/zyoup/image/blob/master/git_all/git命令/前进or后退_本质.jpg "本质")
```
❈ 基于索引值操作[推荐]
	git reset --hard [局部索引值]
	◆ eg: git reset --hard a6ace91
❈ 使用^符号：只能后退
	git reset --hard HEAD^
	◆注：一个^表示后退一步，n个表示后退n步
❈ 使用~符号：只能回退
	git reset --hard HEAD~n
	◆注：表示后退n步
```
>>reset命令的三个参数对比
```
❈ --soft 参数 （不常用）
◆ 仅仅在本地库移动HEAD指针
```
![soft](https://github.com/zyoup/image/blob/master/git_all/git命令/soft.jpg "soft")
```
❈ --mixed 参数（不常用）
◆ 在本地库移动HEAD指针
◆ 重置暂存区
```
![mixed](https://github.com/zyoup/image/blob/master/git_all/git命令/mixed.jpg "mixed")
```
❈ --hard 参数（常用）
◆ 在本地库移动HEAD指针
◆ 重置缓存区
◆ 重置工作区
```
![hard](https://github.com/zyoup/image/blob/master/git_all/git命令/hard.jpg "hard")
