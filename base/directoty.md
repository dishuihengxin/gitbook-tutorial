## Gitbook 目录结构解析

### 1. 文件结构

- 基本结构(初始化)
-

	
	|--- README.md       # Book instruction
	|--- SUMMARY.md      # Article directory

- 复制结构(多章节)
-
	
	
	|--- README.md         # Book instruction
	|--- SUMMARY.md        # Article directory
	|--- book.json         # Book config file
	|--- GLOSSARY.md       # Glossary list
	|--- Chapter1          # Book Chapter 1
	|     |--- demo1.md    # article-1 in chapter
	|	  |--- demo2.md    # article-1 in chapter
	|--- Chapter2          # Book Chapter 1
		  |--- demo3.md    # article-1 in chapter
		  |--- demo4.md    # article-1 in chapter
	....	


### 2. 目录结构定义

Gitbook的目录都由`SUMMARY.md`链接列表来定义，链接的标题作为电子书章节标题，链接的目标是该章节文件的路径。

简单例子：
	
	
	# Summary

	* [Part I](part1/README.md)
   		* [Writing is nice](part1/writing.md)
    	* [GitBook is nice](part1/gitbook.md)
	* [Part II](part2/README.md)
   		* [We love feedback](part2/feedback_please.md)
    	* [Better tools for authors](part2/better_tools.md)

带锚点的目录结构：

	# Summary

	### Part I

	* [Part I](part1/README.md)
    	* [Writing is nice](part1/README.md#writing)
    	* [GitBook is nice](part1/README.md#gitbook)
	* [Part II](part2/README.md)
    	* [We love feedback](part2/README.md#feedback)
    	* [Better tools for authors](part2/README.md#tools)
    	
### 3. 静态资源

Gitbook使用简单的目录结构，对于一些未在`SUMMARY.md`中定义使用的静态资源都将被同步到输出中，除非配置了忽略文件。

Gitbook首先都会检索`.*ignore`文件是否存在，根据`.gitignore`、`.bookignore`、`.ignore`文件来选择是否忽略哪些文件或文件夹。熟悉Git的同学一定不陌生，`.ignore`遵循一定的格式：

	# Ignore single file，example： demo.md
	demo.md
	# Ignore in the some directory，example： node_module/
	node_module
 	# Ignore everything in the directory,example: _book/
	_book/*
	# Ignore matching keywords,example: demo/  demo1.md  demo.txt
	demo*

### 4. 工程项目附加的电子书

对于一个项目，如果我们想增加一个`document`文档说明书，Gitbook也提供了一个解决方案，`root`指定入口文件路径。

	.
	├── book.json
	└── docs/
   		├── README.md
    	└── SUMMARY.md
只需要在`book.json`中定义好Gitbook的入口路径即可：(注意是json格式)

	{
		"root": "./docs"
	}

    
	