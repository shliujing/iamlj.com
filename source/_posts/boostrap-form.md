---
title: Boostrap Form表单的一列两列布局
categories: Tech
tags: [Boostrap,Form]
date: 2016-07-07 17:48:55
---

Bootstrap基础的两列、一列、居中按钮的布局。
可以自行扩展，根据需要做一些页面的详情页的两列排版，非常简洁美观。

## 效果

![](http://7xncbk.com1.z0.glb.clouddn.com/16-7-7/70738442.jpg)

<!--more--> 

## 代码

``` html
<html>
<head>
    <title>Bootstrap Form Demo</title>
    <meta http-equiv="content-type" content="text/html; charset=utf-8"/>
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="./css/bootstrap.min.css" rel="stylesheet">
</head>
<style type="text/css">
    #projectArea {
        width: 90%;
        margin-left: 5%;
        height: 200px
    }

    #projectTitle {
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
    }

    #progressStatus {
        text-align: right;
        margin-right: 1%;
    }

    .progress {
        margin-bottom: 5px;
    }

    a, a:link, a:active, a:hover, a:visited {
        text-decoration: none;
    }

    a:focus {
        outline: none;
    }
</style>
<body>

<div id="projectArea" class="center">
    <div id="projectItem">
        <div id="projectTitle">
            <a style="color: black;"
               href="">基于数据挖掘的信息采集基于数据挖掘的信息采集基于数据挖基于数据挖掘的信息采集基于数据挖掘的信息采集基于数据挖
            </a>
        </div>

        <div id="progress" class="inline progress">
            <div id="progressBar" class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="20"
                 aria-valuemin="0" aria-valuemax="100" style="width: 45%">45
            </div>
            <div id="progressStatus">新建</div>
        </div>
    </div>

    <div id="projectItem">
        <div id="projectTitle">
            <a style="color: black;"
               href="">这是个测试
            </a>
        </div>

        <div id="progress" class="inline progress">
            <div id="progressBar" class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="20"
                 aria-valuemin="0" aria-valuemax="100" style="width: 95%">95
            </div>
            <div id="progressStatus">处理中</div>
        </div>
    </div>
</div>
</body>
</html>
``` 
