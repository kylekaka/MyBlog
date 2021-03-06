# tar命令简介
根据tar的手册上的说明，tar主要是一个用来归档打包文件的工具软件。
tar命令是linux中比较复杂的命令，主要是因为这个命令的参数比较多而且不太好记忆。
个人认为没有必要去死记硬背这些参数，可以通过查看help帮助，
同时利用cheat命令来帮助自己可以在日常工作中使用tar命令。

# tar常用参数
通过tar --help命令可以查看到tar的参数用法。
```
$ tar --help
```
下面列出常用的一些参数的说明。
```
-t, --list                 列出归档内容

-c, --create 创建一个新归档

-x, --extract, --get 从归档中解出文件

-z, --gzip, --gunzip, --ungzip 通过 gzip 过滤归档

-v, --verbose 详细地列出处理的文件

-f, --file=ARCHIVE 使用归档文件或 ARCHIVE 设备
```

# 利用cheat命令查看tar用法
在日常使用中如果忘记了tar的参数，可以通过man命令来查看手册，但是手册中参数太繁多，不是很方便快速找到对应的参数。
这里推荐一个辅助记忆的cheat命令，在终端中输入下面命令
```
$ cheat tar
```
结果输出如下：
```
# To extract an uncompressed archive（提取tar归档文件）
tar -xvf /path/to/foo.tar

# To create an uncompressed archive（创建未压缩的tar归档文件）
tar -cvf /path/to/foo.tar /path/to/foo/

# To extract a .gz archive:（解压缩提取.gz文件）
tar -xzvf /path/to/foo.tgz

# To create a .gz archive:（创建.gz压缩文件）
tar -czvf /path/to/foo.tgz /path/to/foo/

--snip--

# To use parallel (multi-threaded) implementation of compression algorithms:
tar -z ... -> tar -Ipigz ...
tar -j ... -> tar -Ipbzip2 ...
tar -J ... -> tar -Ipixz ...
```
可以看到cheat命令已经列出了tar命令常见的用法，例如压缩和打包.gz和对应的解压缩.gz文件等。
这样再结合上面查询到的tar帮助文档中的常见参数，就可以直接使用tar命令了。

#小结
最后，个人认为学习linux命令最关键还是多多使用，进行更多的实践。这样就自然可以记住常用的命令。
