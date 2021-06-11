实验目的：通过主机PC2网页访问，了解涉及的协议

<div align=left><img width="400" height="400" src="./test-images/DNS-HTTP.PNG"/></div> 

1. PC2: 输入网址 www.porttest.com，主机向DNS服务器发送一个DNS查询报文（根据网址获取目的IP地址）。使用UDP协议（源端口1029，**目的端口53**-DNS进程熟知端口），报文格式如下：
<div align=left><img width="500" height="700" src="./test-images/DNS1.PNG"/></div> 

2. DNS服务器：服务器回传一个响应报文，该报文中包含主机访问域名所对应的IP地址
<div align=left><img width="500" height="700" src="./test-images/DNS2.PNG"/></div> 
