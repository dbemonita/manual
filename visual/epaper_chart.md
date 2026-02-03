# Grafik

Komponen `chart` untuk jenis visual `epaper` sama seperti pada jenis visual `chart`. Yang membedakan hanyalah `tag` pembukanya sebagai berikut:

```xml
<chart>

</chart>
```

Tag pembuka `<chart>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut          | Tipe Nilai | Nilai Baku | Pilihan                | Keterangan                                |
| ---------------- | ---------- | ---------- | ---------------------- | ----------------------------------------- |
| x                | int        | 0          | _null_                 | Posisi x                                  |
| y                | int        | 0          | _null_                 | Posisi y                                  |
| width            | int        | 0          | _null_                 | Lebar komponen                            |
| height           | int        | 0          | _null_                 | Tinggi komponen                           |
| data_this        | enum       | hour       | hour; day; month; year | Rentang waktu data\*                      |
| refresh_interval | int        | 0          | _null_                 | Interval pengambilan data terbaru (menit) |
| decimal_default  | int        | 2          | _null_                 | Jumlah-angka baku di belakang koma        |

%[{ _data_this.md }]%
