# Tentang Admin Monita

Adalah aplikasi pengelolaan perangkat, aset, titik ukur, serta pengguna.

_Rendering_ aplikasi ini menggunakan metode _Client Side Rendering (CSR)_. Artinya, _build_ aplikasi berupa HTML, JS, dan CSS. Untuk _serving_ bisa menggunakan aplikasi pemrograman apapun, bahkan bisa langsung menggunakan _http server_ seperti Nginx dan Apache.

## Instalasi

- Unduh aplikasi melalui [Google Drive](https://drive.google.com/drive/folders/1WEyAkPY5l4BIUKxb2PAplE1X19I4CmzH) atau [Server Monita](https://download.monita.co.id/admin/).
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

Sejak versi >= 1.9.0, konfigurasi menggunakan _UPPERCASE_ seperti berikut:

```js
API_BASE: "https://sockelat.monita.co.id", // Alamat API backend.
SC_HOST: "sockelat.monita.co.id", // Server socket-cluster.
SC_PATH: "/socketcluster/", // Path socket-cluster. Nilai default '/socketcluster/'.
SC_PORT: 443, // Port socket-cluster. Nilai default 443.
SC_SECURE: true, // Is socket-cluster secure? Nilai default true.
ALARM_NOTIFICATION: false, // Enable fungsi alarm? Nilai default false.
CHAT_WIDGET: false, // Enable fungsi chat AI? Nilai default false.

H5_NAVIGATION: false, // Tampilkan link menu H5? Terkait data-frame BRIN. Nilai default false.
H5_BASE: "", // Endpoint pengolahan data-frame. Terkait BRIN. nilai default kosong.
```

Sejak versi >= 1.10.0, terdapat tambahan konfigurasi FCM (disalin dari FCM Console).

```js
API_KEY: "*****",
AUTH_DOMAIN: "*****.firebaseapp.com",
PROJECT_ID: "*****",
STORAGE_BUCKET: "*****.firebasestorage.app",
MESSAGING_SENDER_ID: "*****",
APP_ID: "*:*****:web:*****",
MEASUREMENT_ID: "G-*****",
```

Pada versi <= 1.8.0, konfigurasi menggunakan _camelCase_ seperti berikut.

```
apiBase
scHost
scPath
scPort
scSecure
alarmNotification
chatWidget

h5Navigation
h5Base
```

### Update Aplikasi Web

Sejak versi >= 5.15.0, untuk update aplikasi versi di atasnya, dapat menjalankan:

```sh
./update
```

atau, `./update <versi>`, contoh:

```sh
./update 5.15.1
```

Pastikan sudah terpasang `unzip` pada server, dengan cara `sudo apt install unzip`.

### Deployment Tanpa Sub-domain

Konfigurasi ini ditujukan untuk deploy tanpa domain/sub-domain. Contoh: `https://example.com/admin/` atau `https://example.com/manage/`.

##### DENGAN PROXY

_Asumsi proxy ke IP lokal dengan port 3000._

Berikut contoh konfigurasi untuk Apache 2:

```
ProxyPass /admin http://172.16.50.14:3000
ProxyPassReverse /admin http://172.16.50.14:3000

ProxyPass /_admin http://172.16.50.14:3000/_admin
ProxyPassReverse /_admin http://172.16.50.14:3000/_admin
```

Berikut contoh konfigurasi untuk Nginx:

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

##### TANPA PROXY

_Asumsi aplikasi berada di /var/www/_

Berikut contoh konfigurasi untuk Apache 2:

Terlebih dahulu pastikan modul `rewrite` aktif dengan cara `a2enmod rewrite`.

```
Alias /admin /var/www/admin
Alias /_admin /var/www/admin/_admin

<Directory /var/www/admin>
    Options FollowSymLinks
    AllowOverride None
    Require all granted

    RewriteEngine On
    RewriteBase /admin/

    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteRule ^ index.html [L]
</Directory>

<Directory /var/www/admin/_admin>
    Options FollowSymLinks
    AllowOverride None
    Require all granted
</Directory>
```

Berikut contoh konfigurasi untuk Nginx:

```
location /admin/ {
    alias /var/www/admin/;

    try_files $uri $uri/ /admin/index.html;
}

location /_admin/ {
    alias /var/www/admin/_admin/;

    access_log off;
    expires 1y;
    add_header Cache-Control "public, immutable";
}
```

Bila posisi aplikasi tidak ada di `/var/www`, maka:

- Misal aplikasi berada di dalam folder `/home/user/apps`.
- Pastikan folder `/home`, `/home/user/`, `/home/user/apps`, dan `/home/user/apps/admin`memiliki permission`755`.
- Semua file di dalam folder `admin` memiliki permission `644` dengan cara `find /home/user/apps/admin -type f -exec chmod 644 {} \;`

##### CATATAN:

- Fitur "deploy tanpa domain/sub-domain" hanya bisa diterapkan pada versi >= 1.8.0.
- Alias `admin` dapat diganti/disesuaikan. Misal `manage`, `lobby`, dsb.
- Alias `_admin` tidak dapat diganti. Folder `_admin` berisi _script_ aplikasi.

---

## Changelog

### 1.11.0 (2026-07-02)

- Tambah info API server pada halaman login (pojok kiri atas).
- Perbaikan posisi toast (z-index) saat form pada sidebar kanan dibuka.
- Tambah argumen "help" pada tool updater (`./update -h` atau `./update --help`).
- Tambah halaman restart server beserta menunya, pada sidebar kiri, untuk role root dan admin.

### 1.10.0 (2026-06-26)

- Menggunakan single file config: `config.js`.
- Di halaman login, tambah info update aplikasi bila tersedia.
- Tambah tools updater untuk update aplikasi: `./update`

### 1.9.0 (2026-06-23)

- Rename key localstorage, membedakan key visual monita saat deploy tanpa sub-domain.
- Perbaikan layout halaman aset, terkait posisi scrollbar.
- Ganti nama variabel konfigurasi menggunakan _UPPERCASE_ (backward compatible).
- Perbaikan lokasi file worker untuk monaco editor (XML editor).

### 1.8.0 (2026-06-19)

- Memungkinkan dijalankan tanpa domain/sub-domain. Contoh: `https://example.com/admin` atau `https://example.com/manage/`.
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
