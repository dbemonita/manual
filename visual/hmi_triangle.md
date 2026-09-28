# Segitiga

Berikut contoh komponen HMI `triangle` (segitiga sama sisi):

```xml
<triangle>
  <caption>Contoh Segitiga 1</caption>
  <length>200</length>
  <border_width>0</border_width>
  <background_gradient>linear; 60; #bd93f9; #8be9fd</background_gradient>
  <x>100</x>
  <y>100</y>
</triangle>
```

#### Contoh:

https://playground.monita.co.id/?component=triangle

![triangle](https://manual.monita.co.id/_assets/images/triangle.png)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku    | Pilihan             | Keterangan                |
| ------------------- | ---------- | ------------- | ------------------- | ------------------------- |
| caption             | string     | Triangle      |                     | Keterangan komponen       |
| length              | float      | 0             |                     | Panjang sisi              |
| background_color    | string     | rgba(0,0,0,0) |                     | Warna latar               |
| background_gradient | string     |               |                     | Warna latar _gradient_ \* |
| border_width        | float      | 1             |                     | Ketebalan garis           |
| border_color        | string     | LightBlue     |                     | Warna garis               |
| link                | string     |               |                     | Tautan                    |
| x                   | float      | 0             |                     | Posisi: Koordinat x       |
| y                   | float      | 0             |                     | Posisi: Koordinat y       |
| z                   | enum       | 0             | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index           |
| rotate              | float      | 0             |                     | Derajat putaran           |

\*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)
