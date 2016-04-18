# ls
列出目录下的子目录和文件

## Usage
```sh
ls [options] [dirname]
```
显示当前目录时选项 `[dirname]` 不需要

## 文件显示颜色含义
* 默认色 普通文件 
* 绿色 可执行文件
* 红色 压缩包
* 蓝色 目录
* 粉紫色 图片
* 青色 链接文件(快捷方式)
* 黄色 设备

## examples
使用命令：
* `ls` 打印当前目录下文件
* `ls -1` 每行只打印一个文件
* `ls -a` 打印目录下所有文件，包括隐藏文件、 `. `和 `..`
* `ls -a --color=none` 打印目录下所有文件，包括隐藏文件、 `. `和 `..`，同时不显示文件颜色
* `ls -A` 打印目录下所有文件，包括隐藏文件，但不打印 `.` 和 `..`
* `ls -A --color=none` 打印目录下所有文件，包括隐藏文件，但不打印 `.` 、 `..`和文件颜色
* `ls -l` 详细列表打印文件，[权限] [连结] [所属者] [群组] [文件大小] [修改日期] [文件或目录名]
* `ls -R` 递归列出子目录下的文件
* `ls -F` 文件名后缀加上一个区别文件类型的字符
* `ls -FR` 递归列出子目录下的文件且文件加后缀区别文件类型
* `ls -lx` 按列排序显示(系统默认按行)

![](http://i.imgur.com/en04QcT.gif)

## 所有参数
* `-1` (阿拉伯数字1)  每行只显示一个文件
* `-a` , `--all`	  显示目录下所有文件，包括隐藏文件、 `. `和 `..` 
* `-A` , `--almost-all`  显示目录下所有文件，包括隐藏文件，但不显示 `.` 和 `..`
* `-b` , `--escape` 文件名中不可输出的字符以反斜杠加字符编码的形式显示
* `-B` , `--ignore-backups` 不显示备份文件(备份文件是以 `~` 结尾的文件 )
* `-c` 以文件状态的更改时间排序，一般结合 `-l` 使用
* `-C` 按列显示，横向排序
* `-d` , `--directory` 显示目录，而不显示目录下的文件
* `-D` , `--dired` 用Emacs的模式产生文件和目录列表
* `-f` 显示文件不排序，且文件颜色不显示，与 `-aU` 相似，后者有颜色显示
* `-F` , `--classify` 文件名后缀加上一个区别文件类型的字符，如 `*` 表示可执行文件，`/` 表示目录，`@` 表示符号链接, `|` 表示FIFOs, `=` 表示套接字(sockets)
* `-g` 与 `-l` 相似，区别于不显示文件所属者，一般无用
* `-G` , `--no-group` 不显示文件所属群组，结合 `-l` 使用相似于 `-g` , 区别于一个不显示所属者，一个不显示群组
* `-h` , `--human-readable` 以“K”、“M”、“G”更容易被人理解的形式显示文件的大小（例如：4096显示为4K）
* `-H` , `--dereference-command-line` 以连结形式存在的文件（即快捷方式）显示真正目录所在地，例如：`-lH`会显示 `netcat -> /etc/alternatives/netcat`
* `-i` , `--inode` 显示文件和目录的 `inode` 号
* `-I` , `--ignore=PATTERN` 不显示符合样式的文件或目录
* `-k` , `--kibibytes` 与指定 `block-size=1024`参数相同，以“K”的形式显示文件大小
* `-l` 详细列表显示文件，[权限] [连结] [所属者] [群组] [文件大小] [修改日期] [文件或目录名]
* `-L` , `--dereference` 当显示符号链接的文件信息时，显示符号链接所指示的对象而并非符号链接本身的信息
* `-m` 以逗号来分隔文件
* `-n` , `--numeric-uid-gid` 类似 -l，但列出UID 及GID 号
* `-N` , `literal` 按文件整体显示，不限制文件长度
* `-o` 显示文件除群组外的详细信息，类似 `-l`
* `-p` , `--indicator-style=slash` 与 `-F` 一样
* `-q` , `--hide-control-chars` 用?代替不可显示的字符
* `-Q` , `--quoting-style=WORD` 文件名以双引号括起来的形式显示
* `-r` , `--reverse` 逆序排列
* `-R` , `--recursive` 递归列出子目录下的文件
* `-s` , `--size` 以块数形式显示每个文件分配的尺寸
* `-S` 以文件大小排序
* `-t` 以时间排序
* `-T` , ` --tabsize=COLS` 设<tab>字符间隔宽度为COLS,预设为8
* `-u` 根据上次存取时间排序
* `-U` 不排序，显示项目的默认顺序
* `-v` 以版本进行排序显示
* `-w` , `--width=COLS` 假设画面的宽度为COLS取代当前值，即自定义显示屏幕宽度
* `-x` 按列排序显示(系统默认按行)
* `-X` 以文件扩展名排序显示
* `-Z`, `--context` 打印文件的 `SELinux`(Security-Enhanced Linux)
* `--author` 配合 `-l` ，打印文件的创建者
* `--block-size=SIZE` 指定文件大小显示类别，“K”，“M”，“G”等，但是会向上取整
* `--color[=WHEN]` 设置显示颜色，默认为 `always` 总是显示，可设置为 `never` 不显示， 或者 `auto` 自动显示
* `--file-type` 与 `-F` 一样，除了不追加 `*`
* `--format=WORD` `horizontal` 和 `across` 等同于 `-X`，`commas` 等同于 `-m`，`long` 、 `single-column` 和 `verbose` 等同于 `-l`，`vertical` 等同于 `-C`
* `--full-time` 与 `-l` 相似，完整的显示时间
* `--group-directories-first` 在文件前分组目录。此选项可与 `--sort` 一起使用， 但是一旦使用 `--sort=none`  (-U)将禁用分组
* `--si` 与 `-h` 类似，但是使用1000 为基底而非1024
* `--dereference-command-line-symlink-to-dir` 跟随命令行列出的目录的符号链接
* `--hide=PATTERN` 隐藏符合PATTERN 模式的项目，与 `-I` 相似(`-a` 或 `-A` 将覆盖此选项)
* `--indicator-style=WORD` 指定在每个项目名称后加上指示符号方式：none (默认)，classify (-F)，file-type (-p) 
* `--show-control-chars` 直接显示无法打印的字符 (这是默认方式，除非调用的程序名称是"ls"而且是在终端输出结果)
* `--quoting-style=WORD` 使用指定的quoting 方式显示条目的名称： `literal` 、`locale` 、`shell` 、`shell-always` 、`c` 、`escape`
* `--sort=WORD` `node` 相当于 `-U`，`extension` 相当于 `-X`，`size` 相当于 `-S`，`time` 相当于 `-t` ， `version` 相当于 `-V`
* `--time=WORD` 与 `-l` 配合使用，`atime` 、`access` 、`use` 相当于 `-u` ，`ctime` 、 `status` 相当于 `-c` 
* `--time-style=STYLE` 和 `-l` 同时使用时根据 `STYLE` 代表的格式显示时间，`STYLE` 有 `full-iso`, `long-iso`, `iso`, `locale`, `+FORMAT`
* `--help` 显示此帮助信息并退出
* `--version` 显示版本信息并退出
