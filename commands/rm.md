# rm
删除目标文件或目录

## Usage
```sh
rm [options]... file...
```
## examples
使用命令：
* `rm aaa` 删除文件aaa
* `rm -f aaa` 文件不存在也不提示信息
* `rm -i test` 交互式删除文件
* `rm -R -v test2` 递归删除目录且每一步都提示信息

![](http://i.imgur.com/Dr7HQi2.gif)

## 所有参数
* `-f`，`--force` 忽略不存在的文件和对象，从不提示
* `-i` 删除之前都给出提示（交互式）
* `-I` 在删除超过三个文件或者递归删除前要求确认。此选项比 `-i` 提示内容更少，但同样可以阻止大多数错误发生
* `--interactive[=WHEN]` 根据指定的WHEN 进行确认提示：`never`，`once (-I)`，或者`always (-i)`。如果此参数不加WHEN 则总是提示
* `--one-file-system` 递归删除一个层级时，跳过所有不符合命令行参数的文件系统上的文件
* `--no-preserve-root` 不特殊对待"/"
* `--preserve-root` 不允许删除"/"(默认)
* `-r`，`-R`，`--recursive` 递归删除目录及其内容
* `-d`，`--dir` 删除空的目录
* `-v`，`--verbose` 详细显示进行的步骤
* `--help` 显示此帮助信息并退出
* `version` 显示版本信息并退出

## PS
请注意，如果使用rm 来删除文件，通常仍可以将该文件恢复原状。如果想保证该文件的内容无法还原，请考虑使用 `shred` 。