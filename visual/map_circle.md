# Lingkaran

Berikut contoh komponen peta `circle` (lingkaran):

```xml
<circle>
  <caption>Contoh Lingkaran</caption>
  <latlngs>
    [50.5, 30.5]
  </latlngs>
  <radius>200</radius>
  <color>red</color>
</circle>
```

#### Properti selengkapnya:

| Properti     | Tipe Nilai | Nilai Baku | Keterangan          |
| ------------ | ---------- | ---------- | ------------------- |
| caption      | string     | Circle     | Keterangan komponen |
| radius       | float      | 0          | Radius dalam meter  |
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

Komponen ini **berbeda** dari komponen _lingkaran_ pada fitur HMI.
