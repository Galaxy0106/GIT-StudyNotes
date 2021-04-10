## 三个概念

本地分支

远程分支(remote/分支名)

远程跟踪分支

## 远程协作的基本流程

1.项目经理创建一个空的远程仓库

2.项目经理创建一个待推送的本地仓库

3.为远程仓库配别名，配用户名，配邮箱

4.在本地仓库中初始化代码，提交代码

5.推送

6.邀请成员

7.成员克隆远程仓库

8.成员做出修改

9.成员推送自己的修改

10.项目经理拉取成员的修改

```shell
# 做跟踪
	克隆仓库时
	本地没有分支
		git checkout --track 远程跟踪分支（remote/分支名）
	本地已经创建了分支
		git branch -u 远程跟踪分支（remote/分支名）
# 推送
	git push [别名] [分支名]
# 拉取
	git pull
# 使用频率最高的命令
	git status
	git add
	git commit
	git push
	git pull
# pull request
	让第三方人员参与到项目中 fork
	
```

## 忽略某些文件

一些文件不需要纳入git的管理，也不希望它们总出现在未跟踪的文件列表，可以创建名为.gitignore的文件，列出要忽略的文件模式

```
.gitignore的格式规范
eg:

doc/**/*.txt
```























