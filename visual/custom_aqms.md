# Dashboard dan Laporan AQMS

Contoh konfigurasi:

```js
// Custom Pages.
globalThis.__CUSTOM_PAGES__ = [
  {
    usernames: ["kecbogortengah.trial"], // List username yang dapat mengakses halaman custom ini
    path: "display/1", // Path file lokasi halaman custom
    title: "Dashboard", // Judul halaman custom
    options: {
      stationName: "Stasiun Kecamatan Bogor Tengah", // Nama stasiun pemantauan
      region: "Kota Bogor, Provinsi Jawa Barat", // Wilayah pemantauan
      points: [
        {
          // 0-15.5 baik
          // 15.6-55.4 sedang
          // 55.5-150.4 tidak sehat
          // 150.5-250.4 sangat tidak sehat
          // >250.5 berbahaya
          key: "pm25",
          id: 310102,
          name: "PM 2.5",
          short: "PM2.5",
          unit: "μg/m³",
          min: 0,
          max: 500,
        },
        {
          // 0-15.5 baik
          // 15.6-55.4 sedang
          // 55.5-150.4 tidak sehat
          // 150.5-250.4 sangat tidak sehat
          // >250.5 berbahaya
          key: "pm10",
          id: 310103,
          name: "PM 10",
          short: "PM10",
          unit: "μg/m³",
          min: 0,
          max: 500,
        },
        {
          // <40 kering
          // 40-65 normal
          // >65 lembab
          key: "humidity",
          id: 310124,
          name: "Humidty",
          short: "Hum",
          unit: "%",
          min: 0,
          max: 100,
        },
        {
          // <21°C Dingin
          // 21°C – 32°C Normal
          // 32°C – 34°C Panas
          // >34°C Terik
          key: "temperature",
          id: 310123,
          name: "Temperatur",
          short: "Temp",
          unit: "degC",
          min: 0,
          max: 40,
        },
        {
          // Skala 0 (Tenang): 0 - 0,2 m/s – Asap naik lurus ke atas
          // Skala 1 (Angin ringan): 0,3 - 1,5 m/s – Arah angin terlihat dari gerak asap
          // Skala 2 (Angin sepoi-sepoi): 1,6 - 3,3 m/s – Angin terasa di wajah, daun berdesir
          // Skala 3 (Angin sepoi): 3,4 - 5,4 m/s – Ranting kecil bergerak, bendera berkibar
          // Skala 4 (Angin sedang): 5,5 - 7,9 m/s – Debu dan kertas terangkat
          // Skala 5 (Angin segar): 8,0 - 10,7 m/s – Pohon kecil mulai bergoyang
          // Skala 6 (Angin kuat): 10,8 - 13,8 m/s – Cabang pohon besar bergoyang, sulit pakai payung
          // Skala 7 (Angin kencang): 13,9 - 17,1 m/s – Seluruh pohon bergoyang, susah berjalan melawan angin
          key: "windSpeed",
          id: 310125,
          name: "Wind Speed",
          short: "Wind",
          unit: "m/s",
          min: 0,
          max: 40,
        },
        {
          key: "windDirection",
          id: 310127,
          name: "Wind Direction",
          short: "Direct",
          unit: "deg",
          min: 0,
          max: 359,
        },
        {
          // 0 W/m²: Total darkness (nighttime)
          // 50 - 100 W/m²: Very thick, dark storm or rain clouds
          // 200 - 400 W/m²: Heavy overcast or early morning/late afternoon hours
          // 500 - 700 W/m²: Light haze, thin clouds, or partial sun
          // 800 - 1000 W/m²: Clear, bright sunny sky at midday (Standard Test Condition for solar panels is 1000 W/m²)
          // 1361 W/m²: Direct solar intensity at the top of Earth's atmosphere
          key: "solarRadiation",
          id: 310121,
          name: "Solar Radiation",
          short: "Rad",
          unit: "W/m²",
          min: 0,
          max: 1361,
        },
        {
          // Hujan sangat ringan: Kurang dari 1 mm/jam
          // Hujan ringan: 1 sampai 5 mm/jam
          // Hujan normal/sedang: 5 sampai 10 mm/jam
          // Hujan lebat: 10 sampai 20 mm/jam
          // Hujan sangat lebat: Lebih dari 20 mm/jam
          key: "rainIntensity",
          id: 310128,
          name: "Rain Intensity",
          short: "Rain",
          unit: "mm/h",
          min: 0,
          max: 20,
        },
        {
          // Batas Bawah: 900 hPa
          // Batas Atas: 1030 hPa
          key: "pressure",
          id: 310129,
          name: "Pressure",
          short: "Press",
          unit: "hPa ",
          min: 900,
          max: 1030,
        },
        {
          // Skala < 10,7 m/s (Aman): Embusan normal, tidak membahayakan struktur otomatis AQMS/AWS
          // Skala 10,8 - 17,1 m/s (Waspada): Embusan kuat, ranting patah, memicu penyebaran cepat api karhutla
          // Skala 17,2 - 24,4 m/s (Sangat Kencang): Kerusakan struktural ringan, genteng terbang, pohon muda tumbang
          // Skala 24,5 - 32,6 m/s (Badai/Storm): Pohon besar tumbang, kerusakan parah pada tenda darurat/posko KLHK
          // Skala > 32,6 m/s (Topan/Hurricane): Kerusakan fatal skala luas, risiko tinggi pada menara sensor lapangan
          key: "gustSpeed",
          id: 310126,
          name: "Gust Speed",
          short: "Gust",
          unit: "m/s",
          min: 0,
          max: 40,
        },
      ],
      ispuParamKeys: ["pm10", "pm25", "so2", "co", "o3", "no2", "hc"], // Parameter ISPU
      weatherParamKeys: [
        // List widget informasi cuaca
        "humidity",
        "solarRadiation",
        "rainIntensity",
        "temperature",
        "pressure",
        "windSpeed",
        "gustSpeed",
        "windDirection",
      ],
      weatherTrendKeys: ["temperature", "humidity", "windSpeed"],
      dataSourceKey: "average", // "data" or "average"
      refetchEvery: 1, // minutes
    },
  },
  {
    usernames: ["kecbogortengah.trial"], // List username yang dapat mengakses halaman custom ini
    path: "display/2", // Path file lokasi halaman custom
    title: "Laporan", // Judul halaman custom
    options: {
      logoUrl: "https://kemenlh.go.id/assets/images/logo/logo-klh-plain.png", // Logo pada A4
      title: "LAPORAN", // Judul pada A4
      subTitle: "INDEKS STANDAR PENCEMAR UDARA", // Sub-judul pada A4
      stationName: "Stasiun Kecamatan Bogor Tengah",
      region: "Kota Bogor, Provinsi Jawa Barat",
      points: [
        {
          // 0-15.5 baik
          // 15.6-55.4 sedang
          // 55.5-150.4 tidak sehat
          // 150.5-250.4 sangat tidak sehat
          // >250.5 berbahaya
          key: "pm25",
          id: 310102,
          name: "PM 2.5",
          short: "PM2.5",
          unit: "μg/m³",
          min: 0,
          max: 500,
        },
        {
          // 0-15.5 baik
          // 15.6-55.4 sedang
          // 55.5-150.4 tidak sehat
          // 150.5-250.4 sangat tidak sehat
          // >250.5 berbahaya
          key: "pm10",
          id: 310103,
          name: "PM 10",
          short: "PM10",
          unit: "μg/m³",
          min: 0,
          max: 500,
        },
      ],
      ispuParamKeys: ["pm10", "pm25"],
      dataSourceKey: "average", // "data" or "average"
    },
  },
];
```
