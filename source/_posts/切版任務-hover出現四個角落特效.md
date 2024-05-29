---
title: 切版任務-hover出現四個角落特效
date: 2024-05-29 10:37:56
tags:
    -CSS
---

實作如下
<!--more-->

關鍵語法為 border-(left/right/top/bottom) : none;
可讓邊線消失

## HTML
```
<div class="wrap">
  <ul class="list">
    <li class="list-text">
      <a href="./">
        <span class="border_corner border-corner-top-left"></span>
        <span class="border_corner border-corner-top-right"></span>
        <span class="border_corner border-corner-bottom-left"></span>
        <span class="border_corner border-corner-bottom-right"></span>
        作品集</a>
    </li>
  </ul>
</div>
```

## CSS
```
body {
  font-family: "Noto Sans TC", sans-serif;
  line-height: 1.5;
}
a {
  text-decoration: none;
  color: black;
  font-size: 30px;
}
.wrap {
  width: 480px;
  margin: 20px auto;
}
.list-text {
  font-weight: 600;
  display: inline-block;
  text-align: center;
}
.list-text a {
  padding: 4px 8px;
  position: relative;
}
.border_corner {
  position: absolute;
  width: 8px;
  height: 8px;
  opacity: 0;
  border: 2px solid gray;
}
.border-corner-top-left {
  border-bottom: none;
  border-right: none;
  top: 0;
  left: 0;
}
.border-corner-top-right {
  border-bottom: none;
  border-left: none;
  top: 0;
  right: 0;
}
.border-corner-bottom-left {
  border-top: none;
  border-right: none;
  bottom: 0;
  left: 0;
}
.border-corner-bottom-right {
  border-top: none;
  border-left: none;
  bottom: 0;
  right: 0;
}
.list-text:hover .border_corner {
  opacity: 1;
}
```
