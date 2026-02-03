# Apa itu Tabel?

Tabel (data _historian_), dalam konteks Visual Monita, merupakan halaman antarmuka yang menampilkan data-data _per request_ atau sekali waktu (tidak _realtime_). Tujuan dari jenis visual ini umumnya untuk menampilkan ringkasan dan/atau histori data pada periode tertentu. Kode tipe antarmuka ini adalah `table`. Jenis visual ini sudah mendukung `rowspan` dan `colspan` seperti laiknya tabel pada HTML. Namun perlu diperhatikan bahwa `table` pada Visual Monita berbeda dengan `table` pada HTML.

#### Petunjuk penggunaan:

Berkas untuk jenis visual ini didefinisikan dengan membuat atribut `type` berisi nilai `table` pada _root tag_ `monita`. Berikut contoh penggunaannya:

```xml
<monita type="table"></monita>
```
