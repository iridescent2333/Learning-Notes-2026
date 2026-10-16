### 简要概念
- **Redis**，基于内存的key-value结构数据库，读写性能高，适合储存热点数据，处理短期的大量请求，对SQL的补充，[Redis中文网站](https://www.redis.net.cn/)
- 下载与安装，略，redis.conf，配置文件，redis-cli.exe，命令行，redis-server.exe，服务器，默认端口号6379，本地，连接云端，`redis-cli.exe -h localhost -p 6379 -a 123456`，默认没有配置密码，不需要用户名，设置密码，conf配置文件找到`# requirepass foobared`改为`requirepass 123456`
- 图形化界面，**Another Redis Desktop Manager**，熟悉基本使用
- Redis存储的是key-value结构的数据，其中key是字符串类型，value有5种常用的数据类型：字符串string，哈希hash，列表list，集合set，有序集合sorted set/zset，Redis有序集合是string类型元素的集合，且不允许有重复成员。每个元素都会关联一个double类型的分数，score大者在前
- 有效时间/秒，TTL，-ex，设置时间，-nx，不存在执行成功并返回1，列表头插入，双端队列，命令和SQL一样不区分大小写
### 常用命令

| 数据类型 | 常用命令1 | 常用命令2 | 常用命令3 | 常用命令4 | 常用命令5 | 常用命令6 |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| string（字符串） | `SET key value`<br>设置指定key的值 | `GET key`<br>获取指定key的值 | `SETEX key seconds value`<br>设置值并指定过期秒数 | `SETNX key value`<br>key不存在才设置 | — | — |
| hash（哈希） | `HSET key field value`<br>设置哈希表字段值 | `HGET key field`<br>获取哈希指定字段值 | `HDEL key field`<br>删除哈希指定字段 | `HKEYS key`<br>获取哈希所有字段名 | `HVALS key`<br>获取哈希所有字段值 | — |
| list（列表） | `LPUSH key value1 [value2]`<br>列表头部插入元素 | `LRANGE key start stop`<br>获取区间内元素 | `RPOP key`<br>移除并返回尾部元素 | `LLEN key`<br>获取列表长度 | — | — |
| set（集合） | `SADD key member1 [member2]`<br>添加集合成员 | `SMEMBERS key`<br>返回集合全部成员 | `SCARD key`<br>获取集合成员数量 | `SINTER key1 [key2]`<br>求集合交集 | `SUNION key1 [key2]`<br>求集合并集 | `SREM key member1 [member2]`<br>删除集合成员 |
| zset（有序集合） | `ZADD key score1 member1 [score2 member2]`<br>添加有序集合成员 | `ZRANGE key start stop [WITHSCORES]`<br>按索引区间查询 | `ZINCRBY key increment member`<br>成员分数增加增量 | `ZREM key member [member...]`<br>移除有序集合成员 | — | — |
| 通用命令 | `KEYS pattern`<br>按模式查找key | `EXISTS key`<br>检查key是否存在 | `TYPE key`<br>查看key存储类型 | `DEL key`<br>删除存在的key | — | — |

- 
