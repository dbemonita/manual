# Apa itu THMI?

THMI (_Table-based_ HMI), dalam konteks Visual Monita, merupakan halaman antarmuka yang menampilkan data-data _realtime_ dalam bentuk tabel. Tujuan dari jenis visual ini adalah untuk menyederhanakan tampilan data secara _compact_ terhadap data-data yang dapat dikelompokkan. Kode tipe antarmuka ini adalah `thmi`. Jenis visual ini sudah mendukung `rowspan` dan `colspan` seperti laiknya tabel pada HTML.

#### Petunjuk penggunaan:

Berkas untuk jenis visual ini didefinisikan dengan membuat atribut `type` berisi nilai `thmi` pada _root tag_ `monita`. Berikut contoh penggunaannya:

```xml
<monita type="thmi"></monita>
```
