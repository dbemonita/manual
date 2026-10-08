# Marker

Berikut contoh komponen peta `marker` (marker statis/diam):

```xml
<marker>
  <caption>Marker 1</caption>
  <asset_id>101</asset_id>
  <latitude>-6.164</latitude>
  <longitude>106.822</longitude>
  <icon_source>/images/marker.png</icon_source>
  <icon_width>50</icon_width>
  <icon_height>50</icon_height>
</marker>
```

#### Properti selengkapnya:

| Properti         | Tipe Nilai | Nilai Baku | Pilihan Nilai | Keterangan                          |
| ---------------- | ---------- | ---------- | ------------- | ----------------------------------- |
| caption          | string     | Marker     |               | Keterangan komponen                 |
| asset_id         | int        | 0          |               | ID aset                             |
| latitude         | float      | 0          |               | Nilai latitude                      |
| longitude        | float      | 0          |               | Nilai longitude                     |
| icon_source      | string     |            |               | URL icon\*                          |
| icon_color       | string     | auto       |               | Warna icon, bila format icon svg    |
| icon_width       | float      | 25         |               | Lebar icon                          |
| icon_height      | float      | 40         |               | Tinggi icon                         |
| popup_title      | string     |            |               | Judul popup                         |
| popup_open       | boolean    | _false_    |               | Popup otomatis muncul?              |
| popup_point_id1  | int        | 1          |               | Isi popup: ID titik ukur ke-1       |
| popup_point_id2  | int        | 1          |               | Isi popup: ID titik ukur ke-2       |
| popup_point_id3  | int        | 1          |               | Isi popup: ID titik ukur ke-3       |
| popup_point_id4  | int        | 1          |               | Isi popup: ID titik ukur ke-4       |
| popup_point_id5  | int        | 1          |               | Isi popup: ID titik ukur ke-5       |
| popup_auto_close | boolean    | _true_     |               | _Toggle_ popup?                     |
| tooltip_open     | boolean    | _false_    |               | Tooltip otomatis muncul?            |
| decimal          | int        | 2          |               | _Decimal places to round number to_ |
| link             | string     |            |               | Tautan                              |

- \*) URL pada properti `source` relatif ke API server.
