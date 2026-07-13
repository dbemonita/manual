# Changelog

Informasi perubahan aplikasi [Visual Monita](https://beta.monita.co.id/).

### 5.16.2 (2026-07-09) - _Android Release #4_

- Perbaikan halaman list alarm pada device android.
- Perbaikan warna icon dengan class `.warning` pada device android.

### 5.16.1 (2026-07-08)

- Perbaikan tombol download PDF pada tipe visual epaper.

### 5.16.0 (2026-07-07)

- Logo dinamis mengikuti subdomain.
- Server api memungkinkan dinamis `<origin>/api`. set `API_BASE: 'auto'`.
- Perbaikan sidebar pada saat tidak ada visual/menu.
- Tambah tombol show/hide password pada form login.

### 5.15.0 (2026-06-26)

- Menggunakan single file config: `config.js`.
- Di halaman login, tambah info update aplikasi bila tersedia.
- Tambah tools updater untuk update aplikasi: `./update`

### 5.14.0 (2026-06-17) - _Android Release #3_

- Tambah prop `allowed_roles` untuk komponen 2 arah (input).
- Tambah prop UI untuk komponen `input` dan `input_date`.
- Tambah info `domain:port` pada deviceName.
- Unreg service worker saat logout.
- Update sumber data push notif dari `.notification` ke `.data`.
- Update route ke halaman detil alarm saat notif diklik/tap.
- Tambah info `Ref. ID` pada halaman alarm.

### 5.13.0 (2026-05-29) - _Android Release #2_

- Memungkinkan berjalan di http dengan IP address.
- Auto disable fungsi-fungsi yang memerlukan isSecureContext.

### 5.12.0 (2026-05-26)

- Tambah widget alarm pada sidebar.
- Tambah halaman detail alarm.
- Perbaikan latest data (race condition).

### 5.11.0 (2026-05-20)

- Hapus tipe visual alarm-report.
- Tambah FCM push notification for android.
- Tambah FCM push notification for web.
- Tambah halaman alarm history.
- Perbaikan initial data untuk marker popup.
- Kembalikan tipe visual `dash`.

### 5.10.0 (2026-04-13) - _Android Release #1_

- Versi perdana untuk Google Play.
- Hapus local/push notification.

### 5.9.3 (2026-03-30)

- Perbaikan UI untuk Android generasi menengah dengan top-notch.
- Perbaikan UI untuk Android pada mode gelap (dark-mode).

### 5.9.2 (2026-03-27)

- PoC Push Notification (server: vmpush.monita.co.id).
- Update UI untuk Android generasi baru (edge-to-edge).

### 5.9.1 (2026-03-16)

- Tambah privacy-policy untuk comply Google Play.

### 5.9.0 (2026-03-12)

- Tambah library @capacitor/\* untuk wrapper ke mobile/APK.
- Hapus config `API_HOST`, `API_PATH`, `API_PORT`, digantikan dengan `API_BASE`.
- Hapus parser untuk tipe visual `dash`.

### 5.8.0 (2026-03-09)

- Menggunakan mode CSR.
- Hapus closingProcess.
- Hapus closingProcessStrict.
- Hapus dataReprocess.
- Kembalikan maindataPrefixed.
- Kembalikan maindataFixed.
