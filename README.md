# **Git-Command**

> Git中经常使用的命令


## **基本操作**

> ***在当前目录创建本地git代码仓库（让git托管）***

> `git init` 

> ***提交到代码仓库的暂存区（代码仓库有暂存区和分支区两个区***

> `git add (文件名 例：index.html)`	

> ***添加所有文件到暂存区***

> `git add .`        			

> ***提交到分支区***

> `git commit -m "注明信息（操作了什么加了什么功能）"`	

> ***绑定远程仓库***

> `git remote add origin (远程仓库连接)`	

> `ssh-keygen -t rsa -C "远程仓库账户"`		

> ***提交到远程仓库中master分支***

> `git push origin master`			

> *如果推送不成功则运行命令* `git pull --rebase origin master` *下载仓库的东西 再去提交*

---

##  **分支管理**

> ***创建分支***

> `git branch （name）`	

> ***查看分支***

> `git branch`				

> ***切换分支***

> `git checkout (name)`			

> ***创建并且切换到这个分支***

> `git checkout -b （name）`		

> ***合并分支***

> `git merge （name）`			

> ***加上--no-ff 表示禁用Fast forward（删除分支后，保存分支信息）***

> `git merge --no-ff （name）`		 

> ***删除分支***

> `git branch -d	（name）`		

> ***强行删除未合并的分支***

> `git branch -D 	（name）`		

> ***克隆***

> `git clone （连接地址）`			

> ***回退到某个版本***

> `git reset --hard (commit 前几位id)`	

> ***查看历史记录***

> `git log`  				

> ***查看分支合并图***

> `git log --graph`           		

> ***查看历史命令***

> `git reflog` 				

> ***把文件在工作区的修改撤销（回退到最近一次git commit 或者git add）***

> `git checkout -- file`        

> ***如果已经提交到暂存区 可以用此命令把暂存区的修改撤销 放回工作区***

> `git reset HEAD file`             

> ***删除版本库的文件***

> `git rm file`			

> ***保存当前工作 去做其他的事 做完后在继续***

> `git stash`				

> ***查看保存起来的工作***

> `git stash list`			

> ***使用此条命令恢复工作 但不会删除***

> `git stash apply`			

> ***删除stash内容***

> `git stash drop`			

> ***恢复的同时把stash内容删除***

> `git stash pop`			

> ***指定恢复哪个stash***

> `git stash apply stash@{0}`	

> ***查看远程库的信息***

> `git remote`				

> ***查看远程库的信息（显示更详细的）***

> `git remote -v`			

---

## **标签操作**

> ***新建标签***

> `git tag （tagName）`

> ***查看所有标签***

> `git tag`

> ***对某个commit 打上标签***

> `git tag （tagName） （commitID）`

> ***查看标签信息***

> `git show （tagName）`

> ***创建带有说明的标签***

> `git tag -a （tagName） -m （说明文字） （commitID）`

> ***删除标签***

> `git tag -d （tagName）`
 

> ***推送标签到远程***

> `git push origin （tagName）`
 

> ***一次性推送全部尚未推送到远程的本地标签***

> `git push origin --tags`
 

> ***如果标签已经推送到远程 要删除的话如下：***

>> ***先删除本地的***

>> `git tag -d （tagName）`
 
>> ***在远程删除***

>> `git push origin :refs/tags/（tagName）`
 
---


> 如果你同事的最新提交和你试图推送的起冲突 先用`git pull`把最新的提交从origin/dev（dev代表你要提交的分支）下载下来 在本地合并，解决冲突，再推送

> 如再次失败 原因是没有指定本地dev分支与远程origin/dev分支的链接，

> 根据提示，设置dev和origin/dev的链接 `git branch --set-upstream dev origin/dev` 再pull

## **写在最后**

git简单命令备忘录在此了，`\(^o^)/`