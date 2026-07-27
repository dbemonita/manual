# Elips

Berikut contoh komponen HMI `ellipse` (elips):

```xml
<ellipse>
  <caption>Contoh Elips 1</caption>
  <width>300</width>
  <height>150</height>
  <x>100</x>
  <y>100</y>
</ellipse>
```

#### Contoh

![ellipse](https://hackmd.io/_uploads/ByrHuLNHfg.jpg)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku    | Pilihan             | Keterangan               |
| ------------------- | ---------- | ------------- | ------------------- | ------------------------ |
| caption             | string     | Ellipse       | _null_              | Keterangan komponen      |
| width               | float      | 0             | _null_              | Lebar                    |
| height              | float      | 0             | _null_              | Tinggi                   |
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
