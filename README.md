# interview
```
       _____    __   ____
 ___  / /\ \  /  \  / /
  \ \/ /  \ \/ /\ \/ /
   \__/    \__/  \__/
```
## 数据库
#### 1-如何优化索引？
1. 对常用字段建立索引，选择区分度大的字段
2. 前缀索引
3. 覆盖索引
4. 主键自增
5. 防止索引失效（or非索引列、联合索引非最左匹配、对索引列计算或函数、查询数据范围过大）
#### 2-如何优化SQL语句？



## 计算机网络
#### 1-TIME_WAIT状态过多？
原因：大量并发短连接（HTTP connection头部被设为close），由【服务端】主动发起关闭连接；因此服务端大量端口会被占据，2MSL=4min。会占用大量TCP端口（共65535个）。

解决方案：
  * 客户端：HTTP头connection设置为keep-alive（长连接，通常由客户端关闭连接），避免短时间内大量出现TIME_WAIT。
  * 服务端：多个socket复用端口/连接；缩短TIME_WAIT时间为1MSL。


## LC
#### 双指针
611: https://leetcode.com/problems/valid-triangle-number/

15: https://leetcode.com/problems/3sum/

#### 哈希
1224：https://leetcode.com/problems/maximum-equal-frequency/

#### 01背包
416：https://leetcode.com/problems/partition-equal-subset-sum/

518：https://leetcode.com/problems/coin-change-ii/

474：https://leetcode.com/problems/ones-and-zeroes/
