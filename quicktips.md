# Quick tips

1. Deleting all keys matching a pattern (prefix:...) in Redis

    `EVAL "return redis.call('del', unpack(redis.call('keys', ARGV[1])))" 0 prefix:*`
