# 简单的 Git 使用


- [简单的 Git 使用](#简单的-git-使用)
  - [初级使用方法](#初级使用方法)
    - [Clone](#clone)
    - [Remote](#remote)
  - [分支操作](#分支操作)
  - [连接远程仓库](#连接远程仓库)
  - [设置 ssh 密钥连接](#设置-ssh-密钥连接)


## 初级使用方法
### Clone
```
1.  git clone URL
2.  git fetch 
3.  git add / commit
4.  git push -u origin main
```
### Remote
```
1.  git remote add origin URL
2.  git fetch
3.  git checkout -b main
4.  git pull origin main
5.  git add / commit
6.  git push -u origin main
```

## 分支操作
```
创建新的分支
$   git branch name

跳转到新的分支
$   git checkout branch-name
```
## 连接远程仓库
```
连接远程仓库
$   git remote add origin URL

第一次提交并且设置远程仓库为分支上游
$   git push -u origin main
```

## 设置 ssh 密钥连接
```
产生公钥
$   ssh-keygen -t rsa -C "your-email"
```


