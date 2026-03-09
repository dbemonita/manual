# THMI

Berikut contoh berkas konfigurasi untuk membuat halaman **THMI**:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.0?>
<?title Contoh THMI?>
<?author Monita?>
<?revised 2020-01-01 08:00?>
<?locale id?>

<monita type="thmi">

  <row type="head">
    <cell>GRUP</cell>
    <cell>Param 1</cell>
    <cell>Param 2</cell>
    <cell>Param 3</cell>
  </row>

  <row type="body">
    <cell>GRUP-001</cell>
    <cell point_id="1001"/>
    <cell point_id="1002"/>
    <cell point_id="1003"/>
  </row>

  <row type="body">
    <cell>GRUP-002</cell>
    <cell point_id="2001"/>
    <cell point_id="2002"/>
    <cell point_id="2003"/>
  </row>

</monita>
```

## Contoh Tampilan

Output layout dari visual tersebut akan seperti ini:

| GRUP     | Param 1                                      | Param 2                                      | Param 3                                      |
| -------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| GRUP-001 | <i class="fa fa-circle-o-notch fa-spin"></i> | <i class="fa fa-circle-o-notch fa-spin"></i> | <i class="fa fa-circle-o-notch fa-spin"></i> |
| GRUP-002 | <i class="fa fa-circle-o-notch fa-spin"></i> | <i class="fa fa-circle-o-notch fa-spin"></i> | <i class="fa fa-circle-o-notch fa-spin"></i> |

## Penjelasan

> `<?xml version="1.0" encoding="UTF-8"?>`
> `<?visualmonita 5.0?>`
> `<?title Contoh THMI?>`
> `<?author Monita?>`
> `<?revised 2020-01-01 08:00?>`
> `<?locale id?>`

Format dokumen dan _meta data_. [Referensi&rarr;](ref_process_instruction.md)

> `<monita type="thmi">`

_Root tag_ `monita` menandakan dokumen Monita.
Pada _tag_ ini berisi atribut `type` dengan nilai `thmi`. Selain itu:

- `title` untuk mendefinisikan judul, default _null_.
- `subtitle` untuk mendefinisikan subjudul, default _null_.
- `decimal_default` untuk mendefinisikan nilai baku atribut `decimal` di tiap properti `cell`.
- `expired_in` (dalam menit) berfungsi untuk menampilkan data minimum atau N/A bila usia data lebih dari waktu tersebut.

> `<row type="head">` | `<row type="body">`

Pada tabel HTML, `row` bisa diartikan sebagai `tr`. Memiliki atribut `type` dengan nilai `head` bila digunakan sebagai _heading_/_thead_, atau nilai `body` bila digunakan sebagai konten/_tbody_. Dapat juga diberi atribut `colspan` atau `rowspan` bila diperlukan (hanya berlaku pada `type="head"`).

> `<cell>GRUP-001</cell>` | `<cell point_id="1001"/>`

Pada tabel HTML, `cell` bisa diartikan sebagai `th` atau `td`. Bisa diisikan dengan teks statis, maupun teks dinamis (nilai yang dikirim oleh server) dengan menambahkan atribut `point_id`.
