# Peta

Berikut contoh berkas konfigurasi untuk membuat halaman **peta**:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.3?>
<?title Contoh Peta?>
<?author Andi Prianto?>
<?revised 2020-01-01 08:00?>
<?locale id?>

<monita type="map">

  <!-- Area komponen peta -->

</monita>
```

## Penjelasan

> `<?xml version="1.0" encoding="UTF-8"?>`  
> `<?visualmonita 5.3?>`  
> `<?title Contoh Peta?>`  
> `<?author Andi Prianto?>`  
> `<?revised 2020-01-01 08:00?>`  
> `<?locale id?>`

Format dokumen dan _meta data_. [Referensi&rarr;](ref_process_instruction.md)

> `<monita type="map">`

_Root tag_ `monita` menandakan dokumen Monita.
Pada _tag_ ini berisi atribut `type` dengan nilai `map`. Selain itu:

- `title` untuk mendefinisikan judul, default _null_.
- `subtitle` untuk mendefinisikan subjudul, default _null_.
- `decimal_default` untuk mendefinisikan nilai baku atribut `decimal` di tiap properti `cell`.
- `expired_in` (dalam menit) berfungsi untuk menampilkan data minimum atau N/A bila usia data lebih dari waktu tersebut.
- `layer_group_name` untuk mendefinisikan nama grup layer pada _widget_ _Layer_ di _sidebar_ kanan. Contoh: `layer_group_name="Nama Grup 1, Nama Grup 2, Nama Grup 3"`.\*

\*) Ketarangan:

- Grup 1 memuat marker aktif.
- Grup 2 memuat marker statis.
- Grup 3 memuat geojson dan geometri (garis, kotak, lingkaran, garis).
