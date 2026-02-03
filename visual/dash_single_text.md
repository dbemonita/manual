# Single Text

Komponen ini berfungsi untuk menunjukkan data titik ukur sesuai nilai yang dikirim oleh _server_. Tampilan komponen ini berbentuk teks. Berikut contoh komponen `single_text`:

```xml
<single_text>
  <point_id>1001</point_id>
</single_text>
```

Tag pembuka `<single_text>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut          | Tipe Nilai | Nilai Baku | Pilihan                            | Keterangan                                |
| ---------------- | ---------- | ---------- | ---------------------------------- | ----------------------------------------- |
| column_size      | enum       | 0          | 1;2;3;4;5;6;7;8;9;10;11;12         | Lebar komponen                            |
| icon             | string     | _null_     | [Referensi&rarr;](ref_icon.md) | _Icon_ komponen                           |
| data_this        | enum       | hour       | hour; day; month; year             | Rentang waktu data\*                      |
| summary          | enum       | last       | min; max; sum; avg; first; last    | Jenis ringkasan data                      |
| refresh_interval | int        | 0          | _null_                             | Interval pengambilan data terbaru (menit) |
| flex             | boolean    | _false_    | _null_                             |                                           |
| break            | boolean    | _false_    | _null_                             |                                           |

%[{ _data_this.md }]%

#### Properti selengkapnya:

| Properti | Tipe Nilai | Nilai Baku | Keterangan      |
| -------- | ---------- | ---------- | --------------- |
| name     | string     | _null_     | Nama komponen\* |
| point_id | int        | 0          | Titik ukur      |
| decimal  | int        | 2          | Jumlah desimal  |

\*) Nama titik ukur secara baku menggunakan data dari database. Untuk _override_, definisikan properti `name`.
