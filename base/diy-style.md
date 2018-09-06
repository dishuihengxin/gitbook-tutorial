## book.json 配置说明

该文件是Gitbook主要的自定义配置文件，可以设定电子书名，作者信息，主题风格，插件等等。下面给出一个完整的`book.json`配置例子：

	{
    "title": "Gitbook Handbook - Gitbook学习总结 by kalid",
    "description": "Gitbook Handbook - 记录了本人学习使用Gitbook的心路历程，同时也希望可以帮助到有需要的同学，共同进步！",
    "language": "zh-hans",
    "author": "kalid",
	"links":{
		"sidebar":{
			"Kalid's Blog": "https://kalid.io"
		}
	},
    "plugins": [
        "codesnippet",
        "splitter",
        "page-toc-button",
        "image-captions",
        "back-to-top-button",
        "-lunr", 
		"-search", 
		"search-plus",        
        "favicon@^0.0.2",
        "tbfed-pagefooter@^0.0.1",
        "theme-default"
    ],
    "pluginsConfig": {
        "theme-default": {
            "showLevel": true
        },
        "image-captions": {
            "caption": "图片 - _CAPTION_"
        },
        "tbfed-pagefooter": {
            "copyright": "Copyright © kalid.io 2018",
            "modify_label": "Updated:",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
        "favicon": {
            "shortcut": "favicon.ico",
            "bookmark": "favicon.ico"
        }
    }
	}

大家可以根据自己的需求来设置`book.json`内容。

官方给出的配置参考文档：[https://toolchain.gitbook.com/config.html](https://toolchain.gitbook.com/config.html)