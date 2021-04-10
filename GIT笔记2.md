## git分支

```shell
分支的本质是一个提交对象
HEAD一个时刻只能指向一个分支
有新的提交时，HEAD会携带当前的分支持续往前移动

# 创建
git branch branchname
# 切换
git checkout branchname
# 创建 & 切换
git checkout -b branchname
# 普通删除
git branch -d branchname
# 强制删除
git branch -D branchname


### 合并分支
git merge branchname
# 快进合并
不会产生冲突
# 典型合并
有机会产生冲突
# 解决冲突
打开冲突的文件修改
add + commit

# 版本穿梭
git branch branchname commitHash

# 查看分支列表
git branch
# 查看合并到当前分支的分支
git branch --merged

# 查看没有合并到当前分支的分支
git branch --no-merged

在切换的时候一定要保证当前分支是干净的
	允许切换分支：分支上所有内容处于已提交状态
				分支上的内容是初始化创建	处于未跟踪状态
				
```











```shell
# 后悔药
撤销工作目录的修改：git checkout -- filename
撤销暂存区的修改：git reset HEAD filename
撤销提交：git commit --amend

# reset三部曲
git reset --soft commithash ---> 重置HEAD,用commitHash的内容重置HEAD
git reset --mixed commithash ---> 用commitHash的内容重置HEAD内容，重置暂存区
git reset --hard commithash ---> 用commitHash的内容重置HEAD内容，重置暂存区，重置工作目录

# 路径reset
所有的路径reset都要省略第一步
第一步是重置HEAD内容
HEAD可以代表一系列文件的状态
git reset --mixed commithash filename

# 用commithash中filename的内容重置暂存区

### checkout深入了解
git checkout branchname 跟 git reset --hard commithash很像
共同点：
	都需要重置HEAD，暂存区和工作目录
不同点：
	checkout对工作目录是安全的的，reset --hard是强制覆盖
	checkout不带着分支走而是切换分支，reset --hard是带着分支走
	
checkout + 路径
	git checkout commitHash filename
		重置暂存区
		重置工作目录
	git checkout -- filename
		重置工作目录
```



