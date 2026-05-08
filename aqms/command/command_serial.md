> Perintah Konfigurasi melalui Serial

- Konfigurasi via Kabel USB Micro
    | Perintah | Opsi | Keterangan |
    |:--------|:----|:----------|
    |reboot | | restart module |
    |config| | melihat isi dari konfigurasi saat ini |
    |||contoh :  <br> Serial Num : AQMS_841FE8099470 <br>Nama : Aqms_SENSOR <br>WiFi SSID  : monita_aqms <br>WiFi Pass  : Mxxxxxxx <br>MODE  : 3 -> MODE_PM2_5 <br>SLAVE_ID : 11 <br>FOTA_SERVER : https://server.monita.co.id <br>WEATHER SENSOR : ON <br>DEBUG MODE: OFF|
    |set_config|<nama / ssid / pass / mode> <value>|untuk melakukan konfigurasi|
    ||- nama <value>| mengisi nama module dengan nama yang diinginkan |
    |||contoh: <br> "set_config nama module_baru"|
    ||- ssid <value>| mengisi nama SSID wifi yang akan di koneksikan |
    |||contoh:<br>"set_config ssid wifi_baru"|
    ||- pass <value>| mengisi password wifi yang akan di koneksikan |
    |||contoh:<br>"set_config pass xxx123xxx"|
    ||- mode <value>| mengisi jenis mode sensor, value diisi dengan angka 0-3 <br> 0 - NO_SENSOR <br> 1 - FIXED (PM25,PM10,udara complete) <br> 2 - PORTABLE (PM2.5, PM10, udara sebagian) <br> 3 - PM25_ONLY |
    |||contoh :<br>"set_config mode 3" <br> ini untuk set module untuk sensor PM2.5 saja.|
    ||- debug | aktivasi mode debug, <br> opsi <1/0> <br> 1 = ON, 0 = OFF |
    ||- cuaca | aktivasi sensor cuaca via modbus (MISOL). <br> opsi <1/0> <br> 1 = ON, 0 = OFF | 
    |barcode|| melihat informasi semua barcode sesnor yang terpasang |
    |||contoh:<br>========== BARCODE DATA ==========<br>=== SO2 ===<br>Barcode    : 050323010234 110610 SO2 2305 46.00<br>SN         : 050323010234<br>Sensitivity: 46000 |
    |set_barcode|<barcode sensor (SN PN GAS CREATED SENSITIVITY)>|set isi barcode sesuai sensor |
    |||contoh:<br>set_barcode 050323010234 110610 SO2 2305 46.00|
    |sensor| SO2 Z|Zeroing sensor SO2<br> "sensor SO2 Z"|
    | | NO2 Z|Zeroing sensor NO2<br> "sensor NO2 Z"|
    | | CO Z|Zeroing sensor CO<br> "sensor CO Z"|
    | | O3 Z|Zeroing sensor O3<br> "sensor O3 Z"|
    | | HC Z|Zeroing sensor HC<br> "sensor HC Z"|
    | info | | Menampilkan informasi module, isinya:<br>Module : AQMS_SENSOR<br>Version : 2.2.1<br>Build on : 20260127_192055 |
    | fota | | Melakukan Update Firmware OTA |

---
    