# Teks Indikator

Komponen ini berfungsi untuk menunjukkan data titik ukur dalam bentuk teks _boolean_ (misal: `ON|OFF`, `RUN|STOP`, `OPEN|CLOSE`, `GOOD|BAD`, dsb.) berdasarkan nilai yang dikirim oleh _server_. Berikut contoh komponen HMI `indicator_text` (teks indikator):

```xml
<indicator_text>
  <caption>Contoh Teks Indikator 1</caption>
  <point_id>1001</point_id>
  <content>N/A</content>
  <content_0>STOP</content_0>
  <content_1>START</content_1>
  <width>100</width>
  <height>50</height>
  <x>100</x>
  <y>100</y>
</indicator_text>
```

Tag pembuka `<indicator_text>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut                  | Tipe Nilai | Nilai Baku | Keterangan                         |
| ------------------------ | ---------- | ---------- | ---------------------------------- |
| default_color            | string     | _null_     | Nilai baku untuk semua warna teks  |
| default_background_color | string     | _null_     | Nilai baku untuk semua warna latar |

#### Contoh

![indicator_text](https://hackmd.io/_uploads/B1m0H7xIMe.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan             |
| ------------------ | ---------- | ---------------------------- | ------------------------------ | ---------------------- |
| caption            | string     | IndicatorText                | _null_                         | Keterangan komponen    |
| point_id           | int        | 0                            | _null_                         | Titik ukur             |
| font               | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf            |
| size               | float      | 12                           | _null_                         | Ukuran huruf           |
| style              | enum       | normal                       | normal; italic                 | Bentuk huruf           |
| weight             | enum       | normal                       | normal; bold                   | Ketebalan huruf        |
| width              | float      | 0                            | _null_                         | Lebar kotak teks       |
| height             | float      | 0                            | _null_                         | Tinggi kotak teks      |
| content            | string     | n/a                          | _null_                         | Isi teks _initial_     |
| content_0          | string     | _null_                       | _null_                         | Isi teks nilai 0       |
| content_1          | string     | _null_                       | _null_                         | Isi teks nilai 1       |
| color              | string     | LightBlue                    | _null_                         | Warna teks _initial_   |
| color_0            | string     | LightBlue                    | _null_                         | Warna teks nilai 0     |
| color_1            | string     | LightBlue                    | _null_                         | Warna teks nilai 1     |
| background_color   | string     | DarkSlateGray                | _null_                         | Warna latar _initial_  |
| background_color_0 | string     | DarkSlateGray                | _null_                         | Warna latar nilai 0    |
| background_color_1 | string     | DarkSlateGray                | _null_                         | Warna latar nilai 1    |
| border_width       | float      | 2                            | _null_                         | Ketebalan garis tepi   |
| border_color       | string     |                              | _null_                         | Warna garis tepi       |
| border_radius      | float      | 0                            | _null_                         | Radius garis tepi      |
| anchor             | enum       | middle                       | start; middle; end             | Rata kiri/tengah/kanan |
| link               | string     | _null_                       | _null_                         | Tautan                 |
| x                  | float      | 0                            | _null_                         | Posisi: Koordinat x    |
| y                  | float      | 0                            | _null_                         | Posisi: Koordinat y    |
| rotate             | float      | 0                            | _null_                         | Derajat putaran        |
