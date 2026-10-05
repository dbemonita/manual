# Liquid Level

```xml
<liquid_level>
  <caption>Contoh Liquid Level 1</caption>
  <point_id>1001</point_id>
  <width>150</width>
  <height>200</height>
  <interval>20</interval>
  <label_width>50</label_width>
  <label_height>25</label_height>
  <x>100</x>
  <y>100</y>
</liquid_level>
```

#### Contoh:

https://playground.monita.co.id/?component=liquid_level

![liquid_level](https://manual.monita.co.id/_assets/images/liquid_level.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan                                    |
| ------------------ | ---------- | ---------------------------- | ------------------------------ | --------------------------------------------- |
| caption            | string     | LiquidLevel                  |                                | Keterangan komponen                           |
| point_id           | int        | 0                            |                                | Titik ukur                                    |
| decimal            | int        | 0                            |                                | Jumlah desimal                                |
| unit               | string     |                              |                                | Satuan                                        |
| font               | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf                                   |
| size               | float      | 12                           |                                | Ukuran huruf                                  |
| weight             | enum       | normal                       | normal; bold                   | Ketebalan huruf                               |
| label_width        | float      | 0                            |                                | Lebar label                                   |
| label_height       | float      | 0                            |                                | Tinggi label                                  |
| label_radius       | float      | _auto_                       |                                | Radius label                                  |
| text_color_low2    | string     | LightBlue                    |                                | Warna teks label batas bawah 2                |
| text_color_low1    | string     | LightBlue                    |                                | Warna teks label batas bawah 1                |
| text_color         | string     | LightBlue                    |                                | Warna teks label normal                       |
| text_color_high1   | string     | LightBlue                    |                                | Warna teks label batas atas 1                 |
| text_color_high2   | string     | LightBlue                    |                                | Warna teks batas atas 2                       |
| label_color_low2   | string     | DarkSlateGray                |                                | Warna latar label batas bawah 2               |
| label_color_low1   | string     | DarkSlateGray                |                                | Warna latar label batas bawah 1               |
| label_color        | string     | DarkSlateGray                |                                | Warna latar label normal                      |
| label_color_high1  | string     | DarkSlateGray                |                                | Warna latar label batas atas 1                |
| label_color_high2  | string     | DarkSlateGray                |                                | Warna latar label batas atas 2                |
| interval           | float      | 10                           |                                | Interval _marker_                             |
| width              | float      | 0                            |                                | Lebar kotak teks                              |
| height             | float      | 0                            |                                | Tinggi kotak teks                             |
| base_ratio         | float      | 1                            |                                | Rasio sisi bawah dan atas, antara 0.5 s/d 1.0 |
| background_visible | boolean    | _true_                       |                                | Tampilkan gambar latar (tangki)?              |
| fill_color_low2    | string     | Aqua                         |                                | Warna liquid batas bawah 2                    |
| fill_color_low1    | string     | Aqua                         |                                | Warna liquid batas bawah 1                    |
| fill_color         | string     | Aqua                         |                                | Warna liquid normal                           |
| fill_color_high1   | string     | Aqua                         |                                | Warna liquid batas atas 1                     |
| fill_color_high2   | string     | Aqua                         |                                | Warna liquid batas atas 2                     |
| link               | string     |                              |                                | Tautan                                        |
| x                  | float      | 0                            |                                | Posisi: Koordinat x                           |
| y                  | float      | 0                            |                                | Posisi: Koordinat y                           |
