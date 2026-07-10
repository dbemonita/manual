```xml
<toggle>
  <caption>Contoh Toggle 1</caption>
  <point_id>1001</point_id>
  <register_id>100</register_id>
  <width>100</width>
  <height>50</height>
  <source>/images/button_iddle.png</source>
  <source_0>/images/button_off.png</source_0>
  <source_1>/images/button_on.png</source_1>
  <x>100</x>
  <y>100</y>
</toggle>
```

#### Properti selengkapnya:

| Properti      | Tipe Nilai | Nilai Baku | Pilihan Nilai       | Keterangan               |
| ------------- | ---------- | ---------- | ------------------- | ------------------------ |
| caption       | string     | ActiveText | _null_              | Keterangan komponen      |
| point_id      | int        | 0          | _null_              | Titik ukur               |
| register_id   | int        | 0          | _null_              | Register pada _hardware_ |
| width         | float      | 0          | _null_              | Lebar                    |
| height        | float      | 0          | _null_              | Tinggi                   |
| source        | string     | _null_     | _null_              | URL gambar idle \*\*     |
| source_0      | string     | _null_     | _null_              | URL gambar off \*\*      |
| source_1      | string     | _null_     | _null_              | URL gambar on \*\*       |
| allowed_roles | string     | 1,2        | _null_              | Role user \*             |
| x             | float      | 0          | _null_              | Posisi: Koordinat x      |
| y             | float      | 0          | _null_              | Posisi: Koordinat y      |
| z             | enum       | 0          | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index          |

#### Catatan

- \*) Tersedia pada versi >= 5.14.0. Separator koma. Roles:
  - 1 = Root
  - 2 = Admin
  - 3 = Operator
  - 4 = Editor
- \*\*) URL pada properti `source` relatif ke server `sockelat`.
