<a href="https://github.com/ProgrammerZamanNow/belajar-redis" target="_blank">reference</a>


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
| append `<key>` `<value>` | append name " aziz" | menambahkan data di belakang data yang sudah ada|
| get `<key>`|get name|mengambil data|
| | | - dari contoh akan menampilkan _sunu_|
| | | - bila data tidak ada, akan menampilkan _(nil)_|
|exist `<key>`| exist name | mengecek apakah suatu key memiliki value, response berbentuk integer 0 atau 1|
| | | - *0* tidak ada data|
| | | - *1* ada data|
|keys `<pattern>` | keys `*name` | mencari keys yang ada berdasarkan _pattern_|
||| mengambil data dengan keys yang berakhiran _name_ |
|del `<key>` `<key...>`|del name "full name"|hapus data, menghapus data _*name*_ dan *_full name_*|

#### strings range
|Operasi|keterangan|contoh|hasil|
|---|---|---|---|
|setrange `<key>` `<offset>` `<value>` | overwrite data yang sudah ada dari index offset | setrange name 0 aziz | aziz aziz |
|getrange `<key>` `<start>` `<end>` | seperti fungsi _*substr*_, mengambil data sebagian | getrange name 0 2 | sun |

#### multile string
| Operasi | keterangan | contoh |
|---|---|---|
| mget `<key1>` `<key2>` `<...>` | mengambil beberapa data sekaligus | mget name "full name"|
|mset `<key1>` `<value1>` `<key2> <value2>` ... | set data sekaligus | mset name sunu middle aziz last rahayu|

### menghapus data semua data (flush)
| Operasi | Keterangan |
|---------|------------|
|flushdb | menghapus data di database yang sekarang digunakan|
|flushall | menghapus semua data di semua databasee|



## pipeline
digunakan untuk mengirim data ke redis sekaligus, seperti bulk/batch
```
# command
redis-cli --pipe


# example
cat daftar-command-set-di-redis.txt | redis-cli -h localhost --pipe
```
