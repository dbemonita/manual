# Garis

Berikut contoh komponen peta `polyline` (garis):

```xml
<polyline>
  <caption>Contoh Garis</caption>
  <latlngs>
    [
      [45.51, -122.68],
      [37.77, -122.43],
      [34.04, -118.2]
    ]
  </latlngs>
  <color>red</color>
</polyline>
```

#### Properti selengkapnya:

| Properti     | Tipe Nilai | Nilai Baku | Keterangan          |
| ------------ | ---------- | ---------- | ------------------- |
| caption      | string     | Polyline   | Keterangan komponen |
| latlngs      | string     |            | _JSON-encoded_      |
| color        | string     |            | Warna garis         |
| weight       | int        | 1          | Ketebalan garis     |
| opacity      | float      | 1.0        | _Opacity_ garis     |
| line_cap     | string     | 'round'    | Bentuk ujung garis  |
| line_join    | string     | 'round'    | Bentuk sudut garis  |
| dash_array   | string     |            | Pola garis          |
| dash_offset  | string     |            | _Offset_ pola garis |
| fill         | boolean    | _false_    | Diberi warna isi?   |
| fill_color   | string     |            | Warna isi           |
| fill_opacity | float      | 0.2        | _Opacity_ warna isi |
| fill_rule    | string     | evenodd    | Pola warna isi      |

#### Catatan

Komponen ini **berbeda** dari komponen _garis_ pada fitur HMI.
