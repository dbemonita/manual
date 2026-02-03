# Jam Analog

Berikut contoh komponen HMI `clock` (jam analog):

```xml
<clock>
  <caption>Contoh Jam Analog 1</caption>
  <diameter>200</diameter>
  <x>100</x>
  <y>100</y>
</clock>
```

#### Properti selengkapnya:

| Properti          | Tipe Nilai | Nilai Baku     | Pilihan             | Keterangan          |
| ----------------- | ---------- | -------------- | ------------------- | ------------------- |
| caption           | string     | Clock          | _null_              | Keterangan komponen |
| diameter          | float      | 0              | _null_              | Diameter jam        |
| offset            | string     | _Local offset_ | _null_              | _UTC time offsets_  |
| tick_color        | string     | #666           | _null_              | Warna _tick_ tebal  |
| minor_tick_color  | string     | #666           | _null_              | Warna _tick_ tipis  |
| hour_dial_color   | string     | #444           | _null_              | Warna jarum jam     |
| minute_dial_color | string     | #555           | _null_              | Warna jarum menit   |
| second_dial_color | string     | #666           | _null_              | Warna jarum detik   |
| center_dial_color | string     | #666           | _null_              | Warna tengah jam    |
| x                 | float      | 0              | _null_              | Posisi: Koordinat x |
| y                 | float      | 0              | _null_              | Posisi: Koordinat y |
| z                 | enum       | 0              | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index     |

#### Catatan:

- Contoh offset waktu WIB: `+07:00`
- Contoh offset waktu WITA: `+08:00`
- Contoh offset waktu WIT: `+09:00`
