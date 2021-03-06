---
title: "Shell编程参考"
date: 2021-02-06T19:24:10+08:00
lastmod: 2021-02-06T19:24:10+08:00
draft: false
keywords: ["linux", "shell", "script"]
description: "Shell scripting"
tags: ["linux", "shell", "script"]
categories: ["linux", "shell", "script"]
author: ""

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: true
autoCollapseToc: false
postMetaInFooter: false
hiddenFromHomePage: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: false
mathjaxEnableSingleDollar: false
mathjaxEnableAutoNumber: false

# You unlisted posts you might want not want the header or footer to show
hideHeaderAndFooter: false

# You can enable or disable out-of-date content warning for individual post.
# Comment this out to use the global config.
#enableOutdatedInfoWarning: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

<!--more-->
# 说明
作为一个程序员，掌握Linux环境下面的Shell编程，能够让我们的工作生活变得更加轻松愉快。这篇文档将介绍一个简单的Shell脚本的编写，其目的是为了将一个指定目录下面的mkv视频文件转换为mp4文件。
# 脚本源代码
首先来看看代码:
```
 #!/bin/bash
 
 # this script is used to convert .mkv files to .mp4 files by copy original video and audio track
 
 convertMKV2MP4(){
     rootDir=$1
     echo "[INFO] Processing files in: $rootDir"
     
     for file in $rootDir/*
     do
         if test -f $file 
         then
             echo "[INFO] Original file name is: $file"
             newFileName=${file/%.mkv/.mp4}
             echo "[INFO] New file is: $newFileName"
             /usr/local/bin/ffmpeg -i "$file" -vcodec copy -acodec copy "$newFileName"
         else
             echo "[INFO] >>>$file is a folder, processing it..."
             convertMKV2MP4 $file
         fi
     done
 }
 
 targetDir=$1
 
 echo "[INFO] Processing from root directory: $targetDir"
 
 convertMKV2MP4 $targetDir
 
 echo "[INFO] Done"
```

运行：
```
chmod u+x 
./mkv2mp4.sh /Users/yuduan/Downloads/BaiduYun/Dinotrux
```
# 剖析脚本
以下来逐行剖析脚本。
- 1：第一行为Shellbang，格式固定，以#!开始，后面紧跟的是执行该脚本的解释器程序名字。
- 3：注释行，以#开头的（除第一行以外），为注释说明行。
- 5 ~ 23：定义了一个递归函数convertMKV2MP4，遍历并处理指定文件夹下的文件。如果是文件夹，则递归处理之。注意参数不需要显式写出来，而是通过参数$N的形式获取
- 6： 接收函数的参数
- 7：输出提示信息
- 9 ~ 22：一个 for 循环，处理传入的指定路径里面的文件。
- 9：for 循环开始
- 10： do语句
- 11：测试是否是文件
- 12：then语句
- 13：输出提示信息
- 14：替换旧文件名字中的.mkv为.mp4，生成新文件名
- 15：输出新文件名
- 16：使用ffmpeg来转换mkv到mp4
- 17：else语句
- 18：输出提示信息，需要递归处理文件夹里面的文件
- 19：递归调用自身来处理当前文件夹里面的文件
- 20：结束if语句
- 21：结束循环
- 24：获得当前脚本执行时传入的初始路径
- 26：输出提示信息
- 28：针对初始路径，开始执行转换处理
- 30：提示处理完成

# 参考资料
- [Shell scripting](https://www.tutorialspoint.com/unix/shell_scripting.htm)
- [Shell字符串操作](https://www.cnblogs.com/gaochsh/p/6901809.html)
- [Shell目录遍历操作](https://www.cnblogs.com/kaituorensheng/archive/2012/12/19/2825376.html)
- [Shellbang](https://zh.wikipedia.org/wiki/Shebang)
- [Shell script](https://en.wikipedia.org/wiki/Shell_script)




