通过 cisco packet tracer计算机网络仿真软件模拟数据包在网络拓扑中的传输过程。本例中，将两个PC的端口直连，PC4向PC6发送PDU（数据协议单元）。初始状态下，两台主机的MAC地址表均为空。因此，首先需要发送ARP请求数据包，更新MAC地址表。  

<div align=left><img width="400" height="180" src="./test-images/实验-ARP-1.png"/></div> 

总过程如下：
1. ICMP请求
各层传输过程：
<div align=left><img width="600" height="220" src="./test-images/实验-ARP-2.png"/></div> 

数据报封装格式：
<div align=left><img width="400" height="420" src="./test-images/实验-ARP-3.png"/></div> 

2. ARP请求
<div align=left><img width="500" height="220" src="./test-images/实验-ARP-4.png"/></div> 
