### 官方网站

地址：[github门户网站](https://github.com/)，账号密码同QQ。

### 远程操作常用命令

|命令|作用|
|:--|:--|
|git remote -v|列出本地仓库配置的远程仓库名称 -并显示url|
|git remote add 远程仓库名称 远程仓库url|本地仓库添加远程仓库配置(指定远程仓库的名称和url)|
|git push 远程仓库名称 本地仓库分支名称：远程仓库分支名称|将本地仓库的分支变更上传到远程仓库并合并|
|git push -d 远程仓库名称 远程仓库分支名称|删除远程仓库指定分支|
|git fetch 远程仓库名称 远程分支名称|获取远程仓库分支变更到本地仓库不合并|
|git pull 远程仓库名称 远程仓库分支名称:本地仓库分支名称|获取远程仓库的分支变更到本地仓库并合并|

`git pull` 等价于 `git fetch` + `git merge FETCH_HEAD` 两个步骤的结合。