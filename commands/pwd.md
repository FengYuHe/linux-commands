# pwd (print work directory)
显示目前所在的工作目录

## Usage
```sh
pwd [options]
```
## examples
使用命令：
* `ls -l` 打印当前目录文件的详细信息
* `cd share` 切换到 `share` 目录下
* `pwd` 打印目前所在的工作目录
* `pwd -P` 打印实际物理路径
* `pwd -L` 打印连接路径

![](http://i.imgur.com/4wTl284.gif)

## 所有参数
* `-L` ， `--logical`(长参数无效) 目录位连接路径时，显示连接路径
* `-P` ， `--physical`(长参数无效) 显示实际物理路径，而非连接（link）路径
* `--help`(无效) 显示此帮助信息并退出，可使用 `man pwd` 查看帮助信息
* `--version`(无效) 显示版本信息并退出