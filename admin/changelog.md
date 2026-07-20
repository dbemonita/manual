# Changelog

Informasi perubahan aplikasi [Admin Monita](https://beta.monita.co.id/admin/).

### 1.12.0 (2026-07-07)

- Logo dinamis mengikuti subdomain.
- Server api memungkinkan dinamis `<origin>/api`. set `API_BASE: 'auto'`.
- Force logout saat respon server 401 karena di-restart.
- Tambah paginator pada list device di halaman dashboard.
- Perbaikan tombol refresh untuk non-root/admin.

### 1.11.1 (2026-07-03)

- Menampilkan scrollbar pada section parameters, form formula, page asset management.

### 1.11.0 (2026-07-02)

- Tambah info API server pada halaman login (pojok kiri atas).
- Perbaikan posisi toast (z-index) saat form pada sidebar kanan dibuka.
- Tambah argumen "help" pada tool updater (`./update -h` atau `./update --help`).
- Tambah halaman restart service beserta menunya, pada sidebar kiri, untuk role root dan admin.

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
