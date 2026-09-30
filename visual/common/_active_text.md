```xml
<active_text default_background_color="#00bc7d" default_color="white">
  <caption>Contoh Teks Aktif 1</caption>
  <point_id>1001</point_id>
  <width>150</width>
  <height>75</height>
  <size>28</size>
  <border_width>0</border_width>
  <unit>&#x2103;</unit> <!--°C-->
  <x>100</x>
  <y>100</y>
</active_text>
```

Tag pembuka `<active_text>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut                  | Tipe Nilai | Nilai Baku | Keterangan                         |
| ------------------------ | ---------- | ---------- | ---------------------------------- |
| default_color            | string     |            | Nilai baku untuk semua warna teks  |
| default_background_color | string     |            | Nilai baku untuk semua warna latar |

#### Contoh

https://playground.monita.co.id/?component=active_text

![active_text](https://manual.monita.co.id/_assets/images/active_text.png)

#### Properti selengkapnya:

| Properti               | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan                |
| ---------------------- | ---------- | ---------------------------- | ------------------------------ | ------------------------- |
| caption                | string     | ActiveText                   |                                | Keterangan komponen       |
| point_id               | int        | 0                            |                                | Titik ukur                |
| calc                   | string     |                              |                                | Kode operasi/kalkulasi\*  |
| decimal                | int        | 2                            |                                | Jumlah desimal            |
| unit                   | string     |                              |                                | Satuan                    |
| font                   | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf               |
| size                   | float      | 12                           |                                | Ukuran huruf              |
| style                  | enum       | normal                       | normal; italic                 | Bentuk huruf              |
| weight                 | enum       | normal                       | normal; bold                   | Ketebalan huruf           |
| width                  | float      | 0                            |                                | Lebar kotak teks          |
| height                 | float      | 0                            |                                | Tinggi kotak teks         |
| color_low2             | string     | LightBlue                    |                                | Warna teks batas bawah 2  |
| color_low1             | string     | LightBlue                    |                                | Warna teks batas bawah 1  |
| color                  | string     | LightBlue                    |                                | Warna teks normal         |
| color_high1            | string     | LightBlue                    |                                | Warna teks batas atas 1   |
| color_high2            | string     | LightBlue                    |                                | Warna teks batas atas 2   |
| background_color_low2  | string     | DarkSlateGray                |                                | Warna latar batas bawah 2 |
| background_color_low1  | string     | DarkSlateGray                |                                | Warna latar batas bawah 1 |
| background_color       | string     | DarkSlateGray                |                                | Warna latar normal        |
| background_color_high1 | string     | DarkSlateGray                |                                | Warna latar batas atas 1  |
| background_color_high2 | string     | DarkSlateGray                |                                | Warna latar batas atas 2  |
| border_width           | float      | 2                            |                                | Ketebalan garis tepi      |
| border_color           | string     |                              |                                | Warna garis tepi          |
| border_radius          | float      | 0                            |                                | Radius garis tepi         |
| anchor                 | enum       | middle                       | start; middle; end             | Rata kiri/tengah/kanan    |
| link                   | string     |                              |                                | Tautan                    |
| x                      | float      | 0                            |                                | Posisi: Koordinat x       |
| y                      | float      | 0                            |                                | Posisi: Koordinat y       |
| rotate                 | float      | 0                            |                                | Derajat putaran           |
