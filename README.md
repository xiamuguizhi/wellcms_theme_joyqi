## wellcms介绍

WellCMS 是一款具备亿级负载、开源、倾向移动端、轻量级、具有超快反应能力的高负载CMS，是大数据量、高并发访问网站最佳选择的轻CMS。wellcms具有安全、高效、稳定、速度超快、负载超强的特点。是大数据时代下诞生的CMS，低成本解决网站负载和性能问题，专为大数据量站点设计的高性能、高负载的CMS。前后台均可在移动端操作，自适应手机、平板、PC，也可以设置各端加载单独模板，并且URL保持不变，有着非常方便的插件机制。前台部分页面配备API，可通过JSON返回AJAX请求的数据，方便 APP 开发。

## 关于主题

原先有人在群里给我推荐了wellcms这个程序，我一看介绍这也太6了吧，一下就喜欢上了这个程序。但是这个程序的模板是cms方向的虽然也有一些博客模板但是不适合我，我喜欢极简的主题，于是我移植了joyqi.com的主题到wellcms。虽然过程曲折，但是被我甲基吧扯搞成功了 哈哈哈

 - 优化seo标题分页一些地方
 - 简化搜索页面

## 下载

Github：[https://github.com/xiamuguizhi/wellcms_theme_joyqi](https://github.com/xiamuguizhi/wellcms_theme_joyqi)


## 要修改的地方

修改一：

`joyqi/html/header.html`

修改 53行 这里为首页描述

修改二：

评论注册页面

`joyqi/html/read.html`

62/63 行的 `http://192.168.0.111/` 修改为你自己的网站地址

修改三：

全站404错误页面

根目录`/view/htm/message.htm`

```html
<!DOCTYPE HTML>  
<html>  
<head>  
<meta charset="UTF-8" />  
<meta name="viewport" content="width=device-width, initial-scale=1">  
<meta name="robots" content="none" />  
<title>404 Not Found</title>  
<style>  
body {
    background: #F7F7F7;
    font-size: 16px;
    font-family: 'Avenir Next',Avenir,'Helvetica Neue',Helvetica,'Lantinghei SC','Hiragino Sans GB',sans-serif;
    padding: 0;
    margin: 0;
    letter-spacing: 1px;
}
*{font-family:"Microsoft Yahei";margin:0;font-weight:lighter;text-decoration:none;text-align:center;line-height:2.2em;}  
html,body{height:100%;}  
h1{font-size:100px;line-height:1em;}  
table{width:100%;height:100%;border:0;}  
</style>  
</head>  
<body>  
<table cellspacing="0" cellpadding="0">  
<tr>  
<td>  
<table cellspacing="0" cellpadding="0">  
<tr>  
<td>  
<h1>404</h1>  

<h3>大事不妙啦！</h3>  
<p>
    <?php 
    
    
        $str = $_SERVER["QUERY_STRING"].""; 
    
        if(strpos($str,'comment-create')!==false){
            echo '请认真输入内容，在点击回复哦～<br/>';
    
        }else if(strpos($str,'list-')!==false){
    
            echo '这个栏目还没创建诶～<br/>'; 
       
    
        }else if(strpos($str,'read-')!==false){
    
            echo '作者好像没有写过这篇文章,呜呜～<br/>'; 
       
        }else{
    
        echo '竟然被你发现了我的宝藏吗？害怕！！！<br/>'; 
    
        }
    
    
    ?>

<a href="javascript:history.go(-1);">返回页面 ></a>  

</p>  
</td>  
</tr>  
</table>  
</td>  
</tr>  
</table>  
</body>  
</html>  


```

## 预览

测试站：9i3.cn

- 首页

![screencapture-9i3-cn-2020-12-28-13_05_02.png](https://i.loli.net/2020/12/28/WqHuxaBI1mwUQ9Z.png)



- 文章页

![image.png](https://i.loli.net/2020/12/28/SosZRAfFW1aw2y8.png)


