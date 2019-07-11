2019网络工作室暑期留校计划0710记录

### linux基本操作

Linux 文件系统是一个**目录树的结构**，文件系统结构从一个根目录开始，根目录下可以有任意多个文件和子目录，子目录中又可以有任意多个文件和子目录

#### bin 存放二进制可执行文件(ls,cat,mkdir等)

boot 存放用于系统引导时使用的各种文件

dev 用于存放设备文件

#### etc 存放系统配置文件

home 存放所有用户文件的根目录

lib 存放跟文件系统中的程序运行所需要的共享库及内核模块

mnt 系统管理员安装临时文件系统的安装点

#### opt 额外安装的可选应用程序包所放置的位置

proc 虚拟文件系统，存放当前内存的映射

#### root 超级用户目录

sbin 存放二进制可执行文件，只有root才能访问

tmp 用于存放各种临时文件

usr 用于存放系统应用程序，比较重要的目录/usr/local 本地管理员软件安装目录

var 用于存放运行时需要改变数据的文件

#### cd-----切换文件目录

​    cd 切换到当前用户的主目录

​    cd ~ 切换到当前用户的主目录

​    cd . 保持在当前目录不变

​    cd .. 切换到上级目录

​    cd - 可以在最近两次工作目录之间来回切换

​    cd /home/dashen/Desktop 切换到指定绝对路径

#### ls-----查看当前文件夹下内容

​    -a 显示指定目录下所有目录与文件，包括隐藏文件

​    -l 以列表方式显示文件的详细信息

​    -h 配合-l以人性化方式显示文件大小

#### pwd-----查看当前所在目录

#### touch-----如果文件不存在则新建空白文件，如果文件已经存在则可以修改文件的末次修改时间

#### tree-----以树状图列出文件目录结构

​    -d 只显示目录

#### mkdir-----创建一个新目录

​    -p 可以递归创建目录

#### rm-----删除指定的文件名

​    -r 递归地删除目录下的内容，删除文件夹时必须加此参数（删除目录）

​    -f 强制删除，忽略不存在的文件，无需提示

#### cp-----复制文件或者目录

​    -i 覆盖文件前提示

​    -r 递归复制该目录下所有子目录和文件，目标文件必须为一个目录名（复制目录）

#### mv-----移动文件或者目录/文件或者目录重命名

​    -i 覆盖文件前提示

#### cat-----查看文件内容、创建文件、文件合并、追加文件内容等功能

​        (一次性显示所有内容，适合查看内容较少的文本文件)

​    -b 对非空输出行编号

​    -n 对输出的所有行编号

#### more-----分屏显示文件内容

​        (适合查看内容较多的文本文件)

​        (空格键--显示下一页  Enter键--一次滚动一行  b--回滚一屏  f--前滚一屏  q--退出)

#### grep-----搜索文本文件内容，允许对文本进行模式查找（正则表达式）

​    -n 显示匹配行及行号

​    -v 显示不包括匹配文本的所有行（相当于求反）

​    -i 忽略大小写

#### echo-----会在终端中显示参数指定的文字，通常会和重定向联合使用

### 安装ubuntu插件

#### 安装zsh插件

sudo apt-get install zsh

#### 安装fish插件

sudo apt-get install fish

#### 安装oh-my-zsh插件

###### 1.1 安装zsh

$ sudo apt-get install zsh

###### 1.2 把默认的Shell改成zsh，注意：不要使用sudo

$ chsh -s /bin/zsh 

###### 1.3 配置密码文件，解决chsh：PAM认证失败的问题

$ sudo vim /etc/passwd

把第一行的/bin/bash改成/bin/zsh，这个是root用户的

把最后一行的/bin/bash改成/bin/zsh，这个应该是每台电脑的登录用户名+计算机名组成的。

###### 2.1 安装oh-my-zsh

$ sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

###### 2.2 重启电脑

$ sudo reboot

###### 2.3 查看效果

$ LANG

###### 3. 自动补全插件

###### 3.1 下载

$ wget http://mimosa-pudica.net/src/incr-0.2.zsh

###### 3.2 将此插件放到oh-my-zsh目录的插件库下

$ sudo mkdir ~/.oh-my-zsh/plugins/incr/
$ sudo mv incr-0.2.zsh ~/.oh-my-zsh/plugins/incr/incr-0.2.zsh
$ sudo vim ~/.zshrc 

###### 3.3 末尾加上如下代码

source ~/.oh-my-zsh/plugins/incr/incr*.zsh

###### 3.4 更新配置

$ source ~/.zshrc

###### 4. 与vim的提示相冲突的解决方案

###### 4.1 使用自动补全插件可能会与vim的提示功能相冲突，如会报以下错误

$ vim t
_arguments:451: _vim_files: function definition file not found

###### 4.2 解决方法：将~/.zcompdump*删除即可

$ rm -rf ~/.zcompdump*
$ exec zsh

#### 安装oh-my-fish插件

curl -L https://github.com/bpinto/oh-my-fish/raw/master/tools/install.sh | sh

#### 安装htop插件

sudo apt-get install htop

#### 安装i3插件

sudo apt-get install  i3

