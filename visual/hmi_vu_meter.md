# VU Meter

Berikut contoh komponen HMI `vu_meter`:

```xml
<vu_meter>
  <caption>Contoh VU Meter 1</caption>
  <point_id>1001</point_id>
  <width>200</width>
  <x>100</x>
  <y>100</y>
</vu_meter>
```

#### Contoh:

https://playground.monita.co.id/?component=vu_meter

![vu_meter](https://manual.monita.co.id/_assets/images/vu_meter.png)

| Properti | Tipe Nilai | Nilai Baku | Pilihan Nilai | Keterangan          |
| -------- | ---------- | ---------- | ------------- | ------------------- |
| caption  | string     | ActiveText |               | Keterangan komponen |
| point_id | int        | 0          |               | Titik ukur          |
| decimal  | int        | 2          |               | Jumlah desimal      |
| unit     | string     |            |               | Satuan              |
| width    | float      | 0          |               | Lebar kotak teks    |
