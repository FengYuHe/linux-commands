# rmdir (remove directory)
删除一个空的目录

## Usage
```sh
rmdir [options] [dirname]
```
## examples
使用命令：
* `tree` 查看目录树
* `rmdir test1` 删除空文件夹 `test1`
* `rmdir -v test2` 删除空文件夹 `test2` 且提示信息
* `rmdir -pv a/b/c` 递归删除空文件夹 `a/b/c`，`a/b`，`a`,且提示信息
* `rmdir -p q/w/e` 递归删除文件夹`q/w/e`，`q/w`，`q`, `q` 文件夹非空不可删

![](http://i.imgur.com/2MGWWWu.gif)

## 所有参数
* `--ignore-fail-on-non-empty` 删除非空目录时不提示失败信息
* `-p`，`--parents` 删除目录及其父级目录，例如：`rmdir -p a/b/c` 为 `rmdir a/b/c a/b a`
* `-v`，`--verbose` 删除目录时打印提示信息
* `--help` 显示此帮助信息并退出
* `--version` 显示版本信息并退出
