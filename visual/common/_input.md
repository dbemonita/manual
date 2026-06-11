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

| Properti                   | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan             |
| -------------------------- | ---------- | ---------------------------- | ------------------------------ | ---------------------- |
| caption                    | string     | ActiveText                   | _null_                         | Keterangan komponen    |
| point_id                   | int        | 0                            | _null_                         | Titik ukur             |
| register_id                | int        | 0                            | _null_                         | Register               |
| input_font \*              | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf            |
| input_size \*              | float      | 12                           | _null_                         | Ukuran huruf           |
| input_style \*             | enum       | normal                       | normal; italic                 | Bentuk huruf           |
| input_weight \*            | enum       | normal                       | normal; bold                   | Ketebalan huruf        |
| input_width                | float      | 0                            | _null_                         | Lebar input            |
| input_height               | float      | 0                            | _null_                         | Tinggi input           |
| input_color \*             | string     | DarkSlateGray                | _null_                         | Warna teks normal      |
| input_background_color \*  | string     | White                        | _null_                         | Warna latar normal     |
| input_border_width \*      | float      | 2                            | _null_                         | Ketebalan garis tepi   |
| input_border_color \*      | string     | SlateGray                    | _null_                         | Warna garis tepi       |
| input_border_radius \*     | float      | 0                            | _null_                         | Radius garis tepi      |
| input_method \*            | string     | emit                         | emit; get; post                | Metode kirim data      |
| input_url \*               | string     | _null_                       | _null_                         | Target pengiriman data |
| input_data \*\*            | string     | _null_                       | _null_                         | Data yang dikirim      |
| button_width               | float      | 0                            | _null_                         | Lebar tombol           |
| button_height              | float      | 0                            | _null_                         | Tinggi tombol          |
| button_image_source \*\*\* | string     | _null_                       | _null_                         | URL gambar tombol\*    |
| direction                  | enum       | horizontal                   | horizontal;vertical            | Posisi gambar tombol   |
| x                          | float      | 0                            | _null_                         | Posisi: Koordinat x    |
| y                          | float      | 0                            | _null_                         | Posisi: Koordinat y    |
| z                          | enum       | 0                            | 0;1;2;3;4;5;6;7;8;9            | Posisi: z-index        |

\*) Tersedia pada versi >= 5.14.0.

\*\*) Contoh data:

- `{"page":1,"limit":10,"search":"john"} // JSON`
- `{page:1,limit:10,search:'john'} // JS-style`

\*\*) URL pada properti `source` relatif ke server berkas statis yang didefinisikan pada berkas `.env`.
