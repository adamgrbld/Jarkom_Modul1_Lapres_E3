# Jarkom_Modul1_Lapres_E03

## Display Filter

### 1. Simpan webserver yang digunakan pada "testing.mekanis.me"!
```
http.host == "testing.mekanis.me"
```
*buka Follow TCP Stream dengan cara klik kanan pada paket*
![1a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/1a.png)
*setelah buka TCP Stream akan terlihat servernya yaitu nginx*

![1b](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/1b.png)

----

#### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

```
File -> Export Object -> HTTP
```

*Masukkan nama file yang dicari, lalu **Save***
![2](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/2.png)
![2a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/2a.png)

----

#### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
```
http.host contains "ppid.dpr.go.id" && http.request.method == POST
```
![3a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/3a.png)
*buka salah satu paket lalu scroll lalu anda akan menemukan username dan passwordnya*
![3b](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/3b.png)
![3c](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/3c.png)

----

#### 4. Temukan paket dari web-web yang menggunakan basic authentication method!

```
http.authbasic
```

![4](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/4.png)

----

#### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
```
http.host contains "aku.pengen.pw"
```

![5a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/5a.png)
![5b](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/5b.png)
![5c](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/5c.png)

----

#### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

***Mencari file zip***

```
frame contains "Answer.zip"
```

![6](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6.png)

```
Klik kanan -> Follow -> TCP Stream -> Save data as Raw -> Ubah stream menjadi 12
```

![6a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6a.png)

*File akan tersimpan sebagai **zip***

![6b](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6b.png)

*Saat file dibuka terdapat **Open This.pdf** yang jika dibuka kembali meminta masukan **password***
![6c](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6c.png)

------

***Mencari password***

```
frame contains "zipkey.txt"
```

![6d](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6d.png)

```
Klik kanan -> Follow -> TCP Stream -> Save data as ASCII -> Ubah stream menjadi 23
```

![6e](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6e.png)

*File txt akan tersimpan dan berisi **password** yang dibutuhkan*

![6f](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6f.png)

*Masukkan password, dan **Open This.pdf** akan menampilkan seperti dibawah ini*
![6g](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/6g.png)

----

#### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
```
frame contains "Yes.pdf"
```

![7](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/7.png)
*buka follow TCP Stream lalu save data menjadi Raw*
![7b](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/7b.png)
*extract zip lalu akan muncul file pdf seperti berikut*
![7c](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/7c.png)
![7d](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/7d.png)

----

#### 8.Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
```
ftp contains Microsoft
```
*setelaah mendapatkan ip lakukan*
```
ftp.request.command == RETR && ip.dst == 198.246.117.106
```
![8](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/8.png)

----

#### 9. Cari username dan password ketika login FTP pada localhost!
```
fttp.request.command == PASS || fttp.request.command == USER
```
![9](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/9.png)

----

#### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut!

```
frame contains ".pdf"
```

![10](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/10.png)

```
Klik kanan -> Follow -> TCP Stream -> Save data as Raw -> Ubah stream menjadi 15
```

![10a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/10a.png)

*File akan tersimpan sebagai **pdf***

![10b](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/10b.png)

*Ketika file dibuka menampilkan seperti dibwah ini*
![10c](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/10c.png)

----

## Capture Filter

#### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
```
tcp.port == 21
```

![11](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/11.png)

----

#### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

```
tcp.srcport==80
```

![12](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/12.png)

----

#### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

```
tcp.dstport==443
```

![13](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/13.png)

----

#### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

*Mencari **ip** pc dahulu melalui terminal*

![14](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/14.png)

*Capture di Wireshark*

```
ip.scr==192.168.43.254
```

![14a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/14a.png)

----

#### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
pertama tama cari ping monta.if.its.ac.id
karena saya menggunakan windows saya mencarinya menggunakan cmd
setelah didapatkan gunakan cara dibawah ini pada capture filter
```
ip.dst == 103.94.190.11 && http.request.method == GET
```
![15](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/15.png)

----
