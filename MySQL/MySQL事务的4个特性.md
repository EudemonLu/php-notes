# MySQL事务的4个特性

什么是事务?
```
事务是针对数据库的一组操作, 由一条或多条sql组成, 事务中的sql要么都执行, 要么都不执行
```

事务的4个特性(ACID)?
```
事务必须同时满足4个特性: 原子性(Atomicity)、一致性(Consistency)、隔离性(Isolation)、持久性(Durability)

# 原子性
原子性指一个事务必须不可分割, 只有事务中所有操作都执行成功, 才算整个事务执行成功.
如果事务中有任何sql执行失败, 已经执行成功的sql也必须撤销.

# 一致性
一致性指事务执行结束后, 数据库的完整性约束没有被破坏, 事务执行的前后都是合法的数据状态.
数据的完整性约束包括:
    实体完整性(如行的主键存在且唯一)
    列完整性(如字段的类型/大小/长度符合要求)
    外键约束
    用户自定义完整性(如转账前后的两个账户余额和保持不变)
    
# 隔离性
多个并发事务之间互不干扰, 相互隔离.

# 持久性
事务一旦提交, 其所做的修改就会永久保存到数据库中, 即使数据库发生故障也不会对其有任何影响.
```

