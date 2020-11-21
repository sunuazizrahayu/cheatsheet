otomatisasi hapus data

| Operasi | Keterangan | contoh |
|---------|------------|--------|
| expire `<key>` `<seconds>` | setting expire data yang sudah ada dalam detik | expire name 5| 
| setex `<key>` `<seconds>` `<value>` | setting key value langsung dengan expire |
| ttl `<key>` | cek sisa expire | ttl name|
| | bila ttl menghasilkan *-1*, maka artinya datanya permanent | |
