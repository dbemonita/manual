```xml
<active_text>
  <caption>Contoh Teks Aktif 1</caption>
  <point_id>1001</point_id>
  <width>100</width>
  <height>50</height>
  <x>100</x>
  <y>100</y>
</active_text>
```

Tag pembuka `<active_text>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut                  | Tipe Nilai | Nilai Baku | Keterangan                         |
| ------------------------ | ---------- | ---------- | ---------------------------------- |
| default_color            | string     | _null_     | Nilai baku untuk semua warna teks  |
| default_background_color | string     | _null_     | Nilai baku untuk semua warna latar |

#### Contoh

![active_text](https://hackmd.io/_uploads/r1XRhcYHfg.png)

#### Properti selengkapnya:

| Properti               | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan                |
| ---------------------- | ---------- | ---------------------------- | ------------------------------ | ------------------------- |
| caption                | string     | ActiveText                   | _null_                         | Keterangan komponen       |
| point_id               | int        | 0                            | _null_                         | Titik ukur                |
| calc                   | string     | _null_                       | _null_                         | Kode operasi/kalkulasi\*  |
| decimal                | int        | 2                            | _null_                         | Jumlah desimal            |
| unit                   | string     | _null_                       | _null_                         | Satuan                    |
| font                   | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf               |
| size                   | float      | 12                           | _null_                         | Ukuran huruf              |
| style                  | enum       | normal                       | normal; italic                 | Bentuk huruf              |
| weight                 | enum       | normal                       | normal; bold                   | Ketebalan huruf           |
| width                  | float      | 0                            | _null_                         | Lebar kotak teks          |
| height                 | float      | 0                            | _null_                         | Tinggi kotak teks         |
| color_low2             | string     | LightBlue                    | _null_                         | Warna teks batas bawah 2  |
| color_low1             | string     | LightBlue                    | _null_                         | Warna teks batas bawah 1  |
| color                  | string     | LightBlue                    | _null_                         | Warna teks normal         |
| color_high1            | string     | LightBlue                    | _null_                         | Warna teks batas atas 1   |
| color_high2            | string     | LightBlue                    | _null_                         | Warna teks batas atas 2   |
| background_color_low2  | string     | DarkSlateGray                | _null_                         | Warna latar batas bawah 2 |
| background_color_low1  | string     | DarkSlateGray                | _null_                         | Warna latar batas bawah 1 |
| background_color       | string     | DarkSlateGray                | _null_                         | Warna latar normal        |
| background_color_high1 | string     | DarkSlateGray                | _null_                         | Warna latar batas atas 1  |
| background_color_high2 | string     | DarkSlateGray                | _null_                         | Warna latar batas atas 2  |
| border_width           | float      | 2                            | _null_                         | Ketebalan garis tepi      |
| border_color           | string     |                              | _null_                         | Warna garis tepi          |
| border_radius          | float      | 0                            | _null_                         | Radius garis tepi         |
| anchor                 | enum       | middle                       | start; middle; end             | Rata kiri/tengah/kanan    |
| link                   | string     | _null_                       | _null_                         | Tautan                    |
| x                      | float      | 0                            | _null_                         | Posisi: Koordinat x       |
| y                      | float      | 0                            | _null_                         | Posisi: Koordinat y       |
| rotate                 | float      | 0                            | _null_                         | Derajat putaran           |
