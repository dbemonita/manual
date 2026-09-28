# Tabel

Komponen `table` untuk jenis visual `epaper` sama seperti pada jenis visual `table`. Yang membedakan hanyalah `tag` pembukanya sebagai berikut:

```xml
<table>

</table>
```

Tag pembuka `<table>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut          | Tipe Nilai | Nilai Baku | Pilihan                | Keterangan                                |
| ---------------- | ---------- | ---------- | ---------------------- | ----------------------------------------- |
| x                | int        | 0          |                        | Posisi x                                  |
| y                | int        | 0          |                        | Posisi y                                  |
| width            | int        | 0          |                        | Lebar komponen                            |
| height           | int        | 0          |                        | Tinggi komponen                           |
| data_this        | enum       | hour       | hour; day; month; year | Rentang waktu data\*                      |
| refresh_interval | int        | 0          |                        | Interval pengambilan data terbaru (menit) |
| decimal_default  | int        | 2          |                        | Jumlah-angka baku di belakang koma        |

%[{ _data_this.md }]%
