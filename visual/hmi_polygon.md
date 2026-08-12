# Poligon

Berikut contoh komponen HMI `polygon` (poligon):

```xml
<polygon>
  <caption>Contoh Poligon 1</caption>
  <x1>200</x1>
  <y1>100</y1>
  <x2>223</x2>
  <y2>168</y2>
  <x3>295</x3>
  <y3>168</y3>
  <x4>237</x4>
  <y4>210</y4>
  <x5>260</x5>
  <y5>280</y5>
  <x6>200</x6>
  <y6>238</y6>
  <x7>140</x7>
  <y7>280</y7>
  <x8>163</x8>
  <y8>210</y8>
  <x9>105</x9>
  <y9>168</y9>
  <x10>177</x10>
  <y10>168</y10>
  <border_width>0</border_width>
  <background_gradient>linear; 60; #bd93f9; #8be9fd</background_gradient>
</polygon>
```

#### Contoh:

https://playground.monita.co.id/?component=polygon

![polygon](https://hackmd.io/_uploads/BkT3UI4Sfe.jpg)

#### Properti selengkapnya:

| Properti            | Tipe Nilai | Nilai Baku    | Pilihan               | Keterangan               |
| ------------------- | ---------- | ------------- | --------------------- | ------------------------ |
| caption             | string     | Polygon       | _null_                | Keterangan komponen      |
| background_color    | string     | rgba(0,0,0,0) | _null_                | Warna latar              |
| background_gradient | string     | _null_        | _null_                | Warna latar _gradient_\* |
| border_width        | float      | 1             | _null_                | Ketebalan garis          |
| border_color        | string     | LightBlue     | _null_                | Warna garis              |
| border_style        | enum       | solid         | solid; dashed; dotted | Jenis garis              |
| link                | string     | _null_        | _null_                | Tautan                   |
| x1                  | float      | 0             | _null_                | Titik 1: Koordinat x     |
| y1                  | float      | 0             | _null_                | Titik 1: Koordinat y     |
| x2                  | float      | 0             | _null_                | Titik 2: Koordinat x     |
| y2                  | float      | 0             | _null_                | Titik 2: Koordinat y     |
| x3                  | float      | 0             | _null_                | Titik 3: Koordinat x     |
| y3                  | float      | 0             | _null_                | Titik 3: Koordinat y     |
| x4                  | float      | 0             | _null_                | Titik 4: Koordinat x     |
| y4                  | float      | 0             | _null_                | Titik 4: Koordinat y     |
| x5                  | float      | 0             | _null_                | Titik 5: Koordinat x     |
| y5                  | float      | 0             | _null_                | Titik 5: Koordinat y     |
| x6                  | float      | 0             | _null_                | Titik 6: Koordinat x     |
| y6                  | float      | 0             | _null_                | Titik 6: Koordinat y     |
| x7                  | float      | 0             | _null_                | Titik 7: Koordinat x     |
| y7                  | float      | 0             | _null_                | Titik 7: Koordinat y     |
| x8                  | float      | 0             | _null_                | Titik 8: Koordinat x     |
| y8                  | float      | 0             | _null_                | Titik 8: Koordinat y     |
| x9                  | float      | 0             | _null_                | Titik 9: Koordinat x     |
| y9                  | float      | 0             | _null_                | Titik 9: Koordinat y     |
| x10                 | float      | 0             | _null_                | Titik 10: Koordinat x    |
| y10                 | float      | 0             | _null_                | Titik 10: Koordinat y    |
| x11                 | float      | 0             | _null_                | Titik 10: Koordinat x    |
| y11                 | float      | 0             | _null_                | Titik 10: Koordinat y    |
| x12                 | float      | 0             | _null_                | Titik 10: Koordinat x    |
| y12                 | float      | 0             | _null_                | Titik 10: Koordinat y    |
| x13                 | float      | 0             | _null_                | Titik 10: Koordinat x    |
| y13                 | float      | 0             | _null_                | Titik 10: Koordinat y    |
| x14                 | float      | 0             | _null_                | Titik 10: Koordinat x    |
| y14                 | float      | 0             | _null_                | Titik 10: Koordinat y    |
| x15                 | float      | 0             | _null_                | Titik 10: Koordinat x    |
| y15                 | float      | 0             | _null_                | Titik 10: Koordinat y    |
| z                   | enum       | 0             | 0;1;2;3;4;5;6;7;8;9   | Posisi: z-index          |

\*) Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)
