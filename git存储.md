```shell
# 存储
git stash

# 查看存储
git stash list

# 应用栈顶元素但不删除
git stash apply

# 删除
git stash drop $name

#应用并删除
git stash pop
```

设置命令别名
```shell
git config --global alias.xxx git命令之后的部分
```