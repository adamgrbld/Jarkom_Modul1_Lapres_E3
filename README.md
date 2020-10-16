# Jarkom_Modul1_Lapres_E03

## Display Filter

### 1. Simpan webserver yang digunakan pada "testing.mekanis.me"!
```
http.host == "testing.mekanis.me"
```
*buka Follow TCP Stream dengan cara klik kanan pada paket*
![1a](https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/1a.png)
*setelah buka TCP Stream akan terlihat servernya yaitu nginx*
![1b]((https://github.com/adamgrbld/Jarkom_Modul1_Lapres_E3/blob/main/Screenshot/1b.png)

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

#### 5.

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
