**GIT的核心是一个简单的键值数据库，向数据库插入任意类型的内容，它会返回一个键值，可以通过该键值检索**

```shell
git hash-object -w --stdin
#-w 参数决定是否写入数据库

#根据键值拉取数据
git cat-file -p $hash

#查看类型
git cat-file -t $hash

#键值对在git内部是一个blob类型
```
**对文件进行简单的版本控制**
```shell
#创建文件并将其内容写入数据库
git hash-object -w ./test.txt

#每个git对象不能代表项目快照，只是记住文件的每一个版本
```
**问题：**
1. 记住文件的每一个版本所对应的hash值不现实
2. 在GIT中文件名没有被保存，仅保存了文件的内容

