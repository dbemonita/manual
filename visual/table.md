# Tabel

Berikut contoh _basic_ berkas konfigurasi untuk membuat halaman **table**:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.0?>
<?title Contoh Tabel?>
<?author Monita?>
<?revised 2020-01-01 08:00?>
<?locale id?>

<monita type="table">

  <row type="head">
    <cell>Waktu</cell>
    <cell>Param 1</cell>
    <cell>Param 2</cell>
    <cell>Param 3</cell>
  </row>

  <row type="body">
    <cell width="150px" point_id="epochtime"/>
    <cell width="100px" point_id="1001"/>
    <cell width="100px" point_id="1002"/>
    <cell width="100px" point_id="1003"/>
  </row>

</monita>
```

## Contoh Tampilan

Output layout dari visual tersebut akan seperti ini:

| Waktu  | Param 1 | Param 2 | Param 3 |
| ------ | ------- | ------- | ------- |
| &nbsp; | &nbsp;  | &nbsp;  | &nbsp;  |
| &nbsp; | &nbsp;  | &nbsp;  | &nbsp;  |

## Penjelasan

> `<?xml version="1.0" encoding="UTF-8"?>`
> `<?visualmonita 5.0?>`
> `<?title Contoh Tabel?>`
> `<?author Monita?>`
> `<?revised 2020-01-01 08:00?>`
> `<?locale id?>`

Format dokumen dan _meta data_. [Referensi&rarr;](ref_process_instruction.md)

> `<monita type="table">`

_Root tag_ `monita` menandakan dokumen Monita.
Pada _tag_ ini berisi atribut `type` dengan nilai `table`.
Pada _tag_ ini juga berisi atribut:

- `title` untuk mendefiniskan judul
- `subtitle` untuk mendefiniskan subjudul
- `data_trim` untuk mendefinisikan baris data yang dihilangkan, dimulai dari 1
- `data_interval` untuk mendefinisikan jarak waktu antardata: `minute`, `hour`, `day`, `month`
- `decimal_default` untuk mendefinisikan nilai baku atribut `decimal` di tiap properti `cell`
- `bb_left_title` untuk mendefinisikan isi HTML pada area kiri tabel, dengan menggunakan _bb code_
- `bb_right_title` untuk mendefinisikan isi HTML pada area kanan tabel, dengan menggunakan _bb code_

> `<row type="head">` | `<row type="body">` | `<row type="foot">`

Pada tabel HTML, `row` bisa diartikan sebagai `tr`. Memiliki atribut `type` dengan nilai `head`, `body`, atau `foot`.

> `<cell>Waktu</cell>` | `<cell point_id="1001"/>`

Pada tabel HTML, `cell` bisa diartikan sebagai `th` atau `td`. Bisa diisikan dengan teks statis, maupun teks dinamis (nilai yang dikirim oleh server) dengan menambahkan atribut `point_id` (istilah lain adalah `key` pada konteks JSON).

## Catatan

- Jumlah baris data akan muncul setelah dikirim oleh server. Misal, server mengirim _logsheet_ harian per jam, maka akan muncul 24 baris data. Tag `<row type="body">` merupakan _template_ yang akan diiterasi sebanyak jumlah data tersebut.

- `row` bisa diartikan sebagai `tr` pada tabel HTML. Memiliki atribut `type` dengan nilai `head` bila digunakan sebagai _heading_/_thead_, atau nilai `body` bila digunakan sebagai konten/_tbody_, atau nilai `tfoot` bila digunakan sebagai _footer_/_tfoot_. Dapat juga diberi atribut `colspan` atau `rowspan` bila diperlukan.

- Atribut `formula` tersedia pada `row type="body"`. [Referensi &rarr;](ref_formula.md)

- Atribut `summary` tersedia pada `row type="foot"`. [Referensi &rarr;](ref_summary.md)

- Atribut `calc` tersedia pada `row type="body"` dan `row type="foot"`. [Referensi &rarr;](ref_calc.md)

- Pada `row type="foot"` pun memiliki atribut `prefix` dan `suffix`.
