# Tentang Visual Monita 5

Adalah aplikasi visualisasi data melalui web HMI, grafik, tabel, dan peta.

Sejak versi `5.8.0 (2026-03-09)`, _rendering_ aplikasi ini menggunakan metode _Client Side Rendering (CSR)_. Artinya, _build_ aplikasi berupa HTML, JS, dan CSS. Untuk _serving_ bisa menggunakan aplikasi pemrograman apapun, bahkan bisa langsung menggunakan _http server_ seperti Nginx dan Apache.

## Instalasi

Panduan instalasi berikut berlaku untuk versi `5.8.0` atau lebih tinggi.

- Unduh aplikasi melalui [Google Drive](https://drive.google.com/drive/folders/1v4AWUM6w3Alechqg1R1mWl4xM0ARZLBx).
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

DEVELOPMENT_TEXT: false, // Tampilkan teks term of use? Terkait BRIN. nilai default false.
GOOGLE_RECAPTCHA: false, // Menggunakan re-capthca pada form login? Terkait BRIN. nilai default false.
GOOGLE_RECAPTCHA_SITEKEY: "", // Key re-capthca. Terkait BRIN. nilai default kosong.
H5_SERVICE: "", // Endpoint pengolahan data-frame. Terkait BRIN. nilai default kosong.
```

Sejak versi >= 5.15.0, terdapat tambahan konfigurasi FCM (disalin dari FCM Console).

```js
API_KEY: "*****",
AUTH_DOMAIN: "*****.firebaseapp.com",
PROJECT_ID: "*****",
STORAGE_BUCKET: "*****.firebasestorage.app",
MESSAGING_SENDER_ID: "*****",
APP_ID: "*:*****:web:*****",
MEASUREMENT_ID: "G-*****",
```

Sejak versi >= 5.15.0, konfigurasi di-_wrap_ dengan:

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

### Update Aplikasi Web

Sejak versi > 5.15.0, untuk update aplikasi versi di atasnya, dapat dengan menjalankan:

```sh
./update
```

atau, `./update <versi>`, contoh:

```sh
./update 5.15.1
```

### Android App

Aplikasi versi Android dapat diunduh melalui [Google Play](https://play.google.com/store/apps/details?id=id.co.monita.visual).

---

## Changelog

### 5.14.0 (2026-06-17)

- Tambah prop `allowed_roles` untuk komponen 2 arah.
- Tambah prop UI untuk komponent `input` dan `input_date`.
- Tambah info `domain:port` pada deviceName.
- Unreg service worker saat logout.
- Update sumber data push notif dari `.notification` ke `.data`.
- Update route ke halaman detil alarm saat notif diklik/tap.
- Tambah info `Ref. ID` pada halaman alarm.

### 5.13.0 (2026-05-29)

- Memungkinkan berjalan di http dengan IP address.
- Auto disable fungsi-fungsi yang memerlukan isSecureContext.

## 5.12.0 (2026-05-26)

- Tambah widget alarm pada sidebar.
- Tambah halaman detail alarm.
- Perbaikan latest data (race condition).

## 5.11.0 (2026-05-20)

- Hapus tipe visual alarm-report.
- Tambah FCM push notification for android.
- Tambah FCM push notification for web.
- Tambah halaman alarm history.
- Perbaikan initial data untuk marker popup.
- Kembalikan tipe visual `dash`.

## 5.10.0 (2026-04-13)

- Versi perdana untuk Google Play.
- Hapus local/push notification.

## 5.9.3 (2026-03-30)

- Perbaikan UI untuk Android generasi menengah dengan top-notch.
- Perbaikan UI untuk Android pada mode gelap (dark-mode).

## 5.9.2 (2026-03-27)

- PoC Push Notification (server: vmpush.monita.co.id).
- Update UI untuk Android generasi baru (edge-to-edge).

## 5.9.1 (2026-03-16)

- Tambah privacy-policy untuk comply Google Play.

## 5.9.0 (2026-03-12)

- Tambah library @capacitor/\* untuk wrapper ke mobile/APK.
- Hapus config `API_HOST`, `API_PATH`, `API_PORT`, digantikan dengan `API_BASE`.
- Hapus parser untuk tipe visual `dash`.

## 5.8.0 (2026-03-09)

- Menggunakan mode CSR.
- Hapus closingProcess.
- Hapus closingProcessStrict.
- Hapus dataReprocess.
- Kembalikan maindataPrefixed.
- Kembalikan maindataFixed.
