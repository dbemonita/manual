# Kompas

Berikut contoh komponen HMI `compass` (kompas):

```xml
<compass>
  <caption>Contoh Kompas 1</caption>
  <point_id>1001</point_id>
  <diameter>200</diameter>
  <x>100</x>
  <y>100</y>
</compass>
```

#### Contoh:

https://playground.monita.co.id/?component=compass

![compass](https://manual.monita.co.id/_assets/images/compass.png)

| Properti | Tipe Nilai | Nilai Baku | Pilihan Nilai | Keterangan          |
| -------- | ---------- | ---------- | ------------- | ------------------- |
| caption  | string     | ActiveText |               | Keterangan komponen |
| point_id | int        | 0          |               | Titik ukur          |
| decimal  | int        | 2          |               | Jumlah desimal      |
| diameter | float      | 0          |               | Diameter kompas     |
