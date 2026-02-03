# Kotak

Berikut contoh komponen peta `rect` (alias: `rectangle`):

```xml
<rect>
  <caption>Contoh Kotak</caption>
  <latlngs>
    [
      [54.559322, -5.767822],
      [56.1210604, -3.021240]
    ]
  </latlngs>
  <color>red</color>
</rect>
```

#### Properti selengkapnya:

| Properti     | Tipe Nilai | Nilai Baku | Keterangan          |
| ------------ | ---------- | ---------- | ------------------- |
| caption      | string     | Rectangle  | Keterangan komponen |
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

Komponen ini **berbeda** dari komponen _kotak_ pada fitur HMI.
