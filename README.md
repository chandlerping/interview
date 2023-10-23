# interview
## 计算机网络
### Q&A
#### 1. TIME_WAIT状态过多？
原因：大量并发短连接（HTTP connection头部被设为close），由【服务端】主动发起关闭连接；因此服务端大量端口会被占据，2MSL=4min。会占用大量TCP端口（共65535个）。

解决方案：
  * 客户端：HTTP头connection设置为keep-alive（长连接，通常由客户端关闭连接），避免短时间内大量出现TIME_WAIT。
  * 服务端：多个socket复用端口/连接；缩短TIME_WAIT时间为1MSL。


## LC
### 双指针
611: https://leetcode.com/problems/valid-triangle-number/

15: https://leetcode.com/problems/3sum/
