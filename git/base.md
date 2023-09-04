### git 工作机制

#### 基本流程

![[Pasted image 20230902211124.png]]
**说明：**
- workspace：工作区
- staging area：暂存区
- local repository：本地仓库
- remote repository：远程仓库
#### .git文件夹

- config：本地仓库的配置信息
- refs/remotes：远程仓库各分支，head文件始终指向默认远程分支
- refs/heads：本地仓库各分支
- HEAD：当前分支最新的commitID
- FETCH_HEAD：各分支在远程仓库最新的commitID

### git基本操作

|命令|作用|
|:--|:--|
|git -v -h|-查看git版本 -显示最常用的命令|
|git config --user.name(user.email)|查看用户名称(邮箱)|
|git init|本地创建一个新的 Git 仓库或者重新初始化一个已有的git仓库|
|git clone url|远程git仓库拷贝到本地仓库|
|git add pathspec|添加工作区文件到暂存区|
|git restore --staged pathspec|移除暂存区文件到工作区，不撤销文件修改内容|
|git restore pathspec|撤销工作区文件修改内容|
|git mv 源文件 目标文件|移动或重命名工作区指定文件|
|git rm pathspec|删除工作区和暂存区文件|
|git commit -m -a|提交暂存区文件到本地仓库 -备注信息 -git追踪的文件可省略add命令|
|git reset --soft --hard head(版本号) \[pathspec\]|回退至指定版本(所有版本外的更改保存在工作区) --所有版本外的更改保存在暂存区 --所有版本外的更改会丢失|
|git status|查看本地仓库的状态，显示修改的文件|
|git log|查看本地仓库所有历史提交记录|
|git reflog|查看本地仓库所有操作记录|
|git diff \[path...\]|查看工作区和暂存区文件的差异|
|git diff head(版本号) \[path...\]|查看工作区和本地仓库文件的差异|
|git diff 版本号1 版本号2 \[path...\]|查看本地仓库不同版本文件的差异|

### git分支

|命令|作用|
|:--|:--|
|git branch -r -a|查看所有本地分支 -查看所有远程分支 -查看所有分支|
|git branch -d branchname|删除本地分支|
|git branch branchname|创建本地分支|
|git remote prune 远程仓库名称|清理掉远程仓库已删除但本地仓库残留的分支|
|git checkout branchname|切换至指定分支，查找顺序：本地仓库——>远程仓库(本地创建并与远程关联)|
|git stash|隐藏工作区和暂存区的更改，这样通过checkout切换分支时不会将更改内容带过去|
|git stash pop|取出隐藏的更改|
|git merge branchname|合并指定分支到当前分支|
|git merge commitID|合并指定ID到当前分支|


