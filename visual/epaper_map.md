# Peta

Komponen `map` untuk jenis visual `epaper` sama seperti pada jenis visual `map`. Yang membedakan hanyalah `tag` pembukanya sebagai berikut:

```xml
<map>

</map>
```

Tag pembuka `<chart>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut         | Tipe Nilai | Nilai Baku | Pilihan        | Keterangan                         |
| --------------- | ---------- | ---------- | -------------- | ---------------------------------- |
| title           | string     | _null_     | _null_         | Judul                              |
| subtitle        | string     | _null_     | _null_         | Subjudul                           |
| tracelog_time   | int        | 1          | 1;3;6;12;24;48 | Data histori (jam)                 |
| x               | int        | 0          | _null_         | Posisi x                           |
| y               | int        | 0          | _null_         | Posisi y                           |
| width           | int        | 0          | _null_         | Lebar komponen                     |
| height          | int        | 0          | _null_         | Tinggi komponen                    |
| decimal_default | int        | 2          | _null_         | Jumlah-angka baku di belakang koma |
