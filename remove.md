---
title: windows系统下终端删除命令
date: 2021-12-27
sidebar: "auto"
categories:
  #   - 建站
  - Git
tags:
  #   - 思路
  #   - 博客
  - git
---

## 删除文件 del/erase

- 删除某文件：del name（文件名）

- 删除固定后缀的文件： del \*.txt(以.txt 后缀举例）

```
C:\Users\Administrator>del /?
删除一个或数个文件。

DEL [/P] [/F] [/S] [/Q] [/A[[:]attributes]] names
ERASE [/P] [/F] [/S] [/Q] [/A[[:]attributes]] names

  names         指定一个或多个文件或者目录列表。
                通配符可用来删除多个文件。
                如果指定了一个目录，该目录中的所
                有文件都会被删除。

  /P            删除每一个文件之前提示确认。
  /F            强制删除只读文件。
  /S            删除所有子目录中的指定的文件。
  /Q            安静模式。删除全局通配符时，不要求确认
  /A            根据属性选择要删除的文件
  属性           R  只读文件                    S  系统文件
                H  隐藏文件                    A  存档文件
                I  无内容索引文件               L  重分析点
                -  表示“否”的前缀
```

<br/>

## 删除目录 rmdir/rd

- 删除空目录：rmdir name（当前路径下的目录名）

- 删除非空目录：rmdir /s name（同上）

```
C:\Users\Administrator>rmdir /?
删除一个目录。

RMDIR [/S] [/Q] [drive:]path
RD [/S] [/Q] [drive:]path

    /S      除目录本身外，还将删除指定目录下的所有子目录和
            文件。用于删除目录树。

    /Q      安静模式，带 /S 删除目录树时不要求确认
```

参考链接：https://www.cnblogs.com/macrored/p/11415741.html
