# 2019网络工作室暑期留校计划0709记录

### Git常用命令

git init命令创建一个空的Git仓库或重新初始化一个现有仓库。

git add命令将文件内容添加到索引(将修改添加到暂存区)。也就是将要提交的文件的信息添加到索引库中。

git checkout命令用于切换分支或恢复工作树文件。也是git最常用的命令之一，同时也是一个很危险的命令，因为这条命令会重写工作区。

git commit命令用于将更改记录(提交)到存储库。将索引的当前内容与描述更改的用户和日志消息一起存储在新的提交中。

git push命令用于将本地分支的更新，推送到远程主机。

git pull命令用于从另一个存储库或本地分支获取并集成(整合)。

git clone命令将存储库克隆到新目录中。

git status命令用于显示工作目录和暂存区的状态。

git config命令用于获取并设置存储库或全局选项。这些变量可以控制Git的外观和操作的各个方面。

git help命令显示有关Git的帮助信息。

git diff命令用于显示提交和工作树等之间的更改。

git reset命令用于将当前`HEAD`复位到指定状态。一般用于撤消之前的一些操作(如：git add,git commit等)。

git rm命令用于从工作区和索引中删除文件。

git branch命令用于列出，创建或删除分支。

git mv命令用于移动或重命名文件，目录或符号链接。

git merge命令用于将两个或两个以上的开发历史加入(合并)一起。

git mergetool命令用于运行合并冲突解决工具来解决合并冲突。

git log命令用于显示提交日志信息。

git stash命令用于将更改储藏在脏工作目录中。

git tag命令用于创建，列出，删除或验证使用GPG签名的标签对象。

git fetch命令用于从另一个存储库下载对象和引用。

git remote命令管理一组跟踪的存储库。

git submodule命令用于初始化，更新或检查子模块。

git show命令用于显示各种类型的对象。

git shortlog命令用于汇总git日志输出。

git describe命令显示离当前提交最近的标签。

git rebase命令在另一个分支基础之上重新应用，用于把一个分支的修改合并到当前分支。

### markdown基本语法

##### 标题

在要当做标题的左边以#开头以，并一个空格隔开。 
例如： 
\# 这是一个一级标题
通过逐渐追加#，提升标题等级
\## 这是二级标题
\### 这是三级标题
\#### 这是四级标题
最多可达到6级的标题

##### 列表

在文字的左边加上*或者-就可以呈现出无序标题，如果想要使用有序列表则可以
在文字前面加上1. 2. 3. 等等。

##### 引用

在文本前面加入>就可以达到引用的效果

粗体和斜体

文本左右两边个加两个**可以加粗，加一个*可以让文本倾斜

**这是加粗的文本 ** >>> **这是加粗的文本**
*这是倾斜的文本 * >>> *这是倾斜的文本*

##### 代码高亮

在文本的上下两行夹入```高亮显示

```
这是高亮显示
```

##### 分割线

分割线语法只要三个*就可以实现

------

##### 表格

要实现表格效果，可以使用这样的格式即可

```
| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| Text     | Text     | Text     |
```

| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| Text     | Text     | Text     |


