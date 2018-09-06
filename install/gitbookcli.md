## Gitbook cli 初体验

Gitbook已经在电脑上安装好了，先熟悉一下Gitbook cli的命令，以便更好的使用Gitbook进行创作，其实Gitbook的操作命令很简单。

### 1. 创建一本书

准备好电子书文件路径：`D:\gitbook\gitbook-tutorial`

	D:\gitbook\gitbook-tutorial>gitbook init

	warn: no summary file in this book
	info: create README.md
	info: create SUMMARY.md
	info: initialization is finished
执行后会在当前目录下生成`README.md`和`SUMMARY.md`文件，其中`README.md`为电子书的介绍部分，`SUMMARY.md`是整本电子书的目录结构文件。

如果希望电子书创建到指定目录中，可以运行以下命令：

	gitbook init ./directory

### 2. 预览模式

    D:\gitbook\gitbook-tutorial>gitbook serve

	Live reload server started on port: 35729
	Press CTRL+C to quit ...
	
	info: 7 plugins are installed
	info: loading plugin "livereload"... OK
	info: loading plugin "highlight"... OK
	info: loading plugin "search"... OK
	info: loading plugin "lunr"... OK
	info: loading plugin "sharing"... OK
	info: loading plugin "fontsettings"... OK
	info: loading plugin "theme-default"... OK
	info: found 1 pages
	info: found 7 asset files
	info: >> generation finished with success in 1.1s !
	
	Starting server ...
	Serving book on http://localhost:4000
执行后默认会自动安装7个插件，浏览器访问[http://localhost:4000](http://localhost:4000)就可以浏览制作好的电子书了，这很方便让我们去预览或是调式电子书。

### 3. 构建静态文件

当电子书或文档制作完成后，仅需要执行下面这条命令就可以很快速的生成HTML单页面格式的页面，并自动将编译后的HTML单页面存放在`_book`目录下。
	
	gitbook build

单单是这种方式的话，仅仅是生成了一个个对应的单页面文件，还不能自由的切换，所以我们还是将电子书推到Gitbook或是Github上。

### 4. 调式模式

为了更好的预览和调式电子书，需要开启`debug`功能来实现，使用以下命令：

	gitbook build ./ --log=debug --debug
有时候需要不同版本来预览测试电子书，借助Gitbook远程不同版本来实现，查看远程可供版本：

	gitbook ls-remote 

目前所有可用版本：

>
	D:\gitbook\gitbook-tutorial>gitbook ls-remote
	Available GitBook Versions:
>
     4.0.0-alpha.6, 4.0.0-alpha.5, 4.0.0-alpha.4, 4.0.0-alpha.3, 4.0.0-alpha.2, 4.0.0-alpha.1, 3.2.3, 3.2.2, 3.2.1, 3.2.0, 3.2.0-pre.1, 3.2.0-pre.0, 3.1.1, 3.1.0, 3.0.3, 3.0.2, 3.0.1, 3.0.0, 3.0.0-pre.15, 3.0.0-pre.14, 3.0.0-pre.13, 3.0.0-pre.12, 3.0.0-pre.11, 3.0.0-pre.10, 3.0.0-pre.9, 3.0.0-pre.8, 3.0.0-pre.7, 3.0.0-pre.6, 3.0.0-pre.5, 3.0.0-pre.4, 3.0.0-pre.3, 3.0.0-pre.2, 3.0.0-pre.1, 2.6.7, 2.6.6, 2.6.5, 2.6.4, 2.6.3, 2.6.2, 2.6.1, 2.6.0, 2.5.2, 2.5.1, 2.5.0, 2.5.0-beta.7, 2.5.0-beta.6, 2.5.0-beta.5, 2.5.0-beta.4, 2.5.0-beta.3, 2.5.0-beta.2, 2.5.0-beta.1, 2.4.3, 2.4.2, 2.4.1, 2.4.0, 2.3.3, 2.3.2, 2.3.1, 2.3.0, 2.2.0, 2.1.0, 2.0.4, 2.0.3, 2.0.2, 2.0.1, 2.0.0, 2.0.0-beta.5, 2.0.0-beta.4, 2.0.0-beta.3, 2.0.0-beta.2, 2.0.0-beta.1, 2.0.0-alpha.9, 2.0.0-alpha.8, 2.0.0-alpha.7, 2.0.0-alpha.6, 2.0.0-alpha.5, 2.0.0-alpha.4, 2.0.0-alpha.3, 2.0.0-alpha.2, 2.0.0-alpha.1
>
	Tags:
>
     latest : 3.2.3
     pre : 4.0.0-alpha.6


安装指定版本：

	gitbook fetch 3.2.3

好了，马上进入超级打怪模式，Go......

<div align=center><img src="../images/goto.gif"/></div>