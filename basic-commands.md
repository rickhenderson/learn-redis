# Basic Commands in Redis

Since Redis is an in-memory database that stores (primarily) *key-value* pairs, the most basic of commands (other than `ping`) are `set` and `get` to store and retrieve simple string and number values.

```redis
set message 'Hey, dude!'
get message
```

## Searching for Items - Checking Keys

Don't use the `keys` command. It blocks the server which is sub-optimal.

```
scan cursor [MATCH pattern] [COUNT count] [TYPE type]
````
`cursor` is an integer value of the database cursor position to start scanning from.

### List the keys

```redis
scan 0
```

### Search for values

```redis
scan 0 MATCH "rules*"
```

# References

Most of this information comes from Stephen Grider's [Redis:The Complete Developer's Guide](https://www.udemy.com/course/redis-the-complete-developers-guide-p/) course on Udemy.

* <https://www.udemy.com/course/redis-the-complete-developers-guide-p/>
* <https:redis.io/commands>
