
# git常用命令操作整理
## 一、基本操作
### git init ——初始化仓库
### git status ——查看仓库的状态
### git add ——向暂存区中添加文件
### git commit ——保存仓库的历史记录
- git commit -m "提交信息概述"，  -m参数后是提交的简单描述
- git commit ，直接执行git commit 可以详细记述提交的信息
### git log ——查看提交日志
- git log --pretty=short ，在 git log命令后加上 --pretty=short，让程序显示第一行简述信息
- git log 目录或文件，在 git log命令后加上目录名，便会只显示该目录下的日志。如果加的是文件名，就会只显示与该文件相关的日志。
- git log -p 目录或文件，查看提交所带来的改动，可以加上 - p参数，文件的前后差别就会显示在提交信息之后。
### git diff ——查看更改前后的差别
git diff命令可以查看工作树、暂存区、最新提交之间的差别。
- git diff HEAD 命令,查看工作树和最新提交的差别

## 二、分支的操作
通过灵活运用分支，可以让多人同时高效地进行并行开发。
### git branch——显示分支一览表
git branch -a命令查看当前分支的相关信息。添加 -a 参数可以同时显示本地仓库和远程仓库的分支信息。
### git checkout -b——创建、切换分支
### git merge——合并分支
示例：
假设 feature-A 已经实现完毕，想要将它合并到主干分支 master 中。首先切换到 master 分支。
- git checkout master
然后合并 feature-A 分支。为了在历史记录中明确记录下本次分支合并，我们需要创建合并提交。因此，在合并时加上 --no-ff参数。
- git merge --no-ff feature-A
### git log --graph——以图表形式查看分支
### git reflog——查看当前仓库的操作日志

## 三、更改提交的操作
### git reset——回溯历史版本
git reset --hard命令。只要提供目标时间点的哈希值 ，就可以完全恢复至该时间点的状态。
- 示例： git reset --hard fd0cbf0d4a25f747230694d95cac1be72d33441d
### git commit --amend——修改提交信息
### git rebase -i——压缩历史

## 四、推送至远程仓库
将本地仓库推送至远程仓库，创建时请不要勾选 Initialize this repository with a README 选项（图 4.8）。因为一旦勾选该选项，GitHub 一侧的仓库就会自动生成 README 文件，从创建之初便与本地仓库失去了整合性。虽然到时也可以强制覆盖，但为防止这一情况发生还是建议不要勾选该选项，直接点击 Create repository 创建仓库。
### git remote add——添加远程仓库
git remote add命令 将指定的仓库地址设置成本地仓库的远程仓库
### git push——推送至远程仓库

## 五、从远程仓库获取
### git clone——获取远程仓库
将 GitHub 上的仓库 clone 到本地。注意不要与之前操作的仓库在同一目录下。
### git pull——获取最新的远程仓库分支

## 参考学习资料
- 零基础的 Git 学习资料:Pro Git:[http://git-scm.com/book/zh/v1](http://git-scm.com/book/zh/v1) ,可以免费阅读到包括简体中文在内的各国语言版本。https://github.com/schacon.
- 学习 Git 基本操作的网站:LearnGitBranching，[http://pcottle.github.io/learnGitBranching](http://pcottle.github.io/learnGitBranching),可切换各种语言进行学习。
- web网站：tryGit,[http://try.github.io](http://try.github.io)，只有英文版。





