```xml
<select>
  <caption>Contoh select 1</caption>
  <point_id>1001</point_id>
  <register_id>100</register_id>
  <select_width>100</select_width>
  <select_height>50</select_height>
  <button_width>100</button_width>
  <button_height>50</button_height>
  <select_options>1,2,3</select_options>
  <button_image_source>/images/button.png</button_image_source>
  <x>100</x>
  <y>100</y>
</select>
```

#### Contoh:

https://playground.monita.co.id/?component=select

#### Properti selengkapnya:

| Properti                | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan                 |
| ----------------------- | ---------- | ---------------------------- | ------------------------------ | -------------------------- |
| caption                 | string     | ActiveText                   |                                | Keterangan komponen        |
| point_id                | int        | 0                            |                                | Titik ukur                 |
| register_id             | int        | 0                            |                                | Register pada _hardware_   |
| select_font             | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf                |
| select_size             | float      | 12                           |                                | Ukuran huruf               |
| select_style            | enum       | normal                       | normal; italic                 | Bentuk huruf               |
| select_weight           | enum       | normal                       | normal; bold                   | Ketebalan huruf            |
| select_width            | float      | 0                            |                                | Lebar select               |
| select_height           | float      | 0                            |                                | Tinggi select              |
| select_color            | string     | DarkSlateGray                |                                | Warna teks normal          |
| select_background_color | string     | White                        |                                | Warna latar normal         |
| select_border_width     | float      | 2                            |                                | Ketebalan garis tepi       |
| select_border_color     | string     | LightGray                    |                                | Warna garis tepi           |
| select_border_radius    | float      | 0                            |                                | Radius garis tepi          |
| select_options          | string     |                              |                                | Pilihan pada select \*     |
| select_method           | string     | emit                         | emit; get; post                | Metode kirim data          |
| select_url              | string     |                              |                                | Target pengiriman data     |
| select_data             | string     |                              |                                | Data yang dikirim \*\*     |
| button_width            | float      | 0                            |                                | Lebar tombol               |
| button_height           | float      | 0                            |                                | Tinggi tombol              |
| button_image_source     | string     |                              |                                | URL gambar tombol \*\*\*\* |
| allowed_roles           | string     | 1,2                          |                                | Role user \*\*\*           |
| direction               | enum       | horizontal                   | horizontal;vertical            | Posisi gambar tombol       |
| x                       | float      | 0                            |                                | Posisi: Koordinat x        |
| y                       | float      | 0                            |                                | Posisi: Koordinat y        |
| z                       | enum       | 0                            | 0;1;2;3;4;5;6;7;8;9            | Posisi: z-index            |

#### Catatan

Komponen ini tersedia pada versi 5.17.0.

- \*) Contoh: `1,2,3` atau `1:Satu, 2:Dua, 3:Tiga`. Menggunakan separator koma untuk memisahkan antar pilihan.
- \*\*) Tag `select_data` menggunakan format loket Monita: i=SN device, j=Jumlah data, dl=data, f=flag, ts=timestamp.
  - `i:CY1-VIR; j:1; dl:{{select}}; f:0; ts:{{timestamp}}`, _atau_
  - `i:CY1-VIR; dl:{{select}}; ts:{{timestamp}}`, _atau_
  - `i:CY1-VIR`
  - Sehingga, jika `j`, `dl`, `f`, dan `ts` tidak didefinisikan, maka akan otomatis terisi.
- \*\*\*) Separator koma. Roles:
  - 1 = Root
  - 2 = Admin
  - 3 = Operator
  - 4 = Editor
- \*\*\*\*) URL pada properti `button_image_source` relatif ke server `sockelat`.
