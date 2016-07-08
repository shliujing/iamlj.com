---
title: Javascript性能优化
categories: Tech
tags: [Javascript,Optimization]
date: 2016-07-08 09:14:30
---

这是一道Javascript的性能优化，来自大陆集团的开放性试题。总共8题，有`C、Android、Java、Javascript`，我为了赶时间，挑了最简单的`Javascript`。

这里主要是取代采用了事件委托来绑定父节点ul的事件侦听，提高性能。
{% fi http://7xncbk.com1.z0.glb.clouddn.com/16-7-8/94559498.jpg %}

<!--more-->     

## 原题

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>性能优化</title>
    <style>
     #action-list li {
        padding: 10px 15px;
        cursor: pointer;
     }
    </style>
</head>
<body>
    <h2>点击以下做出相应的动作<h2>
    <ul id="action-list">
        <li id="action-a">页面输入hello world</li>
        <li id="action-b">页面弹出hello world</li>
        <li id="action-c">页面确认hello world</li>
    </ul>
    <script>
        var actionA = document.getElementById("action-a");
        actionA.addEventListener("click", function(){
            prompt("输入Hello World：");
        });
        var actionB = document.getElementById("action-b");
        actionB.addEventListener("click", function(){
            alert("Hello World");
        });
        var actionC = document.getElementById("action-c");
        actionC.addEventListener("click", function(){
            confirm("Hello World");
        });
    </script>
</body>
</html>
``` 

## 解题

这里采用事件委托，将在li对象上面要处理的事件委托给父元素或者祖先元素，即为父元素绑定事件侦听。
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>性能优化</title>
    <style>
        #action-list li {
            padding: 10px 15px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h2>点击以下做出相应的动作</h2>
    <ul id="action-list">
        <li id="action-1">页面输入hello world</li>
        <li id="action-2">页面弹出hello world</li>
        <li id="action-3">页面确认hello world</li>
    </ul>
    <script type="text/javascript">
        (function () {
            var a = document.getElementById('action-list');
            a.addEventListener('click', function (e) {
                var b = e.target;
                var idNum = b.id.substring(7);
                doEvent(idNum);
            }, false);
        })();

        function doEvent(idNum) {
            switch (true) {
                case idNum == 1:
                prompt("输入Hello World：");
                break;

                case idNum == 2:
                alert("Hello World");
                break;

                default:
                confirm("Hello World");
                break;
            }
        }
    </script>
</body>
</html>
``` 