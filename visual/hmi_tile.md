# Tile

Berikut contoh komponen HMI `tile`:

```xml
<tile>
  <caption>Contoh Tile 1</caption>
  <width>300</width>
  <height>50</height>
  <image_source>/images/short-pipe-h.png</image_source>
  <x>100</x>
  <y>100</y>
</tile>

<tile>
  <caption>Contoh Tile 1</caption>
  <width>200</width>
  <height>50</height>
  <image_source>/images/short-pipe-h.png</image_source>
  <x>100</x>
  <y>200</y>
</tile>

<tile>
  <caption>Contoh Tile 1</caption>
  <width>100</width>
  <height>50</height>
  <image_source>/images/short-pipe-h.png</image_source>
  <x>100</x>
  <y>300</y>
</tile>
```

#### Contoh:

https://playground.monita.co.id/?component=tile

![tile](https://hackmd.io/_uploads/Hy43r3lHfl.jpg)

#### Properti selengkapnya:

| Properti     | Tipe Nilai | Nilai Baku | Pilihan              | Keterangan          |
| ------------ | ---------- | ---------- | -------------------- | ------------------- |
| caption      | string     | Tile       | ---                  | Keterangan komponen |
| width        | float      | 0          | ---                  | Lebar area          |
| height       | float      | 0          | ---                  | Tinggi area         |
| image_source | string     | _null_     | ---                  | URL gambar\*        |
| direction    | enum       | horizontal | horizontal, vertical | Arah _loop_         |
| link         | string     | _null_     | ---                  | Tautan              |
| x            | float      | 0          | ---                  | Posisi: Koordinat x |
| y            | float      | 0          | ---                  | Posisi: Koordinat y |
| z            | enum       | 0          | 0;1;2;3;4;5;6;7;8;9  | Posisi: z-index     |
| rotate       | float      | 0          | ---                  | Derajat putaran     |
