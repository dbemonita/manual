# Apa itu E-paper?

E-paper, dalam konteks Visual Monita, merupakan halaman antarmuka yang menampilkan data-data _per request_ atau sekali waktu (tidak _realtime_). Jenis visual ini dapat dikatakan sebagai gabungan dari jenis visual [`hmi`](hmi_introduction.md) dan [`table`](table_introduction.md) Tujuan dari jenis visual ini umumnya untuk menampilkan ringkasan dan/atau histori data pada periode tertentu, untuk keperluan laporan tercetak. Fitur utama dari jenis visual ini adalah generator PDF dengan ukuran kertas A4, letter, dan legal. Kode tipe antarmuka ini adalah `epaper`.

#### Petunjuk penggunaan:

Berkas untuk jenis visual ini didefinisikan dengan membuat atribut `type` berisi nilai `epaper` pada _root tag_ `monita`. Berikut contoh penggunaannya:

```xml
<monita type="epaper"></monita>
```
