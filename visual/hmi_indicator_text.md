# Teks Indikator

Komponen ini berfungsi untuk menunjukkan data titik ukur dalam bentuk teks _boolean_ (misal: `ON|OFF`, `RUN|STOP`, `OPEN|CLOSE`, `GOOD|BAD`, dsb.) berdasarkan nilai yang dikirim oleh _server_. Berikut contoh komponen HMI `indicator_text` (teks indikator):

```xml
<indicator_text default_background_color="#68957c" default_color="white">
  <caption>Contoh Teks Indikator 1</caption>
  <point_id>1001</point_id>
  <content>IDLE</content>
  <content_0>STOP</content_0>
  <content_1>START</content_1>
  <width>150</width>
  <height>75</height>
  <size>28</size>
  <border_width>0</border_width>
  <x>100</x>
  <y>100</y>
</indicator_text>
```

Tag pembuka `<indicator_text>` tersebut memiliki atribut-atribut sebagai berikut:

| Atribut                  | Tipe Nilai | Nilai Baku | Keterangan                         |
| ------------------------ | ---------- | ---------- | ---------------------------------- |
| default_color            | string     |            | Nilai baku untuk semua warna teks  |
| default_background_color | string     |            | Nilai baku untuk semua warna latar |

#### Contoh:

https://playground.monita.co.id/?component=indicator_text

![indicator_text](https://hackmd.io/_uploads/B1m0H7xIMe.png)

#### Properti selengkapnya:

| Properti           | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan             |
| ------------------ | ---------- | ---------------------------- | ------------------------------ | ---------------------- |
| caption            | string     | IndicatorText                |                                | Keterangan komponen    |
| point_id           | int        | 0                            |                                | Titik ukur             |
| font               | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf            |
| size               | float      | 12                           |                                | Ukuran huruf           |
| style              | enum       | normal                       | normal; italic                 | Bentuk huruf           |
| weight             | enum       | normal                       | normal; bold                   | Ketebalan huruf        |
| width              | float      | 0                            |                                | Lebar kotak teks       |
| height             | float      | 0                            |                                | Tinggi kotak teks      |
| content            | string     | n/a                          |                                | Isi teks _initial_     |
| content_0          | string     |                              |                                | Isi teks nilai 0       |
| content_1          | string     |                              |                                | Isi teks nilai 1       |
| color              | string     | LightBlue                    |                                | Warna teks _initial_   |
| color_0            | string     | LightBlue                    |                                | Warna teks nilai 0     |
| color_1            | string     | LightBlue                    |                                | Warna teks nilai 1     |
| background_color   | string     | DarkSlateGray                |                                | Warna latar _initial_  |
| background_color_0 | string     | DarkSlateGray                |                                | Warna latar nilai 0    |
| background_color_1 | string     | DarkSlateGray                |                                | Warna latar nilai 1    |
| border_width       | float      | 2                            |                                | Ketebalan garis tepi   |
| border_color       | string     |                              |                                | Warna garis tepi       |
| border_radius      | float      | 0                            |                                | Radius garis tepi      |
| anchor             | enum       | middle                       | start; middle; end             | Rata kiri/tengah/kanan |
| link               | string     |                              |                                | Tautan                 |
| x                  | float      | 0                            |                                | Posisi: Koordinat x    |
| y                  | float      | 0                            |                                | Posisi: Koordinat y    |
| rotate             | float      | 0                            |                                | Derajat putaran        |
