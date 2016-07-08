---
title: Boostrap Popover弹出层div示例
categories: Tech
tags: [Boostrap,Popover]
date: 2016-07-07 17:48:55
---

为了将需求在模块中进行使用描述，所以想着在模块的部分区域提供`使用提示`的字样，来说明模块使用方法。可以更方便用户了解系统的使用操作，提高用户体验，也省的需求需求变更...

## 效果

鼠标移动到字样区域，显示使用说明。
![](http://7xncbk.com1.z0.glb.clouddn.com/16-7-7/39381463.jpg)

<!--more--> 

## 使用说明

使用了`bootstrap`的`tooltip`和`popover`js，请自行添加引用。

1. 设置好字样div的id和`data-placement`显示方向
2. 在js中绑定`.popover()`
3. 设置好`title`和`content`即可

## 代码

``` html
<html>
<head>
    <meta charset="utf-8"> 
    <link href="css/bootstrap.min.css" rel="stylesheet"> 

    <script src="js/jquery-1.9.1.js"></script>
    <script src="js/bootstrap-tooltip.js"></script>
    <script src="js/bootstrap-popover.js"></script>
    <script>
        var title = "个人日程操作提示";
        var content = "1.  添加,点击空白处操作;<br/>2. 编辑,点击已存在日程操作;<br/>3. 删除,在编辑框可选择操作;<br/>4. 拖拽与伸缩;对已存在日程可操作.";
        $(function ()
            { $("#tips").popover({title: title, content:content});
        });
    </script>
</head>

<body>
 <div href="javascript:void(0)" id="tips" class="btn btn-default" style="margin-left: 50%;" rel="popover" data-placement="bottom" >使用提示</div>
</body>
</html>

``` 
