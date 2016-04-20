# touch
一、把已存在的文件时间标签更新到系统当前时间(默认方式)
二、创建空文件

## Usage
```sh
touch [OPTION]... FILE...
```
## examples
1.创建一个空的名为 `test` 的文件
```sh
touch test
```
2.用 `test` 文件的时间设置为文件 `test2` 的时间
```sh
touch -r test test2
```

## 所有参数
* `-a` 只更改存取时间(访问时间)
* `-c`，`--no-create` 不建立任何文件
* `-d`，`--date=STRING` 解析日期时间，代替文件的当前时间
* `-f` (忽略不处理)
* `-h`，`--no-dereference` 影响文件的每个符号连接(仅在可以更改符号链接的时间戳的系统上有用)
* `-m` 只更改修改时间
* `-r`，`--reference=FILE` 使用此文件`[FILE]` 时间，而不是当前时间
* `-t [STAMP]` 使用 `[[CC]YY]MMDDhhmm[.ss]` 而不是当前时间
* `--time=WORD` `access`，`atime`，`use` 等同于 `-a`，`modify`，`mtime` 等同于 `-m`
* `--help` 显示此帮助信息并退出
* `--version` 显示版本信息并退出

ps: `[[CC]YY]MMDDhhmm[.ss]`中，CC为年的前两位，YY为年的后两位，MM为月份，DD为天数，hh为小时，mm为分钟，SS为秒(范围0~61，目的处理闰秒)