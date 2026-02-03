# Overlay

Berikut contoh komponen peta `overlay`:

```xml
<overlay>
  <caption>Wind</caption>
  <url>http://{s}.tile.openweathermap.org/map/wind/{z}/{x}/{y}.png?appid={apiKey}</url>
  <api_key>l0r3m1p5umd0l0r51t4m3t</api_key>
  <attribution>Map data &#xa9; OpenWeatherMap</attribution>
  <opacity>0.5</opacity>
</overlay>
```

#### Properti selengkapnya:

| Properti      | Tipe Nilai | Nilai Baku | Keterangan                          |
| ------------- | ---------- | ---------- | ----------------------------------- |
| caption       | string     | Overlay    | Keterangan komponen                 |
| url           | string     | _null_     | URL _tile layer_                    |
| subdomains    | string     | abc        | Keterangan komponen                 |
| min_zoom      | int        | 0          | _Zoom_ minimum                      |
| max_zoom      | int        | 18         | _Zoom_ maksimum                     |
| zoom_offset   | int        | 0          | _Zoom offset_                       |
| zoom_reverse  | boolean    | _false_    | Membalik nilai _zoom_?              |
| tms           | boolean    | _false_    | Membalik sumbu Y?                   |
| detect_retina | boolean    | _false_    | Deteksi _retina display_?           |
| cross_origin  | any        | _false_    | Menggunakan atribut _corss origin_? |

#### Properti tambahan (opsional) sesuai kebutuhan penyedia layanan _tile layer_:

| Properti    | Tipe Nilai | Nilai Baku | Keterangan                    |
| ----------- | ---------- | ---------- | ----------------------------- |
| api_key     | string     | _null_     | Nilai parameter _apiKey_      |
| map_id      | string     | _null_     | Nilai parameter _mapID_       |
| attribution | string     | _null_     | Nilai parameter _attribution_ |
| bounds      | string     | _null_     | Nilai parameter _bounds_      |
| base        | string     | _null_     | Nilai parameter _base_        |
| variant     | string     | _null_     | Nilai parameter _variant_     |
| opacity     | string     | _null_     | Nilai parameter _opacity_     |
| style       | string     | _null_     | Nilai parameter _style_       |
| type        | string     | _null_     | Nilai parameter _type_        |
| size        | string     | _null_     | Nilai parameter _size_        |
| format      | string     | _null_     | Nilai parameter _format_      |
| ext         | string     | _null_     | Nilai parameter _ext_         |
| language    | string     | _null_     | Nilai parameter _language_    |
