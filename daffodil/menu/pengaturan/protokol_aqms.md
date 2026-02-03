# Protokol AQMS

| Nama          | Deskripsi                                                                                 | Keterangan                |
| :------------ | :---------------------------------------------------------------------------------------- | :------------------------ |
| Status        | Pilihan pengiriman protokol. <br><ul><li>Disable</li><li>Modem</li><li>Ethernet</li></ul> |
| Protokol Mode | Pilih Mode AQMS yang digunakan. <br><ul><li>PORTABLE</li><li>FIX STATION</li></ul>        |                           |
| Domain        | Alamat DNS atau IP Server AQMS                                                            | sesuai dokumen AQMS       |
| Port          | No Port                                                                                   | http (80) <br>https (443) |
| Interval      | Interval pengiriman data dalam __detik__                                                  |                           |

- Jika dipilih __PORTABLE__

| Nama        | Deskripsi                                    | Keterangan          |
| :---------- | :------------------------------------------- | :------------------ |
| Kode Jadwal | Kode protokol AQMS                           | sesuai dokumen AQMS |
| API URL     | path url protokol AQMS                       | sesuai dokumen AQMS |
| API KEY     | key protokol AQMS                            | sesuai dokumen AQMS |
| API Secret  | secret protokol AQMS                         | sesuai dokumen AQMS |
| Sort Data   | Urutan ID Tag yang akan dikirimkan ke server | misal : 1,2,3       |


- Jika dipilih __PORTABLE__

| Nama       | Deskripsi                                    | Keterangan          |
| :--------- | :------------------------------------------- | :------------------ |
| Username   | username protokol AQMS                       | sesuai dokumen AQMS |
| Password   | password protokol AQMS                       | sesuai dokumen AQMS |
| API Auth   | path url auth protokol AQMS                  | sesuai dokumen AQMS |
| API Data   | path url data protokol AQMS                  | sesuai dokumen AQMS |
| ID Station | kode station protokol AQMS                   | sesuai dokumen AQMS |
| Sort Data  | Urutan ID Tag yang akan dikirimkan ke server | misal : 1,2,3       |