<div align=left><img width="900" height="580" src="./test-images/IP协议转发过程.PNG"/></div> 

PC0 -----> PC2 通信过程如下：
1. PC0:根据目的IP地址查询路由表（将目的IP地址与本机子网掩码相与，若和本机IP地址与本机子网掩码相与 结果相同，则是处于同一网络中，**直接交付**），发现目的主机不在该网络中，主机PC0将