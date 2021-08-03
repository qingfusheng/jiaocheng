# Ubuntu20.10配置git环境

标签（空格分隔）： git 环境配置 Ubuntu

---
Git是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。也是Linus Torvalds为了帮助管理Linux内核开发而开发的一个开放源码的版本控制软件。

## 1. 更换软件源

## 2. 安装git
```shell
sudo apt-get install -y git
```
## 3. 配置git
- 配置用户名和邮箱
```shell
git config --global user.name "{username}"  //username为github注册用户名
git config --global user.email "{email}"    //email为github注册绑定邮箱
```
- 查看git配置
```shell
git config --list  //查看git配置
```
- 配置SSH
```shell
ssh-keygen -t rsa -C "{email}"
```
- 查看生成秘钥
```shell
cat ~/.ssh/id_rsa.pub
```
- Github官网配置SSH

    进入Github主页并转到Settings页面，进入后点击SSH and GPG Keys进入子界面并添加新的SSH Key

![file-list](https://raw.githubusercontent.com/qingfusheng/material/master/image/3.png)

![file-list](https://raw.githubusercontent.com/qingfusheng/material/master/image/2.png)
## 4. git的使用
### 1. git常用命令
```git
git remote add origin git@github.com:yeszao/dofiler.git # 配置远程git版本库
git pull origin master # 下载代码及快速合并
git push origin master # 上传代码及快速合并
git fetch origin # 从远程库获取代码

git branch # 显示所有分支
git checkout master # 切换到master分支
git checkout -b dev # 创建并切换到dev分支
git commit -m "first version" # 提交

git status # 查看状态
git log # 查看提交历史

git config --global core.editor vim # 设置默认编辑器为vim（git默认用nano）
git config core.ignorecase false # 设置大小写敏感
git config --global user.name "YOUR NAME" # 设置用户名
git config --global user.email "YOUR EMAIL ADDRESS" # 设置邮箱

git add <文件路径>  # 把指定的文件添加到暂存区中
git commit -m "<提交的描述信息>"  # 把暂存区中的文件提交到本地仓库，调用文本编辑器输入该次提交的描述信息
git pull origin master  # 从远程仓库获取最新版本。
git pull origin master  # 把本地仓库的分支推送到远程仓库的指定分支

```
