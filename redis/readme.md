## konek redis server
```
redis-cli -h <host> -p <port>
```

## operasi database
| Operasi | Contoh | Keterangan |
|---------|------------|------------|
| select `<nomor database>`|  select 0 |memilih nomor dari database|

### strings
| Operasi | Contoh | Keterangan |
|---------|------------|------------|
| set `<key>` `<value>`| set name sunu |gunakan _double quotes_ pada _key_ ataupun _value_ kalau memiliki spasi|
| | set name "kang sunu"| |
| | set "full name" "kang sunu"||
