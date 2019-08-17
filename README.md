# clip
 Distributed memory synchronization

clip是做什么的？
------------------
clip是为了解决分布式内存一致性而产生

ELCP | Election | s| s| s| s| s|s | s| s|s
------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
head|sid|epoch|txid|type|elcepoch|lid|校验|s|s|s
2|8|2|2|1=1|4|8|2|s|s|s


First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column
