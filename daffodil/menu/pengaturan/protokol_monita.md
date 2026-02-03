# Protokol Monita


![Protokol](../../assets/images/protokol_monita.PNG)

#### Pengaturan Protokol Monita

| Nama          | Deskripsi                                                                                 | Keterangan |
| :------------ | :---------------------------------------------------------------------------------------- | :--------- |
| Status        | Pilihan pengiriman protokol. <br><ul><li>Disable</li><li>Modem</li><li>Ethernet</li></ul> |
| Protokol Mode | Pilih Mode pengiriman yang digunakan. <br><ul><li>REST API</li><li>MQTT</li></ul>         |            |

- Jika dipilih __REST API__
| Nama      | Deskripsi                                    | Keterangan                |
| :-------- | :------------------------------------------- | :------------------------ |
| Domain    | Alamat DNS atau IP Server Monita             |                           |
| Port      | No Port                                      | http (80) <br>https (443) |
| Interval  | Interval pengiriman data dalam __detik__     |                           |
| Sort Data | Urutan ID Tag yang akan dikirimkan ke server | misal : 1,2,3             |

- Jika dipilih __MQTT__
| Nama          | Deskripsi                                    | Keterangan                    |
| :------------ | :------------------------------------------- | :---------------------------- |
| Broker Domain | Alamat Broker                                |                               |
| Broker Port   | No Port Broker                               | mqqt (1883) <br> mqqts (8883) |
| Interval      | Interval pengiriman data dalam __detik__     |                               |
| Username      | Username broker MQTT                         |                               |
| Password      | Password broker MQTT                         |                               |
| Sort Data     | Urutan ID Tag yang akan dikirimkan ke server | misal : 1,2,3                 |
