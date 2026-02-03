# Referensi _Summary_

Fitur Summary merupakan fitur pelengkap dari fitur Formula yang hanya tersedia pada fitur Tabel dengan row bertipe foot. Bila fitur Formula bertujuan untuk kalkulasi horizontal, maka fitur Summary bertujuan untuk kalkulasi horizontal dan vertikal. Berikut contohnya:

```xml
<row type="foot">
  <cell id=”1001” summary=”( last[$] - first_padstart[$] ) / num_rows”/>
</row>
```

Contoh lainnya:

```xml
<row type="foot">
  <cell summary=”last[1001] - last[1002]”/>
</row>
```

## Keywords

- first_padstart
- first
- first_positive
- last_positive
- last
- last_padend
- sum_padstart
- sum
- sum_padend
- sum_pad
- min_padstart
- min
- min_padend
- min_pad
- max_padstart
- max
- max_padend
- max_pad
- avg_padstart
- avg
- avg_padend
- avg_pad
- num_rows
