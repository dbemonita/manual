# Tentang Versi 5

Versi ini dibuat berdasarkan elemen visual pada aplikasi Monita 3 dengan pembaruan yang signifikan, baik secara sistem maupun konfigurasi. Dengan memisahkan elemen visual menjadi aplikasi terpisah.

Berkas konfigurasi pada versi ini menggunakan format `.xml` versi 1.0.

## Instalasi

### _Setup_

Silakan salin (`ctrl+c`) URL aplikasi _web_ Visual Monita 5.3.2 (Node 14) berikut:

> http:/<span></span>/alpha.daunbiru.com:8084/dl/vismon-5.3.2-node-14.tar.gz

Lalu _download_ dan _extract_ di server tujuan:

```sh
mkdir /apps/vismon && cd $_
wget <download_link>
tar -xf vismon*gz
cp config.js.example config.js && nano $_
```

### _Process Manager_

Bila menggunakan PM2, jalankan:

```sh
HOST=127.0.0.1 PORT=8080 pm2 start ./vismon-pm2.json
pm2 save
```

Catatan: Bila tidak menggunakan _proxy_, konfigurasikan `HOST=0.0.0.0`

### _Proxy Server_

Bila menggunakan port 80 (dan/atau 443) melalui Haproxy, pada berkas `haproxy.cfg`, tambahkan:

```sh
frontend vismon_front
   bind *:80
   # bind *:443 ssl crt /path/to/file.pem
   default_backend vismon_back

backend vismon_back
   balance roundrobin
   server vismon 127.0.0.1:8080 check
```

Catatan: Untuk membuat berkas **.pem**, gunakan perintah `cat /path/to/file.crt /path/to/file.key | tee /path/to/file.pem`

### HTTP/2

Untuk mengaktifkan protokol `http/2` melalui Haproxy, gunakan konfigurasi berikut:

```sh
frontend vismon_front
   bind *:80
   bind *:443 ssl crt /path/to/file.pem alpn h2,http/1.1
   mode http
   default_backend vismon_back

backend vismon_back
   balance roundrobin
   mode http
   server vismon 127.0.0.1:8080 check
```

## Kompatibilitas Browser

Visual Monita dapat berjalan baik pada browser-browser berikut:

| Platform | Engine    | Browser               | Versi Minimum | Download                                                                         |
| -------- | --------- | --------------------- | ------------- | -------------------------------------------------------------------------------- |
| Desktop  | Gecko     | **Firefox**           |               | [Download](https://www.mozilla.org/en-US/firefox/new/)                           |
| Desktop  | Gecko     | **Firefox Developer** |               | [Download](https://www.mozilla.org/en-US/firefox/developer/)                     |
| Desktop  | Blink     | **Chrome**            |               | [Download](https://www.google.com/intl/en_us/chrome/)                            |
| Desktop  | Blink     | **Brave**             |               | [Download](https://brave-browser.readthedocs.io/en/latest/installing-brave.html) |
| Desktop  | Blink     | **Vivaldi**           |               | [Download](https://vivaldi.com/download/)                                        |
| Desktop  | Blink     | **Opera**             |               | [Download](https://www.opera.com/)                                               |
| Desktop  | Blink     | **Min**               |               | [Download](https://minbrowser.github.io/min/)                                    |
| Desktop  | Blink     | **Edge**              | 79            | [Download](https://www.microsoft.com/en-us/edge/)                                |
| Android  | GeckoView | **Firefox**           |               | [Download](https://play.google.com/store/apps/details?id=org.mozilla.firefox)    |
| Android  | WebView   | **Chrome**            |               | [Download](https://play.google.com/store/apps/details?id=com.android.chrome)     |
| Android  | WebView   | **Opera**             |               | [Download](https://play.google.com/store/apps/details?id=com.opera.browser)      |

Catatan:

- Microsoft Edge versi 79 merupakan versi pertama _Chromium-based_ pada browser tersebut.
- Sejak Android 4.4 "KitKat", komponen WebView dibuat berdasarkan _engine_ Blink (tidak lagi WebKit).
- Visual Monita tidak dapat berjalan optimal pada browser Safari dan browser lain yang menggunakan _engine_ WebKit.
- Visual Monita tidak dapat berjalan optimal pada seluruh browser di perangkat iOS dan iPadOS dikarenakan batasan dari Apple yang mengharuskan semua browser yang terdaftar di App Store untuk menggunakan _engine_ WebKit (referensi: https://developer.apple.com/app-store/review/guidelines/#2.5.6).
