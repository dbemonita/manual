# Solid Gauge

Komponen `solid_gauge` untuk jenis visual `epaper` sama seperti pada jenis visual `hmi`.

Berikut contoh komponen `solid_gauge`:

%[{ common/_solid_gauge.md }]%

Yang membedakan tag pembuka `<solid_gauge>` memiliki atribut-atribut sebagai berikut:

| Atribut          | Tipe Nilai | Nilai Baku | Pilihan                         | Keterangan                                |
| ---------------- | ---------- | ---------- | ------------------------------- | ----------------------------------------- |
| data_this        | enum       | hour       | hour; day; month; year          | Rentang waktu data\*                      |
| summary          | enum       | last       | min; max; sum; avg; first; last | Jenis ringkasan data                      |
| refresh_interval | int        | 0          | _null_                          | Interval pengambilan data terbaru (menit) |

%[{ _data_this.md }]%
