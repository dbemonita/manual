# Gambar Indikator

Komponen ini berfungsi untuk menunjukkan data titik ukur dalam bentuk gambar dengan data _boolean_ (misal: `ON|OFF`, `RUN|STOP`, `OPEN|CLOSE`, `GOOD|BAD`, dsb.) berdasarkan nilai yang dikirim oleh _server_. Berikut contoh komponen HMI `indicator_image` (gambar indikator):

```xml
<indicator_image>
  <caption>Contoh Gambar Indikator 1</caption>
  <point_id>1001</point_id>
  <source>/images/propeller_na.png</source>
  <source_0>/images/propeller_off.png</source_0>
  <source_1>/images/propeller_on.png</source_1>
  <animation>rotate</animation>
  <width>200</width>
  <height>200</height>
  <x>100</x>
  <y>100</y>
</indicator_image>
```

#### Contoh

![indicator_image](https://hackmd.io/_uploads/HkEr3mlUzg.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku     | Pilihan Nilai         | Keterangan              |
| ------------------ | ---------- | -------------- | --------------------- | ----------------------- |
| caption            | string     | IndicatorImage | _null_                | Keterangan komponen     |
| point_id           | int        | 0              | _null_                | Titik ukur              |
| width              | float      | 0              | _null_                | Lebar gambar            |
| height             | float      | 0              | _null_                | Tinggi gambar           |
| source             | string     | _null_         | _null_                | URL gambar _initial_\*  |
| source_0           | string     | _null_         | _null_                | URL gambar nilai 0\*    |
| source_1           | string     | _null_         | _null_                | URL gambar nilai 1\*    |
| animation          | enum       | _null_         | rotate; move; reverse | Jenis animasi           |
| animation_duration | string     | _null_         | _null_                | Durasi animasi (ms)     |
| preserve_ratio     | enum       | xMidYMid meet  | xMidYMid meet; none   | _Preserve ratio_\*\*    |
| link               | string     | _null_         | _null_                | Tautan                  |
| x                  | float      | 0              | _null_                | Posisi: Koordinat x     |
| y                  | float      | 0              | _null_                | Posisi: Koordinat y     |
| from_x             | float      | 0              | _null_                | Gerak dari: Koordinat x |
| from_y             | float      | 0              | _null_                | Gerak dari: Koordinat y |
| to_x               | float      | 0              | _null_                | Gerak ke: Koordinat x   |
| to_y               | float      | 0              | _null_                | Gerak ke: Koordinat y   |

#### Catatan:

- Pastikan gambar pada `source`, `source_0`, `source_1` memiliki dimensi yang sama.
- Untuk animasi `rotate`, pastikan nilai `from_x` dan `to_x` sama dengan `x`. Lalu, `from_y` dan `to_y` sama dengan `y`.
- Properti `from_x`, `from_y`, `to_x`, `to_y` hanya perlu didefinisikan bila properti `animation` juga didefinisikan `move` atau `reverse`. Pada kondisi ini, properti `x`, `y` dapat diabaikan.

\*) URL pada properti `source` relatif ke server `sockelat`.

\*\*) Bila properti `preserve_ratio` diset `none`, maka gambar akan _stretch_ mengikuti properti `width` dan `height`.
