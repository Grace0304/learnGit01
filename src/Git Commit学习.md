## 什么是Git

Git是一个开源的**分布式版本控制系统**，用于敏捷高效地处理任何或大或小的项目。



## Git Commit常用命令

设置用户名和邮箱

```
git config --global user.name Grace0303
git config --global user.email 1135990606@qq.com
```

配置好之后可以使用

```
git config -l
```

查看配置

<img src=C:\Users\Think\AppData\Roaming\Typora\typora-user-images\image-20210807171205277.png style="float :left;" />

初始化仓库

```
git init
```

添加文件到暂缓区(把本地所修改的文件暂存到缓存区)

```
git add .
```

查看仓库当前的状态，显示有变更的文件

```
git status
```

创建文件夹

```
mkdir src(文件夹名)
```

创建文件

```
touch readme.txt(文件名)
```

进入文件编写内容

```
vi readme.txt
```

返回上一级

```
cd ../
```

进入和退出编辑状态

```
按i进入编辑文本状态
编辑完后按Esc，然后在命令框地下输入:wq就能退出
```

拷贝一份远程仓库(也就是下载一个项目)

```
git clone https://github.com/Grace0304/learnGit.git
```

提交暂缓区到本地仓库(相当于准备去推送到远程仓库，去做一个描述)

```
git commit -m "你的文件说明"
```

传到远程仓库

```
git remote add origin https://github.com/Grace0304/learnGit.git
```

推送到远程仓库master分支

```
git push origin master//origin是远程库名称
```



## Git Commit相关规范

用于说明git commit的类别，只允许使用下面的标识。

|  标识名  |                             作用                             |
| :------: | :----------------------------------------------------------: |
|   feat   |                    代表新的内容(feature)                     |
|   fix    | 修复bug(产生diff并自动修复问题，适合于一次提交直接修复问题)  |
|    to    | 修复bug(产生diff并不自动修复问题，适合于多次提交。最终修复问题提交时使用fix) |
|  chore   |             代表了有一些简单的内容、样式上的修改             |
|   docs   |                     文档(documentation)                      |
|  style   |                  格式(不影响代码运行的变动)                  |
| refactor |        重构(即不是新增功能，也不是修改bug的代码变动)         |
|   perf   |                 优化相关，比如提升性能、体验                 |
|   test   |                           增加测试                           |
|  revert  |                       回滚到上一个版本                       |
|  merge   |                           代码合并                           |
|   sync   |               同步主线或分支的Bug(synchronize)               |

