## ping程序
**ping进程主要用于描述 到目标主机 网络是否通畅。**
<div align=left><img width="800" height="300" src="./test-images/实验-ICMP.PNG"/></div> 

通过命令单步仿真ICMP报文传输过程：
1. 主机PC0发送ICMP请求报文，输出格式如下：
1.1  PING进程开始下一个PING请求。
1.2  PING进程创建了一个ICMP“回送请求”报文并将其传递给下层进程。
1.3  源IP地址未指定。设备将其设置为该端口的IP地址。
1.4  目的IP地址与源IP地址不在同一子网，并且不是一个广播地址。
1.5  默认网关已设置。设备设置下一跳为默认网关。
<div align=left><img width="500" height="600" src="./test-images/ping1.PNG"/></div> 


2. PC1接收到ICMP请求报文后，需要回传一个ICMP响应报文
2.1 ICMP进程通过将ICMP类型字段设置为“回送回答”以响应“回送请求”报文。
2.2 ICMP进程发送了一个“回送回答”响应报文。
2.3 目的IP地址与源IP地址不在同一子网，并且不是一个广播地址。
2.4 默认网关已设置。设备设置下一跳为默认网关。
<div align=left><img width="500" height="600" src="./test-images/ping2.PNG"/></div> 

ping进程一般会进行连续四次的探测，命令结果如下：
<div align=left><img width="400" height="300" src="./test-images/ping3.PNG"/></div> 

## tracert程序
**tracert进程主要用于描述 从源主机到目的主机结果的路由器情况**。具体仿真过程如下：
1. PC0发送一个ICMP请求报文，该报文中“TTL=1” ：
1.1 Trace route进程启动下一个追踪。
1.2 Trace route进程创建一个ICMP“回送请求”报文并将其发送给下一层进程。
1.3 源IP地址未指定。设备将其设置为该端口的IP地址。
1.4 设备设置数据包首部的**TTL字段**。
1.5 目的IP地址与源IP地址不在同一子网，并且不是一个广播地址。
1.6 默认网关已设置。设备设置下一跳为默认网关。
<div align=left><img width="500" height="600" src="./test-images/tracert1.PNG"/></div> 

2. 当ICMP请求报文到达路由器0时，**TTL=0**。此时，路由器会发送PC0一个“超时”的ICMP错误报文。PC0接收到报文后根据源IP地址判断经过的第一个路由器。
<div align=left><img width="500" height="600" src="./test-images/tracert2.PNG"/></div> 

3. 主机PC0再次发送“TTL=2”的ICMP请求报文，超时后获得第二个经过的路由器信息，以此类推。

最终，命令结果如下（每个TTL会重复发三次）：
<div align=left><img width="400" height="300" src="./test-images/tracert3.PNG"/></div> 
