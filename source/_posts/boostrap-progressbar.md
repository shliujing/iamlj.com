---
title: Boostrap ProgressBar进度条的布局
categories: Tech
tags: [Boostrap,ProgressBar]
date: 2016-07-07 17:48:55
---

Bootstrap基础的进度条的布局，应用在项目进度的显示上。大家可以根据需要自行扩展。

主要解决了每项的__标题、进度条、状态显示的排版，内联，文字溢出__的问题。整体上还是比较简洁美观的。

## 效果

![](http://7xncbk.com1.z0.glb.clouddn.com/16-7-8/41033631.jpg)

<!--more--> 

## 代码

请自行添加`Bootstrap`的css引用。

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
                 aria-valuemin="0" aria-valuemax="80" style="width: 80%">95
            </div>
            <div id="progressStatus">处理中</div>
        </div>
    </div>
</div>
</body>
</html>
``` 
