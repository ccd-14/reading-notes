# ARAP:逆地址解析协议
如果局域网中的主机只知道自己的MAC地址，不知道IP地址，可以通过ARAP协议发出广播请求，由ARAP服务器回答。
它是许多[无盘系统(https://baike.baidu.com/item/%E6%97%A0%E7%9B%98%E7%B3%BB%E7%BB%9F/10644051?fr=aladdin)在引导时用来获取IP地址。
## ARAP数据帧格式
与[ARP数据帧格式](chap4_ARP-protocol.md/#ARP数据帧格式)基本相同，主要区别在于：
- RARP请求或应答帧类型为0X8035;
- RARP请求的操作码为3，应答操作码为4；

ARP和RARP以**广播方式请求**，以**单播方式应答**。
