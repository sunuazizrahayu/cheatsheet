melihat informasi server
# server information

## masuk ke redis-cli
```redis
redis-cli -h localhost
```

# general
## server info
menampilkan semua info
```redis-cli
info
```

menampilkan sebagian info
```
# cmd
info <section>

# contoh, menampilkan memori
info memory
```

## config
```
config help

#contoh
config get <section>
```

contoh
```
#mengambil data sesuai redis.conf
config get *

#info db
config get databases
```

## slowlog
```
slowlog help
```


# client connection
```client list```

```client id```

```client kill <ip>:<port>```
