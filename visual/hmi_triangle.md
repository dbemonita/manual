# Segitiga

Berikut contoh komponen HMI `triangle` (segitiga sama sisi):

```xml
<triangle>
  <caption>Contoh Segitiga 1</caption>
  <length>300</length>
  <x>100</x>
  <y>100</y>
</triangle>
```

#### Contoh

![triangle](https://hackmd.io/_uploads/H1oMY8VBMx.jpg)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku    | Pilihan             | Keterangan               |
| ------------------- | ---------- | ------------- | ------------------- | ------------------------ |
| caption             | string     | Triangle      | _null_              | Keterangan komponen      |
| length              | float      | 0             | _null_              | Panjang sisi             |
| background_color    | string     | rgba(0,0,0,0) | _null_              | Warna latar              |
| background_gradient | string     | _null_        | _null_              | Warna latar _gradient_\* |
| border_width        | float      | 1             | _null_              | Ketebalan garis          |
| border_color        | string     | LightBlue     | _null_              | Warna garis              |
| link                | string     | _null_        | _null_              | Tautan                   |
| x                   | float      | 0             | _null_              | Posisi: Koordinat x      |
| y                   | float      | 0             | _null_              | Posisi: Koordinat y      |
| z                   | enum       | 0             | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index          |
| rotate              | float      | 0             | _null_              | Derajat putaran          |

\*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)
