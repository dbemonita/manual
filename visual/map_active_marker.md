# Marker Aktif

Berikut contoh komponen peta `active_marker` (marker aktif/bergerak):

```xml
<active_marker>
  <caption>Mobil Merah</caption>
  <asset_id>101</asset_id>
  <latitude_id>1001</latitude_id>
  <longitude_id>1002</longitude_id>
  <heading_id>1003</heading_id>
  <icon_source>/images/car_red.png</icon_source>
  <icon_width>50</icon_width>
  <icon_height>50</icon_height>
</active_marker>
```

#### Properti selengkapnya:

| Properti         | Tipe Nilai | Nilai Baku   | Pilihan Nilai | Keterangan                          |
| ---------------- | ---------- | ------------ | ------------- | ----------------------------------- |
| caption          | string     | ActiveMarker | _null_        | Keterangan komponen                 |
| asset_id         | int        | 0            | _null_        | ID aset                             |
| latitude_id      | int        | 0            | _null_        | ID titik ukur latitude              |
| longitude_id     | int        | 0            | _null_        | ID titik ukur longitude             |
| heading_id       | int        | 0            | _null_        | ID titik ukur longitude             |
| icon_source      | string     | _null_       | _null_        | URL icon\*                          |
| icon_color       | string     | auto         | _null_        | Warna icon, bila format icon svg    |
| icon_width       | float      | 50           | _null_        | Lebar icon                          |
| icon_height      | float      | 50           | _null_        | Tinggi icon                         |
| popup_title      | string     | _null_       | _null_        | Judul popup                         |
| popup_open       | boolean    | _false_      | _null_        | Popup otomatis muncul?              |
| popup_point_id1  | int        | 1            | _null_        | Isi popup: ID titik ukur ke-1       |
| popup_point_id2  | int        | 1            | _null_        | Isi popup: ID titik ukur ke-2       |
| popup_point_id3  | int        | 1            | _null_        | Isi popup: ID titik ukur ke-3       |
| popup_point_id4  | int        | 1            | _null_        | Isi popup: ID titik ukur ke-4       |
| popup_point_id5  | int        | 1            | _null_        | Isi popup: ID titik ukur ke-5       |
| popup_auto_close | boolean    | _true_       | _null_        | _Toggle_ popup?                     |
| tooltip_open     | boolean    | _false_      | _null_        | Tooltip otomatis muncul?            |
| decimal          | int        | 2            | _null_        | _Decimal places to round number to_ |
| link             | string     | _null_       | _null_        | Tautan                              |

\*) URL pada properti `source` relatif ke API server.
