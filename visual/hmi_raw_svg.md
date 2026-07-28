# Raw SVG

Berikut contoh komponen HMI `raw_svg`:

```xml
<raw_svg>
  <caption>Contoh Raw SVG</caption>
  <encoded_content>&lt;circle cx=&quot;100&quot; cy=&quot;100&quot; r=&quot;50&quot; fill=&quot;blue&quot; /&gt;</encoded_content>
</raw_svg>
```

#### Contoh

![raw_svg](https://hackmd.io/_uploads/SJzl3YSHMx.jpg)

#### Properti selengkapnya:

| Properti        | Tipe Nilai | Nilai Baku | Pilihan             | Keterangan          |
| --------------- | ---------- | ---------- | ------------------- | ------------------- |
| caption         | string     | Text       | _null_              | Keterangan komponen |
| encoded_content | string     | _null_     | _null_              | _Raw SVG_           |
| z               | enum       | 0          | 0;1;2;3;4;5;6;7;8;9 | Posisi: z-index     |
