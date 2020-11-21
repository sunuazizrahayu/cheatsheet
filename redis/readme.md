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
| | set "name full" "kang sunu"||
| append `<key>` `<value>` | append name " aziz" | menambahkan data di belakang data yang sudah ada|
| get `<key>`|get name|mengambil data|
| | | - dari contoh akan menampilkan _sunu_|
| | | - bila data tidak ada, akan menampilkan _(nil)_|
|exist `<key>`| exist name | mengecek apakah suatu key memiliki value, response berbentuk integer 0 atau 1|
| | | - *0* tidak ada data|
| | | - *1* ada data|
|keys `<pattern>` | keys name* | mengambil data berdasarkan _pattern_|
||| mengambil data dengan keys yang berawalan _name_ |
|del `<key>` `<key...>`|del name "full name"|hapus data, menghapus data _*name*_ dan *_full name_*|
