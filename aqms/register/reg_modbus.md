> Data Register Module AQMS

- Baudrate 9600
- Slave ID default : 0x0B (hex) = 11 (dec)
- register:
    | reg | item data | tipe data | remark     | category |
    |:---:|:---------:|:---------:|:----------:|:--------:|
    | 0   | uptime    | uint32    |            |          |
    | 2   | lux       | uint16    |            | weather (lux) |
    | 3   | solar radiation | uint16 |         | weather (W/m<sup>2</sup>) |
    | 4   | uv       | uint16    |             | weather  |
    | 5   | temp       | uint16    | value / 10 | weather (&deg;C) |
    | 6   | rel. humid | uint16    | value / 10 | weather (%) |
    | 7   | wind speed | uint16    | value / 10 | weather (m/s) |
    | 8   | wind dir. | uint16    |            | weather (&deg) |
    | 9   | rainfall | uint16     | value / 100 | weather (mm/hour) (v2.2.10 later) |
    | 10  | air press. | uint16    | value / 10 | weather (hPa) |
    | 11  | pm1       | uint16    |             | PM (ug/m<sup>3</sup>) |
    | 12  | pm2.5     | uint16    |             | PM (ug/m<sup>3</sup>) |
    | 13  | pm4       | uint16    |             | PM (ug/m<sup>3</sup>) |
    | 14  | pm10      | uint16    |             | PM (ug/m<sup>3</sup>) |
    | 15  | SO2_ppb   | int16     |             | udara (ppb) |
    | 16  | SO2_temp  | int16     |             | udara (&deg;C) |
    | 17  | SO2_rh    | uint16    |             | udara (%) |
    | 18  | NO2_ppb   | int16     |             | udara (ppb) |
    | 19  | NO2_temp  | int16     |             | udara (&deg;C) |
    | 20  | NO2_rh    | uint16    |             | udara (%) |
    | 21  | CO_ppb    | int16     |             | udara (ppb) |
    | 22  | CO_temp   | int16     |             | udara (&deg;C) |
    | 23  | CO_rh     | uint16    |             | udara (%) |
    | 24  | O3_ppb    | int16     |             | udara (ppb) |
    | 25  | O3_temp   | int16     |             | udara (&deg;C) |
    | 26  | O3_rh     | uint16    |             | udara (%) |
    | 27  | HC_ppb    | int16     |             | udara (ppb) |
    | 28  | HC_temp   | int16     |             | udara (&deg;C) |
    | 29  | HC_rh     | uint16    |             | udara (%) |
    | 30  | ISPU_PM2.5 | uint16   |             | ISPU avg_5_mnt |
    | 31  | ISPU_PM10  | uint16   |             | ISPU avg_5_mnt |
    | 32  | ISPU_SO2  | uint16    |             | ISPU avg_5_mnt |
    | 33  | ISPU_NO2  | uint16    |             | ISPU avg_5_mnt |
    | 34  | ISPU_CO   | uint16    |             | ISPU avg_5_mnt |
    | 35  | ISPU_O3   | uint16    |             | ISPU avg_5_mnt |
    | 36  | ISPU_HC   | uint16    |             | ISPU avg_5_mnt |
    | 37  | PM2.5 AVG | uint16    |             | Data avg_5_mnt |
    | 38  | PM10  AVG | uint16    |             | Data avg_5_mnt |
    | 39  | SO2 AVG | uint16    |             | Data avg_5_mnt |
    | 40  | NO2 AVG | uint16    |             | Data avg_5_mnt |
    | 41  | CO AVG | uint16    |             | Data avg_5_mnt |
    | 42  | O3 AVG | uint16    |             | Data avg_5_mnt |
    | 43  | HC AVG | uint16    |             | Data avg_5_mnt |
    | 44  | Temp Internal | uint16 | val/100   | (&deg;C) |
    | 45  | RH Internal | uint16 | val/100    | (%) |