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