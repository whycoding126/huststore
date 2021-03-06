Test
--

All the below scripts rely on [requests](https://github.com/request/request).

### Script for automatic test ###

Path: `hustdb/ha/nginx/test/autotest.py`

    usage:
        python autotest [uri] [action]
            [uri]
                uri: ip:port
            [action]
                put | get | get2 | del | exist |
                hset | hget | hget2 |hdel | hexist |
                sadd | srem | sismember | sismember2 |
                zadd | zrem | zismember | zscore | zscore2 |
                cache_exist | cache_get | cache_ttl | 
                cache_put | cache_append | cache_del | cache_expire |
                cache_hexist | cache_hget | cache_hset | cache_hdel |
                cache_hincrby | cache_hincrbyfloat |
                stat_all | sync_status | sync_alive | get_table | loop
    sample:
        python autotest.py localhost:8082 loop
        python autotest.py localhost:8082 stat_all
        python autotest.py localhost:8082 sync_status

### Script for stress test ###

Path: `hustdb/ha/nginx/multi_test.py`

    usage:
        python multi_test [number] [uri]
            number : number of process
            uri    : ip:port
    sample:
        python multi_test.py 2 localhost:8082

[Previous](../ha.md)

[Home](../../index.md)