
# [Download Firmware Daffodil](https://drive.google.com/drive/folders/1dz1C6Nq6wBmktp0kvZMXbmvK5L_d4aHb)

## V6.3.4 (B) / V6.3.5 (F) (9 November 2026)   

- [X] Optimasi Config non volatil system, supaya ketika fw di flash tidak menghilangkan informasi config sebelumnya.
- [x] Optimasi fitur MQTTS dengan port yang fleksibel.
- [x] Penambahan informasi Device monitoring Info untuk monitoring dari Local Daun biru. 
- [x] Penambahan VPN Wireguard untuk membantu proses tunnelling IP sehingga dapat diakses secara remote dari mana saja.
- [x] Penambahan Informasi Active dan Non - Active pada section Ethernet dan Celullar.
- [x] update Algorithm pada tab jaringan, jika versi terdeteksi NO-MODEM maka pilihan "Network Interface"  ditiadakan dan informasi section cellular di hilangkan. 
- [X] Optimasi Algoritma "penggunaan memori", setiap kali persentase menunjukkan nilai penggunaan memori 95% maka sistem akan restart otomatis. 
- [X] Optimasi persamaan y = mx + c dapat digunakan dan hasil operasi akan di tampilkan mulai alamat 101 dengan nama data_manipulasi. 
- [X] Terjadi kesalahan setting pada broker_domain yang belum sesuai, sudah disesuaikan dan berjalan lancar. 
- [x] Penambahan fitur MQTTS via Port 8883.
- [X] Support multi connection ke MQTT broker, sudah bisa connect ke dua broker MQTT.
- [X] Optimasi pada tab Data sehingga setiap kali reload atau pindah page tidak mudah hang. 

# v6.3.2 (B) / v6.3.3 (F)  (25 September 2026)
- [x] revisi perbaikan konfigurasi pengiriman domain untuk MQTT monitoring, menjadi broker_domain.
- [x] perubahan metode cek server apakah ok atau tidak dengan cara cek server is Alive, menggantikan cara ping (ICMP) karena ternyata ada beberapa vps yang tetiba mematikan fungsi ICMP.

# v6.3.0 (18 Agustus 2026)
- [x] config non volatil system, dibuat bisa di update apabila ada perubahan atau penambahan. metode baca tulis flash jadi berubah.

# v6.2.3_xxx - 08 Juli 2026

- [x] Race Condition pcb close di Lwip. penambahan timeout juka network tidak bisa di shutdown.
- [x] perbiaiakn di app ethernet dan app mqtt.


# v6.2.2.122_NO-MODEM - 24 Juni 2026

- [x] Versi Modem - No Modem disetting firmware di Makefile, jadi harus buuil 2 jenis (MODEM dan NO_MODEM)
- [x] Versioning ditambahkan date build (YYYYMMDD)
- [x] Penyimpanan data ke SD-CARD juga untuk data yang sudah Sent, Unsent, Resent, UnResent 
- [x] MQTTYield di firmware lama tiba-tiba closed, coba benahi algoritma di MQTTYield connection dan reset koneksi.
- [x] optimasi algoritma pengiriman ulang data unsent, perlu juga cek optimasi untuk data send.
- [x] mqtt heartbeat di lambankan ke 30 detik periodik
- [x] penambahan stack size (1024 * 2) dan priority (NORMALPRIO + 8) untuk Thread ethernet.
- [x] Firmware No Modem [v6.2.2.125.20260701_NO-MODEM](https://sockelat.monita.co.id/dl/firmware/daffodil-6.2.2.125.20260701-NO_MODEM_framed.bin)
- [x] Firmware Modem [v6.2.2.125.20260701](https://sockelat.monita.co.id/dl/firmware/daffodil-6.2.2.125.20260701_framed.bin)
- atau download di google drive 
- [x] manual diarahkan ke [manual.monita.com/#/daffodil](https://manual.monita.co.id/daffodil/#/)