
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
