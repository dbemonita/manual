# Lingkaran

Berikut contoh komponen HMI `circle` (lingkaran):

```xml
<circle>
  <caption>Contoh Lingkaran 1</caption>
  <diameter>200</diameter>
  <border_width>0</border_width>
  <background_gradient>linear; 60; #bd93f9; #8be9fd</background_gradient>
  <x>100</x>
  <y>100</y>
</circle>
```

#### Contoh:

https://playground.monita.co.id/?component=circle

![circle](https://manual.monita.co.id/_assets/images/circle.png)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku    | Pilihan             | Keterangan                |
| ------------------- | ---------- | ------------- | ------------------- | ------------------------- |
| caption             | string     | Circle        |                     | Keterangan komponen       |
| diameter            | float      | 0             |                     | Diameter lingkaran\*\*    |
| radius              | float      | 0             |                     | Radius lingkaran\*\*      |
| background_color    | string     | rgba(0,0,0,0) |                     | Warna latar               |
| background_gradient | string     |               |                     | Warna latar _gradient_ \* |
| border_width        | float      | 1             |                     | Ketebalan garis           |
| border_color        | string     | LightBlue     |                     | Warna garis               |
| link                | string     |               |                     | Tautan                    |
| x                   | float      | 0             |                     | Posisi: Koordinat x       |
| y                   | float      | 0             |                     | Posisi: Koordinat y       |
| z                   | enum       | 0             | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index           |

\*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)

\*\*) Pilih salah satu. Bila didefinisikan keduanya maka yang digunakan adalah diameter.
