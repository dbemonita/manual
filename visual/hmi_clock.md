# Jam Analog

Berikut contoh komponen HMI `clock` (jam analog):

```xml
<clock>
  <caption>Contoh Jam Analog 1</caption>
  <diameter>200</diameter>
  <x>100</x>
  <y>100</y>
</clock>

<circle>
  <caption>Contoh Lingkaran 1</caption>
  <diameter>180</diameter>
  <border_width>0</border_width>
  <background_gradient>linear; 60; #fff; #8be9fd</background_gradient>
  <x>110</x>
  <y>110</y>
</circle>
```

#### Contoh:

https://playground.monita.co.id/?component=clock

![clock](https://manual.monita.co.id/_assets/images/clock.png)

#### Properti selengkapnya:

| Properti          | Tipe Nilai | Nilai Baku     | Pilihan             | Keterangan          |
| ----------------- | ---------- | -------------- | ------------------- | ------------------- |
| caption           | string     | Clock          |                     | Keterangan komponen |
| diameter          | float      | 0              |                     | Diameter jam        |
| offset            | string     | _Local offset_ |                     | _UTC time offsets_  |
| tick_color        | string     | #666           |                     | Warna _tick_ tebal  |
| minor_tick_color  | string     | #666           |                     | Warna _tick_ tipis  |
| hour_dial_color   | string     | #444           |                     | Warna jarum jam     |
| minute_dial_color | string     | #555           |                     | Warna jarum menit   |
| second_dial_color | string     | #666           |                     | Warna jarum detik   |
| center_dial_color | string     | #666           |                     | Warna tengah jam    |
| x                 | float      | 0              |                     | Posisi: Koordinat x |
| y                 | float      | 0              |                     | Posisi: Koordinat y |
| z                 | enum       | 0              | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index     |

#### Catatan:

- Contoh offset waktu WIB: `+07:00`
- Contoh offset waktu WITA: `+08:00`
- Contoh offset waktu WIT: `+09:00`
