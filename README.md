# redis-dbrestore 工具

1. redis-dbrestore是用shell编写的，用来在线迁移redis数据的工具。
2. 可以实现redis源实例dbX迁移至目标实例dbY.

## 安装redis-dbrestore

```bash
wget -O /usr/local/bin/redis-dbrestore https://raw.githubusercontent.com/Vastxiao/redis-dbrestore/master/redis-dbrestore
chmod +x /usr/local/bin/redis-dbrestore
```

## redis-dbrestore 工具使用

```bash
# 查看命令帮助:
redis-dbrestore -h

# 进行数据迁移
redis-dbrestore --src-host 192.168.1.2 --src-db 0 --dst-host 192.168.3 --dst-db 1
```
