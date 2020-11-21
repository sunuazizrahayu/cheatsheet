melihat informasi server

## masuk ke redis-cli
```redis
redis-cli -h localhost
```

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
```

contoh
```
#mengambil data sesuai redis.conf
config get *

#info db
config get databases
```

# slowlog
```
slowlog help
```
