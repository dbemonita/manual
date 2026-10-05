# Tentang Visual Monita 5

Adalah aplikasi visualisasi data melalui web HMI, grafik, tabel, dan peta.

Pada versi `5.8.0 (2026-03-09)`, _rendering_ aplikasi ini menggunakan metode _Client Side Rendering (CSR)_. Artinya, _build_ aplikasi berupa HTML, JS, dan CSS. Untuk _serving_ bisa menggunakan aplikasi pemrograman apapun, bahkan bisa langsung menggunakan _http server_ seperti Nginx dan Apache.

## Instalasi

Panduan instalasi berikut berlaku untuk versi `5.8.0` atau lebih tinggi.

- Unduh aplikasi melalui [Google Drive](https://drive.google.com/drive/folders/1v4AWUM6w3Alechqg1R1mWl4xM0ARZLBx) atau [Server Monita](https://download.monita.co.id/visual/).
- Dengan aplikasi `unzip`, _extract_ aplikasi di _server_ tujuan.
- Jalankan aplikasi.
  - Contoh dengan PHP: `php -S localhost:8000`
  - Contoh dengan python: `python -m http.server 8000`
  - Bisa juga _deploy_ ke:
    - Netlify
    - Cloudflare Pages
    - Vercel
    - GitHub Pages

### Konfigurasi

Konfigurasi ada pada file `config.js` (atau, bisa di-copy dari `config.js.example`). Isinya sebagai berikut:

```js
API_BASE: "https://sockelat.monita.co.id", // Alamat API backend.
SC_HOST: "sockelat.monita.co.id", // Server socket-cluster.
SC_PATH: "/socketcluster/", // Path socket-cluster. Nilai default '/socketcluster/'.
SC_PORT: 443, // Port socket-cluster. Nilai default 443.
SC_SECURE: true, // Is socket-cluster secure? Nilai default true.
ALARM_NOTIFICATION: false, // Enable fungsi alarm? Nilai default false.
WIDGET_CHAT: false, // Enable fungsi chat AI? Nilai default false.
DOWNLOAD_SITE: 'https://download.monita.co.id', // Server build/zip Monita.

DEVELOPMENT_TEXT: false, // Tampilkan teks term of use? Terkait BRIN. nilai default false.
GOOGLE_RECAPTCHA: false, // Menggunakan re-capthca pada form login? Terkait BRIN. nilai default false.
GOOGLE_RECAPTCHA_SITEKEY: "", // Key re-capthca. Terkait BRIN. nilai default kosong.
H5_SERVICE: "", // Endpoint pengolahan data-frame. Terkait BRIN. nilai default kosong.
```

Pada versi >= 5.16.0, konfigurasi `API_BASE` dapat diisikan dengan nilai `auto`. Sehingga aplikasi akan mengarah ke `<origin>/api`.

Pada versi >= 5.15.0, terdapat tambahan konfigurasi FCM (disalin dari FCM Console).

```js
API_KEY: "*****",
AUTH_DOMAIN: "*****.firebaseapp.com",
PROJECT_ID: "*****",
STORAGE_BUCKET: "*****.firebasestorage.app",
MESSAGING_SENDER_ID: "*****",
APP_ID: "*:*****:web:*****",
MEASUREMENT_ID: "G-*****",
```

Pada versi >= 5.15.0, konfigurasi di-_wrap_ dengan:

```js
.__APP_CONFIG__ = {
  // Variabel konfigurasi di atas.
};
```

Pada versi <= 5.14.0 konfigurasi di-_wrap_ dengan:

```js
.APP_CONFIG = {
  // Variabel konfigurasi di atas.
};
```

#### Halaman _Custom_

Pada versi >= 5.17.0 terdapat konfigurasi opsional untuk halaman _custom_:

```js
.__CUSTOM_PAGES__ = [
  {
    usernames: [], // List username yang dapat mengakses halaman custom ini
    path: "", // Path file lokasi halaman custom
    title: "", // Judul halaman custom
    options: {
      // Konfigurasi spesifik tiap-tiap halaman custom
    },
  },
];
```

Contoh konfigurasi halaman custom:

- [Dashboard dan Laporan AQMS &rarr;](custom_aqms.md)

### Logo

Pada versi >= 5.16.0, logo adaptif menyesuaikan subdomain dengan format PNG.

- Subdomain `pelindo.monita.co.id` file logo `pelindo.png`
- Subdomain `selayar.monita.co.id` file logo `selayar.png`

File logo disertakan di dalam folder aplikasi. Bila tidak tersedia, akan _fallback_ ke file `client.png` (logo Monita).

### Update Aplikasi Web

Pada versi >= 5.15.0, untuk update aplikasi versi di atasnya, dapat menjalankan:

```sh
./update
```

atau, `./update <versi>`, contoh:

```sh
./update 5.15.1
```

Pastikan sudah terpasang `unzip` pada server, dengan cara `sudo apt install unzip`.

### Deployment

##### DENGAN PROXY

Pastikan untuk mengaktifkan modul `proxy` dan `proxy_http`:

```bash
a2enmod proxy
a2enmod proxy_http
```

_Asumsi proxy ke IP lokal dengan port 8000._

Berikut contoh konfigurasi untuk Apache:

```
<VirtualHost *:80>
    ServerName demo.monita.co.id

    ProxyPreserveHost On
    ProxyPass        / http://192.168.1.100:8000/
    ProxyPassReverse / http://192.168.1.100:8000/

    ErrorLog ${APACHE_LOG_DIR}/proxy-error.log
    CustomLog ${APACHE_LOG_DIR}/proxy-access.log combined
</VirtualHost>
```

Berikut contoh konfigurasi untuk Nginx:

```
server {
    listen 80;
    server_name demo.monita.co.id;

    location / {
        proxy_pass http://172.16.50.14:8000/;

        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```

##### TANPA PROXY

_Asumsi aplikasi berada di `/var/www/vismon`_.

Berikut contoh konfigurasi untuk Apache:

Terlebih dahulu pastikan modul `rewrite` aktif dengan cara `a2enmod rewrite`.

```
<VirtualHost *:80>
    ServerName example.com
    DocumentRoot /var/www/vismon

    <Directory /var/www/vismon>
        Options FollowSymLinks
        AllowOverride None
        Require all granted

        RewriteEngine On
        RewriteCond %{REQUEST_FILENAME} !-f
        RewriteCond %{REQUEST_FILENAME} !-d
        RewriteRule ^ /index.html [L]
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/vismon-error.log
    CustomLog ${APACHE_LOG_DIR}/vismon-access.log combined
</VirtualHost>
```

Berikut contoh konfigurasi untuk Nginx:

```
server {
    listen 80;
    server_name example.com;

    root /var/www/vismon;
    index index.html;

    location / {
        try_files $uri $uri/ /index.html;
    }
}
```

Bila aplikasi tidak berada di dalam direktori `/var/www`, misalnya berada di `/home/user/apps/vismon`, pastikan permissions direktori dan file telah dikonfigurasi dengan benar.

- Pastikan direktori induk (`/home`, `/home/user`, dan `/home/user/apps`) memiliki permission `755`.
- Pastikan direktori aplikasi beserta seluruh subdirektorinya memiliki permission `755`.
- Pastikan seluruh file aplikasi memiliki permission `644`.

Gunakan perintah berikut untuk mengatur permission direktori dan file aplikasi:

```bash
find /home/user/apps/vismon -type d -exec chmod 755 {} \;
find /home/user/apps/vismon -type f -exec chmod 644 {} \;
```

### Android App

Aplikasi versi Android dapat diunduh melalui [Google Play](https://play.google.com/store/apps/details?id=id.co.monita.visual).
