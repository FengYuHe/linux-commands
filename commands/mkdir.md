# mkdir (make directory)
创建一个新的目录

## Usage
```sh
mkdir [options] [dirname]
```
不加 `[options]` 目录默认权限（umask）为**rwxr-xr-x**，即755，具体权限介绍看[权限简单叙述](#power)

## examples
使用命令：
* `mkdir test1` 以默认权限创建 `test1` 目录
* `mkdir -m 776 test2` 以自定义权限 `rwxrwxrw-` 创建 `test2` 目录
* `mkdir -pv a/b/c` 递归创建目录 `a`、`b`、`c`，且打印提示信息
* `tree` 查看目录树，具体看 `tree` 命令

![](http://i.imgur.com/V9xLgS3.gif)

## 所有参数
* `-m` ， `--mode=MODE` 创建目录且设定权限，权限值为三个数字组成(具体看[权限简单叙述](#power))
* `-p` ， `--parents` 递归向下创建多层目录，即可直接创建 `a/b/c` 三个目录
* `-v` ， `--verbose` 创建目录是打印提示信息
* `-Z` ， `--context=CTX` 创建目录时设置 `SELinux`(Security-Enhanced Linux)
* `--help` 显示此帮助信息并退出
* `--version` 显示版本信息并退出

<a name="power"></a>
## 权限简单叙述
> 文件权限分为**所属者**、**群组**和**其他人**三种角色权限；每种角色拥有rwx三种权限，分别为**读**、**写**、**运行**。
> `ls -l`命令可查看文件权限，`-rwxrwxrwx`，总共有10格，第一格代表文件类型。剩下9个分别为**所属者**、**群组**和**其他人**的对文件所拥有的权限。
> 读权限以数字4代表，写权限以数字2代表，运行权限以1代表，以这三个数字代表的原理是无论怎么相加，都不会出现相同的情况。
> 每个角色对文件的权限以各种权限数字的和表示，例：7则为读写运行三种权限都拥有。

例：755权限则为 `rwxr-xr-x`。