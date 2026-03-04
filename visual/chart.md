# Grafik

Berikut contoh berkas konfigurasi untuk membuat halaman **chart**:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.3?>
<?title Contoh Grafik?>
<?author Andi Prianto?>
<?revised 2020-01-01 08:00?>
<?locale id?>

<monita type="chart">

  <y_axis>
    <name>Level</name>
    <ref>y1</ref>
    <min>0</min>
    <max>100</max>
    <unit>m</unit>
  </y_axis>

  <series>
    <name>Level Kiri</name>
    <point_id>1001</point_id>
    <y_axis_ref>y1</y_axis_ref>
    <color>LightSeaGreen</color>
  </series>

  <series>
    <name>Level Kanan</name>
    <point_id>1002</point_id>
    <y_axis_ref>y1</y_axis_ref>
    <color>FireBrick</color>
  </series>

</monita>
```

## Penjelasan

> `<?xml version="1.0" encoding="UTF-8"?>`
> `<?visualmonita 5.3?>`
> `<?title Contoh Grafik?>`
> `<?author Andi Prianto?>`
> `<?revised 2020-01-01 08:00?>`
> `<?locale id?>`

Format dokumen dan _meta data_. [Referensi&rarr;](ref_process_instruction.md)

> `<monita type="chart">`

_Root tag_ `monita` menandakan dokumen Monita.
Pada _tag_ ini berisi atribut `type` dengan nilai `chart`.
Pada _tag_ ini juga bisa berisi atribut:

- `title` untuk mendefiniskan judul
- `subtitle` untuk mendefiniskan subjudul
- `data_trim` untuk mendefinisikan baris data yang dihilangkan, dimulai dari 1
- `data_interval` untuk mendefinisikan jarak waktu antardata: `minute`, `hour`, `day`, `month`
- `data_reprocess` (_boolean_) untuk mendefinisikan apakah data dihitung ulang oleh Visual Monita
- `closing_process` (_boolean_) untuk mendefinisikan tutup buku, bila _false_ berarti data dimulai tanggal 1 pukul 00:00, bila _true_ maka data dimulai satu periode ke belakang
- `closing_process_strict` (_boolean_) untuk mendefinisikan periode awal tutup buku, bila _false_ misal dari tanggal 15 sampai dengan tanggal 15, bila _true_ misal dari tanggal 16 sampai dengan tanggal 15; atribut ini digunakan bila parameter `closing_process` bernilai _true_
- `decimal_default` untuk mendefinisikan nilai baku atribut `decimal`
- `windrose` (_boolean_) untuk mendefinisikan grafik dalam bentuk _windrose_

> `<y_axis>`

Komponen **y axis** _mandatory_. Memiliki properti:

- `name`: nama `y axis`; default `yAxis`
- `ref`: keyword atau inisial. Berfungsi sebagai kode referensi untuk direlasikan dengan properti `series`. Tiap `y axis` dapat direlasikan ke banyak series (_one to many_); default _null_
- `min`: nilai minimal; default 0
- `max`: nilai maksimal; default 0
- `unit`: satuan; default _null_

> `<series>`

Komponen **series** _mandatory_. Memiliki properti:

- `name`: nama _series_; default `Series`
- `type`: tipe grafik; default `spline`; [Referensi&rarr;](https://www.highcharts.com/docs/chart-and-series-types/chart-types)
- `point_id`: id titik ukur/parameter; default 0
- `y_axis_ref`: kode referensi `y_axis` yang akan direlasikan ke salah satu `y axis`; default _null_
- `color`: warna garis grafik; default _null_
- `data_label`: tampilkan label data?; default _false_
- `formula`: formula; [Referensi&rarr;](ref_formula.md)
- `calc`: kalkulator; [Referensi&rarr;](ref_calc.md)
- `decimal`: jumlah angka di belakang tanda koma ("."); default 2
- `windrose_component`: penentuan komponen dengan opsi data `speed` atau `direction`

> `<plot_line>`

Komponen **plot_line**. Memiliki properti:

- `name`: nama _plotline_; default _null_
- `dash_style`: _style_ garis; default `solid`; [Referensi&rarr;](https://api.highcharts.com/class-reference/Highcharts#.DashStyleValue)
- `value`: nilai posisi garis; default 0
- `width`: ketebalan garis; default 2
- `color`: warna garis; default _null_

> `<plot_band>`

Komponen **plot_band**. Memiliki properti:

- `name`: nama _plotline_; default _null_
- `from`: nilai awal posisi _band_; default 0
- `to`: nilai akhir posisi _band_; default 0
- `color`: warna _band_; default _null_

> `<plot_option>`

Komponen **plot_option**. Memiliki properti:

- `line_marker`; default _true_
- `series_stacking`; default _null_; pilihan `normal` atau `percent`
- `turbo_threshold`; default 1000

## Windrose

Windrose merupakan bentuk grafik yang digunakan untuk menampilkan data arah dan kecepatan angin dalam bentuk diagram polar. Untuk menampilkan grafik windrose, maka pada komponen `<series>` harus ditambahkan properti `windrose_component` dengan opsi data `speed` atau `direction`. Berikut contoh implementasinya:

```xml
<?xml version="1.0" encoding="UTF-8"?>

<?visualmonita 5.3?>
<?title Contoh Grafik?>
<?author Andi Prianto?>
<?revised 2020-01-01 08:00?>
<?locale id?>

<monita type="chart" windrose="true">
  <y_axis>
    <name>Wind Speed</name>
    <ref>y0</ref>
    <unit>mm/h</unit>
  </y_axis>

  <series>
    <name>Wind Speed</name>
    <point_id>3302</point_id>
    <y_axis_ref>y0</y_axis_ref>
    <windrose_component>speed</windrose_component>
  </series>

  <y_axis>
    <name>Wind Direction</name>
    <ref>y1</ref>
    <unit>&#xb0;</unit>
  </y_axis>

  <series>
    <name>Wind Direction</name>
    <point_id>3303</point_id>
    <y_axis_ref>y1</y_axis_ref>
    <windrose_component>direction</windrose_component>
  </series>
</monita>
```
