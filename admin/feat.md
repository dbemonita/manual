# Fitur/Halaman

Berikut adalah fitur dan/atau halaman yang ada pada aplikasi Admin Monita:

### Dashboard

- Berisi jumlah _devices_, yang aktif, tidak aktif, dan total keseluruhan.
- Aktif atau tidak aktif ditentukan berdasarkan nilai `timeout` pada halaman konfigurasi _device_.
- Terdapat pula list _device_ aktif pada kolom pertama dan list _device_ tidak aktif pada kolom kedua.

### Users

- Ini adalah fitur/halaman pengelolaan pengguna.
- Halaman ini juga berfungsi untuk _assign_ asset dan visual/xml pada pengguna

### Devices

- Ini adalah fitur/halaman pengelolaan _device_.
- Melalui halaman ini juga dapat terpantau pengiriman data terbaru secara realtime.

### Assets

- Ini adalah fitur/halaman pengelolaan _asset_.
- Halaman ini juga berfungsi untuk melakukan pengelolaan titik ukur, formula, dan alarm.

### XML Editor

- Ini adalah fitur/halaman pengelolaan file XML.
- File XML digunakan untuk membuat visualisasi (web HMI).
- Manual tag XML dapat diakses [di sini](https://manual.monita.co.id/visual/#/hmi).

### Firmware

- Ini adalah fitur/halaman pengelolaan file binnary firmware untuk _device_.
- Melalui halaman ini juga dapat dilakukan _flashing_ secara OTA.

### SMTP Config

- Ini adalah fitur/halaman untuk pengelolaan akses/autentikasi SMTP server.
- SMPTP server digunakan umumnya untuk mengiriman laporan via email.

### Running Reports

- Ini adalah fitur/halaman untuk pengelolaan _scheduler_ proses pengiriman email laporan.
- File laporan yang dikirim berdasarkan HMI tipe laporan yang sudah diunduk dalam format PDF.

### Server Info

- Ini adalah fitur/halaman untuk monitoring server yang digunakan untuk menjalankan aplikasi Monita.
- Beberapa informasi yang ditampilkan terkait hardisk, ram, ethernet, operating system, database, proxy server, dsb.

### Alarm History

- Ini adalah fitur/halaman untuk melakukan pengelolaan log alarm.
- Melalui halaman ini juga pengguna dapat melakukan "ACK" pada satu atau lebih log alarm.
