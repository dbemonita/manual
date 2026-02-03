# Teks Aktif

Komponen `active_text` untuk jenis visual `epaper` sama seperti pada jenis visual `hmi`.

Berikut contoh komponen `active_text` (teks aktif):

%[{ common/_active_text.md }]%

Yang membedakan tag pembuka `<active_text>` memiliki atribut-atribut sebagai berikut:

| Atribut                  | Tipe Nilai | Nilai Baku | Pilihan Nilai                   | Keterangan                                |
| ------------------------ | ---------- | ---------- | ------------------------------- | ----------------------------------------- |
| data_this                | enum       | hour       | hour; day; month; year          | Rentang waktu data\*                      |
| summary                  | enum       | last       | min; max; sum; avg; first; last | Jenis ringkasan data                      |
| refresh_interval         | int        | 0          | _null_                          | Interval pengambilan data terbaru (menit) |
| default_color            | string     | _null_     | _null_                          | Nilai baku untuk semua warna teks         |
| default_background_color | string     | _null_     | _null_                          | Nilai baku untuk semua warna latar        |

%[{ _data_this.md }]%
