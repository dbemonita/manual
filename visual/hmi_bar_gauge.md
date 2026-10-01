# Bar Gauge

Berikut contoh komponen HMI `bar_gauge`:

```xml
<bar_gauge>
  <caption>Contoh Bar Gauge 1</caption>
  <point_id>1001</point_id>
  <width>75</width>
  <height>150</height>
  <x>100</x>
  <y>100</y>
</bar_gauge>
```

#### Contoh:

https://playground.monita.co.id/?component=bar_gauge

![bar_gauge](https://manual.monita.co.id/_assets/images/bar_gauge.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku | Keterangan                   |
| ------------------ | ---------- | ---------- | ---------------------------- |
| caption            | string     | BarGauge   | Keterangan komponen          |
| point_id           | int        | 0          | ID titik ukur                |
| width              | float      | 0          | Lebar                        |
| height             | float      | 0          | Tinggi                       |
| marker_num         | int        | 10         | Jumlah _marker_              |
| marker_color_off   | string     |            | Warna _marker_ posisi off    |
| marker_color_low2  | string     | #ef4444    | Warna _marker_ batas bawah 2 |
| marker_color_low1  | string     | #f97316    | Warna _marker_ batas bawah 1 |
| marker_color       | string     | #eab308    | Warna _marker_ batas tengah  |
| marker_color_high1 | string     | #84cc16    | Warna _marker_ batas atas 1  |
| marker_color_high2 | string     | #22c55e    | Warna _marker_ batas atas 2  |
| link               | string     |            | Tautan                       |
| x                  | float      | 0          | Posisi: Koordinat x          |
| y                  | float      | 0          | Posisi: Koordinat y          |
