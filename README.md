# redis-dbrestore 工具

1. redis-dbrestore是用shell编写的，用来在线迁移redis数据的工具。
2. 可以实现redis源实例dbX迁移至目标实例dbY.

## 安装redis-dbrestore

```bash
wget -O /usr/local/bin/redis-dbrestore https://raw.githubusercontent.com/Vastxiao/redis-dbrestore/master/redis-dbrestore
chmod +x /usr/local/bin/redis-dbrestore
```

## redis-dbrestore 工具使用

**帮助信息:**

```
Usage: redis-dbrestore [OPTIONS...]

  OPTION:
    --help, -h          help msg.
    --src-host HOST     default: 127.0.0.1
    --src-port PORT     default: 6379
    --src-auth PASS
    --src-db DB         default: 0
    --src-keys KEYS

    --dst-host HOST     default: 127.0.0.1
    --dst-port PORT     default: 6379
    --dst-auth PASS
    --dst-db DB         default: 0
```

**用法实例:**

```bash
# 查看命令帮助:
redis-dbrestore -h

# 进行数据迁移
redis-dbrestore --src-host 192.168.1.2 --src-db 0 --dst-host 192.168.3 --dst-db 1
```
