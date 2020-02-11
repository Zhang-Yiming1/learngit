开课吧人工智能学院开设了【**python入门人工智能**】。第一期课程进入了【**工程能力提升**】部分，第一次课关于Git，课上知识点丰富，总结一下。
Git 是分布式开发、文件版本控制系统。GitHub是基于Git的协作平台。那我们就进入实践：
### Git安装配置
[根据电脑的系统，下载对应的Git.](https://git-scm.com/downloads)
#### Git配置
配置用户名：   
```shell  
git config --global user.name “xxx”  
```  
配置邮箱：  
```shell  
git config --global user.email “xxx"  
```  
配置大小写敏感：  
```shell   
git config --global core.ignorecase false  
```  
查看配置信息：   
```shell  
git config --list  
```  
### Git原理  

 - Remote：远程仓库，托管代码的服务器，可以理解为GitHub。      
- Repository：仓库区（版本库），就是本地仓库，安全存放数据的位置。      
- Index/Stage：暂存区，用于临时存放你的改动，事实上，它只是一个文件。    
- Workspace：工作区，自己的桌面。

实践过程：

 - [ ] 在工作区，自己电脑上建立文件。
 - [ ] 建立 **learn-git**的文件夹，```cd learn-git```进入文件夹内；
 - [ ] 建立 **test.txt** 文件 ```vim test.txt```；
 - [ ] 写入**hello kaikeba**，用 ```cat test.txt ```查看； 
 - [ ] 建立仓库区，就是本地仓库. ```git init```；
 - [ ] 添加文件到 暂存区 ```git add test.txt```；
 - [ ] 将文件提交到本地仓库 ```git commit -m ```“新增**test.txt**文件”；
### Git常见命令
讲师直接总结出来了两张图，我根据自己的使用频率做了筛选～

- 添加文件: ```git add```
- 添加文件到本地仓库: ```git commit ```
- 显示工作目录和暂存区的状态: ```git status ```
- 将本地修改的文件推送到远程: ```git push ```
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200210120708109.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTA3NTE5NzQ=,size_16,color_FFFFFF,t_70)

### 远程仓库

 - [ ] 注册GitHub账号
 - [ ] 设置SSH Keys ```ssh-keygen -t rsa -C "youremail@exaple.com"  ```
 - [ ] 在github settings页面设置SSH Keys
 - [ ] 在GitHub上建立new repositories，名为learngit的新版本库
 - [ ] 根据GitHub的提示，选择SSH的链接。在本地仓库运行命令：```git remote add origin```
 - [ ] 关联后，使用命令```git push -u origin master```推送文件给远程仓库
 - [ ] 此后，每次本地提交后，只要有必要，就可以使用命令```git push origin master```推送最新修改。
 
### 团队协作中的分支管理与标签管理
#### 分支管理
创建dev分支：  
```shell  
git checkout –b dev /git switch -c dev 
```   
查看分支：   
```shell  
git branch  
```   
分支内容提交：    
```shell  
git commit –a –m “update file“  
```   
切换至master分支：  
```shell  
git checkout master/git switch master  
```  
合并分支：  
```shell  
git merge dev  
```  
删除dev分支：  
```shell  
git branch –d dev  
```  
#### 标签管理  
创建标签：  
```shell  
git tag v1.0  
```   
查看标签：  
```shell  
git tag  
```  
创建带有描述信息的标签：    
```shell  
git tag -a v0.1 -m "version 0.1 released" 1094adb  
```  
用命令可以看到说明文字  
```shell  
git show <tagname>  
```  
如果打错了，可以删除：  
```shell  
git tag –d v0.1  
```   
还可以将标签推到远程仓库：  
```shell  
git push origin v1.0  
```  
删除远程标签需要先删除本地标签：  
```shell  
git tag -d v0.9/git push origin :refs/tags/v0.9  
```  

讲师上课非常强调动手，带着我们反复实践代码，不厌其烦的解释课上知识点。课间休息是学生休息，讲师继续答疑。课间休息之后，还喊着大家赶紧回来。怎么有这么可爱、负责、质朴的讲师。哈哈哈～      
最后讲师布置了一个作业：利用GitHub搭建自己的博客。我要去写作业了，拜拜！