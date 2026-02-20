> Konfigurasi Board DMD unutk LEd Matriks AQMS

## Console Debug
Untuk melakukan konfigurasi menggunakan serial console dari bluetooth.
Di Android bisa install aplikasi Serial Bluetooth Terminal.
Module akan otomatis merename nama Bluetooth menjadi __DMD-123456789ABC__
sesuai mac address dari bluetooth yang terpasang

*Console Command*

|command|opsi|keterangan|
|:---|:---|:---|
|help||bantuan apa saja command yang dapat digunakan|
|info||melihat konfigurasi yang ada saat ini|
|set| name [nama_tempat]| set nama lokasi di led matriks<br> contoh : __set name CIMANGGIS__<br> maksimal 64 karater| 
||sens_addr [alamat_sensor] | set address sensor data<br>contoh : __set sens_addr 40__ <br> nilai address dari 0 - 65535|
||sens_tipe [type] |set tipe data sensor<br>contoh : __set sense_tipe 4__ <br> tipe data <ul><li>0 : int16</li><li>1 : uint16</li><li>2 : int32</li><li>3 : uint32</li><li>4 : float</li></ul> |
||sens_swap [swap]|set mode swap di data <br>contoh : __set sens_swap 0__<br>mode swap: <br><ul><li>0 : normal</li><li>1 : swap byte</li><li>2 : swap word</li><li>3 : swap byte & word</li></ul> |
||time [jam] [menit] [detik] |contoh : __set time 10 30 10__|
||tanggal [tahun] [bulan] [hari]| contoh : __set date 2025 12 01__|
||brightness [nilai]|contoh : __set brightness 40__<br> nilai dalam persen 0%-100%|
||debug_mode [value]|contoh : __set debug_mode 1__ <br>1 untuk _enable_, 0 untuk _disable_|
|save||menyimpan konfigurasi di flash |
|flash||untuk flash firmware over the air via BT|

## FOTA over BT
Untuk melakukan Flash Firmware Over The Air (FOTA) bisa dilakukan melalui koneksi Bluetooth. Berikut langkahnya:

1. simpan firmware DMD Led Matrix diHandphone 
2. gunakan Serial Bluetooth Terminal untuk koneksi via console
3. ketikkan __flash__ diconsole, module akan mengirimkan karaktee C untuk mengunggu file yang akan di flash
4. setelah terkoneksi pilih menu Upload File
    - protocol : pilih Xmodem 1K
    - select file yang sudah dikirimkan contoh namanya *__ledmatrix-firmwarev2_framed.bin__* sesuai lokasi di handphone
    - pilih upload file
5. tunggu sampai proses selesai.