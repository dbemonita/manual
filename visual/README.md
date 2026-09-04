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

### Android App

Aplikasi versi Android dapat diunduh melalui [Google Play](https://play.google.com/store/apps/details?id=id.co.monita.visual).
