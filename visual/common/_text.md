```xml
<text>
  <caption>Contoh Teks 1</caption>
  <content>The quick brown fox jumps over the lazy dog</content>
  <size>32</size>
  <font>Comic Sans MS</font>
  <x>100</x>
  <y>100</y>
</text>

<text>
  <caption>Contoh Teks 2</caption>
  <content>The quick brown fox jumps over the lazy dog</content>
  <size>32</size>
  <font>Consolas</font>
  <x>100</x>
  <y>200</y>
</text>

<text>
  <caption>Contoh Teks 3</caption>
  <content>The quick brown fox jumps over the lazy dog</content>
  <size>32</size>
  <font>Franklin Gothic Medium Cond</font>
  <x>100</x>
  <y>300</y>
</text>
```

#### Contoh:

https://playground.monita.co.id/?component=text

![text](https://manual.monita.co.id/_assets/images/text.png)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                  | Keterangan                |
| ------------------- | ---------- | ---------------------------- | ------------------------------ | ------------------------- |
| caption             | string     | Text                         |                                | Keterangan komponen       |
| content             | string     |                              |                                | Isi teks                  |
| font                | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf               |
| size                | float      | 12                           |                                | Ukuran huruf              |
| style               | enum       | normal                       | normal; italic                 | Bentuk huruf              |
| weight              | enum       | normal                       | normal; bold                   | Ketebalan huruf           |
| width               | float      | 0                            |                                | Lebar kotak teks          |
| height              | float      | 0                            |                                | Tinggi kotak teks         |
| color               | string     | LightBlue                    |                                | Warna teks                |
| background_color    | string     | rgba(0,0,0,0)                |                                | Warna latar               |
| background_gradient | string     |                              |                                | Warna latar _gradient_ \* |
| border_width        | float      | 0                            |                                | Ketebalan garis tepi      |
| border_color        | string     | rgba(0,0,0,0)                |                                | Warna garis tepi          |
| border_radius       | float      | 0                            |                                | Radius garis tepi         |
| anchor              | enum       | start                        | start; middle; end             | Rata kiri/tengah/kanan    |
| link                | string     |                              |                                | Tautan                    |
| x                   | float      | 0                            |                                | Posisi: Koordinat x       |
| y                   | float      | 0                            |                                | Posisi: Koordinat y       |
| z                   | enum       | 0                            | 0;1;2;3;4;5;6;7;8;9            | Posisi: z-index           |
| rotate              | float      | 0                            |                                | Derajat putaran           |

- \*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)

Catatan: Kode simbol/karakter khusus [lihat di sini](ref_unicode).
