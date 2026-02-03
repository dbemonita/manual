# Solid Gauge

Komponen ini berfungsi untuk menunjukkan data titik ukur sesuai nilai yang dikirim oleh _server_. Tampilan komponen ini berbentuk busur. Berikut contoh komponen `solid_gauge`:

```xml
<solid_gauge>
  <point_id>1001</point_id>
</solid_gauge>
```

Tag pembuka `<solid_gauge>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut          | Tipe Nilai | Nilai Baku | Pilihan                            | Keterangan                                |
| ---------------- | ---------- | ---------- | ---------------------------------- | ----------------------------------------- |
| title            | string     | _null_     | _null_                             | Judul komponen                            |
| column_size      | enum       | 0          | 1;2;3;4;5;6;7;8;9;10;11;12         | Lebar komponen                            |
| icon             | string     | _null_     | [Referensi&rarr;](ref_icon.md) | _Icon_ komponen                           |
| data_this        | enum       | hour       | hour; day; month; year             | Rentang waktu data\*                      |
| summary          | enum       | last       | min; max; sum; avg; first; last    | Jenis ringkasan data                      |
| refresh_interval | int        | 0          | _null_                             | Interval pengambilan data terbaru (menit) |
| flex             | boolean    | _false_    | _null_                             |                                           |
| break            | boolean    | _false_    | _null_                             |                                           |

%[{ _data_this.md }]%

#### Properti selengkapnya:

| Properti               | Tipe Nilai | Nilai Baku | Keterangan                |
| ---------------------- | ---------- | ---------- | ------------------------- |
| point_id               | int        | 0          | Titik ukur                |
| decimal                | int        | 2          | Jumlah desimal            |
| background_color_low2  | string     | #0E76BD    | Warna latar batas bawah 2 |
| background_color_low1  | string     | #0E76BD    | Warna latar batas bawah 1 |
| background_color       | string     | #0E76BD    | Warna latar normal        |
| background_color_high1 | string     | #0E76BD    | Warna latar batas atas 1  |
| background_color_high2 | string     | #0E76BD    | Warna latar batas atas 2  |
