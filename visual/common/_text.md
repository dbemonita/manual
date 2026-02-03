```xml
<text>
  <caption>Contoh Teks 1</caption>
  <content>Lorem Ipsum</content>
  <x>100</x>
  <y>100</y>
</text>
```

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                      | Keterangan               |
| ------------------- | ---------- | ---------------------------- | ---------------------------------- | ------------------------ |
| caption             | string     | Text                         | _null_                             | Keterangan komponen      |
| content             | string     | _null_                       | _null_                             | Isi teks                 |
| font                | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf              |
| size                | float      | 12                           | _null_                             | Ukuran huruf             |
| style               | enum       | normal                       | normal; italic                     | Bentuk huruf             |
| weight              | enum       | normal                       | normal; bold                       | Ketebalan huruf          |
| width               | float      | 0                            | _null_                             | Lebar kotak teks         |
| height              | float      | 0                            | _null_                             | Tinggi kotak teks        |
| color               | string     | LightBlue                    | _null_                             | Warna teks               |
| background_color    | string     | rgba(0,0,0,0)                | _null_                             | Warna latar              |
| background_gradient | string     | _null_                       | _null_                             | Warna latar _gradient_\* |
| border_width        | float      | 0                            | _null_                             | Ketebalan garis tepi     |
| border_color        | string     | rgba(0,0,0,0)                | _null_                             | Warna garis tepi         |
| border_radius       | float      | 0                            | _null_                             | Radius garis tepi        |
| anchor              | enum       | start                        | start; middle; end                 | Rata kiri/tengah/kanan   |
| link                | string     | _null_                       | _null_                             | Tautan                   |
| x                   | float      | 0                            | _null_                             | Posisi: Koordinat x      |
| y                   | float      | 0                            | _null_                             | Posisi: Koordinat y      |
| z                   | enum       | 0                            | 0;1;2;3;4;5;6;7;8;9                | Posisi: z-index          |
| rotate              | float      | 0                            | _null_                             | Derajat putaran          |

\*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)

Catatan: Kode simbol/karakter khusus [lihat di sini](ref_unicode).
