```xml
<solid_gauge>
  <caption>Solid Gauge 1</caption>
  <point_id>1001</point_id>
  <width>300</width>
  <unit>&#x2103;</unit> <!--°C-->
  <x>100</x>
  <y>100</y>
</solid_gauge>
```

#### Contoh:

https://playground.monita.co.id/?component=solid_gauge

![solid_gauge](https://manual.monita.co.id/_assets/images/solid_gauge.png)

#### Properti selengkapnya:

| Properti         | Tipe Nilai | Nilai Baku  | Keterangan          |
| ---------------- | ---------- | ----------- | ------------------- |
| caption          | string     | SolidGauge  | Keterangan komponen |
| point_id         | int        | 0           | ID titik ukur       |
| decimal          | int        | 2           | Jumlah desimal      |
| unit             | string     |             | Satuan              |
| width            | float      | 0           | Lebar area _gauge_  |
| color            | string     | White       | Warna teks          |
| background_color | string     | AliceBlue   | Warna latar         |
| border_color     | string     | White       | Warna jarum         |
| fill_color_low2  | string     | DeepSkyBlue | Warna batas bawah 2 |
| fill_color_low1  | string     | DeepSkyBlue | Warna batas bawah 1 |
| fill_color       | string     | DeepSkyBlue | Warna normal        |
| fill_color_high1 | string     | DeepSkyBlue | Warna batas atas 1  |
| fill_color_high2 | string     | DeepSkyBlue | Warna batas atas 2  |
| value_visible    | boolean    | true        | Tampilkan nilai?    |
| x                | float      | 0           | Posisi: Koordinat x |
| y                | float      | 0           | Posisi: Koordinat y |
