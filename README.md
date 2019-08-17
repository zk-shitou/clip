# clip
 Distributed memory synchronization

## clip是做什么的？
clip是为了解决分布式内存一致性而产生，clip各个节点基于JAVA NIO相互通信，协议如下：

### ELCP
head|sid|epoch|txid|type|elcepoch|lid|校验
----|----|----|----|----|----|----|----
2|8|2|2|1=1|4|8|2

### INCP
head|sid|epoch|txid|type|sourceType|len|data|校验
----|----|----|----|----|----|----|----|----
2|8|2|2|1=2|1|2|...|2

### FSNCP
head|sid|epoch|txid|type|sourceType|count|index|len|data|校验
----|----|----|----|----|----|----|----|----|----|----
2|8|2|2|1=3|1|1|1|2|...|2

### HBP
head|sid|epoch|txid|type|校验
----|----|----|----|----|----
2|8|2|2|1=4|2

### FSSEP
head|sid|epoch|txid|type|subtype(0开始/1结束)|len|data|校验
----|----|----|----|----|----|----|----|----
2|8|2|2|1=5|1|2|...|2
