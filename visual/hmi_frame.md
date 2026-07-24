# Bingkai

Berikut contoh komponen HMI `frame` (bingkai):

```xml
<frame>
  <caption>Contoh Frame 1</caption>
  <title>Power Meter 1</title>
  <width>300</width>
  <height>200</height>
  <x>100</x>
  <y>100</y>
</frame>
```

#### Contoh

![frame](https://hackmd.io/_uploads/rk3KNhlBzl.jpg)

#### Properti selengkapnya:

| Properti         | Tipe Nilai | Nilai Baku                   | Pilihan             | Keterangan            |
| ---------------- | ---------- | ---------------------------- | ------------------- | --------------------- |
| caption          | string     | Frame                        | _null_              | Keterangan komponen   |
| title            | string     | _null_                       | _null_              | Judul bingkai         |
| font             | string     | Arial, Helvetica, sans-serif | _null_              | Jenis huruf judul     |
| size             | float      | 12                           | _null_              | Ukuran huruf judul    |
| weight           | enum       | normal                       | normal; bold        | Ketebalan huruf judul |
| color            | string     | White                        | _null_              | Warna huruf judul     |
| width            | float      | 0                            | _null_              | Lebar                 |
| height           | float      | 0                            | _null_              | Tinggi                |
| background_color | string     | LightSlateGray               | _null_              | Warna latar           |
| fill_color       | string     | White                        | _null_              | Warna isi bingkai     |
| border_color     | string     | \_null\_\_                   | _null_              | Warna tepi bingkai    |
| link             | string     | _null_                       | _null_              | Tautan                |
| x                | float      | 0                            | _null_              | Posisi: Koordinat x   |
| y                | float      | 0                            | _null_              | Posisi: Koordinat y   |
| z                | enum       | 0                            | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index       |
