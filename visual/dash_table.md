# Tabel

Komponen `table` untuk jenis visual `dash` sama seperti pada jenis visual `table`. Yang membedakan hanyalah `tag` pembukanya sebagai berikut:

```xml
<table>

</table>
```

Tag pembuka `<table>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut          | Tipe Nilai | Nilai Baku | Pilihan                            | Keterangan                                |
| ---------------- | ---------- | ---------- | ---------------------------------- | ----------------------------------------- |
| title            | string     | _null_     | _null_                             | Judul komponen                            |
| column_size      | enum       | 0          | 1;2;3;4;5;6;7;8;9;10;11;12         | Lebar komponen                            |
| icon             | string     | _null_     | [Referensi&rarr;](ref_icon.md) | _Icon_ komponen                           |
| data_this        | enum       | hour       | hour; day; month; year             | Rentang waktu data\*                      |
| refresh_interval | int        | 0          | _null_                             | Interval pengambilan data terbaru (menit) |
| flex             | boolean    | _false_    | _null_                             |                                           |
| break            | boolean    | _false_    | _null_                             |                                           |

%[{ _data_this.md }]%
