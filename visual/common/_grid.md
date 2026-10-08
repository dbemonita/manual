```xml
<grid>
  <caption>Contoh Grid 1</caption>
  <width>300</width>
  <height>300</height>
  <num_rows>3</num_rows>
  <num_cols>3</num_cols>
  <border_color>white</border_color>
  <border_width>2</border_width>
  <x>100</x>
  <y>100</y>
</grid>
```

#### Contoh:

https://playground.monita.co.id/?component=grid

![grid](https://manual.monita.co.id/_assets/images/grid.png)

#### Properti selengkapnya:

| Properti         | Tipe Nilai | Nilai Baku    | Pilihan             | Keterangan            |
| ---------------- | ---------- | ------------- | ------------------- | --------------------- |
| caption          | string     | Rect          |                     | Keterangan komponen   |
| width            | float      | 0             |                     | Lebar                 |
| height           | float      | 0             |                     | Tinggi                |
| num_rows         | int        | 0             |                     | Jumlah baris          |
| num_cols         | int        | 0             |                     | Jumlah kolom          |
| rows_ratio       | string     | auto          |                     | Rasio tinggi baris\*  |
| cols_ratio       | string     | auto          |                     | Rasio lebar kolom\*\* |
| background_color | string     | rgba(0,0,0,0) |                     | Warna latar           |
| border_width     | float      | 1             |                     | Ketebalan garis       |
| border_color     | string     | LightBlue     |                     | Warna garis           |
| border_style     | enum       | solid         | solid;dotted;dashed | _Style_ garis         |
| outline_visible  | boolean    | true          |                     | Tampilkan _outline_?  |
| x                | float      | 0             |                     | Posisi: Koordinat x   |
| y                | float      | 0             |                     | Posisi: Koordinat y   |
| z                | enum       | 0             | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index       |

- \*) Contoh `height` = 100, `num_rows` = 3, `rows_ratio` = 1:2:1, maka tinggi baris ke-1 = 25, ke-2 = 50, ke-3 = 25
- \*\*) Contoh `width` = 40, `num_cols` = 3, `cols_ratio` = 1:2:1, maka tinggi baris ke-1 = 10, ke-2 = 20, ke-3 = 10
