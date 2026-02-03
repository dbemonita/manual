# Bar Gauge

Berikut contoh komponen HMI `bar_gauge`:

```xml
<bar_gauge>
  <caption>Contoh Bar Gauge 1</caption>
  <point_id>1001</point_id>
  <width>50</width>
  <height>100</height>
  <x>225</x>
  <y>300</y>
</bar_gauge>
```

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku | Keterangan                   |
| ------------------ | ---------- | ---------- | ---------------------------- |
| caption            | string     | BarGauge   | Keterangan komponen          |
| point_id           | int        | 0          | ID titik ukur                |
| width              | float      | 0          | Lebar                        |
| height             | float      | 0          | Tinggi                       |
| marker_num         | int        | 10         | Jumlah _marker_              |
| marker_color_off   | string     | _null_     | Warna _marker_ posisi off    |
| marker_color_low2  | string     | #2F4F4F    | Warna _marker_ batas bawah 2 |
| marker_color_low1  | string     | #2F4F4F    | Warna _marker_ batas bawah 1 |
| marker_color       | string     | #2F4F4F    | Warna _marker_ batas tengah  |
| marker_color_high1 | string     | #2F4F4F    | Warna _marker_ batas atas 1  |
| marker_color_high2 | string     | #2F4F4F    | Warna _marker_ batas atas 2  |
| link               | string     | _null_     | Tautan                       |
| x                  | float      | 0          | Posisi: Koordinat x          |
| y                  | float      | 0          | Posisi: Koordinat y          |
| rotate             | float      | 0          | Derajat putaran              |
