# ls
列出目录下的子目录和文件

## 格式
```sh
ls [options] [dirname]
```
## 参数
* `-1` (阿拉伯数字1)  每行只显示一个文件
* `-a` , `--all`	  显示目录下所有文件，包括隐藏文件、 `. `和 `..` 
* `-A` , `--almost-all`  显示目录下所有文件，包括隐藏文件，但不显示 `.` 和 `..`
* `-b` , `--escape` 文件名中不可输出的字符以反斜杠加字符编码的形式显示
* `-B` ， `--ignore-backups` 不显示备份文件(备份文件是以 `~` 结尾的文件 )
* `-c` 以文件状态的更改时间排序，一般结合 `-l` 使用
* `-C` 按列显示，横向排序
* `-d` , `--directory` 显示目录，而不显示目录下的文件
* `-D` , `--dired` 用Emacs的模式产生文件和目录列表
* `-f` 显示文件不排序，且文件颜色不显示，与 `-aU` 相似，后者有颜色显示
* `-F` , `--classify` 文件名后缀加上一个区别文件类型的字符，如 `*` 表示可执行文件，`/` 表示目录等
* `-g` 与 `-l` 相似，区别于不显示文件所属者，一般无用
* `-G` , `--no-group` 不显示文件所属群组，结合 `-l` 使用相似于 `-g` , 区别于一个不显示所属者，一个不显示群组
* `-h` , `--human-readable` 以“K”、“M”、“G”更容易被人理解的形式显示文件的大小（例如：4096显示为4K）
* `-H` , `--dereference-command-line` 以连结形式存在的文件（即快捷方式）显示真正目录所在地，例如：`-lH`会显示 `netcat -> /etc/alternatives/netcat`
* `-i` , `--inode` 显示文件和目录的 `inode` 号
* `-I` , `--ignore=PATTERN` 不显示符合样式的文件或目录
* `-k` , `--kibibytes` 与指定 `block-size=1024`参数相同，以“K”的形式显示文件大小
* `-l` 详细列表显示文件，[权限] [连结] [所属者] [群组] [文件大小] [修改日期] [文件或目录名]
* `-L` , `--dereference`
* `-m`
* `-n` , `--numeric-uid-gid`
* `-N` , `literal`
* `-o`
* `-p` , `--indicator-style=slash`
* `-q` , `--hide-control-chars`
* `-Q` , `--quoting-style=WORD`
* `-r` , `--reverse`
* `-R` , `--recursive`
* `-s` , `--size`
* `-S`
* `-t`
* `-T` , ` --tabsize=COLS`
* `-u`
* `-U`
* `-v`
* `-w` , `--width=COLS`
* `-x`
* `-X`
* `-z`, `--context`
* `--author`
* `--block-size=SIZE`
* `--color[=WHEN]`
* `--file-type`
* `--format=WORD`
* `--full-time`
* `--group-directories-first`
* `--si`
* `--dereference-command-line-symlink-to-dir`
* `--hide=PATTERN`
* `--indicator-style=WORD`
* `--show-control-chars`
* `--quoting-style=WORD`
* `--sort=WORD`
* `--time=WORD`
* `--time-style=STYLE`
* `--help`
* `--version`