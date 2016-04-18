# tree
以树状图列出目录下的子目录和文件

## Usage
```sh
tree [options] [dirname]
```
显示当前目录时选项 `[dirname]` 不需要

## Installation
`tree`命令系统不自带，需要下载包

```sh
sudo apt-get install tree
```
## examples
使用命令：
* `tree` 以树状图打印当前目录下文件
* `tree -a` 打印目录下所有文件，包括隐藏文件
* `tree -d` 只打印目录
* `tree -f` 显示完整的相对路径名称
* `tree -af` 显示完整的相对路径名称，包括隐藏文件
* `tree -a -L 1` 打印一层目录下的所有文件
* `tree -a -L 2` 打印二层以上目录下的所有文件
* `tree -Q` 文件名用双引号括起来
* `tree -p` 打印文件的权限
* `tree -s` 列出文件或目录大小
* `tree` 以树状图打印当前目录下文件
* `tree -r` 倒序排序
* `tree -i` 不以阶梯状列出文件或目录名称
* `tree -Sn` 以ASCII图形压痕线打印且不显示颜色

![](http://i.imgur.com/djEDUjt.gif)

## 所有参数

### 列表选项
* `-a` 列出目录下所有文件，包括隐藏文件
* `-d` 只列出目录
* `-l` 列出符号连接文件(快捷方式)的原始目录
* `-f` 显示完整的相对路径名称
* `-x` 将范围局限在现行的文件系统中，若指定目录下的某些子目录，其存放于另一个文件系统上，则将该目录予以排除在寻找范围外
* `-L [level]` 指定列出前几级目录，1为只显示一级目录
* `-R` Rerun tree when max dir level reached
* `-P [pattern]` 只显示符合范本样式的文件或目录名称
* `-I [pattern]` 不显示符合范本样式的文件或目录名称
* `--noreport` 关闭文件/目录树列表末尾的计数
* `--charset=X` 使用虚线输出树显示，使用字符集terminal/HTML(`tree --charset`可以显示所有参数)
* `--filelimit #` Do not descend dirs with more than # files in them
* `timefmt <f>` 根据 <f>的格式打印时间
* `-o [filename]` 创建 `[filename]` 文件，打印信息输出到文件中

### 文件选项
* `-q` 用“？”取代无法打印的字符
* `-N` 输出未经处理的项目名称 (如不特别处理控制字符)
* `-Q` 文件名用双引号括起来
* `-p` 打印文件的权限
* `-u` 列出文件或目录的拥有者名称，没有对应的名称时，则显示用户识别码
* `-g` 列出文件或目录的所属群组名称，没有对应的名称时，则显示群组识别码
* `-s` 列出文件或目录大小
* `-h` 以“K”、“M”、“G”更容易被人理解的形式显示文件的大小（例如：4096显示为4K）
* `--si` 与 `-h` 类似，但是使用1000 为基底而非1024
* `-D` 列出文件或目录的修改时间
* `-F` 文件名后缀加上一个区别文件类型的字符，如 `*` 表示可执行文件，`/` 表示目录，`@` 表示符号链接, `|` 表示FIFOs, `=` 表示套接字(sockets)
* `--inodes` 显示文件和目录的 `inode` 号
* `--device` 打印属于每个文件的设备 `ID` 号

### 排序选项
* `-v` 以版本进行排序显示
* `-r` 逆序排序
* `-t` 以最后修改时间排序
* `-c` 以最后状态更改时间排序
* `-U` 不排序，显示项目的默认顺序
* `--dirsfirst` 目录文件在文件之前列出( `-U` 不可用)

### 图形选项
* `-i` 不以阶梯状列出文件或目录名称
* `-A` 使用ASNI绘图字符显示树状图
* `-S` 以ASCII图形压痕线打印
* `-n` 不在文件和目录清单加上颜色(与 `-C` 一起使用会失效)
* `-C` 在文件和目录清单加上色彩，用于于区分各种类型

### XML/HTML选项
* `-X` 以XML格式显示
* `-H [baseHREF]` 生成HTML形式且打印出来，`[baseHREF]`为文件头目录路径
* `-T [string]` 与 `-H` 配合使用，设置HTML头部标签和h1标签
* `--nolinks` 与 `-H` 配合使用，关闭文件的超链接显示

### 其他选项
* `--version` 显示此帮助信息并退出
* `--help` 显示版本信息并退出