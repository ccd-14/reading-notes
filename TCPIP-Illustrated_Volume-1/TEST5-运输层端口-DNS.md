实验目的：通过主机PC2网页访问，了解涉及的协议

<div align=left><img width="400" height="400" src="./test-images/DNS-HTTP.PNG"/></div> 

1. PC2: 输入网址 www.porttest.com, 主机向DNS服务器发送一个**DNS查询报文**（根据网址获取目的IP地址）。使用UDP协议（源端口1029，**目的端口53**-DNS进程熟知端口），报文格式如下：
<div align=left><img width="550" height="700" src="./test-images/DNS1.PNG"/></div> 

2. DNS服务器：服务器回传一个响应报文，该报文中包含主机访问域名所对应的IP地址
<div align=left><img width="550" height="700" src="./test-images/DNS2.PNG"/></div> 

3. PC2: HTTP客户端给服务器发送一个HTTP请求。数据报中使用TCP协议（源端口1032，目的端口80-HTTP进程熟知端口）
<div align=left><img width="550" height="700" src="./test-images/HTTP1.PNG"/></div> 

4. HTTP服务器：给HTTP客户端回传一个HTTP响应报文
5. PC2: HTTP客户端接收到响应报文，在自身的浏览器中显示网页
