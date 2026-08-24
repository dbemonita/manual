# Liquid Level

```xml
<liquid_level>
  <caption>Contoh Liquid Level 1</caption>
  <point_id>1001</point_id>
  <width>300</width>
  <height>300</height>
  <label_width>50</label_width>
  <label_height>25</label_height>
  <x>100</x>
  <y>100</y>
</liquid_level>
```

#### Contoh:

https://playground.monita.co.id/?component=liquid_level

![liquid_level](https://hackmd.io/_uploads/BkA13l_8Gl.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan                                    |
| ------------------ | ---------- | ---------------------------- | ------------------------------ | --------------------------------------------- |
| caption            | string     | LiquidLevel                  | _null_                         | Keterangan komponen                           |
| point_id           | int        | 0                            | _null_                         | Titik ukur                                    |
| decimal            | int        | 0                            | _null_                         | Jumlah desimal                                |
| unit               | string     | _null_                       | _null_                         | Satuan                                        |
| font               | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf                                   |
| size               | float      | 12                           | _null_                         | Ukuran huruf                                  |
| weight             | enum       | normal                       | normal; bold                   | Ketebalan huruf                               |
| label_width        | float      | 0                            | _null_                         | Lebar label                                   |
| label_height       | float      | 0                            | _null_                         | Tinggi label                                  |
| label_radius       | float      | _auto_                       | _null_                         | Radius label                                  |
| text_color_low2    | string     | LightBlue                    | _null_                         | Warna teks label batas bawah 2                |
| text_color_low1    | string     | LightBlue                    | _null_                         | Warna teks label batas bawah 1                |
| text_color         | string     | LightBlue                    | _null_                         | Warna teks label normal                       |
| text_color_high1   | string     | LightBlue                    | _null_                         | Warna teks label batas atas 1                 |
| text_color_high2   | string     | LightBlue                    | _null_                         | Warna teks batas atas 2                       |
| label_color_low2   | string     | DarkSlateGray                | _null_                         | Warna latar label batas bawah 2               |
| label_color_low1   | string     | DarkSlateGray                | _null_                         | Warna latar label batas bawah 1               |
| label_color        | string     | DarkSlateGray                | _null_                         | Warna latar label normal                      |
| label_color_high1  | string     | DarkSlateGray                | _null_                         | Warna latar label batas atas 1                |
| label_color_high2  | string     | DarkSlateGray                | _null_                         | Warna latar label batas atas 2                |
| interval           | float      | 10                           | _null_                         | Interval _marker_                             |
| width              | float      | 0                            | _null_                         | Lebar kotak teks                              |
| height             | float      | 0                            | _null_                         | Tinggi kotak teks                             |
| base_ratio         | float      | 1                            | _null_                         | Rasio sisi bawah dan atas, antara 0.5 s/d 1.0 |
| background_visible | boolean    | _true_                       | _null_                         | Tampilkan gambar latar (tangki)?              |
| fill_color_low2    | string     | Aqua                         | _null_                         | Warna liquid batas bawah 2                    |
| fill_color_low1    | string     | Aqua                         | _null_                         | Warna liquid batas bawah 1                    |
| fill_color         | string     | Aqua                         | _null_                         | Warna liquid normal                           |
| fill_color_high1   | string     | Aqua                         | _null_                         | Warna liquid batas atas 1                     |
| fill_color_high2   | string     | Aqua                         | _null_                         | Warna liquid batas atas 2                     |
| link               | string     | _null_                       | _null_                         | Tautan                                        |
| x                  | float      | 0                            | _null_                         | Posisi: Koordinat x                           |
| y                  | float      | 0                            | _null_                         | Posisi: Koordinat y                           |
