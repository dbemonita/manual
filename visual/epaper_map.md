# Peta

Komponen `map` untuk jenis visual `epaper` sama seperti pada jenis visual `map`. Yang membedakan hanyalah `tag` pembukanya sebagai berikut:

```xml
<map>

</map>
```

Tag pembuka `<chart>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut         | Tipe Nilai | Nilai Baku | Pilihan        | Keterangan                         |
| --------------- | ---------- | ---------- | -------------- | ---------------------------------- |
| title           | string     |            |                | Judul                              |
| subtitle        | string     |            |                | Subjudul                           |
| tracelog_time   | int        | 1          | 1;3;6;12;24;48 | Data histori (jam)                 |
| x               | int        | 0          |                | Posisi x                           |
| y               | int        | 0          |                | Posisi y                           |
| width           | int        | 0          |                | Lebar komponen                     |
| height          | int        | 0          |                | Tinggi komponen                    |
| decimal_default | int        | 2          |                | Jumlah-angka baku di belakang koma |
