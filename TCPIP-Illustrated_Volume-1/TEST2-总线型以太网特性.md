总线型以太网存在以下特性： 广播、竞争总线、冲突  

实验初始状态下，已更新各主机的ARP缓存表，所以不会发送ARP请求/响应报文。  
**同时**让PC4和PC7发送PDU至PC6，发现在集线器处发生**竞争冲突**。  
<div align=left><img width="700" height="280" src="./test-images/实验-总线型以太网1.png"/></div> 


接下来，集线器将碰撞帧以 **广播** 的形式发送至各个端口。各端口相连的主机接收到碰撞帧，会将其丢弃。
 <div align=left><img width="700" height="280" src="./test-images/实验-总线型以太网2.png"/></div> 