# Git相关命令
## 配置git
 ```
git config --global user.name 你的英文名
git config --global user.email 你的邮箱
git config --global push.default matching
git config --global core.quotepath false
git config --global core.editor "vim"
```
## 使用Git命令
```
git init，初始化本地仓库 .git
git status -sb，显示当前所有文件的状态
git add 文件路径，用来将变动加到暂存区
git commit -m "信息"，用来正式提交变动，提交至 .git 仓库
git log 查看变更历史
```
>如果有新的变动，我们只需要依次执行 git add xxx 和 git commit -m 'xxx' 两个命令即可。别看本教程废话那么多，其实就这一句有用！先 add 再 commit，行了，你学会 git 了。
## 将本地仓库上传至GitHub
>参照新建仓库GitHub给的命令
## 下载仓库
```
git clone [仓库地址]
```
# 上传更新文件
```
git add 文件路径
git commit -m "信息"
git pull （相信我，你一定会忘记这一个命令）
git push
```
