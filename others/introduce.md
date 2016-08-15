# **Gitbook 超過兩層目錄結構**

---

因為 Gitbook 作者進行設計時認為一本書的目錄結構應該不要太複雜，所以只設計了兩層目錄結構，但使用者還是希望可以有更深的目錄結構，所以也有開發者針對 Gitbook 進行目錄的功能修正，而作者也將這些程式碼合併到 Gitbook 的開源專案裡面，但是在實際使用上會發現雖然第二層以後的目錄會顯示在網頁上，但是卻沒有該檔案，因此需要一些修正來幫忙輔助 Gitbook 設計書籍。

這邊使用 Python 的小程式來幫忙輔助，透過讀取 SUMMARY.md 檔案後進行，其流程如下。

![](../../assets/python.jpg)

程式碼如下 :

```
# !/usr/bin/python
# -*- coding: utf-8 -*-

import re
import os

for line in open("SUMMARY.md"):
    try:
        src1 = re.search('\((.+?)\)', line)
        src = src1.group(1)
    except:
        print line
    else:
        cnt = src.count('/')
        if cnt == 3:
            str = re.search('(.+?)/(.+?)/(.+?)/(.*)', src)
            path = str.group(1) + "/" + str.group(2) + "/" + str.group(3)
            file = str.group(1) + "/" + str.group(2) + "/" + str.group(3) + "/" + str.group(4)
            if not os.path.isdir(path):
                print "create folder: " + path
                os.mkdir(path)
            if not os.path.isfile(file):
                print "create file: " + file
                open(file, "a").close()
            print str.group(1) + ".." + str.group(2) + ".." + str.group(3) + ".." + str.group(4)

        elif cnt == 2:
            str = re.search('(.+?)/(.+?)/(.*)', src)
            path = str.group(1) + "/" + str.group(2)
            file = str.group(1) + "/" + str.group(2) + "/" + str.group(3)
            if not os.path.isdir(path):
                print "create folder: " + path
                os.mkdir(path)
            if not os.path.isfile(file):
                print "create file: " + file
                open(file, "a").close()
            print str.group(1) + ".." + str.group(2) + ".." + str.group(3)
```

