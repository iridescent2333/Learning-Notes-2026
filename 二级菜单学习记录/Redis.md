### 简要概念
- **Redis**，基于内存的key-value结构数据库，读写性能高，适合储存热点数据，处理短期的大量请求，对SQL的补充，[Redis中文网站](https://www.redis.net.cn/)
- 下载与安装，略，redis.conf，配置文件，redis-cli.exe，命令行，redis-server.exe，服务器，默认端口号6379，本地，连接云端，`redis-cli.exe -h localhost -p 6379 -a 123456`，默认没有配置密码，不需要用户名，设置密码，conf配置文件找到`# requirepass foobared`改为`requirepass 123456`
- 图形化界面，**Another Redis Desktop Manager**，基本使用
- Redis存储的是key-value结构的数据，其中key是字符串类型，value有5种常用的数据类型：字符串string，哈希hash，列表list，集合set，有序集合sorted set/zset
### 常用命令
- #### 字符串string
`SET key value`设置指定key的值，`GET key`获取指定key的值，`SETEX key seconds value`设置指定key的值，并将key的过期时间设为seconds秒，`SETNX key value`只有在key不存在时设置key的值
- #### 哈希hash
`HSET key field value`将哈希表key中的字段 field 的值设为value，`HGET key field`获取存储在哈希表中指定字段的值，`HDEL key field`删除存储在哈希表中的指定字段，`HKEYS key`获取哈希表中所有字段，`HVALS key`获取哈希表中所有值
- #### 列表list
`LPUSH key value1 [value2]`将一个或多个值插入到列表头部，`LRANGE key start stop`获取列表指定范围内的元素，`RPOP key`移除并获取列表最后一个元素，`LLEN key`获取列表长度
- #### 集合set
`SADD keymember1[member2]`向集合添加一个或多个成员，`SMEMBERS key`返回集合中的所有成员，`SCARD key`获取集合的成员数，`SINTER key1 [key2]`返回给定所有集合的交集，`SUNION key1 [key2]`返回所有给定集合的并集，`SREM key member1 [member2]`删除集合中一个或多个成员
- #### 有序集合zset
`ZADD key score1 member1 [score2 member2]`向有序集合添加一个或多个成员，`ZRANGE key start stop [WITHSCORES]`通过索引区间返回有序集合中指定区间内的成员，`ZINCRBY key increment member`有序集合中对指定成员的分数加上增量，`incrementZREM key member [member...]`移除有序集合中的一个或多个成员
- #### 通用命令
`KEYS pattern`查找所有符合给定模式(pattern)的key，`EXISTS key`检查给定 key是否存在，`TYPE key`返回key所储存的值的类型，`DEL key`该命令用于在key存在是删除key
