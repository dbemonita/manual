> Perintah Konfigurasi melalui MQTT - wifi

- Konfigurasi via MQTT

    | Topic Publish | Payload |  Keterangan |Opsi |
    |:--------------|:--------|:----------|:------|
    |aqms/command/[serial_number]|SO2;Z | Zeroing Sensor Udara SO2| Perintah untuk Zeroing Sensor Udara |
    ||NO2;Z| Zeroing Sensor Udara NO2||
    ||CO;Z| Zeroing Sensor Udara CO||
    ||O3;Z| Zeroing Sensor Udara O3||
    ||HC;Z| Zeroing Sensor Udara HC||
    ||config|Isi Config AQMS module||
    ||config;mode;0| melakukan konfigurasi mode,<br>setelah konfig module akan reboot|0= NO_SENSOR<br>1= FIXED<br>2= PORTABLE<br>3=PM_25| 
    ||restart|Restart Module ||
    |aqms/fota/[serial_number]|flash|Flashing OTA Normal ke Module |None / f / force|
    |aqms/fota/[serial_number]|flash;f|Flashing OTA secara force/paksa ke Module | atau flash;force |