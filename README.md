# Git-Command

> Git中经常使用的命令


### 基本操作

> `git init`  				*在当前目录创建本地git代码仓库（让git托管）*

> `git add (文件名 例：index.html)`	*提交到代码仓库的暂存区（代码仓库有暂存区和分支区两个区*

> `git add .`        			*添加所有文件到暂存区*

> `git commit -m "注明信息（操作了什么加了什么功能）"`	*提交到分支区*

> `git remote add origin (远程仓库连接)`	*绑定远程仓库*

> `ssh-keygen -t rsa -C "远程仓库账户"`		*之后一直回车*

> `git push origin master`			*提交到远程仓库中master分支*

> *如果推送不成功则运行命令* `git pull --rebase origin master` *下载仓库的东西 再去提交*

---

###  分支管理

> `git branch （name）`			*创建分支*

> `git branch`				*查看分支*

> `git checkout (name)`			*切换分支*

> `git checkout -b （name）`		*创建并且切换到这个分支*

> `git merge （name）`			*合并分支*

> `git merge --no-ff （name）`		 *加上--no-ff 表示禁用Fast forward（删除分支后，保存分支信息）*

> `git branch -d	（name）`		*删除分支*

> `git branch -D 	（name）`		*强行删除未合并的分支*

> `git clone （连接地址）`			*克隆*

> `git reset --hard (commit 前几位id)`	*回退到某个版本*

> `git log`  				*查看历史记录*

> `git log --graph`           		*查看分支合并图*

> `git reflog` 				*查看历史命令*

> `git checkout -- file`        *把文件在工作区的修改撤销（回退到最近一次git commit 或者git add）*

> `git reset HEAD file`             *如果已经提交到暂存区 可以用此命令把暂存区的修改撤销 放回工作区*

> `git rm file`			*删除版本库的文件*

> `git stash`				*保存当前工作 去做其他的事 做完后在继续*

> `git stash list`			*查看保存起来的工作*

> `git stash apply`			*使用此条命令恢复工作 但不会删除*

> `git stash drop`			*删除stash内容*

> `git stash pop`			*恢复的同时把stash内容删除*

> `git stash apply stash@{0}`	*指定恢复哪个stash*

> `git remote`				*查看远程库的信息*

> `git remote -v`			*查看远程库的信息（显示更详细的）*

---