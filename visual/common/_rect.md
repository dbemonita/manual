```xml
<rect>
  <caption>Contoh Kotak 1</caption>
  <width>200</width>
  <height>100</height>
  <border_width>0</border_width>
  <background_gradient>linear; 60; #bd93f9; #8be9fd</background_gradient>
  <x>100</x>
  <y>100</y>
</rect>
```

#### Contoh:

https://playground.monita.co.id/?component=rect

![rect](https://manual.monita.co.id/_assets/images/rect.png)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku    | Pilihan               | Keterangan                |
| ------------------- | ---------- | ------------- | --------------------- | ------------------------- |
| caption             | string     | Rect          |                       | Keterangan komponen       |
| width               | float      | 0             |                       | Lebar                     |
| height              | float      | 0             |                       | Tinggi                    |
| background_color    | string     | rgba(0,0,0,0) |                       | Warna latar               |
| background_gradient | string     |               |                       | Warna latar _gradient_ \* |
| border_width        | float      | 1             |                       | Ketebalan garis           |
| border_color        | string     | LightBlue     |                       | Warna garis               |
| border_radius       | float      | 0             |                       | Radius garis tepi         |
| border_style        | enum       | solid         | solid; dashed; dotted | Jenis garis               |
| link                | string     |               |                       | Tautan                    |
| x                   | float      | 0             |                       | Posisi: Koordinat x       |
| y                   | float      | 0             |                       | Posisi: Koordinat y       |
| z                   | enum       | 0             | 0;1;2;3;4;5;6;7;8;9   | Posisi: z-index           |
| rotate              | float      | 0             |                       | Derajat putaran           |

- \*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)
