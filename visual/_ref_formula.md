# Referensi Formula

Fitur Formula tersedia pada fitur Tabel dan Grafik. Pada fitur Tabel, untuk membuat formula dapat dilakukan dengan cara sebagai berikut:

```xml
<row type="body">
  <cell point_id="1001" formula=”current[$] - previous[$]”/>
</row>
```

atau,

```xml
<row type="body">
  <cell formula=”current[1001] - current[1002]”/>
</row>
```

Sedangkan pada fitur Grafik dapat dilakukan dengan cara:

```xml
<series>
  <formula>current[$] - previous[$]</formula>
</series>
```

Contoh lainnya:

```xml
<series>
  <formula>current[1001] - current[1002]</formula>
</series>
```

## Keywords

- Tanpa titik ukur:
  - epochtime
  - number
- Dengan titik ukur:
  - previous
  - current
  - next
  - cumulative
