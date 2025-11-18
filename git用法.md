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
