# Contoh Berkas Konfigurasi HMI

Berikut contoh berkas konfigurasi untuk membuat halaman **HMI**:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.0?>
<?title Contoh HMI?>
<?author Monita?>
<?locale id?>

<monita type="hmi" background_color="#0E76BD" grid="true" decimal_default="2">

  <!-- Area komponen HMI -->

</monita>
```

## Penjelasan

> `<?xml version="1.0" encoding="UTF-8"?>`
> `<?visualmonita 5.0?>`
> `<?title Contoh HMI?>`
> `<?author Monita?>`
> `<?locale id?>`

Format dokumen dan _meta data_. [Referensi&rarr;](ref_process_instruction.md)

> `<monita type="hmi" background_color="#0E76BD" grid="true">`

_Root tag_ `monita` menandakan dokumen Monita.
Pada _tag_ ini berisi atribut `type` dengan nilai `hmi`. Selain itu:

- `background_color` untuk mengubah warna latar halaman HMI. Format warna bisa menggunakan format RGB/RGBA, HSL/HSLA, HEX, dan [kode warna](ref_color.md) Bila tidak didefiniskan, maka warna latar adalah `#0E76BD`.
- `background_gradient`. Lihat [Referensi Warna _Gradient_](ref_gradient_color.md)
- `background_image` untuk menambahkan gambar latar pada HMI. Rekomendasi ukuran gambar adalah:
  - 1300\*700 px, 72 dpi
  - 1950\*1050 px, 72 dpi
  - 2600\*1400 px, 72 dpi
- `grid` berfungsi untuk menampilkan (`grid="true"`) atau menyembunyikan (`grid="false"`) garis bantu. Nilai baku konfigurasi ini adalah `true`.
- `decimal_default` berfungsi untuk mendefinisikan jumlah desimal baku pada tiap `active_text` di halaman tersebut.
- `expired_in` (dalam menit) berfungsi untuk menampilkan data minimum atau N/A bila usia data lebih dari waktu tersebut.
