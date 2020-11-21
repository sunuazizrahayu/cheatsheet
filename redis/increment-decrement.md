membuat data seperti AI

| Operasi | Keterangan | contoh |
|---------|------------|--------|
|incr `<key>`|menambahkan data 1 by 1| |
|decr `<key>`|
|incrby `<key>` `<jumlah angka yang akan ditambah>`| menaikkan data sesuai jumlah value | incrby counter 10 |

# manual (not recommended)
| Operasi | Keterangan | contoh |
|---------|------------|--------|
| value = GET `<key>` | | |
| value = value + 1 | | |
| set `<key>` value | | |
