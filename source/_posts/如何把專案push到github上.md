---
title: 如何把專案push到github上
date: 2024-05-29 10:38:23
tags:
    -Git
---

實作將hexo專案push到hithub
<!--more-->


1. repo clone
```
git clone -b source git@github.com:[你的github帳號]/[repo名稱].git
```

2. git 初始化
```
git init
```
基本上此步驟只會執行一次，作為原始碼版控；當出現 Initialized empty Git repository in XXXX 代表成功
檔案變綠色，代表可以加入版控；反之灰色則不會上船也不加入版控

3. 將檔案加入索引
```
git add .
```
或者是
```
git add -A
```
4. 查看狀態
```
git status
```
5. 提交檔案
```
git commit -m "information"
```
後面參數有分 -m 以及 -a，-m 允許輸入註解 (一般常用-m)
按下enter後，底下會跑一堆 create mode XXX

6. 推送檔案
```
git remote add origin https://github.com/<username>/<project>
git push -u origin main
```
以上指令分別代表建立一個遠端分支origin，後面是這分支的 url
然後推送 git 到 origin 的 main分支
註：有時候會 push失敗，多試幾次
其中參數 -u 代表記錄此次推送資訊，下次再推送就只需要輸入以下指令
```
git push
```
7. 創建 git 分支
```
git checkout -b main
```
以上指令為創建 main
