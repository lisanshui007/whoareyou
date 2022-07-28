---
title: windows系统下终端删除.git文件夹
date: 2021-12-27
sidebar: "auto"
categories:
  - Git
tags:
  - git
---

- git 文件夹是隐藏文件

- 删除命令：rm -r -fo name（需要删除的文件名）

- rm 是 Romove、-r 是指-Recurse（递归）、-fo 是指-Force（强行）

```
为了删除[包含]隐藏项的目录，PowerShell的Remove-Itemcmdlet需要传递-Force开关：

Remove-Item -Recurse -Force test
此命令的最短形式（用于交互式而非脚本编写），使用platform-neutralri别名和PowerShell的so-called弹性语法，只要前缀明确，就足以指定参数名的前缀（例如-Recurse的-r）：

ri -r -fo test
请注意-Force如何需要两个字母的前缀，因为-f本身是不明确的：它还可以引用-Filter参数。

git init创建一个.git子目录，该子目录在Windows上被分配了Hidden属性（在Unix-like平台上，名称仅以.开头的事实使目录成为隐藏目录）。
在Windows上，rm、del、rmdir只是built-in的Remove-Item别名，是用于删除文件和目录的单个cmdlet（如果目录不为空，则删除后者需要-Recurse）。（在Unix-like平台上，只有del被定义为别名，以便不影响platform-nativerm和rmdir实用程序。）ri是从名称Remove-Item派生的平台无关别名，因此更可取。要查看为给定命令定义的所有别名，请使用Get-Alias -Definition $name；e、 g.：Get-Alias -Definition Remove-Item
注意：虽然PowerShell通过-Force要求显式opt-in删除隐藏项可能是有益的，这样您就不会意外删除您可能不知道存在的项，但错误消息是次优的，因为问题不是权限问题。
```

参考链接：https://www.5axxw.com/questions/content/iopd0c
