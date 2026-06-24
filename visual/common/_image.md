```xml
<image>
  <caption>Contoh Gambar 1</caption>
  <source>/images/transformator.png</source>
  <width>200</width>
  <height>300</height>
  <x>100</x>
  <y>100</y>
</image>
```

#### Properti selengkapnya:

| Properti       | Tipe Nilai | Nilai Baku    | Pilihan             | Keterangan           |
| -------------- | ---------- | ------------- | ------------------- | -------------------- |
| caption        | string     | Image         | _null_              | Keterangan komponen  |
| source         | string     | _null_        | _null_              | URL gambar\*         |
| width          | float      | 0             | _null_              | Lebar                |
| height         | float      | 0             | _null_              | Tinggi               |
| opacity        | float      | 1             | _null_              | _Opacity_            |
| preserve_ratio | enum       | xMidYMid meet | xMidYMid meet; none | _Preserve ratio_\*\* |
| filter         | float      | 0             | 0.0 s/d 1.0         | _Preserve ratio_\*\* |
| flip           | enum       | _null_        | x; y                | _Flip_               |
| link           | string     | _null_        | _null_              | Tautan               |
| x              | float      | 0             | _null_              | Posisi: Koordinat x  |
| y              | float      | 0             | _null_              | Posisi: Koordinat y  |
| z              | enum       | 0             | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index      |
| rotate         | float      | 0             | _null_              | Derajat putaran      |

\*) URL pada properti `source` relatif ke server `sockelat`.

\*\*) Bila properti `preserve_ratio` diset `none`, maka gambar akan _stretch_ mengikuti properti `width` dan `height`.
