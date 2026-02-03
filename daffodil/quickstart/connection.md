# Koneksi Device

Gunakan PC/laptop yang sudah terpasang _internet browser_ di dalamnya. Koneksi ke _device_ ini bertujuan untuk melakukan konfigurasi pada _device_, yang dilakukan melalui jalur _ethernet_.

### Panduan Koneksi PC/Laptop ke Device melalui Ethernet

  - Sambungkan kabel _ethernet_ dari soket _ethernet_ pada _device_ ke soket _ethernet_ pada PC/Laptop.
  - Bila pada PC/laptop tidak tersedia soket _ethernet_, dapat menggunakan `USB to Ethernet Adapter`.
  - IP _default_ pada _device_ adalah `192.168.0.10`.
  - Untuk pengujian bahwa PC/laptop telah terhubung, lakukan pengujian dengan cara `ping 192.168.0.10`.
  - Bila `ping` berhasil, buka _internet browser_ dan masukkan alamat `http://192.168.0.10`.

### Troubleshoot

Bila PC/laptop belum berhasil terhubung ke _device_, lakukan pemeriksaan sebagai berikut:

  - Kabel _ethernet_ yang digunakan adalah _straight mode_ (TANPA penyilangan kabel).
  - Bila menggunakan `USB to Ethernet Adapter`, pastikan _driver_ telah terpasang pada PC/Laptop.
  - Saat memasukkan alamat pada _internet browser_, pastikan protokol adalah `http` dan bukan `https`.
  - Pastikan konfigurasi _ethernet_ pada PC/Laptop adalah sebagai berikut:

```
IP Address: 192.16.8.0.1
Subnet Mask: 255.255.255.0
```

- Pada OS Windows, konfigurasi _ethernet_ di atas dapat diakses melalui:
    - Masuk ke `Control Panel`.
    - Pilih `Network and Internet`.
    - Pilih `View network status and tasks`.
    - Pilih `Connection: Ethernet <n>` (Catatan: `n` adalah nomor ethernet pada PC/laptop).
    - Klik tombol `Properties`.
    - Pilih `Internet Protocol Version 4 (TCP/IPv4)`.
    - Klik tombol `Properties`.

- Bila IP pada _device_ telah diubah sebelumnya, dapat dilakukan _reset_ ke IP _default_ dengan cara menekan tombol pada _device_ selama ±5 detik. Umumnya tombol ini berada di sebelah soket _ethernet_.