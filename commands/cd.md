# cd
变更工作目录

## Usage
```sh
cd [options] [dirname]
```
`[options]`一般不用，不加`[dirname]`为返回到家目录

## 特殊目录
* `.` 代表此层目录
* `..` 代表上一层目录
* `~` 代表使用者的家目录
* `/` 代表根目录
* `-` 代表前一个工作目录
* `~pi` 代表pi这个用户的家目录

## examples
使用命令：
* `pwd` 显示当前目录
* `cd ..` 返回上级目录
* `cd pi/test/` 转到 `pi/test/` 目录下
* `cd /usr/share` 转到 `/usr/share` 目录下
* `cd -` 返回前一个工作目录
* `cd -P test/share` 转到目录 `share` 的实际物理路径
* `cd` 返回家目录
* `cd -L test/share` 转到目录 `share` 的连接目录

![](http://i.imgur.com/kG27Bax.gif)


## 参数
`-P` 变更到实际物理路径，而不是连接(link)目录
`-L` 目录为连接路径时，变更到连接路径(等同于不加参数)