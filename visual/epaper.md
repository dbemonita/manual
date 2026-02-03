# ePaper

Berikut contoh berkas konfigurasi untuk membuat halaman **ePaper**:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.3?>
<?title Contoh ePaper?>
<?author Andi Prianto?>
<?revised 2020-01-01 08:00?>
<?locale id?>

<monita type="epaper" grid="true" page_number="true">

  <page size="a4" orientation="portrait">

    <!-- Area komponen ePaper -->

  </page>

</monita>
```

## Penjelasan

> `<?xml version="1.0" encoding="UTF-8"?>`  
> `<?visualmonita 5.3?>`  
> `<?title Contoh ePaper?>`  
> `<?author Andi Prianto?>`  
> `<?revised 2020-01-01 08:00?>`  
> `<?locale id?>`

Format dokumen dan _meta data_. [Referensi&rarr;](ref_process_instruction.md)

> `<monita type="epaper">`

_Root tag_ `monita` menandakan dokumen Monita.
Pada _tag_ ini berisi atribut `type` dengan nilai `epaper`. Selain itu:

- `grid` berfungsi untuk menampilkan/menyembunyikan garis bantu. Nilai baku konfigurasi ini adalah `true`.
- `page_number` berfungsi untuk menampilkan/menyembunyikan nomor halaman. Nilai baku konfigurasi ini adalah `true`.
- `request_delay` berfungsi untuk memberi waktu jeda antar-_request_ ke server ( dalam milidetik). Nilai baku konfigurasi ini adalah `0`.
- `datepicker_autoopen` berfungsi untuk menampilkan _popup datepicker_. Nilai baku konfigurasi ini adalah `false`.

> `<page size="a4" orientation="portrait" grid="true">`

Tag `page` merupakan halaman/lembar yang akan dibuat. Dapat memuat lebih dari 1 halaman/lembar.
Pada _tag_ ini berisi atribut `size` dengan pilihan nilai:

- a4
- letter
- legal

Terdapat pula atribut `orientation` dengan pilihan nilai:

- portrait
- landscape
