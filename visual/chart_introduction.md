# Apa itu Grafik?

Grafik (data _historian_), dalam konteks Visual Monita, merupakan halaman antarmuka yang menampilkan data-data _per request_ atau sekali waktu (tidak _realtime_). Tujuan dari jenis visual ini umumnya untuk menampilkan ringkasan dan/atau histori data pada periode tertentu. Kode tipe antarmuka ini adalah `chart`. Secara umum jenis visual ini serupa dengan jenis visual [`table`](table_introduction.md), yang membedakan hanyalah visual penyajian datanya.

#### Petunjuk penggunaan:

Berkas untuk jenis visual ini didefinisikan dengan membuat atribut `type` berisi nilai `chart` pada _root tag_ `monita`. Berikut contoh penggunaannya:

```xml
<monita type="chart"></monita>
```
