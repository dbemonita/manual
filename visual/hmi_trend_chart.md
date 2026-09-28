# Grafik Trend

Komponen ini tersedia pada versi `>=5.18.0`. Berikut contoh komponen HMI `trend_chart`:

```xml
<trend_chart>
  <caption>Grafik Trend 1</caption>
  <point_id>1001</point_id>
  <width>400</width>
  <height>200</height>
  <x>50</x>
  <y>50</y>
</trend_chart>
```

#### Contoh:

https://playground.monita.co.id/?component=trend_chart

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku                                           | Pilihan Nilai                  | Keterangan                      |
| ------------------ | ---------- | ---------------------------------------------------- | ------------------------------ | ------------------------------- |
| caption            | string     | TrendChart                                           | _null_                         | Keterangan komponen             |
| point_id           | int        | 0                                                    | _null_                         | ID titik ukur                   |
| type               | string     | line-area                                            | line; line-area; bar; bar-line | Jenis grafik                    |
| color              | string     | DodgerBlue                                           | _null_                         | Warna line/bar grafik           |
| grid_color         | string     | LightSlateGray                                       | _null_                         | Warna grid                      |
| background_color   | string     | transparent                                          | _null_                         | Warna latar area                |
| title              | string     |                                                      | _null_                         | Judul grafik                    |
| title_color        | string     | DarkSlateGray                                        | _null_                         | Warna judul                     |
| title_font         | string     | Roboto, Arial, Helvetica Neue, Helvetica, sans-serif | _null_                         | Jenis huruf judul               |
| title_size         | float      | 10                                                   | _null_                         | Ukuran huruf judul              |
| show_x_axis_label  | boolean    | _true_                                               | _null_                         | Tampilkan nilai x-axis?         |
| show_y_axis_label  | boolean    | _true_                                               | _null_                         | Tampilkan nilai y-axis?         |
| show_y_axis_grid   | boolean    | _true_                                               | _null_                         | Tampilkan grid y-axis?          |
| axis_label_color   | string     | DarkSlateGray                                        | _null_                         | Warna huruf nilai xy axis       |
| axis_label_font    | string     | Roboto, Arial, Helvetica Neue, Helvetica, sans-serif | _null_                         | Jenis huruf nilai xy axis       |
| axis_label_size    | float      | 9                                                    | _null_                         | Ukuran huruf nilai xy axis      |
| axis_label_decimal | integer    | 2                                                    | _null_                         | Jumlah desimal nilai xy axis    |
| show_value         | boolean    | _true_                                               | _null_                         | Tampilkan huruf nilai series?   |
| value_color        | string     | DarkSlateGray                                        | _null_                         | Warna huruf nilai series        |
| value_font         | string     | Roboto, Arial, Helvetica Neue, Helvetica, sans-serif | _null_                         | Jenis huruf nilai series        |
| value_size         | float      | 8                                                    | _null_                         | Ukuran huruf nilai series       |
| value_decimal      | integer    | 2                                                    | _null_                         | Jumlah desimal nilai series     |
| enable_fullscreen  | boolean    | _false_                                              | _null_                         | Tampilkan tombol _fullscreen_ ? |
| width              | float      | 0                                                    | _null_                         | Lebar grafik                    |
| height             | float      | 0                                                    | _null_                         | Tinggi grafik                   |
| x                  | float      | 0                                                    | _null_                         | Posisi: Koordinat x             |
| y                  | float      | 0                                                    | _null_                         | Posisi: Koordinat y             |
