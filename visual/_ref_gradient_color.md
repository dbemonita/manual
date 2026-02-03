# Referensi Warna _Gradient_

Pada beberapa komponen, Visual Monita 5 mendukung format warna _gradient_ dengan parameter:

```
type; deg; color-1; color-2; color-n
```

## Penjelasan

| type            | deg                | color-1       | color-2     | color-n    |
| --------------- | ------------------ | ------------- | ----------- | ---------- |
| Tipe _gradient_ | Arah gradasi warna | Warna pertama | Warna kedua | Warna ke-n |

## Catatan

- Tipe _gradient_: `linear` atau `radial`
- Arah warna berdasarkan derajat (untuk tipe `linear`), misal:
  - 0: arah dari kiri ke kanan
  - 45: arah dari kiri atas ke kanan bawah
  - 90: arah dari atas ke bawah
  - 135: arah dari kanan atas ke kiri bawah
  - 180: arah dari kanan ke kiri
- Jumlah warna minimal 2, maksimal 5
