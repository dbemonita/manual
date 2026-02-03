```xml
<timestamp>
  <caption>Contoh Timestamp 1</caption>
  <width>100</width>
  <height>50</height>
  <x>100</x>
  <y>100</y>
</timestamp>
```

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku                   | Pilihan Nilai                      | Keterangan                  |
| ------------------- | ---------- | ---------------------------- | ---------------------------------- | --------------------------- |
| caption             | string     | Timestamp                    | _null_                             | Keterangan komponen         |
| prefix              | string     | _null_                       | _null_                             | Teks awalan                 |
| suffix              | string     | _null_                       | _null_                             | Teks akhiran                |
| format              | string     | DD MMMM YYYY                 | _null_                             | Format waktu                |
| locale              | string     | id                           | _null_                             | Bahasa                      |
| offset              | string     | _Local offset_               | _null_                             | _UTC time offsets_          |
| override            | boolean    | _false_                      | _null_                             | _Overridden by datepicker?_ |
| font                | string     | Arial, Helvetica, sans-serif | [Referensi&rarr;](ref_font.md) | Jenis huruf                 |
| size                | float      | 12                           | _null_                             | Ukuran huruf                |
| style               | enum       | normal                       | normal; italic                     | Bentuk huruf                |
| weight              | enum       | normal                       | normal; bold                       | Ketebalan huruf             |
| transform           | enum       | none                         | capitalize; uppercase; lowercase   | Transformasi                |
| width               | float      | 0                            | _null_                             | Lebar kotak teks            |
| height              | float      | 0                            | _null_                             | Tinggi kotak teks           |
| color               | string     | LightBlue                    | _null_                             | Warna teks                  |
| background_color    | string     | rgba(0,0,0,0)                | _null_                             | Warna latar                 |
| background_gradient | string     | _null_                       | _null_                             | Warna latar _gradient_\*    |
| border_width        | float      | 0                            | _null_                             | Ketebalan garis tepi        |
| border_color        | string     | rgba(0,0,0,0)                | _null_                             | Warna garis tepi            |
| border_radius       | float      | 0                            | _null_                             | Radius garis tepi           |
| anchor              | enum       | start                        | start; middle; end                 | Rata kiri/tengah/kanan      |
| realtime            | boolean    | _false_                      | _null_                             | _Realtime_                  |
| x                   | float      | 0                            | _null_                             | Posisi: Koordinat x         |
| y                   | float      | 0                            | _null_                             | Posisi: Koordinat y         |
| z                   | enum       | 0                            | 0;1;2;3;4;5;6;7;8;9                | Posisi: z-index             |
| rotate              | float      | 0                            | _null_                             | Derajat putaran             |

\*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)

#### Catatan:

- Contoh format `Tanggal/Bulan/Tahun`: `DD/MM/YYYY`
- Contoh format `Tahun-Bulan-Tanggal Jam:Menit`: `YYYY-MM-DD HH:mm`
- Contoh offset waktu WIB: `+07:00`
- Contoh offset waktu WITA: `+08:00`
- Contoh offset waktu WIT: `+09:00`
