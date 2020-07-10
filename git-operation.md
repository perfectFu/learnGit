```js
1、初始化仓库
	git init
  
2、添加文件到仓库
	git add <file>，可以反复使用，添加多个文件
	git commit -m <message> 完成提交

3、版本回退
	git reset --hard commit_id 回退到指定版本
  git reset --hard HEAD^ 回退到上一个版本，HEAD指向的是当前版本

4、穿梭前 用git log查看历史版本，已确定要回退到哪个版本
	 要重返未来，用git reflog 查看命令历史，以便确定回到未来的哪个版本
   
5、工作区、暂存区的概念
	git add 将工作的修改保存到 暂存区，git commit 提交暂存区的修改
  
6、撤销修改
	撤销工作区修改：git checkout -- file
  撤销暂存区修改：分两步：1、git reset HEAD <file>  2、git checkout -- file
  如果已经提交，需要撤回提交，参考版本回退操作
 
7、删除文件
	git rm file 从版本库中删除该文件
  删错了，可以使用git checkout -- file 恢复
  
8、添加远程仓库
	关联远程仓库：git remote add origin https://github.com/perfectFu/learngit.git
  推送master分支所有内容到仓库：git push -u origin master
  此后本地修改需要提交可以直接使用 git push origin master

9、克隆仓库
	git clone repo  Git支持多种协议，包括https，ssh最快
  
10、创建合并分支
	git branch 合并分支
  git branch <name> 创建分支
  git checkout <name> 或 git switch <name> 切换分支
  git checkout -b <name> 或 git switch -c <name> 创建并切换分支
  git merge <name> 合并某分支到当前分支
  git branch -d <name> 删除分支
 
11、解决冲突
    当发生合并冲突时，需要我们手动解决冲突。解决冲突完成后，在提交，合并完成
    git log --graph 查看分支合并图

12、bug分支
    git stash 保存当前未完成的工作现场
    git stash pop 回到工作现场
    git cherry-pick <commit> 将commit提交的修改复制到 当前分支，避免重复劳动
   
13、feature分支
    开发新的功能，最好新建一个分支
    如果要丢弃一个没有被合并过的分支，可以通过git branch -D <name>强行删除
    
14、多人协作流程
    查看远程库信息，使用git remote -v；
    本地新建的分支如果不推送到远程，对其他人就是不可见的；
    从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；
    在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；
    建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；
    从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。
    
15、rebase
   
16、标签
    git tag <tagname>用于新建一个标签，默认为HEAD，也可以指定一个commit id；
		git tag -a <tagname> -m "blablabla..."可以指定标签信息；
		git tag可以查看所有标签
    git push origin <tagname>可以推送一个本地标签；
		git push origin --tags可以推送全部未推送过的本地标签；
		git tag -d <tagname>可以删除一个本地标签；
		git push origin :refs/tags/<tagname>可以删除一个远程标签
    
    
    
    
```

