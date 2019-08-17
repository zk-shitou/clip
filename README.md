# clip
 Distributed memory synchronization

clip是做什么的？
------------------
clip是为了解决分布式内存一致性而产生

ELCP|Election
------|------|------|------|------|------|------|------|------|------|------|
head|sid|epoch|txid|type|elcepoch|lid|校验
2|8|2|2|1=1|4|8|2|
