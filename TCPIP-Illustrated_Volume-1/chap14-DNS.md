## DNS:域名系统
DNS是一种用于TCP/IP应用程序的分布式数据库，提供主机名字和IP地址之间的转换功能。在一个应用程序请求建立TCP连接或UDP发送数据报之前，必须将主机名转换为一个IP地址。对DNS的访问是通过地址解析器完成，主要通过两个库函数访问:
- gethostbyname(3):接收到主机名字返回IP地址；
- gethostbyaddr(3):接收IP地址返回主机名字。

## DNS报文格式
报文由12个字节长的首部和4个长度可变的字段组成。
<div align=left><img width="520" height="150" src="./images/DNS报文.JPG"/></div>

其中：
- 标识字段：