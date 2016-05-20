title: 'Code snippets, save time'
categories: Development
tags:
  - Xcode
date: 2016-05-19 16:58:19
---

WWDC上Apple的工程师经常在demo的时候拖自己的code snippet，为什么不用completion shortcut，是提醒懒人们多用这功能吗？


<!--more-->
### 例子：初始化view controller
习惯新建view controller 同时选择生成同名xib的童鞋，也会经常用以下init选择初始化时候的nib文件。这样写的好处是不管view controller在不在被使用的bundle里，都能随便用。


	- (instancetype)init
	{
	    self = [super initWithNibName:[[self class] description] bundle:[NSBundle bundleForClass:[self class]]];
	    if (self) {
	        ;
	    }
	    return self;
	}
把这段代码拖到code snippet里，再编辑个completion shortcut，如下图：

![Example](/img/Code_snippets_save_time/1.png)

以后只要敲initvc，这段代码就可以自动补全了。

### 同步
为了方便在不同机器之间同步和随时更新code snippet(假装很勤劳的样子)
在`~/Library/Developer/Xcode/UserData/CodeSnippets` init一个repo， 放在github上吧。

