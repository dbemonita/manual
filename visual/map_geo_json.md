# GeoJson

Berikut contoh komponen peta `geo_json`:

```xml
<geo_json>
  <caption>Contoh GeoJson</caption>
  <source>/json/feature.json</source>
  <color>red</color>
</geo_json>
```

#### Properti selengkapnya:

| Properti     | Tipe Nilai | Nilai Baku | Keterangan                 |
| ------------ | ---------- | ---------- | -------------------------- |
| caption      | string     | Polygon    | Keterangan komponen        |
| source       | string     | _null_     | _Relative url_ berkas JSON |
| color        | string     | _null_     | Warna garis                |
| weight       | int        | 1          | Ketebalan garis            |
| opacity      | float      | 1.0        | _Opacity_ garis            |
| line_cap     | string     | 'round'    | Bentuk ujung garis         |
| line_join    | string     | 'round'    | Bentuk sudut garis         |
| dash_array   | string     | _null_     | Pola garis                 |
| dash_offset  | string     | _null_     | _Offset_ pola garis        |
| fill         | boolean    | _false_    | Diberi warna isi?          |
| fill_color   | string     | _null_     | Warna isi                  |
| fill_opacity | float      | 0.2        | _Opacity_ warna isi        |
| fill_rule    | string     | evenodd    | Pola warna isi             |
