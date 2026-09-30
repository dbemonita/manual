# Grafik Trend

Komponen ini tersedia pada versi `>=5.18.0`. Bertujuan untuk menampilkan data tren 24 jam terakhir. Misal saat ini pukul 11.15, maka tren akan menunjukkan pukul pukul 11 kemarin hingga pukul 10 hari ini yang berasal dari akuisisi data dari pukul 11.00.00 kemarin hingga pukul 10.59.59 hari ini. Berikut contoh penggunaan komponen HMI `trend_chart`:

```xml
<trend_chart>
  <caption>Contoh Trend Chart 1</caption>
  <point_id>1001</point_id>
  <type>line-area</type>
  <title>Trend Chart 1</title>
  <width>400</width>
  <height>200</height>
  <x>50</x>
  <y>50</y>
</trend_chart>
```

#### Contoh:

https://playground.monita.co.id/?component=trend_chart

![trend_chart](https://manual.monita.co.id/_assets/images/trend_chart.png)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku                                           | Pilihan Nilai                  | Keterangan                      |
| ------------------- | ---------- | ---------------------------------------------------- | ------------------------------ | ------------------------------- |
| caption             | string     | TrendChart                                           |                                | Keterangan komponen             |
| point_id            | int        | 0                                                    |                                | ID titik ukur                   |
| type                | string     | line-area                                            | line; line-area; bar; bar-line | Jenis grafik                    |
| color               | string     | DodgerBlue                                           |                                | Warna line/bar grafik           |
| grid_color          | string     | LightSlateGray                                       |                                | Warna grid                      |
| background_color    | string     | White                                                |                                | Warna latar area                |
| background_gradient | string     |                                                      |                                | Warna latar _gradient_ \*       |
| title               | string     |                                                      |                                | Judul grafik                    |
| title_color         | string     | DarkSlateGray                                        |                                | Warna judul                     |
| title_font          | string     | Roboto, Arial, Helvetica Neue, Helvetica, sans-serif |                                | Jenis huruf judul               |
| title_size          | float      | 12                                                   |                                | Ukuran huruf judul              |
| show_x_axis_label   | boolean    | _true_                                               |                                | Tampilkan nilai x-axis?         |
| show_y_axis_label   | boolean    | _true_                                               |                                | Tampilkan nilai y-axis?         |
| show_y_axis_grid    | boolean    | _true_                                               |                                | Tampilkan grid y-axis?          |
| axis_label_color    | string     | DarkSlateGray                                        |                                | Warna huruf nilai xy axis       |
| axis_label_font     | string     | Roboto, Arial, Helvetica Neue, Helvetica, sans-serif |                                | Jenis huruf nilai xy axis       |
| axis_label_size     | float      | 11                                                   |                                | Ukuran huruf nilai xy axis      |
| axis_label_decimal  | integer    | 2                                                    |                                | Jumlah desimal nilai xy axis    |
| show_value          | boolean    | _true_                                               |                                | Tampilkan huruf nilai series?   |
| value_color         | string     | DarkSlateGray                                        |                                | Warna huruf nilai series        |
| value_font          | string     | Roboto, Arial, Helvetica Neue, Helvetica, sans-serif |                                | Jenis huruf nilai series        |
| value_size          | float      | 10                                                   |                                | Ukuran huruf nilai series       |
| value_decimal       | integer    | 1                                                    |                                | Jumlah desimal nilai series     |
| enable_fullscreen   | boolean    | _false_                                              |                                | Tampilkan tombol _fullscreen_ ? |
| width               | float      | 0                                                    |                                | Lebar grafik                    |
| height              | float      | 0                                                    |                                | Tinggi grafik                   |
| x                   | float      | 0                                                    |                                | Posisi: Koordinat x             |
| y                   | float      | 0                                                    |                                | Posisi: Koordinat y             |

\*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)
