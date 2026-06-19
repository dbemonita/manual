# Tentang Admin Monita

Adalah aplikasi pengelolaan perangkat, aset, titik ukur, serta pengguna.

_Rendering_ aplikasi ini menggunakan metode _Client Side Rendering (CSR)_. Artinya, _build_ aplikasi berupa HTML, JS, dan CSS. Untuk _serving_ bisa menggunakan aplikasi pemrograman apapun, bahkan bisa langsung menggunakan _http server_ seperti NGINX dan Apache.

### Instalasi

- Unduh aplikasi melalui [Google Drive](https://drive.google.com/drive/folders/1WEyAkPY5l4BIUKxb2PAplE1X19I4CmzH).
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
window.__APP_CONFIG__ = {
  apiBase: "https://sockelat.monita.co.id", // Alamat API backend.
  h5Navigation: false, // Terkait data-frame BRIN. Nilai default false.
  h5Base: "", // Terkait data-frame BRIN. nilai default kosong.
  scHost: "sockelat.monita.co.id", // Server socket-cluster.
  scPort: 443, // Port socket-cluster. Nilai default 443.
  scSecure: true, // Is socket-cluster? Nilai default true.
  scPath: "/socketcluster/", // Path socket-cluster. Nilai default '/socketcluster/'.
  alarmNotification: false, // Enable fungsi alarm? Nilai default false.
  chatWidget: false, // Enable fungsi chat AI? Nilai default false.
};
```

### Deployment Subfolder-like

Konfigurasi ini ditujukan agar dapat menjalankan aplikasi seperti *https://example.com/admin/*.

Berikut contoh konfigurasi untuk Apache:

```
ProxyPass /admin http://172.16.50.14:3000
ProxyPassReverse /admin http://172.16.50.14:3000

ProxyPass /_admin http://172.16.50.14:3000/_admin
ProxyPassReverse /admin http://172.16.50.14:3000/_admin
```

Berikut contoh konfigurasi untuk NGINX:

```
location /admin/ {
    proxy_pass http://172.16.50.14:3000/;

    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
}

location /_admin/ {
    proxy_pass http://172.16.50.14:3000/_admin/;

    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
}
```

Catatan: Fitur _subfolder-like_ hanya bisa diterapkan pada versi >= 1.8.0.

---

## Changelog

### 1.8.0 (2026-06-15)

- Memungkinkan dijalankan dengan format URL `https://example.com/admin`.
- Hapus auto-reload pada halaman `alarm`, digantikan trigger dari FCM.

### 1.7.0 (2026-06-15)

- Tambah halaman user's gadget `/#/user/gadget`.
- Tambah info `domain:port` pada deviceName.
- Unreg service worker saat logout.
- Update sumber data push notif dari `.notification` ke `.data`.
- Update route ke halaman detil alarm saat notif diklik/tap.
- Tambah info `ID` pada halaman detil alarm.
- Seragamkan format datetime di semua halaman.

### 1.6.1 (2026-06-04)

- Mengubah tampilan dashboard:
  - Jumlah total device, device aktif, dan device tidak aktif.
  - Memisahkan list device aktif dan tidak aktif.
  - Efisiensi ruang (widget lebih tipis).
  - Filter device berdasarkan teks.
  - Tombol pause 60s-auto-refresh.

### 1.6.0 (2026-05-29)

- Memungkinkan berjalan di http dengan IP address.
- Auto disable fungsi-fungsi yang memerlukan isSecureContext.

### 1.5.0 (2026-05-26)

- Tambah halaman detail alarm.

### 1.4.1 (2026-05-20)

- Perbaikan menu pada sidebar.
- Tambah fitur alarm history refetcher tiap 60 detik.

### 1.4.0 (2026-05-20)

- Tambah halaman histori alarm dan ACK.
- Configurable H5, Chatbox, FCM.
- Perbaikan input number untuk data float.
- Ubah theme menjadi Nora.

### 1.3.1 (2026-04-27)

- Ubah session user, dibuat tidak expired.
- Tambah "stop push notif" saat user logout.
- Tambah teks "Admin/<versi>" pada device name.

### 1.3.0 (2026-04-21)

- Tambah halaman list notifikasi (alarm).

### 1.2.0 (2026-04-20)

- Tambah fitur pengelolaan notifikasi.

### 1.1.0 (2026-03-13)

- Menggunakan mode CSR.
- Tambah form API Base URL pada halaman login.
