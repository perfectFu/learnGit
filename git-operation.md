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
  
10、
```

