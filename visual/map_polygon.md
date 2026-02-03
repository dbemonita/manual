# Poligon

Berikut contoh komponen peta `polygon` (poligon):

```xml
<polygon>
  <caption>Contoh Poligon</caption>
  <latlngs>
    [
      [37, -109.05],
      [41, -109.03],
      [41, -102.05],
      [37, -102.04]
    ]
  </latlngs>
  <color>red</color>
</polygon>
```

#### Properti selengkapnya:

| Properti     | Tipe Nilai | Nilai Baku | Keterangan          |
| ------------ | ---------- | ---------- | ------------------- |
| caption      | string     | Polygon    | Keterangan komponen |
| latlngs      | string     | _null_     | _JSON-encoded_      |
| color        | string     | _null_     | Warna garis         |
| weight       | int        | 1          | Ketebalan garis     |
| opacity      | float      | 1.0        | _Opacity_ garis     |
| line_cap     | string     | 'round'    | Bentuk ujung garis  |
| line_join    | string     | 'round'    | Bentuk sudut garis  |
| dash_array   | string     | _null_     | Pola garis          |
| dash_offset  | string     | _null_     | _Offset_ pola garis |
| fill         | boolean    | _false_    | Diberi warna isi?   |
| fill_color   | string     | _null_     | Warna isi           |
| fill_opacity | float      | 0.2        | _Opacity_ warna isi |
| fill_rule    | string     | evenodd    | Pola warna isi      |

#### Catatan

Komponen ini **berbeda** dari komponen _poligon_ pada fitur HMI.
