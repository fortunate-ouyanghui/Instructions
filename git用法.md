# 上传本地代码至远程仓库
- 添加公私密钥（指定用户才可上传代码至远程仓库）
```C
略
```
- 添加要操作的远程仓库
```C
git remote add origin 远程仓库的SSH(如:git@gitee.com:MA_17/Infantry.git)  #origin是给远程仓库取得别名
git remote                                                               #查看可操作的远程仓库
```
- 上传本地代码至远程仓库
```C
git push -f origin main:master                                           #-f表示强制上传，origin表示要上传的远程仓库，main:master表示将本地main分支的代码上传至远程仓库的master仓库
或者
git pull origin master --allow-unrelated-histories                       #拉取远程 master 分支并合并
git push origin main:master                                              
```
# git 常用命令
## 记录
- git log --all 显示所有分支
- git log --graph 以图的形式显示
- git reset --hard commitID 版本回退
- git reflog 查看记录（含回退和不回退）
- git log 查看记录
## 分支
- git branch 查看本地分支
- git branch 分支名 创建新的分支
- git branch -d 分支 删除分支
- git checkout 分支名 切换到分支
- git checkout -b 分支名 创建分支并切换到该分支
- git merge 分支名1 将该分支1的提交合并到本分支
## 冲突
- 两个人（两个分支）修改了同一个文件中的同一行代码，然后使用git merge 进行融合，产生冲突
- 手动解决
