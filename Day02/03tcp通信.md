# TCP特点

### 1.面向连接

通信双方必须先建立才能进行数据的传输,双方都必须为该连接分配必要的系统内核资源,一贯李连杰的状态和连接上的传输.

双方间的数据传输都可以通过一个连接进行

完成数据交换后,双方必须断开此连接,以释放系统资源.

这种连接是一对一的,因此TCP不适用于广播的应用程序,基于广播的应用程序请使用UDP协议.

### 2.可靠性

#### 	1.tcp采用发送应答机制

​		TCP发送的每个报文段都必须得到对方的应答才认为这段tcp报文段传输成功

#### 	2.超时重传

​		发送端发出一个报文段之后就会启动定时器,如果在定时时间内没有收到应答就重新发送这段报文

​		TCP为了保证不发生丢包,就给每一个包一个序号,同时也保证了传送到接收端实体的包按序接收,然后接收端实体对已经成功收到的包发回一个相应的确认(**ACK**);如果发送端实体在合理的往返时延(**RTT**)内未收到确认,那么对应的数据包就被假设为已丢失将会被重新重传

#### 	3.错误校验

​		TCP用一个校验函数来检验数据是否有错误,在发送和接受时都要计算校验和.

#### 	4.流量控制和阻塞管理

​		流量控制避免主机发送得过快而使接收方来不及接收 

### 3.TCP与UDP的不同点

- <u>面向连接(确认有创建三方交握,连接已创建才传输.</u>

- <u>有序数据传输</u>

- <u>重发丢失的数据包</u>

- <u>舍弃重复的数据包</u>

- <u>无差错的数据传输</u>

- <u>阻塞/流量控制</u>

  

	## 4.UDP通信模型	

		udp通信模型中,在同学开始之前不需要建立相关的链接,只需要发送数据即可.



![02-就业班-02-1](D:\随笔\复习\Day02\素材\02-就业班-02-1.jpg)



### 5.TCP通信模型

​	udp通信模型中,在通信开始之前,一定要建立相关的链接,才能收发数据,例如打电话



![02-就业班-02-12](D:\随笔\复习\Day02\素材\02-就业班-02-12.png)