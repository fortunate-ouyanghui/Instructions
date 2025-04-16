# 使用git命令上传代码到github
## 创建SSH Keys
- 打开终端输入：
```C
ssh-keygen -t rsa -C 3622570635@qq.com(这里填github账号的邮箱)
```
- 找到~/.ssh/id_rsa.pub文件下的密钥，将生成的密钥粘贴到github上。如图所示：
![1](https://github.com/user-attachments/assets/fe53cbc6-4d61-4622-b3f2-ea06af1497d3)
- 设置本地git的用户名和邮箱
```C
git config --global user.name "yourname"
git config --global user.email "email@email.com"
```
- 此时终端输入：
```C
ssh -T git@github.com
```
若显示下图，则表示成功  
![2](https://github.com/user-attachments/assets/c6675be2-71e4-4e36-8b3c-0c563d82b311)
## 上传项目到Github
### 如果是新建项目（没有.git文件）
- 终端输入
```C
echo "# project_name" >> README.md #打印# project_name到READEME.md
git init #git初始化
git add README.md #添加README.md文件
git commit -m "first commit" #提交更改到缓冲区
git branch -M master #创建master分支
git checkout master #切换到master分支
git remote add origin git@github.com:fortunate-ouyanghui/Infantry-Robot.git（这是远程关联github某个项目)
git push -u origin master #上传代码到github
```
### 如果已经是存在的项目（有.git文件）
- 终端输入：
```C
git remote add origin git@github.com:fortunate-ouyanghui/Infantry-Robot.git #远程关联
```
- 若出现报错
```C
fatal: remote origin already exists.
```
- 先查看远程仓库信息，终端输入:
```C
git remote -v
```
- 结果显示
```C
origin  git@github.com:xygxgn/project_name.git (fetch)
origin  git@github.com:xygxgn/project_name.git (push)
```
- 只需删除已关联的远程仓库即可，终端输入
```C
git remote remove origin
```
- 此时再输入：
```C
git remote add origin git@github.com:fortunate-ouyanghui/Infantry-Robot.git #远程关联
git branch -M master
git push -u origin master
```

