# Dasboard

Berikut contoh berkas konfigurasi untuk membuat halaman **Dasboard**:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.3?>
<?title Contoh Dashboard?>
<?author Andi Prianto?>
<?revised 2020-01-01 08:00?>
<?locale id?>

<monita type="dash">

  <!-- Area komponen dashboard -->

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

> `<monita type="dash">`

_Root tag_ `monita` menandakan dokumen Monita.
Pada _tag_ ini berisi atribut `type` dengan nilai `dash`.
