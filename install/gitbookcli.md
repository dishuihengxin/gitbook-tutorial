## Gitbook cli初体验

Gitbook已经在电脑上安装好了，先熟悉一下Gitbook cli的命令，以便更好的使用Gitbook进行创作，其实Gitbook的操作命令很简单。

### 1. 初始化：

准备好电子书文件路径：`D:\gitbook\gitbook-tutorial`

	D:\gitbook\gitbook-tutorial>gitbook init

	warn: no summary file in this book
	info: create README.md
	info: create SUMMARY.md
	info: initialization is finished
执行后会在当前目录下生成`README.md`和`SUMMARY.md`文件，其中`README.md`为电子书的介绍部分，`SUMMARY.md`是整本电子书的目录结构文件。

### 2. 本地调式：

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

### 3. 发布

当电子书制作完成后，我们就可以放到github上，关联Gitbook