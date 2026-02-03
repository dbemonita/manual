```xml
<input>
  <caption>Contoh Input 1</caption>
  <point_id>1001</point_id>
  <register_id>100</register_id>
  <input_width>100</input_width>
  <input_height>50</input_height>
  <button_width>100</button_width>
  <button_height>50</button_height>
  <button_image_source>/images/button.png</button_image_source>
  <x>100</x>
  <y>100</y>
</input>
```

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku | Pilihan Nilai       | Keterangan           |
| ------------------- | ---------- | ---------- | ------------------- | -------------------- |
| caption             | string     | ActiveText | _null_              | Keterangan komponen  |
| point_id            | int        | 0          | _null_              | Titik ukur           |
| register_id         | int        | 0          | _null_              | Register             |
| input_width         | float      | 0          | _null_              | Lebar input          |
| input_height        | float      | 0          | _null_              | Tinggi input         |
| button_width        | float      | 0          | _null_              | Lebar tombol         |
| button_height       | float      | 0          | _null_              | Tinggi tombol        |
| button_image_source | string     | _null_     | _null_              | URL gambar tombol\*  |
| direction           | enum       | horizontal | horizontal;vertical | Posisi gambar tombol |
| x                   | float      | 0          | _null_              | Posisi: Koordinat x  |
| y                   | float      | 0          | _null_              | Posisi: Koordinat y  |
| z                   | enum       | 0          | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index      |

\*) URL pada properti `source` relatif ke server berkas statis yang didefinisikan pada berkas `.env`.
