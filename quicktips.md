# Quick tips

1. Deleting all keys which match a pattern: 
```EVAL "return redis.call('del', unpack(redis.call('keys', ARGV[1])))" 0 prefix:*```
