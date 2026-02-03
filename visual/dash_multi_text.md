# Multi Text

Komponen ini berfungsi untuk menunjukkan data titik ukur sesuai nilai yang dikirim oleh _server_. Tampilan komponen ini berbentuk kumpulan nilai. Berikut contoh komponen `multi_text`:

```xml
<multi_text>
  <point_id1>1001</point_id1>
  <point_id2>1002</point_id2>
</multi_text>
```

Tag pembuka `<multi_text>` tersebut memiliki atribut-atribut sebagai berikut:

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

| Properti   | Tipe Nilai | Nilai Baku | Keterangan          |
| ---------- | ---------- | ---------- | ------------------- |
| name1      | string     | _null_     | Nama komponen #1\*  |
| point_id1  | int        | 0          | Titik ukur #1       |
| decimal1   | int        | 2          | Jumlah desimal #1   |
| name2      | string     | _null_     | Nama komponen #2\*  |
| point_id2  | int        | 0          | Titik ukur #2       |
| decimal2   | int        | 2          | Jumlah desimal #2   |
| name3      | string     | _null_     | Nama komponen #3\*  |
| point_id3  | int        | 0          | Titik ukur #3       |
| decimal3   | int        | 2          | Jumlah desimal #3   |
| name4      | string     | _null_     | Nama komponen #4\*  |
| point_id4  | int        | 0          | Titik ukur #4       |
| decimal4   | int        | 2          | Jumlah desimal #4   |
| name5      | string     | _null_     | Nama komponen #5\*  |
| point_id5  | int        | 0          | Titik ukur #5       |
| decimal5   | int        | 2          | Jumlah desimal #5   |
| name6      | string     | _null_     | Nama komponen #6\*  |
| point\*id6 | int        | 0          | Titik ukur #6       |
| decimal6   | int        | 2          | Jumlah desimal #6   |
| name7      | string     | _null_     | Nama komponen #7\*  |
| point\*id7 | int        | 0          | Titik ukur #7       |
| decimal7   | int        | 2          | Jumlah desimal #7   |
| name8      | string     | _null_     | Nama komponen #8\*  |
| point\*id8 | int        | 0          | Titik ukur #8       |
| decimal8   | int        | 2          | Jumlah desimal #8   |
| name9      | string     | _null_     | Nama komponen #9\*  |
| point\*id9 | int        | 0          | Titik ukur #9       |
| decimal9   | int        | 2          | Jumlah desimal #9   |
| name10     | string     | _null_     | Nama komponen #10\* |
| point_id10 | int        | 0          | Titik ukur #10      |
| decimal10  | int        | 2          | Jumlah desimal #10  |

\*) Nama titik ukur secara baku menggunakan data dari database. Untuk _override_, definisikan properti `name1` s/d `name10`.
