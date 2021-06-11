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


