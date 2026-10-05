```xml
<toggle>
  <caption>Contoh Toggle 1</caption>
  <point_id>1001</point_id>
  <register_id>100</register_id>
  <width>100</width>
  <height>50</height>
  <image_source>/images/toggle_idle.png</image_source>
  <image_source_0>/images/toggle_off.png</image_source_0>
  <image_source_1>/images/toggle_on.png</image_source_1>
  <x>100</x>
  <y>100</y>
</toggle>
```

#### Contoh:

https://playground.monita.co.id/?component=toggle

#### Properti selengkapnya:

| Properti       | Tipe Nilai | Nilai Baku | Pilihan Nilai       | Keterangan               |
| -------------- | ---------- | ---------- | ------------------- | ------------------------ |
| caption        | string     | ActiveText |                     | Keterangan komponen      |
| point_id       | int        | 0          |                     | Titik ukur               |
| register_id    | int        | 0          |                     | Register pada _hardware_ |
| width          | float      | 0          |                     | Lebar                    |
| height         | float      | 0          |                     | Tinggi                   |
| image_source   | string     |            |                     | URL gambar idle \*\*     |
| image_source_0 | string     |            |                     | URL gambar off \*\*      |
| image_source_1 | string     |            |                     | URL gambar on \*\*       |
| allowed_roles  | string     | 1,2        |                     | Role user \*             |
| x              | float      | 0          |                     | Posisi: Koordinat x      |
| y              | float      | 0          |                     | Posisi: Koordinat y      |
| z              | enum       | 0          | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index          |

#### Catatan

- \*) Tersedia pada versi >= 5.14.0. Separator koma. Roles:
  - 1 = Root
  - 2 = Admin
  - 3 = Operator
  - 4 = Editor
- \*\*) URL pada properti `source` relatif ke server `sockelat`.
