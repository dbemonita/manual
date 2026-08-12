# Dial Gauge

Berikut contoh komponen HMI `dial_gauge`:

```xml
<dial_gauge>
  <caption>Gauge 1</caption>
  <point_id>1001</point_id>
  <diameter>150</diameter>
  <fill_color_low2>#f73531</fill_color_low2>
  <fill_color_low1>#f76800</fill_color_low1>
  <fill_color_high1>#f6bb00</fill_color_high1>
  <fill_color_high2>#67bf39</fill_color_high2>
  <x>100</x>
  <y>100</y>
</dial_gauge>
```

#### Contoh:

https://playground.monita.co.id/?component=dial_gauge

![dial_gauge](https://hackmd.io/_uploads/HJGDigOIze.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku | Keterangan               |
| ------------------ | ---------- | ---------- | ------------------------ |
| caption            | string     | DialGauge  | Keterangan komponen      |
| point_id           | int        | 0          | ID titik ukur            |
| diameter           | float      | 0          | Diameter                 |
| background_visible | boolean    | _true_     | Menggunakan warna latar? |
| background_color   | string     | #F0F8FF    | Warna latar              |
| hand_color         | string     | #FF4500    | Warna jarum              |
| text_color         | string     | #2F4F4F    | Warna teks               |
| fill_color_low2    | string     | _null_     | Warna batas bawah 2      |
| fill_color_low1    | string     | _null_     | Warna batas bawah 1      |
| fill_color         | string     | _null_     | Warna normal             |
| fill_color_high1   | string     | _null_     | Warna batas atas 1       |
| fill_color_high2   | string     | _null_     | Warna batas atas 2       |
| fill_gradient      | boolean    | _true_     | Gradasi warna batas?     |
| interval           | float      | 20         | Interval _marker_        |
| link               | string     | _null_     | Tautan                   |
| x                  | float      | 0          | Posisi: Koordinat x      |
| y                  | float      | 0          | Posisi: Koordinat y      |
