# Kotak Indikator

Berikut contoh komponen HMI `indicator_rect` (kotak indikator):

```xml
<indicator_rect default_background_color="#62748e">
  <caption>Contoh Kotak Indikator 1</caption>
  <point_id>1001</point_id>
  <width>150</width>
  <height>75</height>
  <size>28</size>
  <background_color_0>#f0b100</background_color_0>
  <background_color_1>#00bc7d</background_color_1>
  <border_width>0</border_width>
  <x>100</x>
  <y>100</y>
</indicator_rect>
```

Tag pembuka `<indicator_rect>` tersebut memiliki atribut berikut:

| Atribut                  | Tipe Nilai | Nilai Baku | Keterangan                         |
| ------------------------ | ---------- | ---------- | ---------------------------------- |
| default_background_color | string     |            | Nilai baku untuk semua warna latar |

#### Contoh:

https://playground.monita.co.id/?component=indicator_rect

![indicator_rect](https://manual.monita.co.id/_assets/images/indicator_rect.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku    | Pilihan               | Keterangan            |
| ------------------ | ---------- | ------------- | --------------------- | --------------------- |
| caption            | string     | Rect          | ---                   | Keterangan komponen   |
| width              | float      | 0             | ---                   | Lebar                 |
| height             | float      | 0             | ---                   | Tinggi                |
| background_color   | string     | DarkSlateGray | ---                   | Warna latar _initial_ |
| background_color_0 | string     | DarkSlateGray | ---                   | Warna latar nilai 0   |
| background_color_1 | string     | DarkSlateGray | ---                   | Warna latar nilai 1   |
| border_width       | float      | 1             | ---                   | Ketebalan garis       |
| border_color       | string     | LightBlue     | ---                   | Warna garis           |
| border_radius      | float      | 0             | ---                   | Radius garis tepi     |
| border_style       | enum       | solid         | solid; dashed; dotted | Jenis garis           |
| link               | string     | \_null\*      | ---                   | Tautan                |
| x                  | float      | 0             | ---                   | Posisi: Koordinat x   |
| y                  | float      | 0             | ---                   | Posisi: Koordinat y   |
| rotate             | float      | 0             | ---                   | Derajat putaran       |
