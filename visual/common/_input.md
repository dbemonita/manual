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

#### Contoh:

https://playground.monita.co.id/?component=input

![input](https://manual.monita.co.id/_assets/images/input.png)

#### Properti selengkapnya:

| Properti               | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan                 |
| ---------------------- | ---------- | ---------------------------- | ------------------------------ | -------------------------- |
| caption                | string     | ActiveText                   |                                | Keterangan komponen        |
| point_id               | int        | 0                            |                                | Titik ukur                 |
| register_id            | int        | 0                            |                                | Register pada _hardware_   |
| input_font             | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf \*             |
| input_size             | float      | 12                           |                                | Ukuran huruf \*            |
| input_style            | enum       | normal                       | normal; italic                 | Bentuk huruf \*            |
| input_weight           | enum       | normal                       | normal; bold                   | Ketebalan huruf \*         |
| input_width            | float      | 0                            |                                | Lebar input                |
| input_height           | float      | 0                            |                                | Tinggi input               |
| input_color            | string     | DarkSlateGray                |                                | Warna teks normal \*       |
| input_background_color | string     | White                        |                                | Warna latar normal \*      |
| input_border_width     | float      | 2                            |                                | Ketebalan garis tepi \*    |
| input_border_color     | string     | LightGray                    |                                | Warna garis tepi \*        |
| input_border_radius    | float      | 0                            |                                | Radius garis tepi \*       |
| input_method           | string     | emit                         | emit; get; post                | Metode kirim data \*       |
| input_url              | string     |                              |                                | Target pengiriman data \*  |
| input_data             | string     |                              |                                | Data yang dikirim \*\*     |
| button_width           | float      | 0                            |                                | Lebar tombol               |
| button_height          | float      | 0                            |                                | Tinggi tombol              |
| button_image_source    | string     |                              |                                | URL gambar tombol \*\*\*\* |
| allowed_roles          | string     | 1,2                          |                                | Role user \*\*\*           |
| direction              | enum       | horizontal                   | horizontal;vertical            | Posisi gambar tombol       |
| x                      | float      | 0                            |                                | Posisi: Koordinat x        |
| y                      | float      | 0                            |                                | Posisi: Koordinat y        |
| z                      | enum       | 0                            | 0;1;2;3;4;5;6;7;8;9            | Posisi: z-index            |

#### Catatan

- \*) Tersedia pada versi >= 5.14.0.
- \*\*) Tersedia pada versi >= 5.14.0. Tag `input_data` menggunakan format loket Monita: i=SN device, j=Jumlah data, dl=data, f=flag, ts=timestamp.
  - `i:CY1-VIR; j:1; dl:{{input}}; f:0; ts:{{timestamp}}`, _atau_
  - `i:CY1-VIR; dl:{{input}}; ts:{{timestamp}}`, _atau_
  - `i:CY1-VIR`
  - Sehingga, jika `j`, `dl`, `f`, dan `ts` tidak didefinisikan, maka akan otomatis terisi.
- \*\*\*) Tersedia pada versi >= 5.14.0. Separator koma. Roles:
  - 1 = Root
  - 2 = Admin
  - 3 = Operator
  - 4 = Editor
- \*\*\*\*) URL pada properti `button_image_source` relatif ke server `sockelat`.
