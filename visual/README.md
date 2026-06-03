# Tentang Visual Monita 5

Adalah aplikasi visualisasi data melalui web HMI, grafik, tabel, dan peta.

Sejak versi `5.8.0 (2026-03-09)`, _rendering_ aplikasi ini menggunakan metode _Client Side Rendering (CSR)_. Artinya, _build_ aplikasi berupa HTML, JS, dan CSS. Untuk _serving_ bisa menggunakan aplikasi pemrograman apapun, bahkan bisa langsung menggunakan _http server_ seperti NGINX dan Apache.

## Instalasi

Panduan instalasi berikut berlaku untuk versi `5.8.0` atau lebih tinggi.

- Unduh aplikasi melalui [Google Drive](https://drive.google.com/drive/folders/1v4AWUM6w3Alechqg1R1mWl4xM0ARZLBx).
- Dengan apliaksi `unzip`, _extract_ aplikasi di _server_ tujuan.
- Jalankan aplikasi.
  - Contoh dengan PHP: `php -S localhost:8000`
  - Contoh dengan python: `python -m http.server 8000`
  - Bisa juga _deploy_ ke:
    - Netlify
    - Cloudflare Pages
    - Vercel
    - GitHub Pages

## Changelog

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

- Versi perdana untuk Android PlayStore.
- Hapus local/push notification.

## 5.9.3 (2026-03-30)

- Perbaikan UI untuk Android generasi menengah dengan top-notch.
- Perbaikan UI untuk Android pada mode gelap (dark-mode).

## 5.9.2 (2026-03-27)

- PoC Push Notification (server: vmpush.monita.co.id).
- Update UI untuk Android generasi baru (edge-to-edge).

## 5.9.1 (2026-03-16)

- Tambah privacy-policy untuk comply play store.

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
